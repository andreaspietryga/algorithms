Der Code zu "Paper2 TD Search non-learning distribution creator" ist identisch zu dem Code "Paper2 TD Search learning distribution creator" mit einem Unterschied. Wie auch im Fall, in dem das Auto lernt, wird ihm im ersten Schritt aufgetragen alle 60 Routen abzufahren. Der Unterschied befindet sich in den Befehlen die nach der Markierung "Beginning of the non learning - Loop" kommt. Hier wird dem AV sozusagen eines seiner 60 verschiedenen "Gehirne", die es entwickelt hat als es die 60 Routen abgefahren ist, eingepflanzt. Dies geschieht durch:

totalsconst = Flatten[totalslist[[ss]]];

  nstateconst = Flatten[nstatelist[[ss]]];

  Qstateconst = Qstatelist[[ss]][[1]]];

ss steht dabei für safety stock. Für ss=1 wurde demnach 1GE investiert und das AV ist bereits eine Route abgefahren. Mit diesem "Gehirn" wird ihm aufgetragen, alle 60 Routen abzufahren ohne dabei zu lernen. Weshalb alle 60 Routen? Da wir im Vorfeld nicht wissen, welche Route das AV im nicht-lern Modus abfahren wird und alle Routen sich voneinander unterscheiden, wollen wir damit beitragen einen guten Schätzer zu erzielen. 

Die Realisationen dieser Fahrten wurden in der Datei "Paper2 distribution" abgetragen und daraufhin ein Durchschnittswert gebildet für die jeweiligen safety stocks/Routen. Diese Daten wurden verwendet um Figures 2.5 bis 2.7 zu erstellen, sowie gingen sie bei der Berechnung in den Code für "Paper2 Investmentproblem Open-Loop Strategy" ein.
