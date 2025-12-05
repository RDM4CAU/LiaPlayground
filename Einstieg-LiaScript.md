<!--
author: Britta Petersen
email: b.petersen@rz.uni-kiel.de
version: 0.0.1
date: 2024-10-17
comment: Ergebnis der Hands-On-Phase; Einstieg in LiaScript
language: de
narrator: Deutsch Female
repository: https://github.com/RDM4CAU/LiaPlayground
icon: https://raw.githubusercontent.com/RDM4CAU/TtL-FDM/main/images/fdm_lehre.png
-->

# LiaScript Einstieg

Guten Morgen! :-)

# A. Grundlage: Markdown
LiaScript ist eine Erweiterung von Markdown. Die Entwickler:innen von LiaScript haben sich an GitHub Flavored Markdown orientiert und dieses um Funktionen erweitert, die einen erweiterten Einsatz von Multimedia sowie verschiedene Interaktionen mit Nutzenden ermöglichen.

**Die Sytax, die ggf. von Markdown schon bekannt ist, kann also auch hier angewendet werden - mit kleinen Abweichungen und einigen Erweiterungen. :-D** 

-> LiaScript-Dokumente sind Textdokumente, deren Inhalt in einfachsten Texteditoren gelesen und bearbeitet werden können.  



## A.1 Inhalte strukturieren

LiaScript arbeitet, wie Markdown, mit dem #️⃣ zur Einteilung von Inhalten in Kapitel. Wie in normalem Markdown auch definiert die Anzahl #️⃣ die Kapitelebenen.

Ebene 1: #

Ebene 2: ##

Ebene 3: ###

usw.

Es sind maximal 6 Ebenen möglich. 

---

__Achtung!__

LiaScript legt automatisch eine neue Seite für jede eingefügte Überschrift an, egal auf welcher Ebene.

Wenn nicht gewünscht ist, dass eine neue Seite angelegt wird, können Überschriften folgendermaßen erzwungen werden:

```
<section>
## Wir brauchen hier eine Überschrift!

Hier folgt dann der Inhalt.... 

</section>
```
Ergebnis:

<section>
# Wir brauchen hier eine Überschrift!

Hier folgt dann der Inhalt.... 

Das funktioniert auch mit `<article>` statt `<section>`:

```
<article>
## Wir brauchen hier eine weitere Überschrift!

Und noch ein bisschen mehr Inhalt... 

</article>
```

</section>

<article>
## Wir brauchen hier eine weitere Überschrift!

Und noch ein bisschen mehr Inhalt... 

</article>

---

😨Zu kompliziert? Na, gut. Es geht auch noch anders:

```
Huch? So geht es auch?
===

Und so?
---
```

Huch so geht es auch?
===

Und so?
---


Absätze
===
LiaScript braucht eine Leerzeile zwischen Textblöcken, um einen Absatz erkennen zu können. 




Mehrere Leerzeilen hintereinander werden nicht als mehrere Leerzeilen erkannt. Zusätzlicher Abstand muss z. B. mit `<br>` erzwungen werden:

```
Ich will mehr
<br>
<br>
<br>
Abstand
```
---
Ich will mehr
<br>
<br>
<br>
Abstand.

---
...oder mit dem Backslash \\

```
Ich will mehr\
\
\
\
Abstand
```

---

Ich will mehr\
\
\
\
Abstand

---


Horizontale Linien: `---`

---




## A.2 Text formatieren

Auszeichnungen für Textformatierungen sind vielleicht von Markdown her schon bekannt. Hier nochmal eine ganz schnell eine Wiederholung:

_kursiv_ --> Gleiches Ergebnis mit Unterstrich oder Sternchen: `_kursiv_` oder `*kursiv*`

__fett__ --> Gleiches Ergebnis mit doppeltem Unterstrich oder doppeltem Sternchen: `__fett__` oder `**fett**`

~durchgestrichen~ --> einfache Welle `~durchgestrichen~` 

~~unterstrichen~~ --> doppelte Welle `~~unterstrichen~~`

_Diese ~~Formatierungsangaben~~ sind **beliebig** kombinier- und verschachtelbar._ --> `_Diese ~~Formatierungsangaben~~ sind **beliebig** kombinier- und verschachtelbar._`

:-O Sonderzeichen können Funktionen haben! Daher benötigen wir ein sogenanntes Escapezeichen, um Sonderzeichen bei Bedarf ihre Funtion zu entziehen. Als Escapezeichen fungiert der Backslash. 

