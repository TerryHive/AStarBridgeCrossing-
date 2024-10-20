
# AStarBridgeCrossing

An implementation of the A* algorithm to solve the classic bridge-crossing problem using Artificial Intelligence techniques. This project is structured in Java and demonstrates the application of heuristic-based search to find the optimal path for a group of individuals crossing a bridge under time constraints.

## Table of Contents
- [Description](#description)
- [Files](#files)
- [How It Works](#how-it-works)
- [Usage](#usage)
- [Installation](#installation)
- [Example](#example)
- [Additional Resources](#additional-resources)


## Description

The **AStarBridgeCrossing** project implements the A* algorithm to solve a problem where multiple individuals need to cross a bridge in the shortest time possible. Each person has a different crossing time, and only two individuals can cross at a time with the slower person determining the crossing time. Additionally, the individuals must use a flashlight, which must be brought back and forth.

The goal of the program is to find the optimal sequence of moves that minimizes the total time for all individuals to cross the bridge, taking into account the constraints.

## Files

- **`src/Main.java`**: The entry point of the program. It initializes the problem with given inputs and triggers the A* search.
- **`src/SpaceSearcher.java`**: Contains the implementation of the A* algorithm, including state exploration and pathfinding logic.
- **`src/State.java`**: Defines the state structure used in the search, including the positions of individuals and the time taken.
- **`docs/ΕΡΓΑΣΙΑ ΤΕΧΝΗΤΗΣ ΝΟΗΜΟΣΥΝΗΣ.docx`**: Documentation providing an in-depth explanation of the algorithm and the implementation details.

## How It Works

The program uses the A* algorithm to explore different states, where each state represents the configuration of individuals on either side of the bridge and the total time taken so far. 

### Heuristic Function
The heuristic function estimates the remaining time needed to complete the bridge crossing. It uses the maximum time from the individuals who have yet to cross, underestimating the time to ensure admissibility and optimality.

### Algorithm Characteristics
- **Complete**: The algorithm is guaranteed to find a solution if one exists because the branching factor is finite.
- **Optimal**: The heuristic function is admissible, meaning the algorithm will find the least-cost solution.

## Usage

### Prerequisites
Ensure you have Java installed. You can check with:
```bash
java -version
```

### Compile the Java Files
Navigate to the `src` directory and compile the files:
```bash
javac *.java
```

### Run the Program
To execute the program, run:
```bash
java Main [number_of_people] [crossing_times] [maximum_time]
```
- **`number_of_people`**: The number of individuals attempting to cross.
- **`crossing_times`**: A series of integers representing the crossing time for each individual.
- **`maximum_time`**: The maximum time allowed for all individuals to cross the bridge.

### Example
```bash
java Main 4 1 2 5 10 30
```
This command will attempt to find the optimal path for 4 individuals with crossing times of 1, 2, 5, and 10 minutes, within a maximum allowed time of 30 minutes.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/AStarBridgeCrossing.git
   cd AStarBridgeCrossing
   ```
2. Compile the code:
   ```bash
   javac src/*.java
   ```
3. Run the program as described in the [Usage](#usage) section.

## Example

### Input
```bash
java Main 5 1 3 6 8 12 30
```

### Output
The program outputs whether a solution was found and the sequence of steps to achieve the optimal time, including the time taken for each crossing.

## Additional Resources

For a visual explanation of the bridge-crossing problem, check out the video below:

[![Bridge Crossing Problem](https://img.youtube.com/vi/Ppx7-Y9_ub0/0.jpg)](https://www.youtube.com/watch?v=Ppx7-Y9_ub0&t=1s)

Click on the image above to watch the video.


