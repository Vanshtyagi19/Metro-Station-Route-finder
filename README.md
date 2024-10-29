
# Metro Station Route Finder

## Project Overview

This project simulates a metro system where users can find routes between metro stations, check the nearest metro station to a tourist place, and recharge their smart cards. The program implements a graph-based approach to represent the metro network, using Dijkstra's algorithm for finding the most economical path and BFS for finding the shortest path between two stations.

## Features
- **Find routes between stations**: Allows users to choose between the most economical path and the shortest path.
- **Check nearest metro station to a tourist place**: Given a tourist place, find the nearest metro station.
- **Recharge Smart Card**: Users can recharge their smart cards by entering their card ID and the recharge amount.

## Project Structure

```bash
├── metro.cpp                     # Main program file
├── paisa.txt                    # File containing smart card balances (card ID and balance)
├── tourplace.txt                # File mapping tourist places to nearest metro stations
├── blueline.txt                 # File with stations on the blue metro line
├── yellowline.txt               # File with stations on the yellow metro line
├── redline.txt                  # File with stations on the red metro line
├── greenline.txt                # File with stations on the green metro line
├── violetline.txt               # File with stations on the violet metro line
├── orangeline.txt               # File with stations on the orange metro line
├── bluext.txt                   # File with stations on blue line extensions
└── list.txt                     # List of all metro stations and their respective index
```


## Files Description:
- **paisa.txt**: Stores card IDs and their current balance.
- **tourplace.txt**: Contains tourist places and their nearest metro stations.
- **Metro Line Files (blueline.txt, yellowline.txt, etc.)**: Each file contains the stations of the respective metro lines in order.
- **list.txt**: Maps the station names to their internal indices used in the graph.

## How to Run

### 1. Compile the Code:
First, you need to compile the `main.cpp` file. You can use any C++ compiler like `g++`:

```bash
g++ -o metro main.cpp
```

### 2. Run the Program:
After compiling, you can run the program using the command below:

```bash
./metro
```

### 3. Inputs for Program:
Once the program starts, you can interact with it through a text-based menu. The options are:

- **Route Between Two Stations**: Input two metro stations and find either the most economical or shortest path.
- **Nearest Metro Station to Tourist Place**: Input a tourist place and get the nearest metro station.
- **Recharge Your Smart Card**: Input your card ID and the recharge amount to update the balance in `paisa.txt`.

### 4. Data Files:
Ensure that all the data files (`paisa.txt`, `tourplace.txt`, `blueline.txt`, etc.) are in the same directory as the compiled executable (`metro`). The program reads from these files to get information about metro stations, tourist places, and smart card balances.

## Example

### Finding a Route Between Two Stations:
```bash
Enter station 1:
Rajiv Chowk
Enter station 2:
Hauz Khas
1. For most economic path
2. For shortest path
2
Rajiv Chowk
Yellow line
INA
Green line
Hauz Khas
```

### Checking Nearest Metro Station to a Tourist Place:
```bash
Enter a place:
Qutub Minar
Nearest Metro Station: Qutub Minar (Yellow Line)
```

### Recharging a Smart Card:
```bash
Enter Card ID:
101
Enter Amount:
500
Recharge Details:
Card ID: 101
Initial Balance: 200
Recharge Amount: 500
Total Balance: 700
```

## Algorithms Used
- **Breadth-First Search (BFS)**: Used to find the shortest path between two stations.
- **Dijkstra’s Algorithm**: Used to find the most economical path (path with the least weight).

### How the Graph is Constructed:
- Each station is a node, and each connection between stations is an edge.
- Metro lines are represented as different edges with distinct colors, indicating line changes.
- Edges are weighted for the most economical path using distance or fare, while BFS is used for the shortest path.

## Future Improvements
- Implement a more dynamic fare system based on distance.
- Add real-time traffic data for route adjustments.
- Integrate a graphical user interface (GUI).


If you have any questions or need further details, feel free to contact me at: [vasutyagi2003@gmail.com]

