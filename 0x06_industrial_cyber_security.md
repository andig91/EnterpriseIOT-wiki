# Industrial Cyber Security

Autoren: Elmar-Rene Risska, Eduardo Vizcaya, Herbert Dirnberger



In unserer heutigen Welt sind immer mehr Geräte intelligent, miteinander vernetzt und kommunizieren sowohl miteinander, als auch mit uns. Dies bringt eine Unzahl an Vorteilen für unser tägliches Leben mit sich, jedoch ergeben sich auch Abhängigkeiten welche im Falle eines Ausbleibens dieser „Vorteile“ mit großen Komplikationen verbunden sind. Mit der steigenden Vernetzung steigt jedoch auch die Gefahr für Angriffe auf derartige Netzwerke, sowohl im privaten Bereich als auch in der Industrie. 

Als solche Anlagen können nicht nur Fertigungsbetriebe gesehen werden, vielmehr auch die kritische Infrastruktur worunter Kraftwerke jeglicher Art, Wasseraufbereitungsanlagen, Informations- und Kommunikationstechnologie, Krankenhäuser, öffentlicher Verkehr und einige weitere. 

Um es den zu schützenden Betrieben, den Herstellern von Schutzmechanismen sowie den Firmen welche sie in bestehende oder neue Anlagen implementieren (Integratoren), einfacher zu machen und einen Qualitätsstandard einzuziehen wurde die Norm IEC 62443 entwickelt. Gemäß dieser Norm ist es essenziell einheitliche Vorgaben zu schaffen um Betreiber, Integratoren und Herstellern aufeinander abzustimmen, da nur mit ineinandergreifenden Maßnahmen ein optimaler Schutz möglich ist.

Grundsätzlich werden diese drei Aufgaben von separaten Unternehmen durchgeführt, jedoch ist es in größeren Firmen durchaus üblich, dass eigene Abteilungen innerhalb der Firma für die jeweiligen Sparten zur Verfügung stehen. 

## Betreiber (Asset Owner)
Unter Betreiber versteht man denjenigen, welcher für den Betrieb, die Wartung, den Aufbau bzw. Abbau einer Automatisierungsanlage zuständig ist. Die Wartung wird hierbei jedoch nicht zwingend allein durch den Betreiber durchgeführt, es besteht auch die Möglichkeit dies gesondert an spezialisierte Firmen auszulagern.

Der Betreiber versorgt hierbei Hersteller sowie Integratoren mit den im Vorfeld bereits bekannten und vorhersagbaren Parametern und Größen die während des Betriebs verwendet werden um einen durchgängigen Ablauf zu gewährleisten.

## Hersteller
Der Hersteller ist für die Entwicklung und Vertrieb von Automatisierungskomponenten verantwortlich. Unter Umständen kann der Hersteller auch als externer Dienstleister für die Wartung der Komponenten beauftragt werden. 

## Integrator
Der Integrator ist für das Design, sowie die Inbetriebsetzung der verschiedenen Komponenten verantwortlich. Zwischen Integrator und Betreiber sind enge Absprachen notwendig, da beide für die Planung der Automatisierungslösungen verantwortlich sind, um nachfolgend dem Hersteller die genauen Spezifikationen mitteilen zu können.

Häufig werden deshalb Begriffe wie Infosecurity oder IT-Security verwendet die, auch wenn Ähnlichkeiten im Namen bestehen, zwei unterschiedliche Themen umfassen. Um sich im industriellen Bereich von der IT-Security im Büroumfeld abzugrenzen wird deshalb der Begriff „Industrial Security“ verwendet. 

## Infosecurity
Bei Infosecurity steht die Sicherheit der Informationen bzw. Daten im Vordergrund. Dies macht besonders in Büroumgebungen Sinn, da häufig eine Vielzahl von Leuten aufhältig sind, oft auch Betriebsfremde Personen wie Lieferanten, Reinigungskräfte oder externe Dienstleister. Durch die Anwesenheit dieser Personen besteht leicht die Gefahr, dass vulnerable Daten oder firmeninterne Schriftstücke in die falschen Hände geraten könnten. Dies ist besonders problematisch, wenn im Anschluss Lösegeldforderungen erpresst werden, um das Veröffentlichen dieser Informationen zu verhindern.

