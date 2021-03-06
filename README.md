Bi-directional search applied to  Pacman and Rubik’s cube problem.


Pacman Bidirectional Search
==========
python pacman.py -l [Maze] -p SearchAgent -a fn=[search_algorithm]

Maze can be one of the following:

1. tinyMaze
2. smallMaze
3. mediumMaze
4. bigMaze

fn can be one of the following:

1. bfs = breadthFirstSearch
2. dfs = depthFirstSearch
3. astar = aStarSearch
4. ucs = uniformCostSearch
5. **bi = bidirection**

Example Usage:
python pacman.py -l tinyMaze -p SearchAgent -a fn=bi



************************************************************************************
Bidirectional Iterative Deepening A* Rubik's Cube Solver
==========

[Rushikesh Sargar](https://github.com/RishiSargar)
[Raj Sadaye](https://github.com/RjSadaye)
[Arsh Padda](https://github.com/ArshPadda)
[Shubham Gondane](https://github.com/ShubhamGondane)
ASU CSE571 - Artificial Intelligence "Fall 2018" "Bidirectional Search to Solve Rubik's Cube"


Problem
-----------
Given any Rubik's Cube state, return a list of moves to solve the Rubik's Cube using [Korf's Algorithm](http://en.wikipedia.org/wiki/Optimal_solutions_for_Rubik%27s_Cube#Korf.27s_Algorithm).

Solution
-----------
- Representing a 3D cube in a 2D state
- Generating 3 distinct pattern databases: corner cubies, edge cubies set 1, edge cubies set 2
- Performing Bidirectional Iterative Deepening A* (BD_IDA*) search on the possible moves using the 3 aforementioned pattern databases as the heuristic look up tables
- Return an optimal solution in the form of the face to turn and how many clockwise turns to do

Relaxed Constraints
---------------------------
- Only handle clockwise turns of a face

Running the Solver
------------------
Compile the Java source files in src directory:
- `cd src`
- `javac *.java`

If you would like to generate the heuristic tables, you can run the generateHeuristics.sh file in src directory after giving it sufficient privileges:
- `chmod 777 generateHeuristics.sh`
-	`./generateHeuristics.sh`

To run the program to solve a cube from a file:
- `java -Xmx2048M Cube "Full file path to input file"
