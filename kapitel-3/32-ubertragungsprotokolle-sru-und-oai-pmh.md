# 3.2 Übertragungsprotokolle SRU und OAI-PMH

Es gibt zahlreiche Übertragungsprotokolle im Bibliotheks- und Archivbereich. Drei davon sind besonders weit verbreitet:

* [Z39.50](https://www.loc.gov/z3950/) \(Library of Congress\)
* [SRU](http://www.loc.gov/standards/sru/) - Search/Retrieve via URL \(Library of Congress\)
* [OAI-PMH](https://www.openarchives.org/pmh/) - Open Archives Initiative Protocol for Metadata Harvesting \(Open Archives Initiative\)

Z39.50 ist sehr alt, aber immer noch im Einsatz. Meist wird das modernere SRU als Ergänzung angeboten.

Während Z39.50 und SRU sich besonders für Live-Abfragen oder gezielten Datenabruf mit vielen Parametern eignet, zielt OAI-PMH vor allem auf größere Datenabzüge und regelmäßige Aktualisierungen. Das Schöne an SRU und OAI-PMH ist, dass die Anfragen als Internetadresse (URL) zusammengestellt werden können und direkt über den Browser ohne Zusatzsoftware aufrufbar sind.

Bevor wir konkrete Testdaten für unser "Wissensportal" herunterladen, wollen wir zunächst die Möglichkeiten der Schnittstellen erkunden. Wir orientieren uns an dem Schweizer Projekt Swissbib, das öffentliche Schnittstellen nach SRU und OAI-PMH bereitstellt und diese auch gut dokumentiert hat:

* Dokumentation SRU: [http://www.swissbib.org/wiki/index.php?title=SRU](http://www.swissbib.org/wiki/index.php?title=SRU)
* Dokumentation OAI: [http://www.swissbib.org/wiki/index.php?title=Swissbib\_oai](http://www.swissbib.org/wiki/index.php?title=Swissbib_oai)

Bitte schauen Sie sich dort um und lösen Sie die folgenden Aufgaben. Zum Laden und Speichern der Daten über die Kommandozeile können Sie wieder das Programm `curl` nutzen, dass Sie in [Kapitel 1.5]() kennengelernt haben. Um die Aufgaben vollständig lösen zu können, müssen Sie die Dokumentation genau lesen und etwas stöbern.

## Aufgabe 1

Laden Sie 100 Datensätze der ETH-Bibliothek \(Hauptbibliothek Rämistrasse 101, 8092 Zürich\) für den Suchbegriff `Albert Einstein` \(über alle Felder\) im Format MARC21. Speichern Sie die Daten in der Datei `einstein.xml`.

## Aufgabe 2

Laden Sie einige Datensätze aus dem gesamten Swissbib-Verbund, die seit dem 31.10.2017 verändert wurden im Format MARC21. Speichern Sie die Daten in der Datei `swissbib-2017-10-31.xml`.

## Bonusaufgabe

Finden Sie heraus, nach welchen Regeln die SRU-Schnittstelle von Swissbib MARC21 in Dublin Core transformiert.

## Lösungen

Die Lösungen für die obigen Aufgaben sind auf der Seite [Lösungen](/losungen.md) dokumentiert.

## Aktuelle Entwicklungen

[Resourcesync](http://www.openarchives.org/rs/) ist ein vielversprechender neuer Standard, der schnellere und spezifischere Synchronisierungen ermöglicht, als es mit OAI-PMH möglich ist. Aktuell ist Resourcesync noch selten im Einsatz, wird aber in nächster Zeit als Ergänzung zu OAI-PMH immer öfter anzutreffen sein und könnte OAI-PMH auf längere Sicht vielleicht sogar ablösen. Es gibt Referenzimplementierungen in Python für [Data Provider](https://github.com/resourcesync/py-resourcesync) und für [Harvester](https://github.com/resync/resync).

Grundlegende Informationen und aktuelle Anwendungen sind der folgenden Präsentation zu entnehmen:

> Martin Klein, Gretchen Gueguen, Mark Matienzo, Petr Knoth \(20.4.2017\): ResourceSync - Overview and Real-World Use Cases for Discovery, Harvesting, and Synchronization of Resources on the Web. Präsentation auf DPLAfest 2017. [https://www.slideshare.net/martinklein0815/resourcesync-overview-and-realworld-use-cases-for-discovery-harvesting-and-synchronization-of-resources-on-the-web](https://www.slideshare.net/martinklein0815/resourcesync-overview-and-realworld-use-cases-for-discovery-harvesting-and-synchronization-of-resources-on-the-web)

Ein ganz anderes Feld sind die vielfältigen Linked Data Schnittstellen. Damit werden wir uns später in [Kapitel 7](/kapitel-7.md) \(11.01.18\) beschäftigen.