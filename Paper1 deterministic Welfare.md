Die Datei "Paper1 deterministic Welfare" beinhaltet den Code, welcher zur Bestimmung der Werte für Tabelle 1.1 bis 1.4 verwendet wird. 
Möchte man einen spezifischen Wert innerhalb einer der Tabellen reproduzieren, muss zuerst der entsprechende Werte in der Innitierung angepasst werden. Z.b. möchte man sehen, welcher Wert von beta sich ergibt, für A=75 (Tabelle 1.2), muss  dementsprechen in der Initierung A=75 gesetzt werden. 
Der Algorithmus verwendet das Gauss Seidel Verfahren, was bedeutet, dass rekursiv Schätzer als neue Schätzer in die Gleichungen einfließen, bis sie den gesuchten Wert approximieren und sich nicht mehr signifikant verändern. 
Ich habe keine Schleife für das Gauss Seidel Verfahren geschrieben, d.h. nach der Initierung der Werte, müssen die multiplen Zeilen, die zu einem Befehl zusammengefasst wurden, mehrfach ausgeführt werden, bis die gewünschte Genauigkeit erreicht wurde. Als output erhält man die entsprechenden Werte für die Investitionen und beta (zb.):
{I12 -> 1.05134}

{I11 -> 2.07321}

{I10 -> 3.08851}

{I9 -> 4.12186}

{I8 -> 5.20165}

{I7 -> 6.36156}

{I6 -> 7.63812}

{I5 -> 9.04436}

{I4 -> 10.3909}

{I3 -> 9.89608}

{I2 -> 9.42484}

{I1 -> 8.97603}

{beta -> 0.682182}

Wenn diese Werte sich nicht mehr verändern, ist die Lösung approximiert worden. Mit der Lösung können dann weiteren Werte, welche von Interesse sind, gefunden werden, indem sie aktuallisiert werden, wie zb. welfare usw..
Nach diesem Prinzip lassen sich alle Werte innerhalb von Tabelle 1.2 bis 1.4 bestimmen. Für die Werte in Tabelle 1.1 muss die Gleichung für welfare (welche beta bestimmt) herausgenommen werden aus "multiple Zeilen" , weil wir wollen, dass beta fixe Werte annimmt.
