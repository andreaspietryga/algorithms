Der Algorithmus in "Paper 3 Collusion with Tabular Q Learning Model 1" beinhaltet reines Tabular Q-Learning, mit welchem Kollusion in den Figures 3.1 und 3.2 unter Verwengung unseres Ausgangsmodells aufgezeigt wird.
Wie ist der Algorithmus zu verwenden? Im Prinzip muss man die Angezeigten Befehle nur auswählen und ausführen und der Code reproduziert die gewünschten Ergebnisse. 
Die Variable distribution={}; die gleich zu Beginn definiert wird, dient dazu zu notieren, wie viele Episoden es gebraucht hat, um das Nash-Equilibrium zu erreichen. 
In der Regel wird kein Equilibrium angenommen, daher haben wir eine Obergrenze definiert, wie viele Episoden durchlaufen werden dürfen:
While[n <= 50001 && Length[dsize1] < 100 ||  n <= 50001 &&  Length[dsize2] < 100,

Die While Schleife wiederholt solange das Geschehen zwischen den beiden Anbietern, bis entweder die Maximale Anzahl an Episoden erreicht wird, in diesem Fall 50000 oder aber beide Firmen 100 Mal hintereinander den
Equilibriumpreis (6,6) wählen. Dies wird eingefangen durch Length[dsize1] < 100 und Length[dsize2] < 100 

dsize ist folgendermaßen definiert:

dsize1 = Position[Take[monQpricepath1, -100], 6];

dsize2 = Position[Take[monQpricepath2, -100], 6];

Innerhalb des Preispfad der beiden Spieler wird für die letzten 100 Episoden gezählt, wie oft der Preis 6 gewählt wurde. Wenn er nicht jeweils 100 Mal gewählt wurde, ist noch kein langfristiges Equilibrium erreicht.

Die Fehlermeldung am Ende des codes ist darauf zurückzuführen, dass der Preispfad zu Beginn des Spiels noch zu kurz ist, dsize aber dennoch bereits auf die 100 letzten Preise zurückgreifen will:

Take::take: Cannot take positions -100 through -1 in {3,6}.

Take::take: Cannot take positions -100 through -1 in {2,5}.

Take::take: Cannot take positions -100 through -1 in {3,6,9}.

General::stop: Further output of Take::take will be suppressed during this calculation.

Möchte man mehrere runs durchlaufen lassen und gucken, ob ein Equilibrium angenommen wurde, muss folgende Zeile gleich zu Beginn berücksichtig werden:

For[xxx = 1, xxx < 3, xxx++,

xxx beschreibt wie viele Male der gesamte Code durchlaufen soll, um ein Equilibrium zu finden, falls denn eins erreicht werden kann.

Die wichtigsten Ergebnisse und welche Variablen dazu aufgerufen werden müssen, ist am Ende des codes aufgelistet und erklärt.
