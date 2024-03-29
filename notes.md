## Problemstellung:

Es geht grundsätzlich um die Ähnlichkeit von geometrischen Graphen (also Graphen eingebettet in die Ebene). Zum Beispiel können dies zwei Repräsentationen desselben Strassennetzwerkes sein (zB OSM verglichen mit Google Maps oder einer kommerziellen Karte). 

Um die Ähnlichkeit zu messen, gibt es verschiedene Masse, und die algorithmische Herausforderung ist, diese effizient zu berechnen. Wobei es gar nicht so viele geeignete Ähnlichkeitsmaße gibt, da viele Graphähnlichkeitsmaße abstrakte Graphen (ohne die geometrische Einbettung) vergleichen.
Aus diesem Grund wurde in [1]"graphs_eurocg_2020_weitergedacht2" ein neues Maß definiert, welches "strong" und "weak graph distance" genannt wird.
Bisher gezeigt wurde dabei, dass dieses unter bestimmten Bedingungen an die Graphen bzw. das Maß NP-schwer ist bzw. sich polynomiell berechnen lässt: polynomiell berechnen lässt es sich zB falls der erste Graph ein Baum ist, oder auf planaren Graphen mit einer weiteren Eigenschaft für den schwachen Graphabstand. Allgemeiner ist das Problem allerdings NP-schwer.

 Der Graphabstand beruht darauf, dass ein Graph auf den anderen abgebildet wird (diese Abbildung muss weder injektiv noch surjektiv sein). Für eine solche Abbildung nimmt der Graphabstand dann den Wert des größten Abstandes an. Wir nennen dies ein "bottleneck distance measure", da der größte Abstand im Graphen den gesamten Abstand bestimmt. Als Abstand im Graphen betrachten wir genauer den Abstand einer Kante im ersten Graphen zu dem Pfad im zweiten Graphen, auf den die Kante abgebildet wird. 

 Hierbei wiederum verwenden wir ein Abstandsmass auf Kurven, den sogenannten Frechet Abstand (siehe dazu [2]"frechet-distance"). Dieser ist ebenfalls ein bottleneck distance, dh. er nimmt den größten Abstand einer Abbildung der Kante auf den Pfad an. Der Grund, dass hier ein Maximum (und keine Summe oder Durchschnitt) gewählt wird, ist, dass das Maß so eine Metrik auf dem Raum der Kurven ist. 

 Dennoch ist es nicht immer praktisch, nur das Maximum zu kennen. Insbesondere wenn man sich für die Abbildung auf den Kurven bzw. Graphen interessiert, dann wäre es eigentlich wünschenswert nicht nur das Maximum zu optimieren, sondern alle Abstände auf der Kurve bzw. Graphen. Für Kurven gibt es hierzu auch einen geeigneten Ansatz, den sogenannten "lexicographic" Frechet Abstand.  Eine Frage, die man sich dazu anschauen könnte, ist, ob dies auch auf Graphen zu übertragen wäre. Eine direkte Übertragung ist allerdings nicht möglich, hier wurden dann neue Ansätze entwickelt.

Bei diesen sind noch einige Fragen offen, welche im Rahmen der Bachelor-Arbeit ausgearbeitet werden.

## Aufgabenstellungen:

1) Detaillierte Darstellung des Algorithmus für den min-sum Graph Abstand auf Bäumen mit der Einschränkung, dass Knoten auf den nächsten Punkt im epsilon-Placement abgebildet werden
2) Beweis der NP-Schwerheit des min-sum Graph Abstands auf Graphen
3) optional: Anpassung des Algorithmus, wenn der Fréchet Abstand auf Kanten durch den summierten diskreten Fréchet Abstrand (bzw. Dynamic Time Warping) ersetzt wird


## Zeitplan

- 06/23 - 07/23: Einarbeitung (Komplexitätstheorie, Referenz-Paper, ...)
- 08/23 - 10/23: Ausarbeitung und Formalisierung der Ergebnisse
- 11/04 - Anmeldung der Bachelorarbeit
- 11/23: Vortrag der Ergebnisse im Oberseminar
- 12/29: Abgabefrist



