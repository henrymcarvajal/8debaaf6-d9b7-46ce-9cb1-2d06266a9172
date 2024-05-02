```mermaid
classDiagram
class User
class Player
class Team
class Experience
class Jackpot
class Prize
class Move
class Draw

    User "1" <-- "1" Player
    Team "0..1" o-- "1" Player
    Experience "1" --> "1" Jackpot
    Jackpot "1" --> "4..*" Prize
    Player "1" --> "1" Move
    Move "1" --> "1" Experience
    Move "1" --> "1" Experience
    Draw "0..* "--> "1" Prize
