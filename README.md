# Pokémon Game Simulation
This project is a basic implementation of a Pokémon game using Java. It includes the core functionalities and classes to simulate Pokémon battles, catching wild Pokémon, and managing trainers and their Pokémon teams. The code follows Object-Oriented Programming principles for better organization and reusability.

# Core Classes

## Pokemon: 
Represents a Pokémon with various attributes and methods for battling and leveling up.

Attributes: Name, type, health, attack, defence, special attack, special defence, speed, level, experience, moves (list of Move objects), is wild.
Methods:
attack(Pokemon opponent, Move move): Calculates and inflicts damage on the opponent based on types and stats.
takeDamage(int damage): Reduces health and handles potential faints.
gainExperience(int exp): Increases experience and checks for level up.
levelUp(): Increases stats and potentially learns new moves.
learnMove(Move move): Adds a new move to the Pokémon’s repertoire.
getStat(String stat): Accesses a specific stat value.

## Move:
Represents a move that a Pokémon can use in battle.

Attributes: Name, type, power, accuracy, category (physical, special), effect (optional).
Methods:
applyEffect(Pokemon target): Executes the move's effect (if any).

## Trainer
Represents a Pokémon trainer who can catch Pokémon, use items, and engage in battles.

Attributes: Name, team (list of Pokémon objects), inventory (list of Item objects).
Methods:
catchPokemon(Pokemon wildPokemon, Pokeball pokeball): Attempts to catch a wild Pokémon with a Pokeball.
useItem(Item item, Pokemon target): Applies the item’s effect to a chosen Pokémon.
battle(Trainer opponent): Engages in a turn-based battle with another trainer.
## Item

Represents an item that can be used by a trainer.

Attributes: Name, type, effect.
Methods:
use(Pokemon target): Applies the item’s effect to a chosen Pokémon.
#Pokeball
Represents a Pokeball used for catching Pokémon.

Attributes: Name, type, effect, catchRate.
Methods:
attemptCatch(Pokemon wildPokemon): Attempts to catch a wild Pokémon with a specified catch rate.
Inheritance
Pokémon Subclasses
Create subclasses for different Pokémon types with unique stats and moves, e.g., FirePokemon, WaterPokemon.

## Move Subclasses
Consider subclasses for different categories (Physical Move, Special Move) or effects (Status Move).

## Gameplay Mechanics
Battle System
Implement turn-based combat with move selection and damage calculation.
Utilize random number generation for accuracy checks.
Track and apply status effects (poison, paralysis, etc.).

## Pokémon Catching
Use a Pokeball class with different catch rates based on factors like Pokémon health and level.
Introduce Pokeball types with varying effectiveness.

# Additional Features
Evolution system: Implement evolution mechanisms for certain Pokémon based on level or specific items.
