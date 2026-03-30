Die Datei "Paper2 Investmentproblem Open-Loop Strategy" umfasst den Code, mit der man die Open-Loop Strategie bestimmt. Was genau der Code macht, ist es die Wertefunktionen V für jede Periode zu bestimmen 
und die optimalen Investitionen, die sich daraus ableiten lassen.

Der gesamte Code muss nur einmal ausgeführt werden. Beim Ausführen des Codes werden zuerst die Variablen und Funktionen initialisiert, danach über Bachwardinduktion die Wertefunktionen und Aktionen bestimmt.

Wie sind die Ergebnisse zu lesen und zu interpretieren:

Beispiel: wir betrachten Episode 12, dann steht V120 für die Wertefunktion in Periode 12, wenn das Produkt noch nicht eingeführt wurde.
V120

{0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0.,
0., 0., 0., 0., 0., 0., 0.}

die Liste mit den Einträgen 0 hat eine Länge von 60 Einträgen. Jeder Eintrag beschreibt die Wertefuntion, wenn über einen entsprechenden Safetystock verfügt wird. Demnach ist der Wert der Wertefunktion zum Zeitpunkt 12
0 für jeden safetystock, weil in Episode 12 weiterhin nicht eingeführt wird und damit kein Gewinn erzielt wird.

 V120a

 {{0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, 
{0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, 
{0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, 
{0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, 
{0}, {0}}
