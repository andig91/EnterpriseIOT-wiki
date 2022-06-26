# LoRa-WAN vs Zigbee

Autor: se211306 Wirtner

Diese Reflexion soll einen kurzen Überblick der zwei gängigsten drahtlosen Protokolle für das IoT in der Industrie geben, wo liegen ihre Stärken, aber auch die jeweiligen Einschränkungen.

## Was ist LoRa-WAN
Ein LoRa-WAN ist ein Long-Range-Wide-Area-Network (oder ein Begriff, der auch häufig verwendet wird, ist Low-Power-WAN), das sich durch einen geringen Stromverbrauch, eine niedrige Datenrate und eine Funkkommunikation mit großer Reichweite auszeichnet. Das macht LoRa-WAN zu einer geeigneten Technologie für batteriebetriebene Sensoren und industrielle IoT-Anwendungsfälle in Branchen wie Wasser-Stromversorgungsunternehmen, Landwirtschaft, Smart Cities, Bergbau, Home Automation usw.. Derzeit wird LoRa-WAN hauptsächlich in freien Frequenzbändern (ISM/SRD) auf der ganzen Welt eingesetzt, darunter 779-787 MHz (in China), 863-870 MHz (in Europa), 902-928 MHz (in den Vereinigten Staaten) usw.

### Vorteile
LoRa-WAN verwendet die Technik der adaptiven Datenrate, um die Ausgangsdatenrate bzw. den HF-Ausgang der Endgeräte zu variieren. Das hilft bei der Maximierung der Batterielebensdauer und der Gesamtkapazität des LoRaWAN-Netzwerks. Die Datenrate kann von 0,3 kbit/s bis 27 kbit/s bei 125 KHz Bandbreite variiert werden. Diese Technologie hat eine sehr große Reichweite von etwa 5 km in städtischen Gebieten und bis zu 40 km im Ländlichen Bereich. Ein einziges LoRa-Gateway-Gerät ist für 1000 Endgeräte ausgelegt.
LoRa-WAN verwendet ein Frequenzspreizungsverfahren (In diesem Verfahren sind die Empfänger hochempfindlich, bei 127 dBm Signalstärke können so auch noch Datenpakete empfangen werden). Bei WLAN & Mobilfunk ist bei knapp 100 dBm Schluss. Durch die Niedrige Frequenz im Vergleich zu WLAN, ist die Durchdringbarkeit von Wänden/Gebäuden und Erreichbarkeit von weit entfernten Geräten besser gewährleistet als mit herkömmlichen Technologien.

### Nachteile
Es kann nur für Anwendungen verwendet werden, die eine niedrige Datenrate erfordern, d.h. bis zu etwa 27 Kbps. Die Größe die ein Datenpaket haben darf wird durch einen Parameter begrenzt, der als Duty Cycle (DC) bezeichnet wird. Dieser ist definiert als Prozentsatz der Zeit, während der der Kanal belegt werden kann. Dieser Parameter ergibt sich aus der Verordnung als wichtigster begrenzender Faktor für den Datentransfer im LoRa-WAN. Bei Frequenzbändern, wo mit erhöhter Leistung gesendet wird, wird ein DC von 1% vorgeschrieben.

## Was ist Zigbee
ZigBee ist ein lokales Netzwerkprotokoll mit geringem Stromverbrauch, das auf dem IEEE802.15.4-Standard basiert. Zigbee wird hauptsächlich für die Datenübertragung zwischen verschiedenen elektronischen Geräten mit kurzen Entfernungen, geringem Stromverbrauch und niedrigen Übertragungsraten sowie für typische Anwendungen mit periodischen Daten, intermittierenden Daten und Datenübertragungen mit geringer Reaktionszeit verwendet.
Gegenwärtig arbeitet Zigbee auf drei Frequenzbändern: 2,4 GHz, (Weltweit) 868 MHz (in Europa) und 915 MHz (in den Vereinigten Staaten), mit Übertragungsgeschwindigkeiten von bis zu 250kbit/s (2,4 GHz), 20kbit/s (868 MHz) bzw. 40kbit/s (915 MHz). Die Übertragungsdistanz liegt im Bereich von 10-75m, kann aber weiter erhöht werden.

