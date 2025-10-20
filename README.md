# bmb-elpub5-2025

Modul Elektronisches Publizieren V im Studiengang Buch- und Medienproduktion an der HTWK Leipzig

Inhalt          | Beschreibung
----------------|-------------
Moduldauer      | 8 Wochen
Regelsemester   | Wintersemester 7. Semester
Umfang          | 4 SWS
Typ             | Wahlmodul
ECTS            | 5
Sprache         | Deutsch
Voraussetzungen | Grundlegendes Kenntnisse in den Technologien XML, XSLT, HTML und CSS
Arbeitslast     | 150 Stunden, davon 64 SWS (entspricht 4 SWS), 85 Stunden angeleitetes Selbststudium und Prüfungsvorbereitung, 1 Stunde Prüfung (Präsentation)

## Hilfsmittel

Alle Hilfsmittel sind erlaubt, auch KI-Assistenten.

## Remote

Die Veranstaltung kann auch Remote angeboten werden.

Zur Kommunikation und zum Teilen von Inhalten wird ein Gruppenchat bereitgestellt bereit. Der Gruppenchat wird nach der Prüfung wieder entfernt.

Nachfragen können natürlich auch via E-Mail gestellt werden.

## Veranstaltungen

| Nr. | Datum  | Zeit        | Beschreibung     |
|-----|--------|-------------|------------------|
| 1.  | 23.10. |  9:30-12:45 | Einführung, JATS |
| 2.  | 27.10. |  9:30-12:45 | XSLT             |
| 3.  | 03.11. |  9:30-12:45 | XSLT             |
| 4.  | 10.11. |  9:30-12:45 | Schematron       |
| 5.  | 17.11. |  9:30-12:45 | PrintCSS         |
| 6.  | 24.11. |  9:30-12:45 | PrintCSS         |
| 7.  | 01.12. |  9:30-12:45 | Konsultation     |
| 8.  | 15.12. |  9:30-12:45 | Prüfung          |

## Aufgaben

