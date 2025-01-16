```xml
<?xml version="1.0" encoding="UTF-8"?>
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" elementFormDefault="qualified">
    <xsd:element name="empresa">
        <xsd:complexType>
            <xsd:sequence>
                <xsd:element name="departamentos">
                    <xsd:complexType>
                        <xsd:sequence>
                            <xsd:element name="departamento">
                                <xsd:complexType>
                                    <xsd:atribute name="id" use="required">
                                        <xsd:restriction base="xsd:string">
                                            <xsd:pattern value="[D][0-9]{3}"/>
                                        </xsd:restriction>
                                    </xsd:atribute>
                                    <xsd:atribute name="nombre" use="required"/>
                                </xsd:complexType>
                            <xsd:element>
                        </xsd:sequence>
                    </xsd:complexType>
                </xsd:element>
                
                <xsd:element name="empleados">
                    <xsd:complexType>
                        <xsd:sequence>
                            <xsd:element name="empleado">
                                <xsd:complexType>
                                    <xsd:atribute name="id" use="required">
                                        <xsd:restriction base="xsd:string">
                                            <xsd:pattern value="[E][0-9]{3}"/>
                                        </xsd:restriction>
                                    </xsd:atribute>
                                    <xsd:atribute name="nombre" use="required"/>
                                    <xsd:atribute name="departamento" use="required">
                                        <xsd:restriction base="xsd:string">
                                            <xsd:pattern value="[D][0-9]{3}"/>
                                        </xsd:restriction>
                                    </xsd:atribute>
                                </xsd:complexType>
                            <xsd:element>
                        </xsd:sequence>
                    </xsd:complexType>
                </xsd:element>
                
                <xsd:element name="proyectos">
                    <xsd:complexType>
                        <xsd:sequence>
                            <xsd:element name="proyecto">
                                <xsd:complexType>
                                    <xsd:atribute name="id" use="required">
                                        <xsd:restriction base="xsd:string">
                                            <xsd:pattern value="[P][0-9]{3}"/>
                                        </xsd:restriction>
                                    </xsd:atribute>
                                    <xsd:atribute name="nombre" use="required"/>
                                    <xsd:atribute name="empleado" use="required">
                                        <xsd:restriction base="xsd:string">
                                            <xsd:pattern value="[E][0-9]{3}"/>
                                        </xsd:restriction>
                                    </xsd:atribute>
                                </xsd:complexType>
                            <xsd:element>
                        </xsd:sequence>
                    </xsd:complexType>
                </xsd:element>
            </xsd:sequence>
        </xsd:complexType>

        <!-- clave -->
        <xsd:key name="claveIdDep">
            <xsd:selector xpath="empresa/departamentos/departamento"/>
            <xsd:field xpath="@id"/>
        </xsd:key>

        <xsd:key name="claveNombreDep">
            <xsd:selector xpath="empresa/departamentos/departamento"/>
            <xsd:field xpath="@nombre"/>
        </xsd:key>

        <xsd:keyref name="claveIdEmp" refer="claveIdDep">
            <xsd:selector xpath="empresa/empleados/empleado"/>
            <xsd:field xpath="@id"/>
        </xsd:keyred>

        <xsd:keyref name="claveNombreEmp" refer="claveNombreDep">
            <xsd:selector xpath="empresa/empleados/empleado"/>
            <xsd:field xpath="@nombre"/>
        </xsd:keyred>

        <xsd:keyref name="claveDepEmp" refer="claveIdDep">
            <xsd:selector xpath="empresa/empleados/empleado"/>
            <xsd:field xpath="@departamento"/>
        </xsd:keyred>

        <xsd:keyref name="claveIdPro" refer="claveIdDep">
            <xsd:selector xpath="empresa/proyectos/proyecto"/>
            <xsd:field xpath="@id"/>
        </xsd:keyred>

        <xsd:keyref name="claveNombrePro" refer="claveNombreDep">
            <xsd:selector xpath="empresa/proyectos/proyecto"/>
            <xsd:field xpath="@nombre"/>
        </xsd:keyred>

        <xsd:keyref name="claveEmpPro" refer="claveIdDep">
            <xsd:selector xpath="empresa/proyectos/proyecto"/>
            <xsd:field xpath="@empleado"/>
        </xsd:keyred>

    </xsd:element>
```