# Order Matching Simulation

[![C++](https://img.shields.io/badge/C++-17-blue)](https://isocpp.org/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE)

**Simple** order book simulator where buy and sell orders are matched according to price priority.

---

## Features

- Interactive console-based input for **buy** and **sell** orders  
- Partial order fulfillment supported (orders can be partially matched)  
- Maintains sorted order vectors for price priority  
- Prints unmatched orders after all processing  
- Lightweight — no external dependencies  

---

## How It Works

- Prompt the user to add orders: buy or sell, price, and quantity  
- For each new order:
  - Check if it can match existing orders on the opposite side  
  - Fulfill orders partially or fully depending on available quantity  
  - Remove fully matched orders from the order book  
- Remaining unmatched orders are stored in sorted vectors:  
  - Buy orders sorted descending (highest price first)  
  - Sell orders sorted ascending (lowest price first)  
- Display the final order book to the user  

---


## Build & Run

### Using CMake

matching_engine folder:


    cd build       # go to existing build folder
    cmake ..       # generate build system (if not already done)
    cmake --build . # compile the project

### Run 
    ./main

## Follow interactive prompts:
- Do you want to add an order? (yes/no)
- Buy or sell?
- Enter price
- Enter quantity

## Example Interaction
    Do you want to add an order? : yes
    Do you want to buy or sell? : buy
    Enter the price: 100
    Enter the quantity: 5
    
    Do you want to add an order? : yes
    Do you want to buy or sell? : sell
    Enter the price: 95
    Enter the quantity: 3
    
    # Order book after matching:
    Buy Orders:
    ID: 1, Price: 100, Qty: 2
    
    Sell Orders:
    <empty>
