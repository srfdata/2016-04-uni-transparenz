# 2016-04-uni-transparenz


## Publikation

Die Daten in diesem Repository beziehen sich auf die Serie [Die Interessenbindungen der Schweizer Universitäten](http://www.srf.ch/news/schweiz/uni-transparenz), publiziert am 20. April 2016. 

## Beschreibung

### Daten

Alle Daten sind in einer relationalen, file-basierten [`sqlite`](https://www.sqlite.org/)-Datenbank gespeichert. In der [interaktiven Visualisierung](http://www.srf.ch/news/interaktive-grafik-alle-interessenbindungen-auf-einen-blick) wird eine Teilmenge/Ansicht davon visualisiert.

* `unitransparenz.mwb` - Datenbankmodell, erstellt mit [MySQL-Workbench](https://github.com/mysql/mysql-workbench) und mit dem [mysql-wb-exportsqlite Plugin](https://github.com/tatsushid/mysql-wb-exportsqlite) exportiert- wo möglich wurde relationelle Integrität implementiert

* `unitransparenz.pdf` - PDF des obigen Modells

* `unitransparenz.sql` - Die Datenbank als SQL-Dump (`sqlite`-Dialekt) - siehe unten

#### Detaillierte Datenbeschreibung und Methodik

folgt. Der Artikel [Uni-Bindungen: Was die Daten aussagen können – und was nicht](http://www.srf.ch/news/schweiz/uni-transparenz/uni-bindungen-was-die-daten-aussagen-koennen-und-was-nicht) enthält eine grobe Beschreibung.

#### Die Daten einlesen

Wir empfehlen, das Firefox-Plugin [SQLiteManager](http://lazierthanthou.github.io/sqlite-manager/) zu verwenden.

* Dort muss zuerst über `Database > New Database` eine neue Datenbank erstellt werden.
* Danach kann der SQL-Dump mit `Database > Import` importiert werden (Encoding "UTF-8", kein Häkchen bei BEGIN TRANSACTION).
* Um Foreign Keys zu forcieren (Empfehlung) sollte bei `Tools > Open On-Connect SQL Tab` das Statement `PRAGMA foreign_keys=ON;` eingefügt werden.
* Happy querying! 

## Haftungsausschluss

Die veröffentlichten Informationen sind sorgfältig zusammengestellt, erheben aber keinen Anspruch auf Aktualität, Vollständigkeit oder Richtigkeit. Es wird keine Haftung übernommen für Schäden, die  durch die Verwendung dieses Scripts oder der daraus gezogenen Informationen entstehen. Dies gilt ebenfalls für Inhalte Dritter, die über dieses Angebot zugänglich sind. 

## Lizenz

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons Lizenzvertrag" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Dataset" property="dct:title" rel="dct:type">2016-04-uni-transparenz</span> von <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/srfdata/2016-04-uni-transparenz" property="cc:attributionName" rel="cc:attributionURL">SRF Data</a> ist lizenziert unter einer <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Namensnennung - Weitergabe unter gleichen Bedingungen 4.0 International Lizenz</a>.

## Kontakt

Bei Fragen wenden Sie sich bitte an timo.grossenbacher(at)srf.ch oder an [@srfdata](https://twitter.com/srfdata)
