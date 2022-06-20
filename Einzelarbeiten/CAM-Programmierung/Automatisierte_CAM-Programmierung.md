# Automatisierte CAM Programmierung

Autor: Martin Haas (se211304)

## CAM – Definition
Die Bezeichnung CAM steht für Computer-Aided Maunfacturing. Es gehört zu dem Überbegriff CAx, der computergestützte Fertigungssysteme zusammenfasst. CAM ist zuständig für die Steuerung und Überwachung von Fertigungsprozessen. Es ist einer der Hauptbestandteile des Computer-Integrated Manufacturing (CIM), ohne den die vollintegrierte computergesteuerte Produktion nicht funktionieren würde. Bei CAM laufen Informationen und Daten aus dem technischen Bereich, wie Modelle und Skizzen, aber auch Informationen aus dem geschäftlichen Planungsbereich, zum Beispiel Produktionsplanung, zusammen. Diese werden dann durch das CAM-System verarbeitet und an NC-Maschinen weitergegeben, welche dann ein Produkt erzeugen. Auf diesen letzten Aspekt wird im Folgenden eingegangen.

## CAM Programmierung
Unter dem Begriff CAM Programmierung versteht man das Erstellen von NC-Programmen, welche an eine CNC-Maschine übergeben werden, die dann das Produkt selbstständig fertigt. Der herkömmliche Weg besteht darin, dass als erstes ein 3D-CAD-Modell erstellt wird. Anschließend erstellt ein Programmierer aus den daraus generierten Daten ein NC-Programm, das die notwendigen Abläufe enthält, die die CNC-Maschine erledigen muss. Dieser Vorgang kann, je nach Komplexität des Modells, einige Zeit in Anspruch nehmen. Außerdem besteht die Gefahr von menschlichen Fehlern, 
wie Flüchtigkeitsfehler beim Schreiben des Codes oder Ungenauigkeit.

Um solche Fehler zu unterbinden und den Prozess vom Modell zum fertigen Produkt zu beschleunigen gibt es die Möglichkeit, diesen Schritt zu automatisieren. Hierbei wird aus dem dreidimensionalen CAD-Modell automatisch ein NC-Code erstellt. Die Erstellung dieses Programmes zählt dann zur Arbeitsvorbereitung und geschieht getrennt von der CNC-Maschine in einem Büro auf einem anderen Computer. Das bedeutet, dass der Mitarbeiter nicht mehr direkt in die Produktionshalle zum Gerät gehen muss, um ein Programm einzugeben, sondern dieses einfach aus dem Büro an die CNC-Maschine übergeben kann. Außerdem können Informationen, wie Werkzeuglisten und Aufspannpläne direkt vom Programm erstellt werden und müssen nicht mehr von Hand geschaffen werden. Zu beachten gilt jedoch, dass dies nur funktioniert, wenn es eine einheitliche Arbeitsumgebung gibt, also dass alle Systeme miteinander kommunizieren können und kein Datenverlust stattfindet.

## Vorteile der automatisierten CAM-Programmierung
- **Keine Abweichungen durch Bedienung:** Durch ein automatisiertes Erstellen von NC-Programmen fällt die Möglichkeit von Abweichungen durch unterschiedliche Programmieroberflächen an der CNC-Maschine weg.

- **Standardisierung und Replizierbarkeit:** Bearbeitungsprozesse können, da sie über dieselbe Schnittstelle laufen standardisiert werden und hinterlegt werden. Diese Informationen stehen dann allen zur Verfügung, wodurch sich Abläufe leichter replizieren lassen.

- **Weniger Stillstandszeiten:** Die in der Arbeitsvorbereitung generierten Programme werden direkt von der CNC-Maschine eingelesen und es muss sich niemand am Shop-Floor um das Programmieren kümmern. Dadurch kann die Maschine meist durchgehend in Betrieb sein.

- **Kontrolle:** Durch eine Simulation des Programms können Fehler und Kollisionen erkannt werden, bevor sie tatsächlich auftreten würden. Außerdem kommt es zu keinen Fehlern beim Schreiben des Codes, da er automatisch generiert wird.

- **Geringere Rüstzeiten:** Aufgrund der im Vorfeld automatisch generierten Werkzeugliste kann man alles Notwendige schneller vorbereiten.

- **Weniger Aufwand für die Mitarbeiter:** Durch eine größtenteils automatische Generierung aller wichtigen Daten fällt ein erheblicher Arbeitsaufwand weg und es werden Kapazitäten für andere Aufgaben frei.

## Nachteile
- **Einspannung:** Bei Modellen, die nicht in nur einer Lage gefertigt werden können, muss die Einspannung geändert werden. Dadurch muss das Programm angepasst werden. Dies braucht wiederum Erfahrung, die ein Mitarbeiter mitbringt, nicht aber das automatisch erstellte Programm.

- **Übertragbarkeit:** Erstellte Makros müssen angepasst werden an ein neues Werkstück. Um möglichst viele Varianten abzudecken sind die Auswahlregeln für das Bearbeitungsverfahren überaus komplex zu gestalten. Dies kann einen erheblichen Mehraufwand darstellen, vor allem, wenn es keine klaren Regeln dafür gibt und mehrere Verfahren theoretisch möglich wären.

- **Informationsverlust:** Wenn in einer Fertigungsstätte unterschiedliche Systeme zum Einsatz kommen, ist es möglich, dass es zum Verlust von Information kommt. Beispielsweise kann die Information verloren gehen, ob an einer Stelle eine einfache Bohrung gemacht werden soll oder ob es sich doch um ein Gewinde handelt. Um dies zu vermeiden, muss man darauf achten ein durchgängiges System zu verwenden.

- **Kosten:** Die Umstellung auf eine automatisierte CAM-Programmierung ist meist mit hohen Kosten verbunden, da in vielen Produktionsunternehmen noch kein einheitliches System besteht und dies erst angeschafft werden muss.

- Bei fehlenden Informationen aus vorangegangenen Prozessen kann die automatisierte Programmierung nicht richtig arbeiten. Bei manchen Fertigungsschritten gibt es unterschiedliche Herangehensweisen. Die richtige Methode muss dann oft trotzdem ein Mitarbeiter aufgrund von Erfahrungswerten auswählen.

## Fazit
Abschließend man feststellen, dass eine automatisierte CAM-Programmierung einen großen Nutzen darstellen kann. Die vollständige Automatisierung hat allerdings noch Probleme, sich unterschiedlichen Situationen anzupassen. Eine teilweise Automatisierung ist allerdings sicher von Vorteil und kann den Produktionsprozess durchaus optimieren und schlanker gestalten.

## Quellen
[1] K. E. Kurbel, Enterprise Resource Planning and Supply Chain Management. Functions, Business Processes and Software for Manufacturing Companies. Berlin: Springer, 2013.

[2] [WeSt GmbH, CAM-Programmierung: Möglichkeit und Grenzen der CAM-Automatisierung.](https://www.west-gmbh.de/blog/cam-pogrammierung-automatisierung)

[3] [WeSt GmbH, 7 Vorteile von CAM Software.](https://www.west-gmbh.de/blog/7-vorteile-von-cam-software)

[4] [Tebis, CNC-Programmierung - automatisiert und sicher.](https://www.tebis.com/de/software/cam-software/cnc-programmierung)


