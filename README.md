# Die SOLID-Prinzipien – Fünf Grundsätze für bessere Software

Die Qualität der Software ist nicht in allen Projekten ideal. Der Einsatz von
Software Engineering soll den Code in all seinen Aspekten verbessern. Mit diesen
fünf Prinzipien kommen Sie dem Ziel näher. Denn guter Code motiviert!

Immer wieder hört man Aussage wie: „Warum sollte ich überhaupt guten Code schreiben?
Interessiert doch eh keinen. Hauptsache, das Projekt ist abgeschlossen!“.
Ein großer Teil der Programmierer gibt sich mit schlechtem Quellcode zufrieden,
ganz nach dem Motto: „Was willst Du denn, es läuft doch?!“

## Doch der Preis von schlechtem Code ist hoch

> Hoher Wartungsaufwand
> Hohe Kosten für die Weiterentwicklung
> Aufwändige Fehlersuche

Die interne Qualität des Codes trägt also langfristig zu einer Reduzierung
der Gesamtkosten bei.

## Warum ist guter Code noch wichtig?

- Code schreiben ist ein relativ kleiner Teil der Softwareentwicklung. Etwa 80%
  der Kosten entfallen auf die anschließende Wartung.
  
- Es wird wenig neuer Code geschrieben. Die hauptsächliche Arbeit besteht aus Änderungen.
  Der größte Anteil an der Arbeit ist nicht das Codieren, sondern das Verstehen (Lesen) von Code.  
  
- Fehlerbehebungen in unverständlichem Code erzeugen schnell neue Fehler.

- Wenn am Anfang des Projektes auf Kosten der Codequalität Zeit gespart wird, wird dies
  am Ende des Projektes ein Vielfaches der eingesparten Zeit kosten.

Prinzipiell ist jedem (erfahrenen) Entwickler bekannt, dass schlechter Code die Arbeit
behindert. Allerdings passiert es immer wieder, dass aufgrund von hohem Druck chaotischer
Code geschrieben wird, damit Termine eingehalten werden können.

Doch das funktioniert nicht. Der schlechte Code führt dazu, dass die Arbeit langsamer vorangeht
und Termine nicht eingehalten werden. Es gibt nur einen Weg: von Anfang sauberen Code schreiben!

## Was ist sauberer Code?

- Sauberer Code ist leichter lesbar.

- Andere Entwickler können ihn besser lesen und verstehen.

- Klassen und Methoden sind auf die Erfüllung einer Aufgabe ausgerichtet und werden nicht durch
  Nebenaufgaben „verunreinigt“.

- Die Abhängigkeiten zu anderem Code sind auf ein Minimum begrenzt.

- Sauberer Code ist gut zu testen.

- Es gibt keine Duplizierungen.

- Der Code enthält keine Überraschungen.

## Guter Code motiviert

- Alle Beteiligten sind stolz auf ihre Arbeit.

- Das Programmieren macht mehr Spaß.

- Der Code enthält weniger Fehler.

- Guter Code ist einfacher zu testen.

Für den Mitarbeiter im Projekt heißt das: Guter Code reduziert unangenehme Arbeit.

## Die Checkliste für sauberen Code

Um die Erstellung guten Codes zu erleichtern, wurden mehrere Prinzipien für
die Softwareentwicklung formuliert. Diese können als eine Art Checkliste gesehen
werden, die in der täglichen Arbeit des Entwicklers als Hilfe dienen, die eigene
Arbeit zu reflektieren bzw. von vornherein Fehler und kritische Konstrukte zu vermeiden.

Prominente Vertreter solcher Prinzipien sind die SOLID-Prinzipien. SOLID wurde
von Robert C. Martin geprägt.

Es ist ein Akronym und steht für:

- S Single-Responsibility-Prinzip
- O Open-Closed-Prinzip
- L Liskovsches Substitutionsprinzip
- I Interface-Segregation-Prinzip
- D Dependency-Inversion-Prinzip

Wenn diese Prinzipien eingehalten werden, entsteht besserer Code, und die Software
wird besser wartbar.

## Das Single-Responsibility-Prinzip

