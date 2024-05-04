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
