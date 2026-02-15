# Grimhand Tactics

1. [Player Quick Reference](#️-player-quick-reference-️)
2. [Game Rules](#️-game-rules-️)

## *Triskai-deka-phobia HD remake*.

This game is a remake of my [js13k2024 Triskai-deka-phobia](https://github.com/romualdk/js13k-2024) entry.

![mockup](./Design/mockup-mobile.png)


## ⚔️ Player Quick Reference 🛡️

**Objective:** Be the last player with HP (Start: 50 HP).


### 🔄 On Your Turn (Choose 1)

1. **Draw:** Take 1 card from the **Attack** or **Defense** deck.
* *Max Hand:* 13 cards per hand. If you exceed 13, that hand is **flushed**.

2. **Attack:** Use all your Attack cards against the opponent's Defense cards.


### 💥 Damage Calculation

Damage is the **Sum of Values**, not the number of cards:

$$\text{Total Attack Value} - \text{Total Defense Value} = \text{HP Lost}$$

* *Note: If Defense is higher than Attack, damage is 0.*
* *After an attack, all used Attack and Defense cards are discarded.*


### 🃏 Special Cards

* **☘️ Lucky Card (7):** Stored in your Lucky Slot. It is your only protection against the Death Card.
* **☠️ Death Card (13):**
* **With Shamrock:** Both cards are discarded. You survive.
* **Without Shamrock:** **INSTANT DEATH.** Game over.


#### 🏆 Winning

* Reduce opponent to **0 HP**.
* Opponent draws a **Death Card** without a **Shamrock**.



## ⚔️ Game Rules 🛡️


### 🎯 Goal of the Game

**Be the last player standing!**
Each player starts with **50 Health Points (HP)**. Use attack and defense cards strategically to reduce your opponent's HP to zero—or survive long enough for them to draw a fatal card.


### 🃏 The Decks

There are two separate decks of cards. Do not mix them.

* **Attack Deck (Red – Swords):** Used to deal damage.
* **Defense Deck (Blue – Shields):** Used to block incoming attacks.

**Card Composition:**
Each deck contains cards numbered **1–13**.

* **1–12:** Standard Value Cards.
* **13 (Purple Skull):** The **Death Card**.
* **7 (Green Shamrock):** The **Lucky Card**.


### 💚 The Game Board Layout

Play takes place on a green casino-style board with specific zones:

1. **Draw Decks:** Center of the board (Attack and Defense decks, face down).
2. **Hand Cards:** Player's hand at the bottom; Opponent's hand at the top.
3. **Lucky Card Slot:** A specific slot to the right of each player’s hand to store drawn Shamrock cards.
4. **Discard Piles:** Next to each deck for flushed or spent cards.


### 🔄 Turn Sequence

Players take turns. On your turn, you must choose **ONE** of the following actions:


#### Action A: Draw a Card

Draw one card from either the Attack Deck or Defense Deck.

**1. Standard Draw Rules:**

* The card goes into your hand.
* **Hand Limit:** You may hold a maximum of **13 cards** per type (attack or defense).
* **Overfill Penalty:** If a hand exceeds 13 cards, the **entire hand** is flushed (discarded) immediately.

**2. ⚠️ The Death Card Mechanic:**
If you draw the **Death Card (13)**, the following occurs immediately:

* **If you have a Lucky Card (Shamrock) in your slot:**
* You survive.
* The **Death Card** and the **Shamrock** are both placed in their respective discard piles.
* The turn ends.


* **If you DO NOT have a Lucky Card:**
* **Instant Death.** You lose the game immediately.


#### Action B: Attack Opponent

You may choose to attack if you have at least one attack card.

**1. Damage Calculation:**
Damage is calculated using the **sum of the card values**, not the quantity of cards.

$$Damage = \sum(\text{Your Attack Card Values}) - \sum(\text{Opponent's Defense Card Values})$$

* *Example:*
* Attacker plays cards **3** and **7**  Total Attack: **10**
* Defender has card **4**  Total Defense: **4**
* **Result:**  Damage.


**2. Resolution:**

* **Apply Damage:** The Opponent loses HP equal to the final damage value.
* **Negative Damage:** If Defense > Attack, damage dealt is **0** (no healing occurs).
* **Flush Cards:** After the attack is resolved, **ALL** attack cards used by the player and **ALL** defense cards held by the opponent are discarded.


### 🍀 Special Cards Legend

| Card Value | Name | Icon | Effect |
| --- | --- | --- | --- |
| **7** | **Lucky Card** | ☘️ | **Protection:** When drawn, place in the "Lucky Card Slot." It sits passively until needed to negate a Death Card. |
| **13** | **Death Card** | ☠️ | **Instant Kill:** If drawn without a Lucky Card in reserve, the player dies instantly and the game ends. |


### ♻️ Refreshing Decks

If a draw deck runs out of cards:

1. Shuffle the corresponding discard pile.
2. Place them face down to form the new draw deck.


## 🏆 Winning the Game

The game ends when one of the following conditions is met:

1. **HP Elimination:** A player's HP reaches **0**.
2. **Sudden Death:** A player draws a **Death Card** and has no **Lucky Card** to protect them.

The surviving player is the winner!