## IT-Security
Die IT-Security beschäftigt sich beispielsweise damit ein System vor einem unbefugten Zugriff zu schützen, der es in seiner Gesamtheit lahmlegen könnte. In einer Industrieanlage könnte ein Ausfall einer Station oder eines Zwischenschrittes im Gesamtablauf zum kompletten Stillstand der Anlage führen. Um dies zu verhindern, können mehrere Methoden wie zb. redundante Systeme, Nachlaufzeiten welche eine Pufferzeit schaffen können oder verschiedene, einzelne Schutzbereiche eingezogen werden.

# Defense in Depth
„Defense in Depth“ werden Sicherheitsmaßnahmen genannt bei denen mehrere Schutzmechanismen zum Einsatz kommen. Diese werden wiederum wie Verteidigungslinien aufgebaut, die jeweils einzeln durchbrochen werden müssen. Ähnliche Strategien sind auch im militärischen Bereich zu finden und haben sich über alle Epochen als funktionell erwiesen. Sollte ein "Schutzring" durchbrochen werden, steht man beim Nächsten Schutzring wieder am Anfang und benötigt eventuell Equipment welches zuvor nicht abgeschätzt werden konnte und nun nicht für einen Angriff zur Verfügung steht.

Um zu verstehen wie man sich effektiv schützen kann, muss zunächst aufgezeigt werden an welchen Stellen Angriffe geschehen können. Ein derartiger mehrschichtiger Schutz kann durch verschiedene Teilkomponenten erzielt werden, wie zum Beispiel ein Awarenesstraining für Mitarbeiter, technische Komponenten wie Firewalls, Router, Antivirensysteme, VPN-Netzwerke und vieles mehr.

## Verteidigungsringe
Im Sicherheitskonzept liegt daher der erste Verteidigungsring beim Betreiber einer solchen Anlage. Er hat die Verantwortungen zur implementierung notwendiger Schulungen, welche Mitarbeiter absolvieren müssen, als auch bauliche Maßnahmen wie z.B. eine Abzäunung des Firmengeländes, versperrbare Bereiche mit Zutrittsregelungen sowie technische Maßnahmen wie Wartezeiten zwischen Anmeldeversuchen, 2 Faktor-Authentifizierungen,  Verschlüsslungen eigener Daten bzw. Backups dieser. Bei der Aufzählung handelt es sich nicht um die taxative Aufzählung möglicher Maßnahmen sondern lediglich um einige Beispiele. Den Schutz sowie die Funktion welche dadurch gewährleistet wird, ist im nachstehenden Kapitel der Coutnermeasures beschrieben.

Ein weiterer Verteidigungsring wird durch die Segmentierung des Netzwerkes in kleinere Subnetzwerke realisiert. Dies geschiet um eine komplette Durchgängigkeit im System zu verhindern. In diesen Subnetzwerken sind wiederum eigene Zertifikate, Passwörter/Schlüssel und Firewalls vorhanden. Dadurch können Mitarbeiter lediglich auf die Bereiche zugreifen, zu denen sie Zugriff haben müssen. Die Verbreitung von infizierten Geräten kann somit im Ernstfall lokal gehalten und Backdoors nach außen vermieden werden. Weiters ergibt sich durch solche Insellösungen der Nutzen, dass beim Ausfall einer Maschine nicht die gesamte Produktion ausfällt, sondern nur einzelne Maschinen.

Der innere Verteidigungsring wird oftmals durch Automatisierungslösungen innerhalb des Abschnittes oder auf den Geräte selbst realisiert. Beispielhafte Anwendungen sind Virenscanner, Verschlüsselungsalgorithmen oder Anmeldeverzögerungen. 

# Threats and Risks 
## Open Source Intelligence (OSINT)
Ein großes Sicherheitsrisiko stellen Angriffe auf Basis von OSINT dar. Bei OSINT werden verhältnismäßig einfach zugängliche Daten dafür verwendet, vorhandene Sicherheitsrisiken auszukundschaften und weitere Angriffe darauf zu planen. Eines der Haupttools welches dabei Verwendung findet ist die Suchmaschine „google.com“. 

Durch den Einsatz der richtigen Operatoren können Suchanfragen so präzise gestaltet werden, dass Dateien zugänglich werden, welche nicht veröffentlicht hätten werden sollen. Über diese Suchanfragen ist es möglich Mailadressen, Passwörter, Finanzdaten oder allgemeine Sicherheitslücken aufzufinden. 

