Dies ist eine Ideen/Hardware Sammlung für Citizen Science Projekte in den OK Labs.
===
Folgende Labs: Wuppertal, Berlin, Karlsruhe und Leipzig werden in 2015 am Projekt "Hack your City" (www.hackyourcity.de) mitmachen und einen Citizen Science Schwerpunkt haben. Alle weiteren Labs Willkommen sich an Citizen Science Projekten zu beteiligen bzw. eigene Projekte zu starten.

Dieses Pad dient der Sammlung von Projekten und Hardware.

Mailingliste: https://lists.okfn.org/mailman/listinfo/codeforde-citizenscience

Projektbeschreibung: https://docs.google.com/document/d/1lNZS8i5XJ-71FcLltJSJ8iZxdQY2Pp05XOdzE_2-q8g/edit

Projektsammlung (International): https://docs.google.com/document/d/1_qDSZVPesIp6KtHEwOcivslgSQK47AaMh_lHhGsENlA/edit#heading=h.2m1wq8t4se97
#Themen:
## Plattformen
#####    Arduino
* http://arduino.cc/
* Open Source
* Zertifizierung (CE, FCC, ...)
* original Boards: ja
* Nachbauten etc.: teilweise
*  Vorteil:
 * Standardisiert
    * Auch für Anfänger schnell und leicht aufgebaut
    * Gut für Prototyping
* Nachteile:
 * Im Vergleich zu reinem Mikrocontroller relativ teuer
 * Stromhungrig durch extra Spannungswandler, USB-Serial-Wandler, Quarz, Power-LEDs

##### Netduino (2 plus)
* http://www.netduino.com/
* Open Source Hardware
* .NET Micro Framework (Apache 2.0)
* Hardware ähnlich zu Arduino, aber andere Firmeware
* Vorteile:
 * Sehr gute Entwicklungs- und Debuggingwerkzeuge
 * C# Micro Framework Code kann auch auf vielen anderen (größere) Hardwareplatformen wiederverwendet werden
* Nachteile:
 * Wie Arduino relativ teuer

##### Waspmote
* http://www.libelium.com/products/waspmote/
* Kompatibel zu Arduino
* Open Source
* Komponenten auch einzeln erhältlich
* Zertifizierung (CE, FCC, ...)
* Boards: ja
* Boards in Kombination mit Kommunikationsmodulen; ja
* Mehr: http://www.cooking-hacks.com/documentation/tutorials/waspmote#waspmote_vs_arduino
* Vorteile:
 * Wesentlich stromsparender als Arduino
* Nachteil:
 * Relativ teuer
* Mikrocontroller + eigene Platine
* Vorteil:
* Nur das was wirklich benötigt wird
* Stromsparender als Arduino
* eventuell Günstiger
* Nachteil
* Schaltungsentwurf und -herstellung notwendig

## Übertragung
##### Ethernet
* Beispiele:
* http://arduino.cc/en/Main/ArduinoEthernetShield
* Vorteil:
 * Stromversorgung möglich
 * Relativ Preisgünstig
* Nachteil
 * Sensoren müssen meist im Freien angebracht werden -> Verlegen von zusätzlichen Kabel eher schwer
 * WLAN
* Beispiele:
 * http://arduino.cc/en/Main/ArduinoWiFiShield

##### ESP8266
* Seit Mitte/Ende 2014 neuer Stern -> mit 2-10 Euro sehr preiswert
* http://www.mikrocontroller.net/articles/ESP8266
* https://nurdspace.nl/ESP8266
* http://www.esp8266.com/
* http://hackaday.com/2014/12/17/esp-gets-fcc-and-ce/
* Vorteile
 * ESP8266 sehr preiswert
 * Nutzung von vorhandenen Infrastrukturen (Freifunk ...)
* Nachteile
 * Im Vergleich zu anderen Funktechniken relativ kurze Reichweite
 * Z-Wave
* Beispiele
 * http://de.wikipedia.org/wiki/Z-Wave
 * http://www.zwave.de/
* Gedacht für Homeautomation

##### ZigBee
* http://de.wikipedia.org/wiki/ZigBee

##### 802.15.4
* http://de.wikipedia.org/wiki/IEEE_802.15.4

#####Funk Sender und Empfänger (433, 868, 915 MHz)
* Beispiel:
* RFM69
* http://www.mikrocontroller.net/articles/RFM69
* Technische Daten:
* Spannung: 1.8 bis 3.6V
* Max. Datenrate: 300 kbit/s
* Sendeleistung: 13dBm
* Empfindlichkeit: -120dB
* Strom:
* Standby: 0.1uA
* Empfangen: 16mA
* Senden: 45mA
* SPI
* AES-Verschlüsselung
* CRC
* 66 Byte FIFO
* Vorteil:
 * Je nach Frequenz größere Entfernungen überbrückbar
 * Stromsparend
 * Antenne relativ einfach möglich (Stückdrat mit Länge x)
