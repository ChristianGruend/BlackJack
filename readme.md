(1)
einlesen der Karten aus json-file
--

(41-44)
double down führt die draw-Funktion einmal aus und überigbt eine 2 für doppelte Punktzahl an die Überprüfungsfunktion
--

(45-79)
setzt alle Punkte und Anzeigen zurück auf default
--

(65-73)
laden von 6 Kartendecks in den Kartenstapel
--

(74)
Mischen der Karten
--

(75)
2x Draw Funktion für die beiden Anfangskarten, die der Spieler erhält
--

(77)
Überprüfung ob die beiden Angangskarten den gleichen Wert haben und ob  damit ein Split möglich ist
--

(78)
Ziehen der ersten Karte für den Dealer
--

(80-89)
Fisher-Yates-Shuffle
--

(94)
doubledown button verstecken, da split und doubleDown nicht gleichzeitig erlaubt sind
--

(96)
eine Karte vom Spieler (optisch)entfernen
--

(97)
hier diese Karte auch aus dem logischen Teil vom Spieler entfernen und dem Split-Stapel hinzufügen
--

(105)
noch eine 2te Karte für den Standard-Spieler ziehen
--

(106)
eine 2te Karte für den Split-Spieler ziehen
--

(116)
verstecken des Split-Buttons, da man keinen Split mehr ausführen darf, sobald man weitere arten gezogen hat
--

(118)
eine Karte aus dem Kartenstapel "ziehen" und dem Spielerstapel hinzufügen
--

(120)
Spielerstapel-Karten nach Werthöhe sortieren, damit zum Schluss die Asse richtig berechnet werden können
--

(125-136)
hier die Überprüfung, ob ein Ass 1 oder 11 Punkte bekommt
--

(140)
updaten der Spielerpunkte, die während des Spiels angezeigt werden
--

(141)
updaten der Spielerpunkte, die zum Abschluss des Spiels angezeigt werden
--

(143-169)
funktioniert wie die Draw-Funktion, nur für den Split-Spieler
--

(171-203)
Draw-Funktion für den Dealer. Wird, bis auf die erste Karte zum Start, erst nachdem der Spieler fertig ist ausgeführt
--

(195-198)
wenn der Funktion die 0 mit übergeben wird, soll nur eine Karte gezogen werden und im Anschluss die Funktion beendet werden, ansonsten...
--

(199-202)
...ruft sich die Funktion erneut selber auf bis der Dealer mindestens 16 Punkte hat.
--

(204-236)
Funktion zum Überprüfen ob Dealer, Player oder beide über 21 Punkte kommen.
--

(238-261)
wie CheckWin-Funktion, nur dass sie Split und Dealer vergleicht, statt Player und Dealer
--

(263-347)
Da jetzt alle Spielparteien ihre finalen Karten gezogen haben, werden die Punktecounts noch einmal auf null gesetzt und ein letztes mal die genauen Punkte ausgerechnet
--

(265)
Player hat seine Spielzüge beendet, jetzt zieht der Dealer seine (restlichen) Karten
--

(304-306)
Updaten von Punktzahlen auf dem Spielfeld und im anschließenden Modal
--

(308-327)
wenn ein Split durchgeführt wurde, werden hier die Splitpunkte mit den Dealerpunkten verglichen
--

(328-347)
vergleichen der Spielerpunkte mit den Dealerpunkten
--