Häufig verwendete Operatoren sind:<br />

|    Operator       | Beschreibung                                                         | 
|:------------------|:---------------------------------------------------------------------|
| „Max Mustermann“  | „“ Gibt exakte Treffer zur angegeben Zeichenfolge aus                | 
| Site:beispiel.com | Es werden nur Ergebnisse von dieser Domain angezeigt                 |
| Filetype:pdf      | Zeigt nur mehr Dateien im gewünschten Format an                      | 
| Inurl:/admin      | Gibt nur mehr URLs aus welche die angegebenen Zeichenfolge aufweisen |
| Intext:beispiel   | Zeigt Datein an, in welchen der angegebene Suchbegriff enthalten ist |


Weiters können auch Mitarbeiter das Ziel eines solchen Angriffes werden. Durch Social Media Plattformen und der Darstellung des privaten Lebens auf eben diesen ist es möglich, sich ein mitunter sehr präzises Bild von Personen zu machen. Je nachdem wie die Sicherheits- und Datenschutzeinstellungen der jeweiligen Profile konfiguriert sind, können der gesamte Name, das Geburtsdatum, Familienmitglieder, Freunde, Gewohnheiten, Besitztümer, Fotos, und vieles mehr abgegriffen werden.  

Dadurch ergeben sich nicht nur für diese Person Risiken, sondern auch für das Unternehmen in dem diese angestellt sind.  Eine mögliche Bedrohung sind Erpressungsversuche, bei denen Daten, Fakten und Fotos an das jeweilige Unternehmen übermittelt werden, wenn nicht gewisse verbotene firmeninterne Handlungen durchgeführt werden oder gar Informationen weitergegeben werden.

Häufiger jedoch werden die durch OSINT gewonnen Daten dafür verwendet, sogenannte Phishingattacken vorzubereiten. Hierbei werden an die Firmen-Mailadressen der Personen Mails versendet die oftmals auf den ersten  Blick nicht von echten Mails zu unterscheiden sind. 
Die darin enthaltenen weiterführenden Links sind, sobald einmal geöffnet, das Einfallstor für Schadsoftware. Durch den nicht immer sofort sichtbaren Schaden haben derartige Viren wiederum die Möglichkeit über einen längeren Zeitraum firmeninterne Daten abzugreifen und anschließend das System und alle erreichbaren Backups zu verschlüsseln. Nachdem alle erreichbaren Daten verschlüsselt wurden, werden meist Lösegeldforderungen geschickt da andernfalls die Daten unbrauchbar bleiben und/oder veröffentlicht werden, was in beiden Fällen zu sehr hohen Schadenssummen bis hin zum Konkurs einer Firma führen kann. 

Eine weitere Gefahr beinhalten Geräte, welche ihren Produktlebenszyklus überschritten haben oder nicht regelmäßig mit Sicherheitsupdates versehen werden. Diese Geräte öffnen Angreifern die Möglichkeit gezielt Schadsoftware zu Injizieren, da sie im Netzwerk kommunizieren dürfen und Datenpakete meist nicht genauer überprüft werden. Sind sie einmal übernommen worden können sie sich im gesamten Netzwerk ausbreiten. Bei solchen Geräten handelt es sich häufig um Kameras oder Sensoren innerhalb einer Anlage, da auch diese Geräte mittlerweile schon über Hardware verfügen auf denen Betriebssysteme implementiert werden können. 

Bereits mit Google als Suchmaschine sind offene Kameras und Router im Internet erreichbar. Da ersichtlich ist um welches Gerät es sich handelt und häufig Benutzerhandbücher frei verfügbar sind können diese Geräte leicht übernommen werden. Bei vielen dieser Geräte werden die Admin-Passwörter nicht gewechselt, wodurch die Möglichkeit besteht, nach dem Zugriff mit dem standardmäßig eingestellten Passwort alle restlichen Einstellungen zu ändern und darüber hinaus auch auf Geräte zuzugreifen, welche wiederum mit dem befallenen Gerät verbunden sind. 

Jedoch gibt es auch abseits von Google noch andere Suchmaschinen wie Censys oder shodan.io, welche ungeschützte Geräte und Ports ersichtlich machen.

# Shodan.io / Censys

