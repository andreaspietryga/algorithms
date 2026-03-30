Der code in "Paper2 TD Search learning distribution creator" beschreibt den Algorithmus TD(0)-Search with eligibility trace, den ich geschrieben habe, um das Lernverhalten des AVs zu simulieren. Im Prinzip wird dem AV vorgebenen alle 60 Routen abzufahren und ihm dabei erlaubt zu lernen. Das Ergebnis des Abfahrens der Routen wird in folgenden Mengen abgespeichert:

Daten`distriacc = {};  --> hier wird für jede einzelne Route abgespeichert, wie viele Unfälle gemacht wurden. Dabei handelt es sich um Crashes mit roten Blöcken

Daten`distriinapp = {}; --> wie oft inappropriate driving beobachtet wurde

Daten`districrash = {}; --> wie viele Unfälle mit anderen Autos beobachtet werden

Daten`districounting = {}; --> wie viele Teilstrecken abgefahren werden 

(die Crashes und Unfälle wurden später zusammengezähl. In einer ersten Version meines Codes wollte ich dies noch gesondert betrachten, habe mich jedoch letztendlich dagegen entschieden)

Um das AV alle 60 Routen abfahren zu lassen, müssen zunächst alle Variablen, die benötigt werden initialisiert werden. 
Der eigentlich Algorithmus, TD(0) läuft im grauen Bereich des Algorithmus ab. Wenn die Befehle im grauen Bereich abgerufen werden, fährt das AV alle 60 Routen ab und lernt währenddessen. 

Die Ergebnisse dieser Fahrt werden, wie in den anfangs erwähnten Mengen, letztendlich abgespeichert:

AppendTo[Daten`distriacc, Acclist];

AppendTo[Daten`distriinapp, Inapplist];

AppendTo[Daten`districrash, Crashlist];

AppendTo[Daten`districounting, Countinglist];


Die Realisationen dieser Läufe, die ich gemacht habe, sind in der Datei "Paper2 distribution" unter distriacc, distriinapp, districrash, districounting zu sehen. Dort wurden die insgesamt 158 Realisationen miteinander aufsummiert für die einzelnen Routen und der Durchschnitt gebildet.
