# ACHT CLEAN CODE-PRINZIPIEN FÜR DAS NAMING

## Zweckbeschreibende Namen wählen

Es wäre schön, wenn der Name selbsterklärend wäre und sich dabei auf das Wesentliche konzentriert. Im Java-Umfeld sieht man leider häufig Hässlichkeiten wie „akzeptiereNeukundenAnlageUndReicheDieDatenWeiterOhnePruefung()“. Wenn möglich, sollte man auf die Bindewörter „und“ und „oder“ in Bezeichnern verzichten und maximal 3-4 Hauptwörter verwenden.

## Fehlinformationen vermeiden

Leider sieht man in der Praxis immer wieder, dass Methoden- oder Variablennamen schlicht falsch sind, oft weil sie mit Copy + Paste aus anderen Kontexten gerissen und anderswo eingefügt wurden. Ein „speichereDaten()“ sollte das auch tun und nicht nur die Prüfungen vor dem Speichern enthalten und dann delegieren. Namen sollten auch einigermaßen vollständig sein, ein „toByteArray(HochgeladeneDatei)“ sollte nicht heimlich die Links entfernen, falls es ein PDF ist.

## Unterschiede deutlich machen

Bei ähnlichen Methoden oder Variablen sollte man die Unterschiede betonen und nicht die Gleichheit ausnutzen. Postfixe wie „A, B, C“ oder „1, 2, 3, …“ sind für das Verständnis schlecht. Statt „berechnungswertA“ und „berechnungswertB“ sollten Namen gewählt werden, die kennzeichnen, wo sich die Berechnungswerte unterscheiden.
Ähnliche Konstrukte sollten jedoch auch ähnlich benannt sein: „starteRaumschiff“ und „spaceshuttleLaunch“ wären hier Negativbeispiele.

## Aussprechbare Namen verwenden

Man sollte sich klar machen: Menschen sprechen Namen aus! Wer Konstrukte anlegt, die sich lächerlich anhören oder die unaussprechlich sind, fördert höchstens die Lachmuskeln der Kollegen. Auch auf humorige Namen wie beispielsweise „bool dozer“ oder „long timeago“ sollte man verzichten.

## Suchbar sollten sie sein

Code wird nicht nur häufig gelesen, er wird auch oft durchsucht. Es hilft dafür wenig, wenn Namen zu häufig vorkommen oder mehrfach in verschiedenen Kontexten verwendet werden. Eine Methode „getData“ in einer großen Codebasis zu suchen, kann sich schnell als unlösbare Aufgabe herausstellen.

## „Ungarische Notation"

Technische Informationen haben im Namen nichts verloren (auch als „ungarische Notation“ bekannt). Beispiel sind hier „fMyCounter“ (hier steht das „f“ als Präfix für „field“) oder „booleanIstKundeAngemeldet“. In weniger streng getypten Sprachen können solche Informationen wichtig sein, in Java (oder anderen streng getypten Sprachen) sind sie in der Regel überflüssiger „Clutter“, der das Lesen stört. Die Informationen werden in der Regel mithilfe der IDE dargestellt. Auch auf Präfixe in Namen sollte man generell verzichten.

## Guck mal, wer da spricht

Naming ist umso wichtiger, umso weitreichender der Quellcode verwendet wird, gerade bei Schnittstellen zu anderen Systemen. Insbesondere bei APIs, in Interfaces, bei abstrakten Klassen, bei Domain Objects und bei der Strukturierung der Anwendung in den Packages und Verzeichnissen gibt unsere Namenswahl maßgeblich die Implementierung von (Fremd-)Code vor, der unsere Namen weiter nutzen wird. Wenn wir nicht wollen, dass die Nutzer unserer Schnittstellen in ihrem Code unverständliche Konstrukte bauen, sollten wir erst einmal selbst klare und verständliche Namen verwenden.