Suchmaschine für Sicherehitslücken, verwendbar von Geräten im Internet
Vollen Funktionsumfang erst nach Registrierung
Suchmaschine durch Begriffe wie zb: Art des Gerätes, Land, Betriebssystem, etc. eingrenzbar
Daten oft nicht lange gültig. 
Ermittelte IP-Adresse ermöglicht oft lokalisation des Gerätes.
Shodan ermittelt IPs unter anderem durch zur bereitstellen eines Zeitservers, dabei erfolgt ein Scan
Je häufiger die IP gewechselt wird, desto schwerer ist der Scan
Gefundene Lücken oft Portnummern von Programmen

# Controls/Countermeasures

- Mitarbeiterschulung: Die Schulung der Mitarbeiter ist eine der wichtigsten Methoden um Probleme zu vermeiden. Wenn die Mitarbeiter wissen was sie tun, ist es weniger wahrscheinlich, dass sie Risiken für das Unternehmen darstellen.

- Physische Security: Diese Art der Sicherheit ist eine der grundlegendsten. Sie basiert darauf, dass nur autorisiertes Personal die Anlage oder Teile davon betreten kann.

- Patching: Ein Patch ist ein Software-Update. Patches werden normalerweise verwendet, um die Stabilität und Funktionalität zu verbessern. Sie dienen jedoch eher nicht der Verbesserung der Sicherheit, obwohl diese dennoch sehr wichtig sind. In der Industrial Cyber Security ist das Erstellen eines Patches nicht so einfach wie in der IT, da man sich normalerweise 20 Minuten lang nicht vom System trennen kann, während das Update durchgeführt wird. Es gibt einen empfohlenen Prozess um zu entscheiden was zu tun ist, wenn man einen Patch in ICS durchführen muss; dieser ist in mehrere Schritte unterteilt.

Der erste Schritt besteht darin zu prüfen, ob dieser Patch das jeweilige ICS betrifft. Für den Fall, dass er Auswirkungen hat, wird der nächste Schritt in Betracht gezogen: Die Überprüfung ob es einen Workaround gibt, zum Beispiel ob ein Virtual Patch möglich ist.

Diese Form des Patchens schützt im Netzwerkbereich, Beispiele hierfür sind IPS- und Firewall. Der Vorteil hierbei ist, dass sie etwas schützen können ohne es vom System zu trennen, und sie genau vor der gefundenen Schwachstelle schützen können. Das Problem dabei ist, dass viele Unternehmen nach der Erstellung des virtuellen Patches aufhören normale Patches zu erstellen. Der nächste Schritt besteht darin sich zu fragen, ob die Notwendigkeit das Asset verbunden zu lassen das Risiko aufwiegt. Wenn das Risiko größer ist, sollte der Patch sofort durchgeführt werden. Wenn die Notwendigkeit, verbunden zu bleiben, größer ist sollte man bis zur nächsten Wartungsroutine mit dem Patch warten.

- Whitelisting: Stellt eine Möglichkeit dar um Malware zu verhindern. Whitelisting funktioniert so, dass nur einige ausführbare Dateien und Anwendungen erlaubt sind und alles andere was das System erreicht, blockiert wird. Aufgrund der Art der Zugriffe im OT ist diese Art der Abwehr sehr effektiv. Sie steht im Gegensatz zu einem normalen Antivirus-Programm, das ständig aktualisiert werden muss und viel Dateiaustausch benötigt.


# Industrial Cyber Security Roadmap

Bevor wir mit der Erstellung einer Roadmap beginnen, müssen wir uns bewusst werden, dass Cyber Security OT/ICS nicht dasselbe ist wie Cyber Security in der IT. Im nächsten Schritt muss man sich darüber klar werden, welche Ziele das Unternehmen verfolgt und was man durch die Verbesserung der Sicherheit erreichen will. Kurz gesagt: Was ist wichtig und was ist das Ziel?

Von diesem Punkt aus kann man damit begonnen sich mit den Herausforderungen zu befassen, die einem begegnen werden. Grundsätzlich stellt die größte Herausforderung den Mangel an Wissen im Bereich Industrial Cyber Security dar, was auf den Mangel an Fachleuten im Unternehmen zurückzuführen ist. Ein weiteres Beispiel ist die Vorstellung, dass sich jeder Software-Ingenieur auch um die Sicherheit kümmern kann. Häufig glauben viele Unternehmen, dass sich der firmeninterne IT-Bereich um alles kümmern kann und über das notwendige Knowhow verfügt. Deshalb ist es wichtig, von Anfang an klarzustellen, dass eine Roadmap von einem Experten erstellt werden muss und nicht von einem Software-Ingenieur oder dem IT-Abteilung.

