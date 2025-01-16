``` xml
<?xml version="1.0" encoding="UTF-8"?>
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" elementFormDefault="qualified">
  <xsd:element name="aeropuerto">
    <xsd:complexType>
      <xsd:sequence>
        <xsd:element name="avion" type="xsd:string" minOccurs="0" maxOccurs="unbounded">
          <xsd:complexType>
            <xsd:sequence>
              <xsd:element name="modelo" base="xsd:string">
              <xsd:element name="compania" base="xsd:string">
              <xsd:element name="capacidad">
                <xsd:simpleType>
                  <xsd:restriction base="xsd:integer">
                    <xsd:minInclusive value="100"/>
                    <xsd:maxInclusive value="300"/>
                  </xsd:restriction>
                </xsd:simpleType>
                                <!-- Crew -->
              <xsd:element name="crew">
                <xsd:complexType>
                  <xsd:sequence>                
                    <xsd:element name="piloto" base="xsd:string"/>
                    <xsd:element name="copiloto" base="xsd:string"/>
                    <xsd:element name="flight_attendance">
                      <xsd:complexType>
                        <xsd:sequence>
                          <xsd:element name="nombre" base="xsd:string"/>
                        </xsd:sequence>
                      </xsd:complexType>
                    </xsd:element>
                  </xsd:sequence>                
                </xsd:complexType>
                                <!-- Pasajeros -->
              <xsd:element name="pasajeros">
                <xsd:complexType>
                  <xsd:sequence>
                    <xsd:element name="pasajero"/>
                      <xsd:complexType>
                        <xsd:atribute name="id"/>
                        <xsd:sequence>
                          <xsd:element name="nombre" base="xsd:string"/>
                          <xsd:element name="nacionalidad" base="xsd:string"/>
                          
                          <xsd:element name="maletas">
                            <xsd:complexType>
                              <xsd:sequence>
                                <xsd:element name="maleta">
                                <xsd:attribute name="peso">
                                  <xsd:simpleType>
                                    <xsd:restriction base="xsd:decimal">
                                      <xsd:fractionDigits value="1"/>
                                      <xsd:minExclusive value="0"/>
                                    </xsd:restriction>
                                  </xsd:simpleType>
                                </xsd:attribute>  
                              </xsd:sequence>
                            </xsd:complexType>
                          </xsd:element>

                        </xsd:sequence>
                      </xsd:complexType>
                    </xsd:element>  
                  </xsd:sequence>
                </xsd:complexType>
              </xsd:element>
              
            </xsd:sequence>
          </xsd:complexType>
                                <!-- Atributo y restricciónes -->
          <xsd:attribute name="id">
            <xsd:simpleType>
              <xsd:restriction base="xsd:string">
                <xsd:pattern value="[A-Z][0-9]{3}"/>
              </xsd:restriction>
            </xsd:simpleType>
          </xsd:attribute>

        </xsd:element>

        <xsd:element name="puertas_embarque" maxOccurs="1">
          <xsd:complexType>
            <xsd:sequence>
              <xsd:element name="puerta" maxOccurs="unbounded">
                <xsd:simpleType>
                  <xsd:restriction base="xsd:string">
                    <xsd:enumeration value="Abierta"/>
                    <xsd:enumeration value="Cerrada"/>
                  </xsd:restriction>
                </xsd:simpleType>
                <xsd:attribute name="id" type="xsd:string"/>
              </xsd:element>
            </xsd:sequence>
          </xsd:complexType>
        </xsd:element>

      </xsd:sequence>
    </xsd:complexType>
  </xsd:element>
```