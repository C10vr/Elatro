# Elatro
Balatro in Python
Difficulty: ⭐⭐

---

### The Start ♦️

The first page that all games have are the home/menu/starting page, the user will be able to press:

- [x]  Play
- [x]  Rules (Explain the rules[ex Full house : 40 *3]
- [x]  Quit

```python
-----------------
     Elatro 🃏
"Ready to Gamble?" #Quote rotation if possible
<Play> <Rules> <Quit>
>play
------------------
```

```python
def start_elatro():
    print("-----------------------------")
    print("""       ELatro 🃏""") #Triple quotation is used to move the spacing
    quote_list = ["\033[92mReady to Gamble?\033[0m",
                  "\033[92mI am different than Balatro\033[0m",
                  "\033[92mStarting to feel the rush?\033[0m",
                  "\033[92mHave a break...& gamble\033[0m"] #4 Quotes for rotation
    random_quote = random.choice(quote_list)
    print ('"' +random_quote+ '"')
    print ("""\033[94m<Play>\033[94m  \033[95m<Rules>\033[0m  \033[91m<Quit>\033[0m""")
    menu_choice = str(input(">"))
    menu_function(menu_choice)
    
def menu_function(menu_choice):
    #Menu functions
    if menu_choice == "play":
        play_elatro()
    elif menu_choice == "rules":
        rules_preview = int(1)
        while rules_preview == 1:
            print("""                           Rules 
                ----------------------------
                    'Ante are stages that you
                need to earn at least the 
                minimum to beat that stage!'

                        Ante 1 : 300🪙
                        Ante 2 : 400🪙
                        Ante 3 : 500🪙
                        Ante 4 : 600🪙
                        Ante 5 : 700🪙
                        Ante 6 : 800🪙
                        Ante 7 : 900🪙
                        Ante 8 :1000🪙
                ----------------------------
                          Combos
                ----------------------------
                    'Get a better hand with 
                different combos that will
                    help you with your run!' 
                    
                    Highcards       - 10 * 1
                    Pair            - 20 * 1
                    Two Pair        - 20 * 2
                    Three of a Kind - 30 * 1
                    Full house      - 30 * 3
                    Straight        - 50 * 3
                    Four of a Kind  - 40 * 4
                    Five of a Kind  - 50 * 5
                ----------------------------
                          Gameplay 
                'When the game start you get
                to choose what type of hand 
                combo you are going to play
                out of 7 cards(given randomly)'

                e.g [K][Q][7][7][7][5][5]

                'So you decided to play 77755,
                this is how the score system
                            works!' 
                
                        -=Base Chip=-
                7+7+7+5+5 (your hand count) +
                30 (hand combo[Full house])
                = 61 (Your total base chips)
                
                        -=Multiplier=-
                You scored a 'Fullhouse' so you
                are eligible for a *2 mult 
                = * 2 

                        -=Final Score=-
                Your total earned chips would
                be as calculated
                    
                61 * 3 = 183 Chips🪙!
                ---------------------------""")
            rules_option = (input("Do you want to exit rules? (Y/N)"))
            if rules_option == "Y":
                rules_preview = 0
                break
            elif rules_option == "N":
                print("No")
            else:
                print("Invalid Input!")
        start_elatro()
    elif menu_choice == "quit":
        exit
    else:
        print("Invalid function!")
    print("-----------------------------")

```

Explaination:

---

### The Beginning 🎲

Build a functioning card rotation for your hand each round, players must be able to see:

- [x]  7 cards in hand (eg. [K] [Q] [9] [5] [3] [3] [2])
- [x]  Score board (eg. Score:0)
- [ ]  Play (player will have to write “play 33”

```python
Paste your final relevent working here...
```

Explaination:

- [ ]  Played hands will give the result to the player showing how much chips they have earned

```python
> play KKKAA
<=Hand type: 'Fullhouse'=
=Combo: 40 * 3=
= Chips Earned: 276🪙=>
------------------
Score: 276🪙
```

```python
Paste your final relevent working here...
```

Explaination:

---

### The Egg 🥚

This part is going to be a tricky part so be ready and learn from this process.

Player will be able to 

- [ ]  Discard cards from the original 52 card deck (card deck contains: 4*A, 4*K , 4*Q, etc..), limit the player to discard only up to 5 cards!

```python
>disc 3245
<=discarded [3][2][4][5]=>
-----------------------
Score:0🪙
Ante 1: 300🪙
commands('play...','disc...','deck', 'combo'))

Your hand: [K][K][K][Q][Q][5][2]
Cards remaining: 47
>

```

After the player have selected the cards to be played, it must go through a process that checks for any 

- [ ]  Combo breakers (eg. Full house, Straight, 5 of a kind, etc…).

```python
>combo
<=High card: 10 * 1=
=Pair card: 20 * 1=
=Two Pairs: 20 * 2=
...
----------------------
Score:0
Ante 1: 300🪙
commands('play...','disc...','deck', 'combo'))

Your hand: [K][K][K][Q][Q][5][2]
Cards remaining: 47
>

```

Player can then  

- [ ]  See what hand did they played for that round (eg. “Prev hand: Full house 40*3”)

Make sure that all the points after each hand played are added to the score board.

```python
>play KKKQQ
<=Hand played: 'Fullhouse'=
=Combo 40 * 3=>
=Chips Earned: 270🪙
-----------------------
Score:0
Ante 1: 300🪙
commands('play...','disc...','deck', 'combo'))

Your hand: [A][A][K][5][3][3][2]
Cards remaining: 47
>

```

```python
Paste your final relevant working here...
```

Explaination:

---

### The Finishing 🏁

After working on this project for a long time, I bet you have learnt a things or two, practice more on how you can implement these codes in your real time projects.

Player will be able to see their 

- [ ]  Required goal of how many chips/points they need to get to win Elatro(eg. 300 Chips)

```python
Ante 1: 300🪙
```

```python

```

Explaination:

When the player have reach the minimum ante requirement,

- [ ]  Player will receive a ‘Congratulation! You Win Within x Rounds!’ and the player will be able to play again or quit

```python
---------------------
🎉 Congratulations!🃏
You Won Within 8 Rounds!
 <Play again?> <Quit>
>
```

```python

```

Explaination:

---

### The AdditionalⓂ️

After player have played ‘discard’, player will be able to 

- [ ]  See the remaining cards in the deck when written in command (eg. “Deck”)

```python
> Deck
-----------------
4[A] 4[K] 4[Q] 4[J]
4[10] 4[9]...
4[5] 4[4]...
```

```python
Your coding here...
```

Explaination:

You can decide if you want to 

- [ ]  Add several levels to the game such as (eg, Ante 1: 300chips), Make sure every round reset the amount of cards in deck(52)

```python
Ante 1: 300🪙
Ante 2: 500🪙
Ante 3: 700🪙
etc..
```

```python

```

Explaination:

- [ ]  Add a shop phase after each Ante have been defeated (can include small upgrades such as [eg, +2chips each round [2C]) Item can be randomly generated with different perks in each store

```python
---------------------
Store
commands('buy', 'exit') ex. 'buy 1'

1. 2C(20 chips) - "Adds +20 base chips"
2. 2M(two mult) - "Adds +2 mult"
3. BK(bonus K) - "If king is played gain +30 chips"

"Here are my wares, dont be hasty now!"
> #Player will write their actions here
```

```python

```

Explaination:

If possible try adding a feature where the

- [ ]  Player is able to view what perks they have bought

```python
>perks
<=Perks: [[2C], [2A]]=>
-----------------------
Score:0
Ante 1: 300🪙
commands('play...','disc...','deck', 'combo','perks'))

Your hand: [A][A][5][4][3][3][2]
Cards Remaining: 47
>
```

```python

```

Explaination:
