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

beschreibt die optimalen Investionen zum Zeitpunkt 12 in Abhängigkeit des safetystocks über den man verfügt. Da keine Gewinne mehr erzielt werden können, sollte man daher nichts investieren.


V121 beschreibt die Wertefunktion, wenn in Periode 12 eingeführt wurde. Die 1 nach der 12 symbolisiert jetzt eingeführt.

{-2., -2., -2., -2., -2., -2., -2., -2., -2., -2., -2., \
0.225999, 0.488499, 0.675999, 4.35345, 0.825999, 0.392669, 0.580169, \
0.692669, 0.730169, 0.498047, -1.64572, -1.75459, 11.5601, 10.6278, \
4.13441, 4.39691, 7.13765, 7.63941, 8.11109, 8.37359, 8.56109, \
8.67359, 8.71109, 9.7203, 9.9828, 10.1703, 11.4206, 11.9103, 6.61882, \
6.65632, 9.23844, 11.999, 12.2615, 12.449, 12.5615, 12.599, 9.724, \
9.7615, 7.84363, 10.5932, 10.8557, 12.4509, 12.7134, 12.9009, 13.0134


V121a

{{0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {0}, {4}, \
{3}, {2}, {5}, {0}, {3}, {2}, {1}, {0}, {0}, {0}, {4}, {5}, {5}, {4}, \
{3}, {4}, {4}, {4}, {3}, {2}, {1}, {0}, {4}, {3}, {2}, {5}, {5}, {1}, \
{0}, {4}, {4}, {3}, {2}, {1}, {0}, {1}, {0}, {3}, {4}, {3}, {4}, {3}, \
{2}, {1}}


V121a beschreibt nun, welche Investitionen in Abhängigkeit des safetystocks zu wählen sind. Erst ab einem safetystock von 12 lohnt es sich überhaupt noch weiter zu investieren und zwar 4. Damit würde man am Ende über einen safetystock von 16 verfügen. 


V1211 beschreibt nun wiederrum die Wertefunktionen in Abhängigkeit der safetystock, jedoch steht die 11 für bereits in der Vergangenheit eingeführt. Es fallen also in Periode 12 keine Eintrittskosten an.