1. Auszeichnung der JATS-XML-Datei. ([Herunterladen](https://www.le-tex.de/dbdownload/SYAi5JyrFUXHBpnprM5QaslIzIQB0XeahFGLIrnD/econ-2025-0158.zip))
2. Konvertierung von [XHTML](https://www.w3.org/TR/xhtml1/) aus [JATS](https://jats.nlm.nih.gov/publishing/tag-library/1.1/index.html)
3. Prüfen der JATS-Daten mit [ISO Schematron](http://schematron.com/)
4. Erstellen einer Druckvorlage mit PrintCSS

### 1. JATS-XML

1. Metadaten müssen ausgezeichnet sein
2. Alternativtexte sind eingefügt
3. Referenzen sind auch als strukturierte Version verfügbar 

### 2. XSLT

1. XSLT muss valide sein
2. XSLT muss lauffähig sein: keine Fehler, keine uneindeutigen Templates (ambiguous)
3. XSLT muss alle Elemente vollständig transformieren
4. Metadaten müssen nicht alle vorhanden sein, aber mindestens: Journal Title, Publisher, Contributors, Volume, Issue, Abstract
5. Es darf kein Text verloren gehen
6. Interne und externe Links müssen funktionsfähig sein
7. Nummerierungen von Sections sollten automatisch erfolgen
8. Redundanter Code sollte vermieden werden
9. Die HTML-Ausgabe muss valide sein

### 3. Schematron

1. Der Inhalt von publisher-name muss "De Gruyter" sein.
2. kwd-group muss mindestens drei kwd-Elemente enthalten
3. die Elemente volume und issue dürfen ausschließlich Zahlen enthalten.
4. pub-date day, month und year entsprechend nur aus Zahlen bestehen bzw. die richtige Anzahl von Stellen.
5. Letzte Seite muss größer als die erste Seite sein.
6. Differenz von letzer und erster Seite muss gleich der Gesamtseitenzahl sein. 
7. Copyright Jahr muss größer als 1990 sein.
8. Der Dateiname in related-article muss immer mit der Endung ".pdf" enden.
9. Journal-Code muss fünfstellig sein.
10. Jede Figure muss einen Alternativtext enthalten

### 4. PrintCSS

1. das CSS muss valide sein (Ausnahme spezielle PrinceCSS-Properties)
2. Print Media Query vorhanden
3. Page Rules für gerade und ungerade Seiten und erste Seite (ohne Seitenzahl und Kolumnentitel)
4. funktionierendes Inhaltsverzeichnis mit Seitenzahl
5. Floats bei Bildern und Tabellen (top)
6. Kolumnentitel
7. Seitenzahl
8. Fußnoten
9. Referenzen
10. mehrspaltiges Layout, außer bei Titelseite, Bildern und Tabellen
11. Schrift eingebunden
12. keine doppelten Elemente

## Abgabe

* bis 8.12. Daten abgeben
* XML, XSLT, Schematron, CSS
* als Zip: `elpub5-2025_nachname_vorname.zip`
* via E-Mail an martin.kraetke@le-tex.de

## Prüfungsablauf

* Dauer: 15 Minuten plus 5 Minuten Vorbereitung plus 5 Minuten Auswertung (gesamt: 25 Minuten)
* fehlerfreie Konvertierung mit oXygen und Prince zeigen
* Präsentation der Konvertierungsergebnisse
* Praktische und theoretische Fragen zu den Themengebieten XSLT, Schematron, PrintCSS

## Editoren

* [oXygen XML Editor](https://www.oxygenxml.com/)
* [Notepad++](https://notepad-plus-plus.org) (mit Plugin _XML-Tools_)
* [VSCode](https://code.visualstudio.com/) mit [XSLT/XPath-Unterstützung](https://marketplace.visualstudio.com/items?itemName=deltaxml.xslt-xpath)

## Literatur

### JATS

#### Dokumentation

[Web-Dokumentation von JATS](https://jats.nlm.nih.gov/publishing/tag-library/1.3/element/journal-id.html)

#### Tutorials

[Introduction to JATS von Debbie Lapeyre](https://www.xml.com/articles/2018/10/12/introduction-jats/)

### XSLT

#### Spec

https://www.w3.org/TR/xslt20/

#### Bücher

* Michael Kay: XSLT 2.0 and XPath 2.0 Programmer's Reference
* Doug Tidwell: XSLT

#### Tutorials

* [Norman Walsh: Introduction to XSLT 2.0](https://nwalsh.com/docs/tutorials/extreme2006/plain.html
)
* [W3Schools: XSLT Introduction](https://www.w3schools.com/xml/xsl_intro.asp)

### Schematron

#### Spec

https://standards.iso.org/ittf/PubliclyAvailableStandards/c055982_ISO_IEC_19757-3_2016.zip

#### Bücher

Marko Hedler, Nico Kutscherauer: Schematron: effiziente XML Business Rules für XML-Dokumente

#### Tutorials

* [data2type: Schematron](https://www.data2type.de/xml-xslt-xslfo/schematron/)
* [David J. Birnbaum : Schematron Introduction](http://dh.obdurodon.org/schematron-intro.xhtml)
* [xml.com Introduction to Schematron](https://www.xml.com/pub/a/2003/11/12/schematron.html)

### PrintCSS

#### Spec

* [CSS Paged Media Module Level 3](https://www.w3.org/TR/css-page-3/)
* [CSS Generated Content for Paged Media Module](https://www.w3.org/TR/css-gcpm-3/)
* [CSS Fragmentation Module Level 3](https://www.w3.org/TR/css-break-3/)

#### Tutorials

* [Andreas Jung: print css rocks](https://print-css.rocks/)
* [Rachel Andrew: A Guide To The State Of Print Stylesheets In 2018](https://www.smashingmagazine.com/2018/05/print-stylesheets-in-2018/)
* [Rachel Andrew: Designing For Print With CSS](https://www.smashingmagazine.com/2015/01/designing-for-print-with-css/)
* [Antenna House: Introduction to CSS for Paged Media](https://www.antennahouse.com/hubfs/PDFS/CSS%20for%20Paged%20Media/CSS-Print-en-2019-02-15.pdf)

