# 🧃 Vending Machine Simulation – Bugs Busters (CS 441 Final Project)

A fully modular and object-oriented vending machine simulation in C++20, built for **CS 441: Software Engineering** at Long Island University. Developed by Team **Bugs Busters**, the project demonstrates real-world software engineering practices including layered architecture, event-driven programming, separation of concerns, and detailed technical documentation.

---

## 📌 Project Purpose

The goal of this project was to design, implement, and document a maintainable, scalable vending machine simulator. It simulates customer transactions, coin insertion and change, beverage dispensing, and maintenance operations—all following proper software development lifecycle (SDLC) practices.

The simulation serves both educational and demonstrative purposes to showcase team-based software engineering, Agile workflows, and C++ system design using SOLID principles.

---

## 🧠 Features

### ✅ Customer Functions
- Insert coins (`nickel`, `dime`, `quarter`) and track total balance
- Cancel a transaction and receive all inserted coins
- Select beverage from available slots
- Receive correct change (if available) or enter **Exact Change Mode** if not
- Collect beverage from a simulated dispenser bin

### 🛠️ Maintenance Functions
- Access maintenance menu via password
- Refill beverage slots
- Refill coin drawers for change
- Collect all inserted money
- Generate transaction reports in plain text format

### 💡 Architecture & Design
- **Object-Oriented Design (OOP)** with clearly defined domain classes
- **Event-driven system** using a custom `EventManager` for decoupled communication
- **MVC Pattern** split between business logic and IO components
- **C++ STL** (`vector`, `map`, `optional`) for performance and flexibility
- **Component Breakdown**:
  - `MoneyHandler`: Validates coins, manages change, collects funds
  - `DispenserContainer`: Manages beverage selection and dispensing
  - `EventManager`: Coordinates system state changes
  - `ReportManager`: Logs transactions and maintenance reports
  - `VendingMachine`: Main controller

---

## 🖥️ How to Run

### Requirements:
- C++20 compiler (Visual Studio 2022 recommended)
- Windows or Linux environment with a console/terminal

### Steps:
1. Clone the repository
2. Open the project in Visual Studio (`CS441_VendingMachine_BugsBusters.sln`)
3. Build and run the solution
4. Follow the on-screen prompts as either a **Customer** or **Maintenance User**

---

## 👥 Team Contributions

### **Danila Ishchanka** – *Dispenser System & Debugging*
- Developed the DispenserContainer, Slot, and DispenserBin
- Managed selection logic, state transitions, and CLI integration
- Conducted unit tests and coordinated component interactions

### **Myra Mulongoti** – *Money Component Lead*
- Drafted team schedule and testing plan
- Created header/implementation files for MoneyHandler and related classes
- Led white-box testing and peer review

### **Sahil Zakaria** – *Event System & Reports*
- Implemented EventManager for inter-component communication
- Developed the ReportManager for transaction logging
- Tested event logic and report accuracy

### **Nodira Kazakova** – *VendingMachine Controller*
- Built the VendingMachine class to manage app flow and integration
- Managed user input/output for both customer and maintenance paths
- Debugged cross-component issues

### **Morena DeVito** – *User Manual & Testing Support*
- Researched user documentation examples
- Wrote and formatted customer and maintenance user instructions
- Assisted in unit testing Money and Dispenser components

---

## ✅ MVP Highlights

- Core user journey: Insert coin → Select drink → Dispense drink → Get change
- Fully functional maintenance interface with refill and reporting tools
- Detailed acceptance criteria met for both customer and maintenance users
- Final report includes architecture overview, class documentation, and list of technical debt

---

## 🚧 Known Limitations (Technical Debt)

- Change is returned from smallest denomination up
- No bill acceptance; only coins supported
- Basic maintenance authentication (plaintext password)
- No automatic drink collection (requires typing `collect`)
- No dynamic pricing across beverages (all same price)

---

## 📄 License

This project is for educational use only and part of the CS 441 course at Long Island University – Post. Distribution beyond course context requires author permission.

---