* Nachteil
 * Protokoll für Sensornetz muss selbst entwickelt werden
 * Einbindung in bestehende Infrastruktur nur über zusätzlichen Gateway möglich


## Protokolle
##### MQTT
* Verbreitet sich gerade bei IoT Bewegung
* http://mqtt.org/
* Server/Broker
 * http://mosquitto.org/
* Client
 * https://eclipse.org/paho/
* Vorträge/Folien
 * http://de.slideshare.net/PeterREgli/mq-telemetry-transport
 * http://de.slideshare.net/Angelo.Corsaro/whats-the-right-messaging-standard-for-the-iot
 * HTTP mit CSV, JSON, BSON content representation
 * ProtocolBuffers, etc.pp

## Infrastruktur:
##### WLAN
 * Freifunk http://freifunk.net/

## Temperatur/Luftfeuchtigkeit:
##### DHT22
* Datenblatt: https://www.sparkfun.com/datasheets/Sensors/Temperature/DHT22.pdf
* Technische Daten:
 * Digitale Temperatur: -40 bis 80°C ±0.5°C
 * Luftfeuchtigkeit: 0-100% 2-5% Genauigkeit
 * Geschwindigkeit: Neue Messwerte alle 2 Sekunden und gleitender Mittelwert
 * Spannung: 3.3 bis 6V
* Vorteil
 * Vergleichbar günstig
* Nachteil
 * Kommunikationsprotokoll ist proprietär
 * Nicht für außen/im Freien geeignet oder bei zu hoher Luftfeuchtigkeit geeignet!

##### DS18B20
* Datenblatt: http://www.adafruit.com/datasheets/DS18B20.pdf
* Technische Daten:
 * 1-Wire
 * Spannung: 3.0 bis 5.5V
 * Temperaturbereich: -55°C to +125°C
 * Genauigkeit: ±0.5 zwischen -10°C bis 85°C
 * Daten: 9 bis 12 Bit (einstellbar)
 * Messzeit: 93.75ms bis 750ms (Je nach Datenbreite)
 * Strom:
	* Aktiv: 1 mA
	* Standby: 750 nA

##### HYT-221
* Datenblatt: http://www.farnell.com/datasheets/1643979.pdf
* Technische Daten:
 * I2C
 * Spannung: 2.7 bis 5.5V
 * Temperaturbereich: -40 bis 125°C
 * Luftfeuchtigkeit: 0 bis 100%
 * Strom:
     * Aktiv: 22uA (bei 1Hz Messrate); max 850uA
     * Standby: < 1uA
 * Vorteil:
     * Sehr guter und sehr schneller (kein gleitender Mittelwer) Sensor
     * I2C-Kommunikation
     * Kann problemlos auch im Freien benutzt werden
 * Nachteil
     * Leider recht teuer


## Luftdruck
leer

## Lichtverschmutzung:
* http://www.lightpollutionmap.info/

##### Grove - Digital Light Sensor
* http://www.seeedstudio.com/wiki/Grove_-_Digital_Light_Sensor
* Technische Daten:
 * I2C-Schnittstelle(400kHZ)
 * 0.1 - 40,000 LUX
 * 16-Bit Wert
* Temperatur: -40°C bis 85°C (-30 bis 70°C) Im Wiki sind zwei Werte hinterlegt
 * Spannung: 3.3 bis 5.1V
 * Zwei Sensoren Sichtbarer und IR und nur IR
* Vorteil:
 * I2C Schnittstelle
 * Ausreichender Temperaturbereich
 * Spannung
* Nachteil
 * Spannungsregler (wenn er zu viel Strom verbraucht)

##### Adafruit TSL2561 digitaler Lichtsensor
* Technische Daten:
 * I2C-Schnittstelle(400kHZ)
 * 0.1 - 40,000 LUX
 * 16-Bit Wert
 * Temperatur: -30°C bis 80°C
 * Spannung: 2.7 bis 3.6V
 * Strom:
 * Aktiv: 0.5mA
 * Power down: 15uA
* Vorteil
 * I2C Schnittstelle
 * Ausreichender Temperaturbereich
 * Spannung
 * Sehr geringer Stromverbrauch
* Nachteile
 * Nicht für 5V Arduino geeignet

## Luftverschmutzung und Feinstaub
##### Sensortypen
* Sharp GP2Y1010AU0F
 * Vorteil: 
	 * günstig (nur ca 5€), verbraucht wenig Energie (0,1W im Betrieb bei 5V)
 * Nachteil: 
	 * kommt unkalibriert daher und Volumen der durchströhmenden Luft ist abhängig vom Versuchsaufbau. Somit lassen sich meiner Meinung nach Messungen von DIY-Gerät1 (mit Lüfter) nicht mit Messungen von DIY-Gerät 2 (ohne Lüfter) vergleichen.
 * Quellen:
 	* Datenblatt: http://media.digikey.com/pdf/Data%20Sheets/Sharp%20PDFs/GP2Y1010AU.pdf
 	* Arduino + Sensor (Code und Verdrahtung): http://sensorapp.net/sharp-dust-sensor-and-arduino/
