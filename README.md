# Washing Machine Queue Control System 🧺📟

A real-time embedded system to manage washing machine access in shared environments like hostels. This project uses an 8051 microcontroller and an RTOS-based approach to maintain a queue of users, trigger washing machine operations, and send notifications to users when it’s their turn to use or collect laundry.

## 🚀 Project Overview

In hostel settings with limited washing machines and large student populations, scheduling laundry becomes chaotic. This project solves that problem by:
- Allowing users to register via a keypad
- Managing their access using a FIFO queue
- Sending turn-based notifications via serial communication (LED blinking)

> 📅 Duration: Oct 27, 2024 – Dec 5, 2024  
> 🎓 Developed as part of the **Embedded Systems (EE3301)** course at **NIT Rourkela**

---

## ✨ Features

- 👥 **Supports up to 5 users per cycle**
- 🕹️ **User input via 4x4 Matrix Keypad**
- 📟 **LCD Display for status prompts**
- 🧠 **Circular Queue using 8051 RAM**
- 🧲 **Hall Sensor detects wash completion**
- 🧼 **Contact Sensor (or push button) confirms laundry pickup/drop**
- 📨 **Serial notifications via decoder & LEDs**
- 🔁 **Interrupt-driven design using INT0/INT1**

---

## 🧰 Tech Stack

| Component          | Description                                |
|--------------------|--------------------------------------------|
| **Microcontroller**| AT89S52 (8051 MCU)                         |
| **Programming**    | 8051 Assembly                      |
| **Simulation**     | Proteus                                    |
| **Sensors**        | MH3144 Hall Sensor, Push Button            |
| **Display**        | 16x2 LCD (LM016L)                          |
| **Decoder**        | 74HC138 (3x8) for serial communication     |
| **Design Tools**   | SolidWorks (Chassis Design)                |

---

## 🔌 Hardware Components

- 8051 Microcontroller Development Board (AT89S52)
- 16x2 LCD Display
- 4x4 Matrix Keypad
- Hall Sensor (MH3144)
- Push Button (as Contact Sensor)
- 74HC138 Decoder
- NAND, AND, NOT Gate ICs (7400 series)
- LED indicators
- Power Supply Adapter (9V, 1A)
- 3D Printed Chassis

*Total Cost: ₹1990 (approx.)*

---

## 🔧 System Flow

1. User enters their room number (0–7) via keypad.
2. System stores the address in a queue (FIFO).
3. Once the queue is full (5 users), no further entries are accepted.
4. Washing machine triggers Hall Sensor → INT0 interrupt.
5. System notifies current user to **collect laundry** (5 LED blinks).
6. After contact sensor triggers (push button) → INT1 interrupt.
7. System notifies next user to **bring laundry** (1 LED blink).
8. Cycle repeats.

---

## 📘 How to Use

1. Power on the system.
2. LCD prompts: `ADDRESS` — enter your room number.
3. Press `#` (Enter) to confirm. Press `C` to clear input.
4. Wait for LED blink + LCD message indicating your turn.
5. After cycle, collect laundry as notified.
6. Repeat steps for next user.

---

## 🎯 Results

- **Accuracy**: ~99% over 200+ iterations
- **Failure Cases**: 3 early-stage errors (fixed via reset)
- **Conclusion**: Efficient and cost-effective hostel utility system

---

## 🚀 Future Improvements

- 🔒 Add password/passkey authentication per user
- ☁️ Cloud-based data backup for user queue (using NodeMCU/WiFi)
- 📱 GSM or Bluetooth-based mobile alerts
- ⚡ Real-time power monitoring using smart energy cable
- ⏲️ Timer accuracy checks for washing cycles

---

## 👨‍💻 Team Members

- Ayush Kumar Sahu  
- Haimavatinandan Pati  
- Aniruddha Sen

🎓 *Guided by: Prof. Supratim Gupta, Dept. of Electrical Engineering, NIT Rourkela*

---

## 📄 License

This project is for academic and non-commercial use. Feel free to fork and build upon it with proper credit.

---

## 📬 Contact

For queries or collaboration:
📧 [your-email@example.com]  
📍 NIT Rourkela, Odisha, India
