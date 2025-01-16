```xml
<?xml version="1.0" encoding="UTF-8"?>
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" elementFormDefault="qualified">
    <xsd:element name="almacen">
        <xsd:complexType>
            <xsd:sequence>
                <xsd:element name="productos">
                    <xsd:complexType>
                        <xsd:sequence>
                            <xsd:element name="producto">
                                <xsd:simpleType>
                                    <xsd:atribute name="codigo" use="required">
                                        <xsd:restriction base="xsd:string">
                                            <xsd:pattern value="[P][0-9]{3}"/>
                                        </xsd:restriction>
                                    </xsd:atribute>
                                </xsd:simpleType>
                            </xsd:element>
                        </xsd:sequence>
                    </xsd:complexType>
                </xsd:element>
                <xsd:element name="pedidos">
                    <xsd:complexType>
                        <xsd:sequence>
                            <xsd:element name="pedido">
                                <xsd:simpleType>
                                    <xsd:atribute name="codigoProducto" use="required">
                                        <xsd:restriction base="xsd:string">
                                            <xsd:pattern value="[P][0-9]{3}"/>
                                        </xsd:restriction>
                                    </xsd:atribute>
                                </xsd:simpleType>
                            </xsd:element>
                        </xsd:sequence>
                    </xsd:complexType>
                </xsd:element>
            </xsd:sequence>
        </xsd:complexType>

        <!-- claves -->
        <xsd:key name="claveProducto">
            <xsd:selector xpath="almacen/productos/producto"/>
            <xsd:field xpath="codigo"/>
        </xsd:key>

        <xsd:keyref name="claveProductoPedido" refer="claveProducto">
            <xsd:selector xpath="almacen/pedidos/pedido"/>
            <xsd:field xpath="codigoProducto"/>
        </xsd:keyref>
    </xsd:element>
```