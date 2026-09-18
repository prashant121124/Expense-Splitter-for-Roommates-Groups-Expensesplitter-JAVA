# Expense-Splitter-for-Roommates-Groups-Expensesplitter-JAVA
Expense Splitter for Roommates/Groups – Problem: manually calculating who owes whom after group expenses is messy. Solution: Splitwise-style logic — minimizes number of transactions needed to settle debts 
# Expense Splitter (Java)

A command-line Java application that helps a group of people (e.g., roommates, trip groups)
track shared expenses and calculates the **minimum number of transactions** needed to settle
all debts, instead of everyone paying everyone back individually.

---

## Problem Statement

When a group shares expenses (rent, groceries, trips, etc.), manually figuring out who owes
whom becomes messy and often results in far more transactions than necessary. This project
solves that by:
1. Tracking who paid for what and how it was split.
2. Calculating each person's net balance.
3. Using a **greedy algorithm** to minimize the number of payments needed to settle everyone up.

---

## Features

- Add group members
- Record expenses with custom split among selected members
- View real-time balances (who owes / who should receive money)
- Generate an optimized settlement plan (minimum transactions)
- Basic input validation and exception handling (invalid names, invalid numbers, etc.)

---

## Prerequisites

You only need the **Java Development Kit (JDK)** installed. No external libraries,
frameworks, databases, or build tools are required.

- JDK 8 or above (JDK 17+ recommended)
- A terminal / command prompt

### Check if Java is already installed

Run the following commands in your terminal:

```
java -version
javac -version
```

If both commands return a version number, you're ready to proceed. If not, install the JDK:

- **Windows/Mac/Linux:** Download from [https://www.oracle.com/java/technologies/downloads/](https://www.oracle.com/java/technologies/downloads/)
  or install OpenJDK via your package manager, e.g.:
  ```
  # Ubuntu/Debian
  sudo apt update
  sudo apt install default-jdk

  # macOS (with Homebrew)
  brew install openjdk
  ```

After installation, ensure `java` and `javac` are available in your system `PATH`.

---

## Project Structure

```
expense-splitter/
│
├── ExpenseSplitter.java   # Main source file (all logic in one file)
└── README.md              # This file
```

---

## Setup Instructions

1. **Clone or download this repository**
   ```
   git clone <your-repository-url>
   cd expense-splitter
   ```
   (Or simply download `ExpenseSplitter.java` into a folder.)

2. **No dependency installation needed** — this project uses only core Java (`java.util.*`),
   so there is nothing else to install or configure.

---

## How to Compile and Run

1. Open a terminal in the project folder (where `ExpenseSplitter.java` is located).

2. **Compile the program:**
   ```
   javac ExpenseSplitter.java
   ```
   This generates a file called `ExpenseSplitter.class` in the same folder.

3. **Run the program:**
   ```
   java ExpenseSplitter
   ```

4. Follow the on-screen prompts:
   - Enter the number of people in the group and their names.
   - Choose from the menu:
     ```
     1. Add Expense
     2. Show Balances
     3. Settle Debts
     4. Exit
     ```

---

## Example Usage

```
=== Expense Splitter ===
Enter number of people in the group: 3
Enter name of person 1: Alice
Enter name of person 2: Bob
Enter name of person 3: Charlie

1. Add Expense
2. Show Balances
3. Settle Debts
4. Exit
Choose option: 1
Who paid? Alice
Enter amount paid: 300
Split among how many people? 3
Enter name of person 1 sharing this expense: Alice
Enter name of person 2 sharing this expense: Bob
Enter name of person 3 sharing this expense: Charlie
Expense added successfully!

Choose option: 3
--- Settlement Plan (Minimum Transactions) ---
Bob pays Rs. 100.00 to Alice
Charlie pays Rs. 100.00 to Alice
```

---

## Notes for Evaluators

- The project is **fully executable via the command line** — no GUI, no IDE required.
- No external dependencies, databases, or configuration files are needed.
- Tested with standard JDK `Scanner`-based console I/O only.