* Grove - Dust Sensor
 * Kurzbeschreibung: "Grove is a modulated, ready-to-use tool set. Much like Lego, it takes a building block approach to assembling electronics." Quelle: http://www.seeedstudio.com/wiki/GROVE_System
 * Der Dust Sensor ist ein Sensor zum messen von Teilchen die größer 1µm sind
 * Der Sensor muss immer aufgehangen werden (siehe oberen beiden Bilder: http://www.howmuchsnow.com/arduino/airquality/grovedust/)
 * Vorteil: 
 	* Wird bereits über die beiden Potentiometer kalibriert ausgeliefert, er besitzt eine eigene Wärmequelle und sorgt somit für einen konstanten Luftstrom durch die Lichtschranke. Ein Lüfter wird nicht benötigt.
 	* Muss 3 Minuten vorheizen
 * Nachteil: 
     * Etwas höherer Energieverbrauch gegenüber den Sharp-Sensor (0,45W im Betrieb bei 5V), etwas teurer (15 bis 25 Euro)
 * Quellen:
 	* Datenblatt: http://www.sca-shinyei.com/pdf/PPD42NS.pdf
 	* Wiki Artikel zum Sensor + Arduino Beispiel: http://www.seeedstudio.com/wiki/Grove_-_Dust_Sensor
 	* Artikel Grove Dust Sensor + Arduino vs 290$ Messgerät: http://www.howmuchsnow.com/arduino/airquality/grovedust/
 	* Bauanleitung Air Quality Test Box (Arduino comatible+ Grove Dust Sensor): http://www.instructables.com/id/Air-Quality-Test-Box/    +  https://github.com/Seeed-Studio/Air_Quality_Test_Box

##### Microcontroller
 * Alle oberen Beispiele verwenden einen Arduino, dieser hat jedoch auch einige Nachteile. So ist er wohl nicht der energiesparenste und Netzwerkkommunikation erfordert extra Module.
 * Auf der Seite http://datacolonia.de/blog/feinstaub.html und https://github.com/marcel12bell/feinstaub-app wird ein ESP8266 und der Grove Dust-Sensor verwendet (@Marcel Belledin: Danke für den Hinweis)
 * Der ESP8266 kostet je nach Ausführung zwischen 3 bis 10 Euro und bietet WLAN (802.11 b/g/n incl. WPA2) an
 * Der ESP kann als Webclient, als auch als Webserver agieren (leider kein https)
 * Für den ESP gibt es die offene Firmware NodeMCU, die es ermöglicht in LUA programme zu schreiben (http://nodemcu.com/index_en.html)
 * Achtung: der ESP8266 darf nur mit 3,3V betrieben werden!! somit steigt der Aufwand, da Arduino und Grove-Dust mit 5V arbeiten
 * Quellen: 
 	* Übersichtsartikel: https://www.mikrocontroller.net/articles/ESP8266
 	* Vorträge: https://wiki.attraktor.org/File:ESP8266_Vortrag_Attraktor_Teil_1.pdf   und  https://wiki.attraktor.org/File:ESP8266_Vortrag_Attraktor_Teil_2.pdf
 * Meine Erkentnisse:
 	* mit NodeMCU ist es nur möglich mit einer Genauigkeit von 1ms die Zustände des Grove Dust Sensors auszuwerten, während der Arduino eine Genauigkeit von 1µs auf weist.
 	* Unterschiede testen konnte ich bisher noch nicht, da mein FTDI-USB-Serial Adapter noch nicht im Briefkasten lag :(
 	* Es wäre auch möglich den ESP als reines Netzwerkgerät an den Arduino zu stecken.

## Lärm:
## Wassermenge (Durchfluss):
## Wasserqualität:
## Pegelstände von Flüssen/Seen/etc.
## Strom/Spannung:
## Müll:
*(Wie könnte man die Müllmenge die jeder produziert sinnvoll messen/wiegen?)
## Fahrradverkehr:
## Verkehrszählung

##Recherche Partner:
* Leipzig (Luftverschmutzung, Fahrradfahren, Gentrifizierung) -  
Partner: Einund Leipzig (http://www.einundleipzig.de/)
* Berlin (Lichtverschmutzung, Fahrradfahren)
* Karlsruhe (Lärm, Fahrradfahren)
* Wuppertal (Mobilität, Energie) - Wuppertal Institut

##Recht/Richtlinien
Ein paar Dinge die beim späteren Verkauf von Sensor-Knoten etc. wichtig sein könnten
 * Zertifizierungen
 * CE, RoHS, WEEE, FCC
 * http://de.wikipedia.org/wiki/Elektro-_und_Elektronikger%C3%A4tegesetz
 * http://de.wikipedia.org/wiki/Richtlinie_2002/96/EG_%C3%BCber_Elektro-_und_Elektronik-Altger%C3%A4te
 * Beispiele
 	* Raspberry Pi http://www.raspberrypi.org/compliance-testing/
 	* Arduino
