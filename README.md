# Pokémon Turn-Based Battle Simulator

## Overview

This project is a simple, text-based Pokémon battle simulator, where two players can choose Pokémon from a dataset and battle them in turn-based combat. The battle is determined by various stats such as Speed, Attack, Defense, and HP.

## Dataset

The Pokémon data used in this simulator comes from the following source:

- [Kaggle Pokémon Dataset](https://www.kaggle.com/datasets/abcsds/pokemon) by Alberto Barradas

This dataset contains the stats and details of all 800+ Pokémon from the first 6 generations, including their types, stats, and whether they are Legendary Pokémon.

## Features

- **Pokémon Selection**: Each player selects a Pokémon by typing its name.
- **Turn-Based Combat**: Battles are conducted in turns based on each Pokémon's Speed stat. The Pokémon with the higher Speed attacks first. Damage is calculated based on attack stats.
- **Stat-Driven Battle**: The battle uses stats such as HP, Attack, Defense, and Speed to determine the outcome.

## How to Use

### 1. Prerequisites

Ensure you have the following Python packages installed:

```bash
pip install pandas
```

### 2. Running the Simulator

To run the battle simulator, simply execute the `turn-battle.py` script:

```bash
python turn-battle.py
```

### 3. Gameplay Instructions

- When prompted, each player selects their Pokémon by typing its name (case-sensitive).
- The battle begins with the Pokémon with the higher Speed attacking first.
- The simulator alternates turns until one Pokémon's HP reaches zero.

### 4. Example Output

Here is an example of what the output might look like during gameplay:

```plaintext
Player 1, select your Pokémon by typing its name:
Bulbasaur
Player 2, select your Pokémon by typing its name:
Charmander
Battle Start! Bulbasaur vs Charmander
Charmander attacks first!
Bulbasaur takes 15 damage!
Bulbasaur attacks back!
Charmander takes 20 damage!
...
Charmander wins!
```

## Code Structure

### Main Functions:

- **`select_pokemon(player)`**: Prompts the player to choose a Pokémon by name. Validates the selection and returns the Pokémon's stats.
- **`battle(pokemon1, pokemon2)`**: Simulates the battle between two Pokémon. Determines turn order based on Speed and alternates attacks until one Pokémon's HP reaches zero.

### Pokémon Stats Utilized:

- **HP**: The health of the Pokémon. Reduced by the opponent's attack each turn.
- **Attack**: Physical attack power, used to determine damage dealt.
- **Defense**: Physical defense, reduces incoming damage.
- **Speed**: Determines the order of turns in battle.

## Customization

You can modify the battle logic by tweaking the damage calculation or introducing new rules, such as including type advantages or special abilities.

## Dataset Details

The following columns from the dataset are used in the simulator:

- **Name**: The name of the Pokémon.
- **Type 1** and **Type 2**: Pokémon's primary and secondary types.
- **HP**: Hit Points, or health, of the Pokémon.
- **Attack**: Physical attack power.
- **Defense**: Physical defense.
- **Speed**: Determines attack order in battles.

## License

This project uses the Pokémon dataset from Kaggle. Ensure that you follow Kaggle's terms of use when distributing or modifying this data.