Eine Roadmap muss sinnvoll sein. Das heißt es muss bekannt sein, welches Asset oder Projekt Priorität hat und was man erreichen will.
Die Roadmap muss mit den Zielen des Unternehmens übereinstimmen. Sie muss relativ einfach zu verstehen sein und ständig aktualisiert und angepasst werden. Es ist bekannt, dass sich die Dinge im Bereich Cyber Security sehr schnell entwickeln, was bedeutet, dass jede Roadmap für dieses Gebiet spätestens alle zwei Jahre überarbeitet werden sollte. Ein weiterer sehr wichtiger Aspekt ist das Wissen, dass jede Roadmap Sicherheitsstandards erfüllen muss. Gleichzeitig soll diese aber auch flexibel sein, da jede Roadmap am Ende einzigartig ist und dies auch sein muss, um an das Unternehmen angepasst zu sein.


## Awareness

Es ist sehr wichtig, die Mitarbeiter zu schulen, die mit OT/ICS Cyber Security relevanten Bereichen in Kontakt kommen werden. An dieser Stelle ist es wichtig zu verstehen, was für einen Wissenstand jeder einzelne Mitarbeiter benötigt, der Geräte innerhalb einer Anlage bedient. Die Mitarbeiter die viel Kontakt und auch viele Zugänge zum System haben, benötigen ein tieferes Wissen, welche Handlungen gefahren für die Industrial Cyber Security darstellen. Diese Mitarbeiter sollten nicht nur die Risiken verstehen und kennen, sondern auch eigenständig Bedrohungen schnell erkennen bzw. verhindern können. Ebenso wird vom Arbeitgeber erwartet, dass er weiß, wie er sich im Falle einer Bedrohung verhalten muss und wie er diese so schnell wie möglich beseitigen kann.

## Asset inventory

Es ist wichtig zu wissen, dass der Asset-Bestand in ständiger Bewegung ist und daher auch ständig gewartet werden muss. In der Industrial Cyber Security muss man, um eine Asset-Inventur durchführen zu können, nicht nur wissen wie viele, sondern auch so viel wie möglich über diese Assets wissen. Es wird empfohlen, dass es sich nicht nur um Auflistungen handelt, sondern um ein leicht einsehbares Inventar. Das Inventar muss alle Software- und Hardware-Assets enthalten. Von jedem Asset muss man wissen, wie aktuell es ist, von wem es verwendet wird oder damit in Kontakt kommt und welche Schwachstellen es hat. Hat dieses Asset Schwachstellen dann muss dokumentiert sein, wie bei Problemfällen damit umgegangen wird (entweder schützen oder Daten beseitigen). 

Des weiteren muss die Auflistung Infos darüber enthalten, ob das Asset über eine Art Schutz verfügt und wenn es einen Backup gibt, wie oft dieses aktualisiert wird. Hier ist anzumerken, dass nicht bei allen Assets die ein Backup haben, dieses jeden Tag aktualisiert wird. Das Wichtigste ist die mögliche Auswirkung dieses Assets innerhalb des OT. Es ist wichtig, so viele Informationen wie möglich im Inventar zu haben. Dieser letzte Punkt entscheidet, wie wichtig dieses Asset ist und entscheidet somit, ob und wie stark einer der anderen Aspekte des Assets verbessert werden muss. Innerhalb des Asset-Inventars ist die Hardware und die Software genauer zu kontrollieren, also sollten Hardware und Software in der Benutzeroberfläche getrennt werden, um die Risiken besser sichtbar zu machen.

Bei der Hardware sollten Punkte wie die Art des Betriebssystems und die Herstellung der verschiedenen Assets gegenübergestellt werden. Natürlich muss auch die Bedeutung der Assets definiert werden und welche die meisten Risiken für die Anlage mit sich bringen. Für seinen Anteil an der Software ist es wichtig zu wissen, wer sie verwaltet, wer sie erstellt hat und wie zuverlässig sie ist. Im Schwachstellenbereich empfiehlt es sich, die Art des Assets zu markieren, das die Schwachstelle mit sich bringt, welche Auswirkungen diese Schwachstelle hat um so das Gesamtrisiko pro Asset berechnen zu können. Auf diese Weise können Sie berechnen, welche die anfälligsten und riskantesten Assets innerhalb des Systems sind.

