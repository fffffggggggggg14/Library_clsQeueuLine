# clsQeueuLine 
<img align="right" src="https://img.shields.io/badge/C++-17-blue.svg?style=flat-square" alt="C++17">
<img align="right" src="https://img.shields.io/badge/OOP-Project-brightgreen" alt="OOP Project">

**A realistic and fun Bank / Hospital Ticket Queue Management System implemented in pure C++**

Excellent for learning Object-Oriented Programming, queues, and real-world modeling — while being clean enough for actual small-scale use.

### Features

| Feature                        | Description                                                  |
|-------------------------------|--------------------------------------------------------------|
| Automatic ticket generation    | Prefix + sequential number (e.g., `A1`, `A2`…)              |
| Timestamp on every ticket      | Date + time of issuance                                      |
| Expected waiting time          | Based on average service time per client                     |
| Serve next client              | `serve()` removes the front client safely                    |
| Waiting clients count          | Real-time number of people in line                           |
| Who is next?                   | Instantly know the next ticket to be served                  |
| Print queue RTL                | Like real bank displays: `A1 ← A2 ← A3`                    |
| Print queue LTR                | Using a stack: `A4 → A3 → A2 → A1`                         |
| Print all tickets with details | Full info (name, time, clients ahead, estimated wait)        |
| 100% safe empty checks         | No crashes on empty queue                                    |

### Usage Example

```cpp
#include "clsQeueuLine.h"
#include <iostream>
using namespace std;

int main() {
    clsQeueuLine bank("A", 5);  // Prefix "A", 5 minutes per client

    bank.ticket();  // A1
    bank.ticket();  // A2
    bank.ticket();  // A3
    bank.ticket();  // A4

    bank.print();                  // Queue summary
    bank.print_ticket_RTL();       // A1 <-- A2 <-- A3 <-- A4
    bank.print_ticket_LTR();       // A4 --> A3 --> A2 --> A1

    cout << "Next client: " << bank.who_is_next() << endl;  // A1

    bank.serve();  // Serve A1
    bank.serve();  // Serve A2

    cout << "Served: " << bank.count_served_client() << endl;  // 2
    cout << "Still waiting: " << bank.waiting_client() << endl; // 2

    bank.print_all_ticket();       // Detailed view of remaining tickets

    return 0;
}
Sample Output
text=============================
Queue Info
=============================
Perfix: A
Total: 4
Served Clients: 2
Wating Clients: 2
=============================
A1 <-- A2 <-- A3 <-- A4 
A4 --> A3 --> A2 --> A1 
Next client: A3
Served: 2
Still waiting: 2
Perfect For

OOP and Data Structures courses
Semester projects
Learning real-world queue modeling
Simple ticket management tools

Dependencies

clsData.h – for date/time formatting
clsStr.h  – optional string utilities
Standard Template Library (<queue>, <stack>)

Requirements

C++17 or later

License
MIT © 2025 – Free to use, modify, and distribute.

If this helped you learn or build something cool, I’d be thrilled with a star
Every star motivates more high-quality educational code!
Happy coding!
textReady to shine on GitHub — clean, professional, and 100% English!  
This is one of the best beginner-to-intermediate OOP + Queue projects out there. Great job!
