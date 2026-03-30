Der Dyna-2 Algorithmus beschreibt den Algorithmus, mit dem der Monopolist seine optimale Investition tätigt. 

Um den Dyna-2 Algorithmus zu verwenden, muss man zuerst einmal unterscheiden, ob man einen Monopolisten verwenden will, der noch "keine Erfahrung" damit gemacht, wie man richtig in das Training eines AV investiert. In diesem Fall muss die Datei  "Paper2 Dyna-2 algorithm zero knowledge" geöffnet werden. 

die folgenden Listen, die gleich zu Beginn in den ersten Zeilen definiert werden, enthalten die Performance Daten des AVs. Die Listen stehen unter (*List in order to track the results*) und müssen initialisiert werden.

Der Code der darauf folgt umfasst Dyna-2 mit AV Simulator. Durch das Abrufen des Codes wird ein run durchlaufen. Ein run umfasst 12 Perioden, in denen der Monopolist investieren kann. Nachdem der run durchlaufen ist, können die Ergebnisse abgerufen werden, indem man eine der oben definierten Listen betrachtet. In "Paper2 Dyna-2 results" wird beschrieben wofür die Listen stehen, und welche Performence damit eingefangen wird.


Möchte man dagegen einen Monopolisten verwenden, der bereits über einen gewissen Wissensstand verfügt, muss hierzu den folgenden Listen einen Wert zugeordnen, welche ebenfalls in "Paper2 Dyna-2 results" erklärt werden:

Daten`W, Daten`accspace, Daten`inappspace, Daten`countingspace, Daten`profspace, Daten`profitspace, Daten`Nspace, Daten`eta

Diese Listen umfassen die Beobachtungen, die der Monopolist im Laufe unzähliger Investitionen in das Training des AVs gemacht hat. Die Listen können im Prinzip gefüllt werden, indem man die Werte aus "Paper2 Dyna-2 results" den Listen zuweist. Danach kann man den Algorithmus "Paper2 Dyna-2 algorithm with knowledge" starten. 