Man soll auch eine gute Übersicht über Patches haben, die den aktuellen Status und die Kategorie der Patches beschreibt. Des weiteren braucht man auch eine Übersicht, welches wichtige Update in Zukunft ansteht um so in der Lage zu sein, die Wichtigkeit und Dringlichkeit der Aktualisierung eines Patches zu kennen. 
Es ist wichtig, das Inventar automatisieren zu können, um aktuelle Daten zu haben. Was etwas kompliziert ist, da man hier keine Scans, Pings, Broadcasts oder ähnliche Anwendungen verwenden möchte, da die Verwendung dieser die Anfälligkeit des Systems erhöhen.

Zusammenfassend sind die Vorteile einer funktionalen und automatisierten Bestandsaufnahme: Sie sparen Zeit in der Zukunft und helfen bei der Sichtung von Schwachstellen und Risiken.

## Risks and Impacts

Hier muss man zunächst überlegen, was im schlimmsten Fall passieren könnte. Dies wird als sogenannter Boom der Cyber Security gewertet. Von hier aus können zwei Richtungen eingeschlagen werden. Die linke Seite des Booms: alles, was getan wird, um das Erreichen des Booms zu verhindern. Auf der rechten Seite des Booms: alles was getan wird, nachdem der Boom vorbei ist. Auf der rechten Seite ist es wichtig, den Boom zu erkennen.

Die Erkennung  muss schnell erfolgen, um ehestmöglich zu handeln, damit die Funktion des Systems wiederhergestellt werden kann. Einen Boom in der Industrial Cyber Security zu erkennen ist nicht einfach und stellt derzeit eines der größten Probleme dar. In der Regel passiert es, dass nicht einmal in Betracht gezogen wird, dass der Ausfall in der Anlage durch ein Cyber Security Problem verursacht wurde. Dies geschieht typischerweise nach einem Boom. Die schlimmsten Auswirkungen treten auf, wenn sie nicht schnell behandelt bzw entdeckt werden. Normalerweise werden Beispiele aus der Vergangenheit verwendet, um Auswirkungen/Risiken abschätzen zu können. 

Einige dieser Beispiele sind die in den letzten Jahren aufgetretenen Fälle von Ransomware, die im besten Fall zu einem Verlust von Geld und Produktion führen. Im schlimmsten Fall sind auch mögliche Terroranschläge nicht auszuschließen. Die Betrachtung vom hypothetischen Standpunkt ist komplizierter, da sie viel Wissen und Erfahrung benötigt. Dies veranlasst uns zu überlegen, welches Sicherheitsniveau unsere Anlage benötigt. Wenn Terroranschläge erwartet werden, verkompliziert das alles im Vergleich zu einem herkömmlichen Ransomware-Angriff.

Ungeachtet der Ausmaße, welche ein solcher Angriff mit sich ziehen kann, ist in unserem Falle das Schlimmste der Totalstillstand der Anlage. Es muss kein großes Ereignis sein, es können kleine zusammenhängende Ereignisse sein. Man muss ernsthaft alle Optionen in Betracht ziehen um entscheiden zu können, welches das wichtigste System ist, um wiederum aus diesem System die Kernfunktion finden zu können. Daraus kann abgeleitet werden, welche Komponenten die ganze Zeit funktionieren müssen, welche Komponenten nicht aufhören dürfen zu arbeiten. So kann man entscheiden, welche Assets mehr Schutz benötigen, und welche mit den Systemen verknüpft sind, die schneller wiederhergestellt werden müssen.

## Maturity and Gaps

Die Norm IEC 62443 gibt ein Reifemodell mit 4 Stufen vor. 
- Die Erste ist „Initial“. Dies ist die grundlegendste Ebene. Die Prozesse haben keinerlei Vorbereitung, sie werden kaum kontrolliert und nichts kann vorhergesagt werden. Das bedeutet, dass sie durch jede Art von Veränderung im Ablauf beendet werden könnten.

- Die zweite Ebene ist „Managed“. Dies ist für die Organisationen, die Projekte mit einem Prozess durchführen. Das bedeutet, dass ähnliche Projekte mit demselben Prozess durchgeführt werden können. Auf dieser Ebene verbessern sich die Dinge bereits, es ist sehr stabil.

