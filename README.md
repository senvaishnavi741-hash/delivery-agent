# Autonomous Delivery Agent 

An AI-based autonomous delivery agent capable of exploring a 2D grid city by employing different pathfinding techniques such as Breadth-First Search (BFS), Uniform-Cost Search (UCS), and A* methods. This project showcases within its scope the dynamic replanning abilities for the case of the agent being unexpectedly obstructed during delivery.

## Project Structure


autonomous_delivery_agent/
│
├── main.py                 # The main entry point is a CLI to run simulations
├── environment.py          # Establishes the class for GridCity environment
├── agent.py                # Creates the DeliveryAgent with its planning algorithms
├── utils.py                # Contains the supporting functions, data structures (e.g., PriorityQueue)
│
├── maps/
│   ├── small_map.txt
│   ├── medium_map.txt
│   ├── large_map.txt
│   └── dynamic_map.txt
│
└── README.md               # The document you are reading


## Map File Format

The layout of the maps consists of text files that depict the grid using the symbols listed below:

- S: Starting point
- G: Destination
- #: Stationary obstacle that cannot be crossed
- . or 1: Ordinary ground (cost of moving is 1)
- 2, 3, ..., 9: Hard ground with the respective integer as the cost of movement

## Installation

Installation of Python version 3.6 or above is the only prerequisite.

## Usage

The main program can be executed with the following command line parameters:

bash
python main.py --map  --algo 


### Arguments

- --map: File with the grid map (mandatory)
- --algo: Which algorithm to apply (mandatory)
  - bfs: Breadth-First Search
  - ucs: Uniform-Cost Search
  - a_star: A* Search
  - dynamic_demo: Dynamic replanning demonstration

### Examples

```bash
# Run BFS on the small map
python main.py --map maps/small_map.txt --algo bfs

# Run UCS on the medium map
python main.py --map maps/medium_map.txt --algo ucs

# Run A* on the l
made by vaishnavi sen
