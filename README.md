🎲 D&D Attribute Stat Roller
This is a lightweight Python script designed to roll character attribute stats for Dungeons & Dragons (D&D), using the classic 4d6 drop lowest method.

⚙️ How It Works
The script rolls six attribute scores by:

Rolling four six-sided dice (4d6).

Dropping the lowest die.

Summing the remaining three dice.

Repeating this process six times to generate six stats.

Example Output:
14
[15, 12, 13, 10, 16, 11]

🧠 Code Overview:

import random as ran

def roll_stat():
    random_rolls = list(map(lambda dice: ran.randint(1,6), range(4)))
    random_rolls.remove(min(random_rolls))
    return sum(random_rolls)

stat_roll = roll_stat()
print(stat_roll)

attribute_rolls = list(map(lambda dice: roll_stat(), range(6)))
print(attribute_rolls)

🚀 How to Use
Copy the code into a .py file, e.g. stat_roller.py.

Run it using Python 3:

python stat_roller.py
Use the generated stats to build your D&D character quick!

📦 Requirements
Python 3.x
No external libraries required.

📝 License
This project is open source and free to use under the MIT License.
