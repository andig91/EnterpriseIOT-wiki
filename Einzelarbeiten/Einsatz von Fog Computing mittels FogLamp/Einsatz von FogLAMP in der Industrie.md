# **Einsatz von FogLAMP in der Industrie**

## **Was Ist FogLAMP**

FogLAMP ist ein Open-Source-Projekt für das industrielle Internet of Things (IIoT). Die Software verwendet eine steckbare modulare Architektur, um beliebig viele Sensoren und IIoT-Geräte einfach zu verbinden und zu verwalten.
Durch die Verwendung eines konsistenten Satzes von RESTful APIs zur Entwicklung, Verwaltung und Sicherung aller IIoT-Anwendungen ist FogLAMP eine herstellerübergreifende Lösung. [1]

## **Hintergrund von FogLAMP**

Die Firma Dianomic, welche FogLAMP vertreibt, ist dem Edge-Projekt der Linux Foundation als Premium-Mitglied beigetreten und steuert FogLAMP zur Foundation bei. [1]

## **Cloud Computing**

Unter Cloud Computing versteht man, dass die Daten nicht vor Ort verarbeitet oder gespeichert werden, sondern dass diese in die Cloud, also zB an eine physisch ausgelagerte Serverfarm oder Rechenzentrum, gesendet werden. Der Vorteil ist, dass man als Firma die Kapazitäten für Rechenleistung oder Speicher bei einer externen Firma zukaufen kann und somit nicht verantwortlich ist für das Erhalten der Infrastruktur. Je nachdem, wie viel Rechenleistung man braucht, kann diese aufgestockt werden.

Populär wurde Cloud Computing mit der nahezu sofortigen Übertragung der Daten durch hohe Übertragungsraten. Da es ein Sammelbegriff ist, kann es mit folgenden Punkten zusammengefasst werden:

\-    On-Demand Self-Service: Nutzer können selbstständige mehr Ressourcen anfordern ohne Autorisierung
\-    Broad Network Access: Zugang zur Cloud funktioniert über das Internet, keine Nischentechnologie benötigt
\-    Resource Pooling: Die Kapazität der Rechenleistung in Serverfarmen werden dynamisch vergeben. Daher ist ein Server nicht physisch an eine Firma gebunden, sondern werden im Pool mit anderen geteilt.
\-    Rapid Elasticity: Die angeforderten Kapazitäten werden automatisiert und in Echtzeit vergeben.
\-    Measured Service: Die Nutzung der Cloud wird getrackt und daher der Prozess transparent dargestellt

Für Cloud Computing gibt es auch mehrere verschiedene Schichtmodelle als Angebot:

\-    Infrastructure as a Service (IAAS): Auf dieser Ebene wird nur die Hardware und Infrastruktur angeboten
\-    Platform as a Service (PAAS): Auf dieser Ebene wird zusätzlich zur Hardware auch die Softwareseitige Umgebung gewartet, upgedatet und instandgehalten.
\-    Software as a Service (SAAS): Hier wird alles in einem Paket angeboten. Vorteilhaft für Endkunden, die sich um nichts kümmern müssen. Auch die Software wird bereitgestellt.

[2][3][4]

## **Edge Computing**

Unter Edge Computing versteht man die Ausführung eines Workloads auf Edge-Geräten. Edge Computing wurde in den letzten Jahren populär, da die Bandbreite immer mehr mit Datenübertragungen belastet wurden. Die Hauptgründe für den Einsatz der Edge ist die Zeitrelevanz und das Datenvolumen. Somit werden die Daten vor Ort an der Edge verarbeitet und dann erst an die Cloud gesendet.

<img src="https://dianomic.com/wp-content/uploads/2019/03/hierarchy_updated.png" alt="Kommunikationsmöglichkeiten" style="zoom:33%;" />[1]

## **Fog Computing**

Der Terminus Fog Computing wurde ursprünglich von Cisco geprägt und sollte eine Alternative zu Cloud Computing sein. Mittlerweile ist es eine Erweiterung von Cloud Computing. Es wird als dezentralisierte Computing Struktur beschrieben und befindet sich zwischen der Cloud und dem Edge, also Geräte bzw Sensoren, welche Daten produzieren.
Da die Datenübertragungsmenge limitiert sind, hat sich von Edge Computing, welche die Daten nach der Verarbeitung direkt in die Cloud sendet, Fog Computing begonnen zu etablieren. Da es immer mehr und mehr Edge Devices gibt, konnte die Datenmasse nicht mehr in Echtzeit an die Cloud gesendet werden. Um dieses Problem zu beheben, wurden zwischen dem Cloud Datencenter und den Edge Devices Fog Nodes zwischengeschaltet, welche Daten analysieren und die wichtigen an die Cloud weiterreichen. Damit wird die Datenübertragungsmenge limitiert und unwichtige Daten herausgefiltert.

<img src="https://dianomic.com/wp-content/uploads/2019/03/hierarchy_updated.png" alt="Kommunikationsmöglichkeiten" style="zoom:33%;" />[1]  

## **Architektur**

Bei FogLAMP gibt es North und South Anbindungen. Es basiert auf einem modularen System, dass jederzeit erweitert werden kann. Endbenutzer und Systemintegratoren können FogLAMP wie es ist verwenden. Sie können die Plugins und Dienste, die sie benötigen, auswählen und ein vollständig unterstütztes Paket von Dianomic herunterladen. Die Pakete laufen auf praktisch jedem Linux-Derivat auf Smart Gateways, virtuellen Maschinen, in Containern oder direkt auf Bare Metal Systemen. Durch die modulare Architektur von FogLAMP kann das Schreiben eines neuen Python-Plugins leicht durchgeführt werden.

<img src="https://dianomic.com/wp-content/uploads/2019/03/FogLAMP_Architecture_Base_bright.png" alt="Kommunikationsmöglichkeiten" style="zoom:33%;" />[1]  

[1]: https://dianomic.com/platform/foglamp/
[2]: https://www.ionos.at/digitalguide/server/knowhow/cloud-computing-definition-erklaerung-geschichte/
[3]: https://www.redhat.com/de/topics/cloud-computing/cloud-vs-edge
[4]: https://www.simplilearn.com/edge-computing-vs-cloud-computing-article
