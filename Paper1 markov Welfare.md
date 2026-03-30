Der Algorithmus "Paper1 markov Welfare" wird zur Bestimmung der Werte innerhalb der Tabelle 1.9 verwendet. Wie auch im Algorithmus für "Paper1 deterministic Welfare" und "Paper1 open loop Welfare" wird hier wiederrum das Gaus Seidel Verfahren verwendet. Der Algorithmus läuft nach dem gleichen Prinzip wie auch zuvor. Innerhalb der Innitierung werden die entsprechenden Werte angepasst, welche innerhalb des betrachteten Falls fix bleiben sollen. 
Innerhalb der Initierung, werden ebenfalls alle für die Berechnung des "beta-qwer" benötigten Gleichungen definiert. Da es innerhalb des Markov Falls zu einem Regimechange kommen kann bezüglich der Haftung beta, muss entsprechend die Nachfrage vor und nach dem Regimechange definert werden. In diesem Sinne bedeutet:

Q2o --> Nachfrage in Periode 2, wenn beta=0 und soweit kein Regimechange vorlag.

Q2b2  --> Nachfrage in Periode 2, wenn beta=beta-quer und der Regimechange bezüglich der Haftung in Periode 2 eintrat. das "b" steht dementsprechend für Eintritt der Haftungsregelung und die 2 wann der Haftungswechsel stattfand. 

(*multiple Lines *) steht wiederrum für die Befehle, die innerhalb des Gaus Seidel Verfahrens iterativ wiederholt werden müssen. Bestimmt werden hier die Schätzer für die Investitionen und beta-qwer:

I2o--> Investition in Periode 2 ohne Haftungswechsel

I2b2--> Investition in Periode 2, wenn Haftungswechsel in Periode 2stattfand.

Die Gleichungen b,bb,...,l,ll die nach (*multiple Lines*) kommen, dienen zur Bestimmung der Genauigkeit der Schätzer. Erst wenn die Differenz aufeinander folgender Werte ungefähr 0 ergeben, ist die Schätzung gut genug.

Darauf folgen die hergeleiteten Investitionspfade, die je nach eintreten des Regimewechsels realisiert werden.

Bezüglich der Gewinne (Beispiel):

(*PI k=4*)  steht für den gesamten Gewinn, den die Firma erzielt hat, wenn der Regimewechsel bezüglich der Haftung in Periode k=4 stattfand. Um die Gewinne vergleichbar zu machen, habe ich die Gewinne vor dem Regimewechsel hinzuaddiert unter der Haftung beta=0 --> d.h. die Gewinne bis zur Periode 3 unter beta=0 und dann alle Gewinne ab Periode 4 unter beta=beta-qwer bis zu Periode 12.
