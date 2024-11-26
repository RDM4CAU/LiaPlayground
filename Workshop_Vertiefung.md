<!--
author: Richard Diebel, Britta Petersen
email: diebel@ub.uni-kiel.de, b.petersen@rz.uni-kiel.de
version: 0.0.1
date: 2024-11-27
link: https://raw.githubusercontent.com/RDM4CAU/Intro-to-RDM/refs/heads/main/cau-style.css
comment: Liacript Vertiefung
language: de
narrator: Deutsch Female
repository: https://github.com/RDM4CAU/LiaPlayground
icon: https://raw.githubusercontent.com/RDM4CAU/TtL-FDM/main/images/fdm_lehre.png
import: https://raw.githubusercontent.com/LiaTemplates/LiveEdit-Embeddings/refs/heads/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/citations/main/README.md
-->

# Liascriptdateien erstellen

## Grundlagen

> ![Markdown Logo](https://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)  
> **Markdown** ist eine leichtgewichtige Auszeichnungssprache, die zur Formatierung von Text verwendet wird. Sie ermöglicht es, Texte einfach und übersichtlich zu strukturieren, indem einfache Symbole wie *, # oder - verwendet werden. Markdown wird vor allem für das Schreiben von Dokumentationen, Blogposts und Readme-Dateien genutzt, da es sich gut in HTML umwandeln lässt. Es ist besonders beliebt, weil der Quelltext auch ohne spezielle Software gut lesbar bleibt.

> ![LiaScript Logo](https://liascript.github.io/images/logo_hu7443897454658306654.webp)  
> **LiaScriptdateien** sind einfach Textdateien (Plaintext), die die Markdown-Dateiendung (*.md) bekommen. Sie sind, ebenso wie Markdown, ohne Software lesbar. Sie lassen sich mit einem Parser in schön formatierte Dokumente umwandeln.
 
> Ein **Parser** ist ein Programm oder eine Komponente in der Softwareentwicklung, die einen Eingabetext analysiert und dessen Struktur gemäß einer bestimmten Grammatik überprüft. Dabei wandelt der Parser den Text in eine für den Computer verständliche, interne Repräsentation (oft einen Syntaxbaum) um. Parser werden häufig in Compilern, Interpretersprachen und bei der Verarbeitung von Dateiformaten wie XML oder JSON eingesetzt, um Eingaben zu analysieren und weiterzuverarbeiten.  
> In unserem Fall liest der Parser die Struktur der LiaScriptdatei und wandelt einzelne Elemente wie Textblöcke, Überschriften oder Listen in ein HTML-Dokument um, welches in einem Browser angezeigt werden kann.

> ![Git Logo](https://git-scm.com/images/logo@2x.png)  
> **Git** ist ein Versionskontrollsystem, das Entwickler verwenden, um Änderungen an Dateien, besonders im Code, zu verfolgen. Es ermöglicht das Speichern von verschiedenen Versionen eines Projekts, das Zurückkehren zu früheren Versionen und die Zusammenarbeit mehrerer Personen. Änderungen werden in sogenannten „Repositories“ gespeichert, die lokal oder online (z. B. auf GitHub oder GitLab) liegen können.

## Lokal

Liascriptdateien können komplett lokal erstellt und dargestellt werden. Als Dateien müssen lediglich Textdateien erstellt werden und die Endung *.txt in *.md geändert werden. Die Dateien können mit jedem beliebigen Texteditor bearbeitet werden (Editor auf Windows, Textedit auf dem Mac und Text Editor unter Linux (Ubuntu)). Für die lokale Darstellung wird jedoch ein Parser benötigt. Dieser findet sich als Plugin im Code-Editor [**Visual Studio Code**](https://code.visualstudio.com/) von Microsoft oder im Open-Source-Editor [**Pulsar**](https://pulsar-edit.dev/). Das jeweilige Plugin für die Darstellung nennt sich: LiaScript-Preview.

✅ Vorteile:
----
- Offline-Nutzung möglich.
- Schnelle Vorschau und Tests.
- Volle Kontrolle über die Umgebung.

❌ Nachteile:
----
- Lokale Installation erforderlich.
- Etwas mehr technischer Aufwand.
- Dateien müssen manuell hochgeladen werden, um online geteilt zu werden.

## Lokal und Online gemischt

Visual Studio Code lässt sich auch komplett online ausführen. Dazu braucht man nur [vscode.dev](https://vscode.dev) aufzurufen. Mit Chromium basierten Browsers (Google Chrome, Microsoft Edge) ist es möglich, Dateien in lokal auf der Festplatte befindlichen Ordnern zu bearbeiten. Der Parser lässt sich online in VS Code als Plugin nachinstallieren, er heißt Liascript-Preview-Web. Für alle anderen Browser (Firefox, Safari) benötigt man die Dateien online in einem Git. Bearbeitungen werden dann in das Git geschrieben und können über den Parser in VS Code gerendert werden.

✅ Vorteile:
----
- Keine lokale Installation notwendig.
- Direktes Arbeiten im Browser.
- Kollaboratives Arbeiten im Git möglich

❌ Nachteile:
----
- Internetverbindung erforderlich.
- Eingeschränkte Leistung im Vergleich zur Desktop-Version.
- Abhängigkeit von den Online-Diensten von VS Code.

## Komplett online

Es ist auch möglich, Dateien komplett online zu erstellen. Die einfachste Variante ist, ein Git zu erstellen und dort Liascriptdateien anzulegen. Um sie zu parsen kann der [Online Parser von Liascript](https://liascript.github.io/) genutzt werden, der auf der Seite von Liascript erreichbar ist. Dort braucht man dann nur die Url zur eigenen Liascriptdatei  eingegeben werden und die Datei wird geparst und im Browser dargestellt. Alternativ kann auch der Liascript-Liveeditor genutzt werden, um die Dateien zu erstellen. Im Liveeditor werden die Dateien allerdings nicht gespeichert - sie sind nur während der Session verfügbar.

??[Liascript](https://liascript.github.io/)

✅ Vorteile:
----
- Keine lokale Installation notwendig.
- Jederzeit von überall zugänglich.
- Einfaches Teilen über Github.

❌ Nachteile:
----
- Internetverbindung erforderlich.
- Weniger flexibel für schnelle Vorschauen oder Tests.
- Keine Syntaxhervorhebung bei Git

# Export

## OLAT Export

Liascript ist für den Onlineeinsatz gemacht. Es bietet jedoch auch die Möglichkeit, in Lernplattformen wie OLAT oder Moodle exportiert zu werden. Dazu muss die Liascriptdatei in das SCORM Format exportiert werden. Die Lernplattform OpenOLAT unterstützt Scorm 1.2. Der Export erfolgt über die Kommandozeilenebene. Die genaue Anleitung ist auf der [Githubseite des Liascriptexporters](https://github.com/LiaScript/LiaScript-Exporter) beschrieben und setzt die Software Node.js (eine JavaScript Umgebung) voraus.

Der Exporter wird dann mit dem Befehl `npm install -g --verbose @liascript/exporter` installiert. Nun ist es möglich, LiaScriptdateien auf der eigenen Festplatte mit dem LiaScript-Exporter umzuwandeln.

Der Befehl hat die Struktur

> liaex -input Dateiname.md --format scorm1.2 --output Outputname --scorm-iframe

und setzt sich wie folgt zusammen:

| Befehl               | Funktion                                                                                         |
| -------------------- | ------------------------------------------------------------------------------------------------ |
| liaex                | Spricht den LiaScript-Exporter an                                                                |
| -input Dateiname.md      | Legt fest welche Datei exportiert wird. Dateiname ist hier durch den Namen der Datei zu ersetzen |
| --format scorm1.2    | Legt das Zielformat fest. Für OpenOLAT wird SCORM 1.2 benötigt                                   |
| --output Outputname  | Legt den Namen der erzeugten Datei fest.                                                         |
| --scorm-iframe        | Behebt eine Inkompatibilität mit OpenOLAT. Ohne diesen Zusatz wird der Kurs nicht funktionieren  |

Der Exporter erzeugt eine zip-Datei im selben Ordner wie die Ausgangsdatei.

## Kommentare

Kommentare, also nur für den Bearbeiter sichtbare Ergänzungen, lassen sich mit HTML Kommentaren einfügen. Dabei gilt zurzeit die Einschränkung, dass keine Sonderzeichen verwendet werden dürfen außer **:**, **-** und **_**. Also

``` html
<!--
Geht: siehste
-->

<!--
Geht nicht.
-->

```

# Erweiterungen

Es existieren einige Erweiterungen (Templates) von Liascript für spezifische Aufgaben. Mit ihnen wird die Syntax von LiaScript so erweitert, dass sie die Aufgaben abdeckt. Sie sind nicht Teil des offiziellen LiaScript-Pakets. Die Erweiterungen sind auf [GitHub](https://github.com/liaTemplates). Um sie zu benutzen müssen die Erweiterungen im Header der LiaScript-Datei importiert werden:

``` html
<!--
author: Richard Diebel, Britta Petersen
email: diebel@ub.uni-kiel.de, b.petersen@rz.uni-kiel.de
version: 0.0.1
date: 2024-11-27
link: https://raw.githubusercontent.com/RDM4CAU/Intro-to-RDM/refs/heads/main/cau-style.css
comment: Liacript Vertiefung
language: de
narrator: Deutsch Female
repository: https://github.com/RDM4CAU/LiaPlayground
icon: https://raw.githubusercontent.com/RDM4CAU/TtL-FDM/main/images/fdm_lehre.png
import: https://raw.githubusercontent.com/LiaTemplates/LiveEdit-Embeddings/refs/heads/main/README.md
-->
```

## Live Editor

``` markdown @embed
# Hello World

This is a simple example that shows how to use the LiveEditor.
```

## Zitationen und Literaturverzeichnis

Dies ist ein Satz
```bibtex @cite
@book{johnson2019book,
  title={Nordelbingen},
  author={Beuckers, Klaus Gereon},
  year={2024},
  publisher={Universitätsverlag Kiel },
  address={Kiel},
  url={https://doi.org/10.38072/2941-3362/i90} 
}
```
der nicht endet.

```bibtex @bibliography.style(ieee)
@book{johnson2019book,
  title     = {The Complete Guide to Examples},
  author    = {Johnson, Emily},
  year      = {2019},
  publisher = {Academic Press},
  address   = {New York},
  url       = {https://doi.org/10.1000/conf.2021.123}
}

@book{texbook,
  author    = {Donald E. Knuth},
  year      = {1986},
  title     = {The {\TeX} Book},
  publisher = {Addison-Wesley Professional}
}
```

```bibtex @bibliography.style(harvard1)
@book{johnson2019book,
  title     = {The Complete Guide to Examples},
  author    = {Johnson, Emily},
  year      = {2019},
  publisher = {Academic Press},
  address   = {New York},
  url       = {https://doi.org/10.1000/conf.2021.123}
}

@book{texbook,
  author    = {Donald E. Knuth},
  year      = {1986},
  title     = {The {\TeX} Book},
  publisher = {Addison-Wesley Professional}
}
```

```bibtex @bibliography.style(vancouver)
@book{johnson2019book,
  title     = {The Complete Guide to Examples},
  author    = {Johnson, Emily},
  year      = {2019},
  publisher = {Academic Press},
  address   = {New York},
  url       = {https://doi.org/10.1000/conf.2021.123}
}

@book{texbook,
  author    = {Donald E. Knuth},
  year      = {1986},
  title     = {The {\TeX} Book},
  publisher = {Addison-Wesley Professional}
}
```


### Rest

- Reaktionsgleichungen (Chemie) (KekuleJS)
- Noten usw.
- Code (ausführbar)

Britta
- Beispieldokumente