- Die Dritte ist „Defined“. Auf dieser Ebene gibt es Standardprozesse, nach denen die Projekte durchgeführt werden.
 
- Die vierte und letzte Stufe ist das „Optimizing“. In dieser erfolgt eine Kontrolle der Prozesse, um diese zu verbessern. Offensichtlich ist an dieser Stelle eines der größten Probleme, dass Organisationen nicht ehrlich mit dem Reifegrad sind in dem sie sich befinden oder schlichtweg überbewertet sind. Das Wichtigste in diesem Teil der Roadmap ist, den Reifegrad ehrlich und wahrheitsgetreu berechnen zu können. Es gibt verschiedene Möglichkeiten, ihn zu berechnen. Sie können beispielsweise ein Bewertungssystem verwenden, bei dem in den verschiedenen Teilen eine Punktzahl von 1 bis 4 vergeben wird, wodurch es ermöglich wird das System korrekt einzuordnen.

## Implement and Measure

Dieser Schritt ist wichtig, um Jahr für Jahr weiter voranzukommen. Man möchte messen können, wie weit Fortschritte bei der Verbesserung der Industrial Cyber Security gemacht wurden. Diese Maßnahmen sind nicht nur für den Bereich Cyber Security wichtig, sondern auch um die erzielten Fortschritte im Management nachweisen zu können. Was ist das Wichtigste, was ich messen kann? Hier gibt es verschiedene Kennzahlen, die sehr nützlich sein können. Die richtige Verwendung von Kennzahlen kann entscheidend für den Fortschritt sein. Es gibt bereits verschiedene Arten von Kennzahlen, zum Beispiel „MTTF“ Mean Time to Fix, die sagt, wie effektiv Probleme behoben werden und wie viele Stunden das ICS-Team die Probleme behebt. Eine andere Kennzahl, die im Awareness-Teil helfen kann, ist die Anzahl der ICS-Skills pro Beschäftigten. Auf diese Weise kann man verfolgen, wie viel Awareness wirklich vorhanden ist und wo nachgebessert werden muss.

## Conclusion

Abschließend muss gesagt werden, dass eine Roadmap von außen einfach, aber von innen sehr spezifisch sein muss. Die Schlüsselpunkte sind Awareness, da hier mit dem geringsten Aufwand gute Ergebnisse erzielt werden können. Ohne Schulung der Personen innerhalb welche im Betrieb tätig sind, ist ein ausreichender Schutz nicht möglich. Unerlässlich ist das Asset-inventory, denn wenn man nicht weiß was verwendet wird, kann man nicht wissen was besonders geschützt werden muss. Es ist auch wichtig, die Risiken zu kennen, aber noch wichtiger ist es sicherheitsrelevante Vorfälle zu erkennen und anschließend die richtigen Maßnahmen für die jeweilige Situation zu setzen. Dafür ist es wichtig, die internen Kennzahlen zu verstehen um dadurch den eigenen Reifegradkorrekt einschätzen zu können und ihn zu verbessern. 




## Literatur & Quellen

[1] Piere Kobes, Guideline Industrial Security 2016 <br />
[2] https://www.pcwelt.de/a/shodan-das-kann-die-suchmaschine-der-hacker,3446476 <br />
[3] https://www.computerweekly.com/de/definition/Google-Dorking-oder-Google-Hacking <br />
[4] https://www.fortinet.com/resources/cyberglossary/defense-in-depth#:~:text=Defense%20in%20depth%20is%20a,are%20stopped%20along%20the%20way <br />
[5] https://www.trendmicro.com/de_de/it-security-best-practices/mit-virtual-patching-schwachstellen-schliessen.html <br />
[6] https://verveindustrial.com/resources/blog/5-steps-to-successful-whitelisting-deployments-in-ot-2/ <br />
[7] https://media.kaspersky.com/en/business-security/kl-industrial-cybersecurity-training-awareness.pdf <br />
[8] https://verveindustrial.com/resources/webinar/asset-inventory-the-foundation-to-a-successful-ot-security-program/ <br />
[9] https://www.youtube.com/watch?v=cnIfqmsRV5U&list=LL&index=3&t=1155s&ab_channel=Dragos%2CInc%3AICSCybersecurity <br />

