# Echtzeit-, Zeitzyklus- und Echtzeitanforderungen an SPSen in der Industrie und Verbesserungsvorschläge:

 

## Definitionen:

### Echtzeit:

Unter Echtzeit oder auch Real-Time im Zusammenhang mit Datenübertragung oder auch Datenverarbeitung versteht man, in einem industriellen Kontext, eine Zeitanforderung an den SPS-Zyklus. Man unterscheidet hier zwischen :

- Harter Echtzeit (definierte Reaktionszeit wird nie überschritten)

- Weiche Echtzeit (geforderte Reaktionszeit wird nur statistische gewährleistet)

- Feste Echtzeit (strengere Reaktionszeitanforderungen als bei der Harten) (1)

### Jitter:

Unter dem Begriff Jitter oder auch Latenz genannt, versteht man die zeitlichen „Pausenintervalle“ die zwischen zwei gesendeten Signalen oder Paketen auftreten und werden grob in gewollt (zur Differenzierung von Signalen) und in ungewollte (treten meist durch Paketkollisionen oder andere Interferenzen auf und behindern dadurch die Signalübertragung) Jitter-Durationen eingeteilt.(2) 

### Zykluszeit:

Die Echtzeit hängt unmittelbar von der Zykluszeit, oder auch dem Zeitzyklus einer SPS genannt, ab. Diese Beschreibt die maximale Zeit pro Abarbeitung des Anwender-Programms die die SPS in Anspruch nehmen darf, ohne dass eine Zykluszeitverletzung auftritt.

Während eines Zyklus laufen Folgende Schritte ab:

-    Clock-Interrupt erkennen und neuen Zyklus triggern

-    Einlesen und determinieren der Ist-Zustände der Eingänge und des Betriebszustandes

-    Übersetzten der Eingänge in digitale Merker/Signale via A/D Konverter

-    Bearbeiten des User-Programmes

-    Via A/D Konverter digital gesetzte Ausgänge auch an den Ausgängen setzten

-    Controller-Variablen setzten 

-    Neuen Zyklus aufrufen (3)

Die Zykluszeit ist für gewöhnlich dynamisch eingestellt, also kann sie der Bearbeitungszeit des Anwender-Programm angepasst werden, darf trotzdem die Maximale nicht überschreiten. Dies kann für gewöhnlich durch einen Programmfehler oder anderen technischen Defekt auftreten.

 

## Anforderungen und Verbesserungen:

Mit der stetigen Entwicklung der Industrie und deren Standards in der Produktion steigen natürlich auch die Anforderungen an die verwendete Technik. 

Wo viele Betriebe noch mit veralteten Komponenten und/oder Standards arbeiten, gibt es ebenso viele Unternehmen, welche am neuesten Stand bleiben wollen und versuchen eine höchstmögliche Effizienz zu erzielen.

Um dies zu erreichen wird stets in den Bereichen der SPS-Hardware sowie Software geforscht und neue Erkenntnisse vorgestellt.

Nimmt man beispielsweise den Begriff der Echtzeit. Dieser wir wie im Abschnitt „Definitionen“ definiert und beschreibt daher keine genormte Zeitdauer. Nichts desto trotz, gibt es hohe Ansprüche an die Echtzeitkommunikation. Nach Jasperneite gibt es eine klare Separierung der Anforderungen innerhalb der klassischen Automationspyramide: Auf dem Cell-Level liegt die Echtzeitanforderung von 1ms bis hin zu 200ms und auf Machine-Level liegt diese bereits bei 16ms bis hin zu wenigen zehn Mikrosekunden (31,5μs). Um diese Zeiten gewährleisten zu können wurden Protokolle wie PRP (Parallel Redundancy Protocol) vorgestellt und eingerichtet.

Das PRP funktioniert auf einem dualen LAN Prinzip. Wo der Empfänger sowie Sender jeweils in LAN_A und LAN_B hängen. Der Sender speist die Packages in beide Netze ein und wobei diese mit einer Sequenznummer im Tailer im PRR-Frame ausgestattet sind. Wodurch bei Störungen in einem LAN die Packages nach wie vor in der angeforderten Zeit ankommen und somit eine verlässliche Übertragung gegeben ist. (4)

 