Das Single-Responsibility-Prinzip besagt, dass eine Klasse nur eine Verantwortlichkeit
haben soll. Änderungen an der Funktionalität sollen nur Auswirkungen auf wenige Klassen
haben. Je mehr Code geändert werden muss, desto höher ist das Fehlerrisiko.

Hält man sich nicht an dieses Prinzip, verursacht das zu viele Abhängigkeiten und hohe
Vernetzung. Das ist wie im wirklichen Leben: Ab einer bestimmten Größe wird ein
Universalwerkzeug unhandlich.

### Wie kann erkannt werden, ob die Klasse mehr als eine Aufgabe erfüllt?

Die Klasse darf nur einen Grund zur Änderung haben. Wenn sich zwei Anforderungen ändern,
darf nur eine davon eine Auswirkung auf die Klasse haben. Hat die Klasse mehrere
Änderungsgründe, erfüllt sie zu viele Aufgaben.

Es ist also besser, viele kleine Klassen zu haben als wenige große.

Der Code wird dadurch nicht umfangreicher – er wird nur anders organisiert. Analogie
aus dem Bastelkeller: Wenn alle Schrauben in einer Kiste liegen, ist es schwer,
die Richtige zu finden. Sind sie gut sortiert auf mehrere Schachteln verteilt, geht
das Suchen viel schneller. Genauso verhält es sich mit den Klassen.

## Das Open-Closed-Prinzip

Nach dem Open-Closed-Prinzip soll eine Klasse offen für Erweiterungen, aber geschlossen
gegenüber Modifikationen sein. Das Verhalten einer Klasse darf erweitert, aber nicht
verändert werden. Dieses Prinzip hilft, Fehler in schon fertigen Codeteilen zu vermeiden.
Wenn eine Erweiterung nur durch Änderungen innerhalb einer Klasse erreicht werden kann,
ist die Gefahr sehr groß, dass durch die Änderung schon fertig implementierte Funktionen
neue Fehler bekommen.

Das Open-Closed-Prinzip lässt sich normalerweise über zwei Wege erreichen:

- Vererbung

- Einsatz von Interfaces

Durch Einhalten dieses Prinzips können einer Applikation neue Funktionen hinzugefügt
werden, ohne bestehende Klassen zu verändern.

## Das Liskovsche Substitutionsprinzip

Das Liskovsche Substitutionsprinzip fordert, dass abgeleitete Klassen immer anstelle
ihrer Basisklasse einsetzbar sein müssen. Subtypen müssen sich so verhalten wie ihr
Basistyp. Das klingt selbstverständlich, aber ist es das auch? Der Compiler weiß,
dass eine abgeleitete Klasse auch vom Typ der Basisklasse ist – also immer in diese
konvertiert werden kann. Ist das ausreichend? Das Liskovsche Substitutionsprinzip
geht weiter als der Compiler.

## Das Interface-Segregation-Prinzip

Das Interface-Segregation-Prinzip besagt, dass ein Client nicht von den Funktionen
eines Servers abhängig sein darf, die er gar nicht benötigt. Ein Interface darf demnach
nur die Funktionen enthalten, die auch wirklich eng zusammengehören. Die Problematik
ist, dass durch „fette“ Interfaces Kopplungen zwischen den ansonsten unabhängigen
Clients entstehen.

Wird ein Aspekt des Interfaces verändert, hat das Auswirkung auf alle Clients, selbst
wenn sie diesen Aspekt nicht nutzen.

## Das Dependency-Inversion-Prinzip

Das Dependency-Inversion-Prinzip besagt, dass Klassen auf einem höheren Abstraktionslevel
nicht von Klassen auf einem niedrigen Abstraktionslevel abhängig sein sollen. Dabei
geht es nicht darum, die Abhängigkeiten einfach umzudrehen. Abhängigkeiten zwischen
Klassen soll es nicht mehr geben; es sollen nur noch Abhängigkeiten zu Interfaces
bestehen (beidseitig). Interfaces sollen nicht von Details abhängig sein, sondern
Details von Interfaces. Beispiel: Die Klassen in Bild 4 sind zu stark miteinander
verkoppelt.

Die Abhängigkeiten sind so stark, dass ohne Codeänderungen der separate Test einer
Klasse nicht möglich ist. Auch Änderungen in den Anforderungen sind durch diese
starke Kopplung schwerer umzusetzen.
