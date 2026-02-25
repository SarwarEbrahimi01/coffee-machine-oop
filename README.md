# Coffee Machine — OOP Version

This repository contains an object-oriented implementation of a simple coffee machine program written in Python. The program models the coffee machine as collaborating classes that handle the menu, resources, and payment processing.

Files

- `coffee_maker.py`: Core class responsible for tracking resources and preparing drinks.
- `menu.py`: Provides the drink menu and a `Menu` class to look up drink recipes and costs.
- `money_machine.py`: Handles coin input, payment validation, and transaction state.
- `main.py`: Entry point that wires the classes together and runs the interactive loop.

Design overview

- `CoffeeMaker`: Manages the machine's resources (water, milk, coffee), checks resource sufficiency for a requested drink, deducts used ingredients when a drink is made, and can report current resources.
- `Menu` / `MenuItem`: Encapsulates available drinks, their ingredients, and cost. Responsible for presenting choices and resolving a selection to a recipe.
- `MoneyMachine`: Accepts coin input, calculates totals, checks if the payment covers the cost, gives change, and updates profit.

Key features

- Clean separation of concerns using classes for resources, menu, and payments.
- Easy to extend: add drinks to the menu or change recipes without modifying business logic.
- Interactive CLI loop implemented in `main.py` that accepts commands such as `off`, `report`, and drink names.

Usage

1. Ensure you have Python 3.8+ installed.
2. Run the program from the repository root:

```powershell
python main.py
```

Commands

- `off`: turn the machine off (exit program).
- `report`: print current resource levels and profit.
- `<drink name>`: order a drink from the menu (e.g., `espresso`, `latte`, `cappuccino`).

Extending the project

- To add a new drink, add a `MenuItem` in `menu.py` with its ingredient requirements and cost.
- To modify how payments are processed, update `MoneyMachine` in `money_machine.py`.

Notes

- This implementation focuses on clarity and OOP principles suitable for learning and small demos.
- See the source files for class-level docstrings and method details.

License

This project is provided for educational purposes.