Beispiel: `\*dieser Text ist nicht kursiv\*` -> \*dieser Text ist nicht kursiv\*

Also, wenn ich dem Sonderzeichen seine Funktion entziehen will und stattdessen das Sonderzeichen sehen will, setze ich einen Backlash davor:

`\*, \~, \_, \#, \{, \}, \[, \], \|, \`, \$, \@, \\, \<, \>`

wird zu --> 

\*, \~, \_, \#, \{, \}, \[, \], \|, \`, \$, \@, \\, \<, \>

Um ein Wort oder einen Satz als Code zu kennzeichnen, wird es in Backticks (`) eingeschlossen.

`Dies ist ein Code`

---

Blöcke
===

Die durch eine Leerzeile getrennten Absätze sind "Blöcke", denen mit html-Kommentaren jeweils noch Eigenschaften zugewiesen werden können, z. B. eine andere Schriftfarbe oder eine andere Hintergrundfarbe.

```
<!-- style="color: red" -->
Dieser Block soll in rotem Text erscheinen.

<!-- style="background-color: lightblue;"-->
Dieser Block soll einen hellblauen Hintergrund haben
```

Ergebnis:

<!-- style="color: red" -->
Dieser Block soll in rotem Text erscheinen.

<!-- style="background-color: lightblue;"-->
Dieser Block soll einen hellblauen Hintergrund haben

## A.3 Listen

Unsortierte Listen können mit `-` oder `*` erzeugt werden.

Für jede weitere Ebene `Leerzeile + Leerzeichen`

- 2 Karotte(n)
- 1 Zwiebel(- n)
- 3 Tomate(n)
- evtl. Kräuter

  - frisch
  - getrocknet

    - next
       
      - next next

- Salz und Pfeffer
- Paprikapulver
- 1 EL Olivenöl

---

Sortierte Listen entstehen nach mit `Ziffer + .`

1. dies
2. das
3. und jenes
10. **Wir müssen selbst auf die korrekte Nummerierung aufpassen!**


## A.4 Tabellen

Für Tabellen gelten die gängigen Markdownregeln:

```markdown

| Header 1   | Header 2   | Header 3   |
| :--------- | ---------: | :--------: |
| Item 1     | Item 2     | Item 3     |

``` 

\

Die Ausrichtung des Textes in den Spalten:

- links ⟶ `:---` oder `---` (default)
- rechts ⟶ `---:`
- zentriert ⟶ `:---:`

\

**Ergebnis:**

| Header 1   | Header 2   | Header 3   |
| :--------- | ---------: | :--------: |
| Item 1     | Item 2     | Item 3     |

---

Wenn Liascript merkt, dass Werte in der Tabelle stehen, bietet es an, die Werte als Diagramm darzustellen:

| Stoff       | Gramm       |
| ----------- | ----------- |
| ~~Eiweiß~~  | 6.31 g      |
| Fett        | 2.75 g      |
| Kohlenhydr. | **26.48 g** |

\

Wenn dies nicht gewünscht ist `<!-- data-type="none" -->` oberhalb der Tabelle. Im selben Kommentar kann man Styles definieren.

```markdown
<!-- data-type="none" style="width: 40%" -->
| Stoff       | Gramm       |
| ----------- | ----------- |
| ~~Eiweiß~~  | 6.31 g      |
| Fett        | 2.75 g      |
| Kohlenhydr. | **26.48 g** |
```

wird zu:

<!-- data-type="none" style="width: 40%" -->
| Stoff       | Gramm       |
| ----------- | ----------- |
| ~~Eiweiß~~  | 6.31 g      |
| Fett        | 2.75 g      |
| Kohlenhydr. | **26.48 g** |

## A.5 Diagramme

Wie wir eben schon gesehen haben bietet Liascript automatisch Diagramme an, wenn Werte in Tabellen stehen.


|   x | dots |
| ---:| ----:|
|   0 |    0 |
|  10 |    2 |
|  20 |    4 |
|  30 |    6 |


Diagramme können aber auch "gezeichnet" werden:

    9 |                                       (* dots)
      |
    y |                              *
    - |
    a |                    *
    x |
    i |          *
    s |
      |*
    0 +------------------------------------
      0            x-axis                 36

Dabei können auch mehrere Datenreihen eingetragen werden:

    9 |                                       (* Sternchen)
      |          +                            (+ Plus)
    y |    b      B       B             *     (b b) 
    - |         b      B       B              (r r) 
    a |                b    *                 (R R) 
    x |                 +                     (B B)
    i |          *         r       R
    s |       +    r             R
      |*  + r *             R         R
    0 +------------------------------------
      0            x-axis                 36

\
\

Die Ausrichtungen der Daten haben Einfluß auf die Darstellung:

| Eiweis | Fett | Kohlehydr. |
| :----- | :--- | :--------- |
| 1      | 2    | 3          |

---

Mit `<!-- data-transpose -->` drehen:

<!-- data-transpose style="width: 40%" -->
| Stoff       | Gramm       |
| ----------- | ----------- |
| ~~Eiweiß~~  | 6.31 g      |
| Fett        | 2.75 g      |
| Kohlenhydr. | **26.48 g** |


## A.6 Hervorhebung und hevorgehobene Zitate

>Die **schleswig-holsteinische Landesinitiative zum FDM** fördert kooperative Lösungen und ermöglicht eine effektive Koordination, Vermittlung von Kompetenzen und Schaffung gemeinsamer Strukturen im Umgang mit Forschungsdaten. Im partnerschaftlichen Engagement sollen Wege gefunden werden, um das zeitgemäße Forschungsdatenmanagement vor Ort gemeinsam zu bewältigen und dabei Know-how und Ressourcen zu teilen.
>
>>https://fdm-sh.de/

>Die schleswig-holsteinische Landesinitiative zum FDM fördert kooperative Lösungen und ermöglicht eine effektive Koordination, Vermittlung von Kompetenzen und Schaffung gemeinsamer Strukturen im Umgang mit Forschungsdaten. Im partnerschaftlichen Engagement sollen Wege gefunden werden, um das zeitgemäße Forschungsdatenmanagement vor Ort gemeinsam zu bewältigen und dabei Know-how und Ressourcen zu teilen.
>
> -- https://fdm-sh.de/

>>**Verschachtelte Hervorhebung und weitere Elemente**
>
>Hervorebungen können ineinander verschachtelt werden und weitere Elemente enthalten, wie z. B.
>
>> - Listen
>>
>> - Tabellen
>
>| Column 1 | Column 2 | Column 3 |
>| -------- | :------: | -------: |
>| Text     |   Text   |     Text |

# B. Animationen

Animationsschritte werden mit `{{Nummer Animationsschritt}}`notiert.

**Achtung!** Die Animationen werden in der Ansicht "Textbook" nicht als Animationen angezeigt.

Animationsschritte können ineinander verschachtelt werden.

Hier ein Beispiel:

{{0}}
>**F**indable

{{1-3}}
***************
Der erste Schritt bei der (Wieder-)Verwendung von Daten besteht darin, sie zu finden. Metadaten und Daten sollten sowohl für Menschen als auch für Computer leicht zu finden sein. Maschinenlesbare Metadaten sind für das automatische Auffinden von Datensätzen und Diensten unerlässlich und daher ein wesentlicher Bestandteil des FAIRification-Prozesses.

F1. (Meta)data are assigned a globally unique and persistent identifier

F2. Data are described with rich metadata (defined by R1 below)

F3. Metadata clearly and explicitly include the identifier of the data they describe

F4. (Meta)data are registered or indexed in a searchable resource

***************

{{0}}
>**A**ccessible

{{2}}
***************
Sobald der Nutzer die gewünschten Daten gefunden hat, muss er wissen, wie er auf sie zugreifen kann, möglicherweise einschließlich Authentifizierung und Autorisierung.

A1. (Meta)data are retrievable by their identifier using a standardised communications protocol

A1.1 The protocol is open, free, and universally implementable

A1.2 The protocol allows for an authentication and authorisation procedure, where necessary

A2. Metadata are accessible, even when the data are no longer available

***************

{{0}}
>**I**nteroperable

{{3}}
***************
Daten sollten in einer Form vorliegen, die die Nutzung mit diversen Anwendungen oder Arbeitsabläufen für die Analyse, Speicherung und Verarbeitung ermöglichen.

I1. (Meta)data use a formal, accessible, shared, and broadly applicable language for knowledge representation.

I2. (Meta)data use vocabularies that follow FAIR principles

I3. (Meta)data include qualified references to other (meta)data

***************

{{0}}
>**R**eusable

{{4}}
***************
Das Ziel von FAIR ist es, die Wiederverwendung von Daten zu optimieren. Um dies zu erreichen, sollten Metadaten und Daten gut dokumentiert und beschrieben sowie mit einer eindeutigen Angabe bzgl. der Nutzungsbedingungen (Lizenzen) versehen sein.

R1. Meta(data) are richly described with a plurality of accurate and relevant attributes

R1.1. (Meta)data are released with a clear and accessible data usage license

R1.2. (Meta)data are associated with detailed provenance

R1.3. (Meta)data meet domain-relevant community standards

***************

Wir können auch Inline {5}{animieren}.

# B.1 Animationen mit Sprachausgabe

{{|>}}
> Achtung! Jetzt gut aufpassen!

LiaScript ermöglicht eine automatische Sprachausgabe bei Annimationsschritten. Hierfür wird die Notation für die Animationen um zwei Minuse am Begin und am Ende der Notation ergänzt: `--{{Nummer Animationsschritt}}--`


___Hier ein Beispiel:___

{{1}}
>**F**indable

{{2}}
***************
Der erste Schritt bei der (Wieder-)Verwendung von Daten besteht darin, sie zu finden. Metadaten und Daten sollten sowohl für Menschen als auch für Computer leicht zu finden sein. Maschinenlesbare Metadaten sind für das automatische Auffinden von Datensätzen und Diensten unerlässlich und daher ein wesentlicher Bestandteil des FAIRification-Prozesses.
***************

{{3}}
***************

F1: (Meta)data are assigned a globally unique and persistent identifier

F2: Data are described with rich metadata (defined by R1 below)

F3: Metadata clearly and explicitly include the identifier of the data they describe

F4: (Meta)data are registered or indexed in a searchable resource

***************

--{{1 UK English Female}}--
**F**indable

--{{2}}--
Der erste Schritt bei der (Wieder-)Verwendung von Daten besteht darin, sie zu finden. Metadaten und Daten sollten sowohl für Menschen als auch für Computer leicht zu finden sein. Maschinenlesbare Metadaten sind für das automatische Auffinden von Datensätzen und Diensten unerlässlich und daher ein wesentlicher Bestandteil des FAIRification-Prozesses.

--{{3 UK English Female}}--
F1: (Meta)data are assigned a globally unique and persistent identifier
F2: Data are described with rich metadata (defined by R1 below)
F3: Metadata clearly and explicitly include the identifier of the data they describe
F4: (Meta)data are registered or indexed in a searchable resource


# C. Verweise
Kurzer Blick auf die Verweismöglichkeiten...

## C.1 Externe Verweise

einfachste Möglichkeit: Link einfügen:
https://liascript.github.io/ 

oder so:
[Geschäftordnung der schleswig-holsteinische Landesinitiative zum Forschungsdatenmanagement](https://macau.uni-kiel.de/receive/macau_mods_00005047)

Beitrag von André Dietrich und Sebastian Zug auf OERinfo:
[Warum braucht offene Bildung eine eigene Sprache? Wie LiaScript OER befördern kann](https://open-educational-resources.de/warum-braucht-offene-bildung-eine-eigene-sprache-warum-liascript/)


## C.2 Interne Verweise

Weiter geht es mit den [Verweisen auf Bilder](#C.2-Bilder)

## C.2 Bilder

![5 V-Freiheiten für Offenheit](https://open-educational-resources.de/wp-content/uploads/20180111Infografik_5V.jpg "5 V-Freiheiten für Offenheit“  unter CC BY 4.0 basierend auf „Defining the ‘Open’ in Open Content and Open Educational Resources“ von David Wiley auf www.opencontent.org/definition/ unter CC BY 4.0.")

![3,5″-Diskette](https://mainzed.pages.gitlab.rlp.net/open-educational-resources/cms/img/uploads/3-5_zoll_floppy_disc.jpg)



## C.3 Sound & Musik

?[Teddybears - Sunshine](https://soundcloud.com/user34473679/sets/teddybears-sunshine)

??[DINI Zertifikat](https://creators.spotify.com/pod/profile/dinitus/episodes/Das-DINI-Zertifikat-e37ctsa)

## C.4 Videos 

!?[OER Erklärvideo](https://www.youtube.com/watch?v=1WnZD7E8FKY "Was versteht man eigentlich unter Open Educational Resources (OER)? Lizenziert unter der Creative Commons-Lizenz CC BY-SA 4.0. ")

!?[Data Sharing and Management](https://www.youtube.com/watch?v=66oNv_DJuPc "Das beliebte Snafu Video")




## C.5 A Modell, Simulationen etc.

??[](https://sketchfab.com/3d-models/silver-tridrachm-of-metapontion-7021310c348c426c8a993760b64636bd)

??[](https://phet.colorado.edu/sims/html/states-of-matter/latest/states-of-matter_all.html)

??[](https://umap.openstreetmap.de/de/map/new/?scaleControl=false&miniMap=false&scrollWheelZoom=true&zoomControl=true&editMode=disabled&moreControl=true&searchControl=true&tilelayersControl=null&embedControl=true&datalayersControl=true&onLoadPanel=none&captionBar=false&captionMenus=true#10/54.3526/10.1129)

## C.6 IFrames

<iframe src="https://macau.uni-kiel.de/content/index.xml" width="100%" height="600" style="border:1px solid black;">
</iframe>

--- 

<iframe src="https://answergarden.ch/embed/4191023" width="100%" height="600px" style="border: none;" scrolling="no" frameborder="0" title="AnswerGarden" allowTransparency="true"><p><a href="https://answergarden.ch/4191023">Go to AnswerGarden</a></p></iframe>

---

<iframe src="https://umap.openstreetmap.de/de/map/new/?scaleControl=false&miniMap=false&scrollWheelZoom=true&zoomControl=true&editMode=disabled&moreControl=true&searchControl=true&tilelayersControl=null&embedControl=true&datalayersControl=true&onLoadPanel=none&captionBar=false&captionMenus=true#10/54.3526/10.1129" width="100%" height="600" style="border:1px solid black;">
</iframe>


# D. Fragen und Quizze


**Single-Choice Quiz Beispiel:**
Wie heißt die Hauptstadt von Frankreich?

    - [( )] London
    - [( )] Berlin
    - [(X)] Paris
    - [( )] Rom
    - [( )] Kiel
***********************************************************************
>Toll! das ist Richtig ! 🔆

***********************************************************************

---

<div style="background-color: lightblue;padding: 25px">
**Multiple-Choice Quiz Beispiel:** Which of the following are primary colors?

- [[X]] Red
- [[X]] Blue
- [[ ]] Green
- [[X]] Yellow
- [[?]] Grün ist falsch

</div>

---

>**Text-Quiz Beipsiel:**
>Frage: Wie heißt der Open Access Textpublikationsdienst der Christian-Albrechts-Universität zu Kiel (Nutze Großbuchstaben)?
>
>[[MACAU]]

---

**Lückentext Quiz Beispiel:**

**Vervollständige den folgenden Satz:**

Leitprinzipien im FDM sind die [[FAIR]]-Prinzipien.

---

<div style="color: tomato;padding: 25px">

**Vervollständige den folgenden Satz:**

Die FAIT-Prinzipien stehen für F=[[findability]], A=[[accessibility]], I=[[interoperability]], and R=[[reusability]].

</div>

---

<div style="background-color: blue;color: white;padding: 150px;">

**Welche Leitlinie der DFG Leitlinien zur guten wissenschaftlichen Praxis beschäftigt sich mit der Dokumentation?**

[[ Leitlinie 1 | Leitlinie 5 | Leitlinie 3 | (Leitlinie 12) ]]
***********************************************************************
![Party-Gif](https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExbjNtY3A1aHI4djV1cnhoeHBpNmk5MGFzengzMDI0c3RpNWt6dDg4ayZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/fUQ4rhUZJYiQsas6WD/giphy.webp)

💓 Richtig! 💓
***********************************************************************

</div>

---

**Matrix-Beispiel:** Ordne die Aussagen den FAIR-Prinzipien zu.

- [[Findable] [Accessible] [Interoperable] [Reusable]]
- [    [ ]           [ ]          [X]        [ ]     ]  Daten sollten in einem möglichst offenen Format vorliegen.
- [    [ ]           [ ]          [ ]        [X]     ]  Daten sollten mit einer eindeutigen Lizenz versehen sein.
- [    [ ]           [X]          [ ]        [X]     ]  Zugang zu Daten, inkl. Authentifizierung und Autorisierung sollte klar beschrieben sein.
- [    [X]           [ ]          [ ]        [X]     ]  Dateinamen sollten auf den Inhalt verweisen.

---



# E. ASCII-Art

Mit Ascii kann man zeichnen 👌

<!-- style="width: 80%;background-color: yellow;"-->
``` ascii

         Ziel🎯
          /\
         /  \
        /____\
  Zeit⏳       Zielgruppe👥 
```




# F. Frag die Künsteliche Intelligenz

>**Wenn Du mal nicht weiter weißt...**
>
>https://phind.com
>
>oder
>
>https://openai.com/chatgpt/
