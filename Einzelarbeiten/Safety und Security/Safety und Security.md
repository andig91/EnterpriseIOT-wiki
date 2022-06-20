# Safety und Security
## Safety
Durch die rasante technologische Entwicklung der Automatisierungs- und Produktionstechnik steigen die Anforderungen an moderne und zukunftsorientierte Sensoren und Steuerungen. Das gleiche Maß an Flexibilität und Leistungsfähigkeit ist für die Maschinen- und Anlagensteuerung sowie die Umsetzung verschiedener Anforderungen an Sicherheitsfunktionen erforderlich, um die jeweiligen potenziellen Risiken zu minimieren. Dabei werden sicherheitsrelevante Funktionen hauptsächlich über Sensoren, berührungslos wirkende Schutzeinrichtungen und programmierbare elektronische Systeme realisiert.

Die Signalerfassung und -verarbeitung erfolgt nicht nur durch sichere Steuerung, sondern auch durch zusätzliche Sicherheitskomponenten.
- Sicherheitssteurung (SPS)
- Sicherheitssensorik (Schalter)
- Sicherheitseingabegerät (Not-Aus)
- Sichere Antriebstechnik (Motorstarter)
- Sicherheitsschaltgeräte (Relais)

Neben der hardwaremäßigen Verknüpfung der unterschiedlichen Komponenten gewinnt die Betrachtung der softwaretechnischen Umsetzung der Sicherheitsfunktionen immer mehr an Bedeutung. Die Tatsache, dass ein einzelnes Gerät den entsprechenden Richtlinien oder der EN-Normen übereinstimmt, garantiert nicht die erforderliche Sicherheit in einem System. Erst die richtige Integration und Nutzung der einzelnen Hardwarekomponenten und Softwaremodule macht aus den einzelnen Elementen ein robustes und sicheres Gesamtsystem.

Moderne Automatisierungstechnik beschränkt sich nicht darauf, neue Maschinen zu bauen und in den Produktionsprozess zu integrieren, sondern muss auch berücksichtigen, dass bestehende Maschinen und Anlagen miteinander verbunden werden müssen. Dies bedeutet in den meisten Fällen, dass Sicherheitskontrollen und deren Verknüpfungen angepasst oder modernisiert werden müssen. 

In Europa sind Maschinenbauer (Produktsicherheit) und Maschinenbetreiber (Arbeitssicherheit) gesetzlich verpflichtet, für die Sicherheit von Menschen und Umwelt zu sorgen. In der Europäischen Union gibt es beispielsweise Anforderungen an Gerätehersteller und -betreiber, die durch europäische Richtlinien, Gesetze und Normen geregelt werden. In den USA hingegen gibt es unterschiedliche regionale und sogar lokale Anforderungen. Für Maschinenbauer und Anlagen Errichter ist es wichtig, immer die Gesetze und Richtlinien am Einsatzort der Maschine oder Anlage anzuwenden.
[1][2][3][4][7]

## Security

Die Maschinen- und Anlagensicherheit betrachtet derzeit nur den Bereich der Betriebssicherheit oder der technischen Sicherheit, wo das Wort „Sicherheit“ verwendet wird. Der Bereich der IT-Sicherheit, sogenannte „Security“, ist in den Richtlinien und Normen zur Maschinensicherheit noch nicht erfasst.

Diese getrennte Betrachtung der beiden Arbeitsbereiche war zunächst nicht wichtig, da mit dem Aufkommen der Automatisierungstechnik zwar Maschinen und Anlagen mit programmierbaren Systemen ausgestattet wurden, die Vernetzung aber erst nach und nach erfolgte. In den letzten Jahren wurde jedoch auch beobachtet, einzelne Maschinen oder komplette Produktionslinien durch Netzwerke innerhalb von Produktionsanlagen oder sogar mit Produktionsanlagen an anderen Standorten zu verbinden. Dabei stellen sich Fragen wie: „Wie werden diese Produktivsysteme eigentlich vor unerwünschten Angriffen von außen geschützt?“

Sicherheitsfunktionen können durch Passivierung oder durch Veränderung der Geschwindigkeit betrieben werden. Es kann auch zu unerwarteten Maschinenanläufen kommen, die das größte Risiko für die Mitarbeiter darstellen.

Betrachtet man die Evolution der Maschinen- und Anlagensteuerung aus der Industrie 4.0-Perspektive, wird deutlich, dass sowohl Safety- als auch Security-Maßnahmen in der Maschinensteuerung dringend berücksichtigt werden müssen. Dabei ging es zunächst um einfachste organisatorische Maßnahmen, etwa um zu verhindern, dass Wartungspersonal Computerviren über USB-Sticks verbreitet, oder beim Update der Werkssteuerung keine direkte Internetverbindung von einem Wartungs-Laptop zu einem möglichen Malware-Einfallstor herzustellen. 
[1][5][7]

## Siemens
Siemens ist einer der Marktführer im Bereich Automatisierungstechnik die eine hohe Priorität auf Safety und Security setzten.

Siemens Safety Komponenten sind mit einem **F** gekennzeichnet. 
- F-CPU (SIMATIC S7-1500F, CPU 1511F-1 PN)
- F-Peripheriegeräte (ET 200SP F)
- F-Module (F-DI 8x 24VDC HF)

**Safety**
- Diskrepanzzeit:
Not-Halt Schalter ist immer zweikanalig verdrahtet.
Sind die zwei Signale länger als 200ms unterschiedlich, so sollte die Baugruppe in Störung gehen.
- Passivieren
Geht eine Baugruppe in Störung, so passiviert sie sich. Dies kann z.B. sein, wenn die Zweikanalüberwachung fehlerhaft ist.
- Geberauswertung
 Hier definiert man, wie die zwei Kanäle ausgewertet werden. Man kann hier 1oo1 (1v1) Auswertung einstellen.
 Dann gibt es die 1oo2 (2v2) Auswärtung. Dies ist eine äquivalente Auswertung.
 Zu Letzt gibt es noch die 1oo2 (2v2) Auswertung. Dies ist eine antiäquivalente Auswertung. Hierbei sollten die zwei Signale immer invers zueinander sein.
- Kurzschlusstest
Wenn jemand das Kabel durchtrennt hat und die zwei Kabelenden Kontakt haben, würde die Anlage starten, aber es wäre nicht sicher. Not-Aus funktioniert nicht. Um dies zu vermeiden, gibt es eine Kurzschlussprüfung. Weiter gibt es den Hell- und Dunkeltest. Auch hier will man Fehler in der Verkabelung Diagnostizieren können.

**Security**
- Anlagensicherheit: Zugangskontrolle
- Netzwerksicherheit: Firewall und VPN
- Zugriffschutz: Nutzerverwaltung

[1][4][5][6]


[1]SIMATIC Safety - Projektieren und Programmieren ProgFAILdeDE_de-DE.pdf(Ausgabe 05/2021)

[2]https://new.siemens.com/de/de/produkte/automatisierung/themenfelder/safety-integrated/fertigungsautomatisierung/safety-consulting.html

[3]https://new.siemens.com/de/de/produkte/automatisierung/themenfelder/safety-integrated/fertigungsautomatisierung/support/normen-richtlinien.html

[4]https://new.siemens.com/de/de/produkte/automatisierung/themenfelder/safety-integrated.html

[5]https://new.siemens.com/at/de/produkte/automatisierung/themenfelder/industrial-security.html

[6]https://support.industry.siemens.com/cs/document/77431846/security-bei-simatic-s7-controllern?dti=0&lc=de-WW

[7]https://www.dguv.de/fb-holzundmetall/sg/sg_maf/steuerungen/index.jsp
