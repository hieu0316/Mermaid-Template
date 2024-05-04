# Reversi Spiel Use Cases

## Use case: UC01 - Spiel starten

| **Actors**                       |        |
| -------------------------------- | ------ |
| Primary actors                   | Spieler   |
| Secondary actors                 | Gegenspieler        |
| **Preconditions**                | Keine |
| **Postconditions**               | Spiel ist initialisiert, Anfangssteine sind positioniert.  |

```mermaid
stateDiagram-v2
    [*] --> SpielBereit
    SpielBereit --> SteinePlatzieren
    SteinePlatzieren --> SpielBeginnt
    SpielBeginnt --> [*]

```
## Use case: UC02 - Spielzug machen

| **Actors**                       |        |
| -------------------------------- | ------ |
| Primary actors                   | Spieler   |
| Secondary actors                 | Gegenspieler        |
| **Preconditions**                | Spieler ist am Zug, gültige Züge sind möglich. |
| **Postconditions**               | Stein gesetzt, betroffene gegnerische Steine umgedreht.|

```mermaid
stateDiagram-v2
    [*] --> Warten
    Warten --> ZugMachen
    ZugMachen --> SteineUmdrehen
    SteineUmdrehen --> ZugEnde
    ZugEnde --> [*]

```
## Use case: UC03 - Spielzug überspringen

| **Actors**                       |        |
| -------------------------------- | ------ |
| Primary actors                   | Spieler   |
| Secondary actors                 | Gegenspieler        |
| **Preconditions**                | Keine gültigen Züge möglich für den Spieler. |
| **Postconditions**               | Zug übersprungen, Gegner ist am Zug.|

```mermaid
stateDiagram-v2
    [*] --> Pruefen
    Pruefen --> KeineZuege
    KeineZuege --> ZugUeberspringen
    ZugUeberspringen --> GegnerZug
    GegnerZug --> [*]

```
## Use case: UC04 - Spielende

| **Actors**                       |        |
| -------------------------------- | ------ |
| Primary actors                   | Spieler   |
| Secondary actors                 | Gegenspieler        |
| **Preconditions**                | Alle Felder belegt oder keine gültigen Züge mehr möglich. |
| **Postconditions**               | Spiel beendet, Gewinner ermittelt. |

```mermaid
stateDiagram-v2
    [*] --> SpielLaeuft
    SpielLaeuft --> PruefenEnde
    PruefenEnde --> SpielEndet
    SpielEndet --> ErmittleGewinner
    ErmittleGewinner --> [*]

```