### Vorteile
Aufgrund der niedrigen Übertragungsrate von ZigBee beträgt die Sendeleistung nur 1 mW, wenn der Schlafmodus verwendet wird, welcher einen geringen Stromverbrauch hat, ist ein ZigBee-Gerät sehr stromsparend. Die Kommunikationsverzögerung und die Verzögerung bei der Aktivierung aus dem Ruhezustand sind sehr kurz. Eine typische Verzögerung des Suchgeräts beträgt 30ms, die Verzögerung bei der Aktivierung aus dem  Ruhezustand ist 15ms und die Verzögerung beim Kanalzugriff des mobilen Geräts beträgt 15ms. Daher eignet sich die ZigBee-Technologie für drahtlose Steuerungen (z.B. industrielle Steuerungen usw.) mit hohen Verzögerungsanforderungen.

### Nachteile
Die Anfälligkeit für Netzwerkstörungen aufgrund von Kanalrauschen und Überfüllung ist einer der Nachteile von Zigbee, da es das selbe 2,4-GHz-Band verwendet, welches auch von Wi-Fi, Bluetooth und anderen Geräten genutzt wird.

## Wie lassen sich LoRa-WAN und Zigbee vergleichen
LoRa-WAN basiert auf einer Sterntopologie, was bedeutet, dass jedes Gerät direkt mit einem Gateway kommunizieren muss. LoRa-WAN eignet sich gut für einfache Messanwendungen, bei denen die Sensoren batteriebetrieben sind und langsame Abfrageraten (Datenaktualisierungsrate) im Bereich von ein paar Mal pro Tag bis hin zu 2-5 Minuten Intervallen haben (3 Betriebsmodi).

Zigbee verfügt über eine flexiblere, zuverlässigere und ausbaufähige Mesh-Netzwerktopologie, die auf Zuverlässigkeit ausgelegt ist und über "Selbstheilungs"-Fähigkeiten und Geräte verfügt, die mit jedem anderen Gerät im Mesh-Netz kommunizieren können, wobei Multi-Hopping über sehr große Entfernungen möglich ist. Zigbee ist außerdem stromsparend und eignet sich mit dem richtigen Gerätedesign ideal für batteriebetriebene Sensoranwendungen, einschließlich Anwendungen, die eine schnelle Abfrage und hohe Zuverlässigkeit erfordern, wie z.B. Steuerung/Automatisierung zusätzlich zu Echtzeit-Sensoranforderungen, wie z.B. Überwachung des Gerätezustands.
Für LoRa-WAN bedeutet das, dass jedes Gerät mit einem bestimmten Gateway kommunizieren muss. Im Fall von Zigbee kann jedes Gerät mit jedem anderen Gerät im Mesh-Netzwerk kommunizieren, was es ideal für entferntes Multi-Hopping macht. Wenn es mit dem richtigen Gerätedesign verwendet wird, kann Zigbee leicht mit der Energieeffizienz von LoRa-WAN mithalten jedoch nicht mit der Reichweite.

## Kosten im Vergleich

Neben den niedrigen Kosten für ein Zigbee-Modul ist ebenfalls die lizenzfreie Verwendung des Zigbee-Protokolls ein Schlüsselfaktor für ZigBee.
LoRa-WAN nutzt lizenzfreie Frequenzen, um diese Technologie zu nutzen. Um sicher zu gehen das ein LoRa fähiges Gerät auch in jedem LoRa-Netzwerk funktioniert, wird von der LoRa-Allianz eine Zertifizierung angeboten. Die Kosten dafür belaufen sich auf ca. 1000 USD.
Zusammenfassend lässt sich sagen, dass sowohl LoRa-WAN als auch Zigbee ihren Platz, in dem sich ständig weiterentwickelnden und wachsenden Bereich IoT haben. LoRa-WAN eignet sich hervorragend für kostengünstige, von der Open-Source-Community betriebene Anwendungen, die nur eine geringe Abfragerate aufweisen. Zigbee ist die bessere Wahl für industrielle Anwendungen, die Zuverlässigkeit, Echtzeit-Überwachung (schnellere Abfragerate), Steuerung oder Automatisierung erfordern.

## Quellen:

[link](https://www.lora-wan.de/)

[link](https://www.rfwireless-world.com/Terminology/LoRa-vs-Zigbee.html)

[link](https://www.quora.com/What-are-the-pros-and-cons-of-Lora-versus-Zigbee?share=1)

[link](https://www.aeq-web.com/lora-wan-gateway-for-internet-of-things/)

[link](https://de.wikipedia.org/wiki/Long_Range_Wide_Area_Network)
