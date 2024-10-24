<!--
author: Richard Diebel, Britta Petersen
email: diebel@ub.uni-kiel.de, b.petersen@rz.uni-kiel.de
version: 0.0.1
date: 2024-10-22
link: https://raw.githubusercontent.com/RDM4CAU/Intro-to-RDM/refs/heads/main/cau-style.css
comment: Eine kurze Einführung, wozu Liascript dienen kann
language: de
narrator: Deutsch Female
repository: https://github.com/RDM4CAU/LiaPlayground
icon: https://raw.githubusercontent.com/RDM4CAU/TtL-FDM/main/images/fdm_lehre.png
-->

# LiaScript Einstieg 

## Vision



     {{0-3}}
******************

> Lehrende möchten motivierende, interaktive Lehrmaterialien mit einem überschaubaren Aufwand realisieren, die optimal auf die eigenen didaktischen Ziele abgestimmt sind.

******************

    {{1-3}}
******************

> Das kann er/sie natürlich alleine realisieren, aber ...

---------------------

******************

    {{2-3}}
******************

**1. Muss er/sie sich über alle Inhalte selbst Gedanken machen**

**2. Muss er/sie sich erheblichen technischen Herausforderungen stellen**

---------------------

******************


## OER

{{0-1}}
>  **Open Courseware / Open Educational Resources** ... teaching, learning and
> research materials in any medium, digital or otherwise,that reside in the
> **public domain** or have been released under an open license that permits
> no-cost access, use, **adaptation** and **redistribution** by others with no or 4
> limited restrictions. Open licensing is built within the existing framework of
> intellectual property rights as defined by relevant international conventions
> and respects the authorship of the work
>
> -- UNESCO 2002 Forum on the Impact of Open Courseware for Higher Education in Developing Countries [(Link)](https://unesdoc.unesco.org/ark:/48223/pf0000128515)


  

{{1-2}}
******************

| Anforderung                  | Bedeutung                                  |
| ---------------------------- | ------------------------------------------ |
| `verwahren/vervielfältigen ` | Download, Speicherung und Vervielfältigung |
| `verwenden`                  | Nutzung im Lernkontext                     |
| `verarbeiten`                | Umgestaltung und Adaption                  |
| `vermischen`                 | Kombination und Extraktion                 |
| `verbreiten`                 | (digitale) Publikation                     |

*_5 V-Freiheiten für Offenheit_ von Jöran Muuß-Merholz und Jörg Lohrer für [open-educational-ressources](https://open-educational-resources.de) - Transferstelle für OER*

******************

{{2-4}}
*********************

__Kritik an der 5V Definiotion__

> _1. Die 5V Definition fokussiert das Open in OER lässt aber das Education beiseite._
>
> _2. Die Verwaltung und Auffindbarkeit von OER Inhalten ist dadurch nicht erfasst._

**********************

{{3-4}}
**********************

<!--
style="width: 100%; max-width: 860px; display: block; margin-left: auto; margin-right: auto;"
-->
```ascii

      Wunsch nach                                             Wunsch nach
  einfacher Umsetzung  -----------> Konflikt <----------- spezifischen Elementen
                                       |                       im Material
                                       |
                                       v
                              OER als Lösungsansatz
```

**********************
    
## Bisherige Praxis

![Powerpoint](https://upload.wikimedia.org/wikipedia/commons/thumb/1/16/Microsoft_PowerPoint_2013-2019_logo.svg/529px-Microsoft_PowerPoint_2013-2019_logo.svg.png) 
![Prezi](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b4/Prezi_logo_transparent_2012.svg/480px-Prezi_logo_transparent_2012.svg.png) 


## Anforderungen

{{1-3}}
> 1. Materialien müssen transformierbar sein, um eine Wiederverwendung zu ermöglichen. (_Verarbeiten/Verwenden/Verbreiten_)
> 2. Materialien brauchen Metadaten, um auffindbar zu sein. (_Verbreiten_)
> 3. Materialien brauchen offenkundige Versionierungen (_Verwalten_)

{{2-3}}
__Offensichtlich brauchen wir Formate, die neben den positiven Aspekten von Textdarstellungen auch das erweiterte Set von Anforderungen abdecken.__

## LiaScript

{{1}}
**********************
LiaScript ist eine freie Erweiterung der Auszeichnungssprache [Markdown](https://de.wikipedia.org/wiki/Markdown). Die Entwickler:innen von LiaScript haben sich an GitHub Flavored Markdown orientiert und dieses um Funktionen erweitert, die einen erweiterten Einsatz von Multimedia sowie verschiedene Interaktionen mit Nutzenden ermöglichen. Mit LiaScript lassen sich interaktive und ansprechende Lehr- und Lehrinhalte erstellen, die ohne die Verwendung eines Servers im Netz verbreitet werden können.

**Die Sytax, die von Markdown schon bekannt ist, könnt Ihr also auch hier anwenden - mit kleinen Abweichungen und einigen Erweiterungen. :-D** 

-> LiaScript-Dokumente sind Textdokumente, deren Inhalt auch von einfachsten Texteditoren gelesen werden können. 

**********************

{{2}}
**********************

LiaScript erfüllt die oben genannten Anforderungen:

> 1. Materialien müssen transformierbar sein, um eine Wiederverwendung zu ermöglichen. (_Verarbeiten/Verwenden/Verbreiten_) --> LiaScript kann in andere Formate wie PDF, Docx, HTML, SCORM u.v.m konvertiert werden
> 2. Materialien brauchen Metadaten, um auffindbar zu sein. (_Verbreiten_) --> LiaScript kann einen Metadatenblock am Anfang jedes Dokuments enthalten, der es auffindbar macht
> 3. Materialien brauchen offenkundige Versionierungen (_Verwalten_) --> LiaScript ist als einfaches Textformat über Git lückenlos Versionierbar

**********************

{{3}}
**********************
Und weitere:

> 1. Einfache Syntax (_Verarbeiten/Vermischen/Verbreiten_)
> 2. Serverloses Hosten (_Verbreiten_) 
> 3. Multimedialität und Interaktivität durch Medien und interaktive Elemente  (_Education_)

**********************
