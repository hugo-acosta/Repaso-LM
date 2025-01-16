```xml
<?xml version="1.0" encoding="UTF-8"?>
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" elementFormDefault="qualified">
    <xsd:element name="usuarios">
        <xsd:complexType>
            <xsd:sequence>
                <xsd:element name="usuario">
                    <xsd:simpleType>
                        <xsd:atribute name="id">
                            <xsd:simpleType>
                                <xsd:restriction base="xsd:string">
                                    <xsd:pattern value="[U][0-9]{3}" use="required"/>
                                </xsd:restriction>
                            </xsd:simpleType>
                        </xsd:atribute>
                    </xsd:simpleType>
                </xsd:element>
            </xsd:sequence>
        </xsd:complexType>

        <!-- Clave -->
        <xsd:key name="idIrrepetible">
            <xsd:selector xpath="usuarios/usuario"/>
            <xsd:field xpath="@id"/>
        </xsd:key>
    </xsd:element>

```