Die Latenz/Jitter-Anforderungen sind natürlich stark mit denen der Echtzeit verbunden, da diese stark von der auftretenden Latenz abhängig sind.

Ein im Jahr 2018 vorgestelltes Konzept befasst sich mit den TSN (Time-Sensitive Networking) Erweiterungen für den Ethernet-Standard. OPC UA PubSub wurde in diesem Zusammenhang vorgestellt. Es handelt sich hierbei um ein Protokoll für echtzeitsensible Netzwerkanwendungen.

Der vorgestellt Part 14 des Protokolls (OPC18) bedient sich der Telegramm-Nachriten mit definiertem Aufbau, welcher in klassischen Feldbussen verwendet wird. Der Nachrichtenaufbau wird als PublishedDataSet definiert und bedient sich ebenfalls eines UDP-basiertem Protokoll (UADP). Eine zusätzliche Eigenschafft zu der Multicast-Natur der gesendeten Informationen zur Auslagerung der Nachrichtenverteilung in die Netzwerkinfrastruktur ist die Übertragung von PubSub über Ethernet-Frames wodurch es sich um eine Layer 2 (OSI-Modell) Adressierung handelt.

In (Feld-)Tests konnte durch die Implementierung des Protokolls beobachtet werden, dass der Jitter in den Verwendeten Systemen von mehreren zehn Mikrosekunden durch die Verwendung des Protokolls auf einige hundert Nanosekunden reduziert werden konnte, was einen Verbesserungsübersetzungsfaktor von 100:1 darstellt.(5) 

 

Zeitzyklus-Anforderungen werden vor allem bei Sortier- und Produktionsvorgängen immer wichtiger. Nimmt man beispielsweise ein Profibusnetz mit Master-Slave Komponenten, so sind Übertragungszeiten von 70μs möglich. Um diese Geschwindigkeiten und damit auch den gesendeten Inhalt bereitstellen zu können sind Zykluszeiten von ca. 530μs erforderlich. (6) 

Da die Zykluszeiten je nach Anwendungszweck so kurz wie möglich gehalten werden sollten, müssen auch die einzelnen durchgeführten Operationen möglichst schnell ablaufen. Bei der Siemens S7-1500er beispielsweise werden einzelne Operationen im ns-Bereich abgearbeitet: 

| Operationen:         | Zeiten (von bis, abhängig von Modell) |
| -------------------- | ------------------------------------- |
| Bitoperationen       | 1 – 60ns                              |
| Wortoperationen      | 2 – 72ns                              |
| Festpunktarithmetik  | 2 – 96ns                              |
| Gelitpunktarithmetik | 6 – 384ns                             |

Diese Geschwindigkeiten sind mehr als beeindruckend und mittlerweile auch bereits Industriestandard in hochwertigen Anlagen.(7)

Im Normalfall arbeiten SPSen das Anwender-Programm via Controller ab, die Firma Hermann Zander hingegen versucht die Zykluszeit via FPGA (Field Programmable Gate Array) also konfigurierbaren Hardwarekomponenten die dem eingespieltem Programm gleichen einzusetzten. Durch diese Herangehensweise sollen Zykluszeiten zur Gänze eliminiert werden. (8)

 

(1)  (Wörn, Echtzeitsysteme, Grundlagen, Funktionsweise, Anwendungen, 2005)

(2)  (Holleczek, Pearl 95 Workshop über Realzeitsysteme Fachtagung der GI-Fachgruppe 4.4.2 Echtzeitprogrammierung, 1995)

(3)  (Dirnberger, Dirnberger2018-4_Industrielle Automatisierungssysteme.pdf, 2018)

(4)  (Jasperneite, Kommunikation und Bildverarbeitung in der Automation, 2018)

(5)  (Jasperneite, Kommunikation und Bildverarbeitung in der Automation, 2018)

(6)  (Schuller, Prozesssignalkopplung bei der Realzeitsimulation komplexer Produktionsmaschinen, 1998)))

(7)  (Siemens, s71500_cycle_and_reaction_times_function_manual_de-DE_de-DE, 2021)

(8)  (Dipl.Ing. Stotz, https://www.elektrotechnik.vogel.de/superschnelle-sps-ohne-zykluszeit-a-257043/, 2010)
