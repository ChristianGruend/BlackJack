(1)
import newDeck from "./deck.json" assert { type: "json" }; 
//einlesen der Karten aus json-file
--

(41-44)
function doubleDown() {
    draw();
    checkWinFertig(2); 
}
//double down führt die draw-Funktion einmal aus und überigbt eine 2 für doppelte Punktzahl an die Überprüfungsfunktion
--

(45-79)
function newGame() 
//setzt alle Punkte und Anzeigen zurück auf default
--

(65-73)
deck = [        
    ...newDeck,
    ...newDeck,
    ...newDeck,
    ...newDeck,
    ...newDeck,
    ...newDeck,
];
    //laden von 6 Kartendecks in den Kartenstapel
--

(74)
Shuffle(deck); 
//Mischen der Karten
--

(75)
draw(); 
draw();
//2x Draw Funktion für die beiden Anfangskarten, die der Spieler erhält
--

(77)
splitCheck(); 
//Überprüfung ob die beiden Angangskarten den gleichen Wert haben und ob  damit ein Split möglich ist
--

(78)
dealerCardsDraw(0); 
//Ziehen der ersten Karte für den Dealer
--

(80-89)
function Shuffle(cards)
//Fisher-Yates-Shuffle
--

(94)
document.getElementById("doubleDown").style.display = "none"; 
//doubledown button verstecken, da split und doubleDown nicht gleichzeitig erlaubt sind
--

(96)
playerContainer.removeChild(playerContainer.children[0]); 
//eine Karte vom Spieler (optisch)entfernen
--

(97)
let splitCard = playerDraw.splice(0, 1)[0]; 
//hier diese Karte auch aus dem logischen Teil vom Spieler entfernen und dem Split-Stapel hinzufügen
--

(105)
draw(); 
//noch eine 2te Karte für den Standard-Spieler ziehen
--

(106)
splitCardsDraw(); 
// eine 2te Karte für den Split-Spieler ziehen
--

(116)
splitBtn.style.display = "none"; 
//verstecken des Split-Buttons, da man keinen Split mehr ausführen darf, sobald man weitere arten gezogen hat
--

(118)
let werte = deck.splice(0, 1)[0]; //eine Karte aus dem Kartenstapel "ziehen" und dem Spielerstapel hinzufügen
--

(120)
playerDraw.sort((a, b) => a.punkte - b.punkte); 
//Spielerstapel-Karten nach Werthöhe sortieren, damit zum Schluss die Asse richtig berechnet werden können
--

(125-136)
for (let i = 0; i < playerDraw.length; i++) 
//hier die Überprüfung, ob ein Ass 1 oder 11 Punkte bekommt
--

(140)
playerPunkte.innerHTML = "<h3>Punkte Player: " + playerCount + "</h3>"; 
//updaten der Spielerpunkte, die während des Spiels angezeigt werden
--

(141)
playerPunkteModal.innerHTML = "<h3>Punkte Player: " + playerCount + "</h3>"; 
//updaten der Spielerpunkte, die zum Abschluss des Spiels angezeigt werden
--

(143-169)
function splitCardsDraw() 
//funktioniert wie die Draw-Funktion, nur für den Split-Spieler
--

(171-203)
function dealerCardsDraw(x) 
//Draw-Funktion für den Dealer. Wird, bis auf die erste Karte zum Start, erst nachdem der Spieler fertig ist ausgeführt
--

(195-198)
if (x === 0) {
    return;        
}
//wenn der Funktion die 0 mit übergeben wird, soll nur eine Karte gezogen werden und im Anschluss die Funktion beendet werden, ansonsten...
--

(199-202)
while (dealerCount < 17) {        
        dealerCardsDraw(1);
}
//...ruft sich die Funktion erneut selber auf bis der Dealer mindestens 16 Punkte hat.
--

(204-236)
function checkWin(x)
// Funktion zum Überprüfen ob Dealer, Player oder beide über 21 Punkte kommen.
--

(238-261)
function checkWinSplit(x)
//wie CheckWin-Funktion, nur dass sie Split und Dealer vergleicht, statt Player und Dealer
--

(263-347)
function checkWinFertig(x, splitToggle)
//Da jetzt alle Spielparteien ihre finalen Karten gezogen haben, werden die Punktecounts noch einmal auf null gesetzt und ein letztes mal die genauen Punkte ausgerechnet
--

(265)
dealerCardsDraw();
//Player hat seine Spielzüge beendet, jetzt zieht der Dealer seine (restlichen) Karten
--

(304-306)
playerPunkte.innerHTML = "<h3>Punkte Player: " + playerCount + "</h3>";
//Updaten von Punktzahlen auf dem Spielfeld und im anschließenden Modal
--

(308-327)
if (splitToggle == true)
//wenn ein Split durchgeführt wurde, werden hier die Splitpunkte mit den Dealerpunkten verglichen
--

(328-347)
if (playerCount < 21 && dealerCount < 21)
//vergleichen der Spielerpunkte mit den Dealerpunkten
--