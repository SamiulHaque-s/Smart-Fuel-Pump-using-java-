# Smart Fuel Pump Management System

A simple desktop app built with **Java** and **Java Swing**. It lets a user search for fuel pumps, check queue status and book fuel, and lets an admin manage pumps, prices, bookings and feedback.

This is a university project made to practice **Object-Oriented Programming (OOP)** in Java.

---

## Features

**User side**
- Select a zone (Mirpur, Gulshan, Nabisco)
- Search a pump by name
- View open pumps / all pumps
- Check queue status
- Book fuel (with queue number and estimated time)
- View and cancel bookings
- Find the nearest open pump
- View last 5 sales
- Rate a pump's service

**Admin side**
- Register a new pump
- Remove a pump
- View all pumps
- View the fuel price list
- View rating summary
- View all bookings
- View all feedback

---

## Built With

- **Java** – main programming language
- **Java Swing** – for the GUI (JFrame, JPanel, JButton, JTable, JComboBox, CardLayout, etc.)
- **ArrayList** – to store pumps, bookings and feedback in memory

---

## OOP Concepts Used

| Concept | Where it is used |
|---|---|
| Encapsulation | `Pump` class keeps its fields `private` and gives access through getters |
| Inheritance | `Pump extends FuelStation`, and `main extends JFrame` |
| Polymorphism | `Pump` overrides `showInfo()` from `FuelStation` using `@Override` |
| Abstraction | `FuelStation` is an abstract class with an abstract method `showInfo()` |

---

## Project Structure

```
SmartFuelPumpManagementSystem/
│
├── main.java        # Contains all classes: FuelStation, Pump, Vehicle, Feedback, main
└── README.md
```

All classes are currently kept in one file, `main.java`, for simplicity.

---

## Requirements

- Java JDK installed (JDK 8 or newer)
- Any code editor (VS Code, IntelliJ, Eclipse) — or just a terminal

Check if Java is installed:

```bash
java -version
javac -version
```

---

## How to Run

1. Clone this repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2. Compile the code

```bash
javac main.java
```

3. Run the program

```bash
java main
```

The app window will open directly — no extra setup needed.

---

## How to Use

1. Run the app. The **Home screen** opens with 4 options: User Panel, Admin Panel, About Project, Exit.
2. Click **User Panel** to search pumps, book fuel, check queue status, or give feedback.
3. Click **Admin Panel** to register/remove pumps, view bookings, or check the price list.
4. All data (pumps, bookings, feedback) is stored in memory only. It resets every time you close and reopen the app.

---

## Troubleshooting

**"java: command not found" or "javac: command not found"**
→ Java JDK is not installed or not added to your system PATH. Install JDK and restart your terminal.

**"Error: Could not find or load main class main"**
→ Make sure you are in the same folder as `main.java`, and that you compiled it first with `javac main.java` before running `java main`.

**Compilation error about `main` not being a valid class name**
→ Java discourages lowercase class names, but it still works. If your editor blocks it, rename the file and class together (keep both names matching).

**Window opens but closes immediately / nothing happens**
→ Check the terminal for an error message. Most issues come from compiling an older version of the file — recompile with `javac main.java` after any change.

**Booking fails or shows "Please fill up all information!"**
→ Make sure the Vehicle Number and Pump Name fields are not empty, and the pump name matches an existing pump exactly (not case-sensitive).

**"Pump not found!" even though the pump exists**
→ Check for extra spaces or typos in the pump name you typed.

---

## Future Improvements

- Save data permanently using a database or file storage instead of memory
- Fix the estimated-time display when the queue has many vehicles
- Add input validation for admin pump registration
- Split classes into separate files for better structure

---

## Author

[Your Name] — [Department], [University Name]
Course: Object Oriented Programming / Java

---

## License

This project is for academic/educational purposes.
