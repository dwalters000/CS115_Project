CSci 115 Fall 2026: Shortest-Path
(Group project, 2 students maximum)

Submission deadline: Week 15 (12/01/2026)
Project presentation: during the lab on 12/01/2026 or 12/03/2026, depending on the lab section
Programming language: C++
Group project: Yes (maximum 2 students)

Learning outcomes:
- Software development with C++
- Object-oriented programming with C++
- Data structures: arrays, lists, matrix, graph, shortest-path algorithms
- Group project

PROJECT DEFINITION

- The project is a 2D application where the user selects a character in the environment and a target location.
- The view is from the top, where a map is displayed. The map is represented by a matrix where each cell contains an image corresponding to a type of terrain.
- The character moves cell by cell toward the target location using the shortest path.
- There are multiple types of characters on the map:
  1. The monkey, which can only walk. It cannot go in the water or cross high mountains.
  2. The bird, which can fly over mountains but cannot go in the desert.
  3. The fish, which must stay in the water.
  4. The frog, which can go everywhere except the mountains and the desert.

- Rule 1: The monkey, bird, fish, and frog cannot be on the same cell on the map.

- The environment is represented as a matrix. It contains five types of cells:
  1) High mountain
  2) Plain
  3) Forest
  4) Desert
  5) Ocean
  You need 5 different tiles to represent these blocks on the map.

- Rule 2: With the terrain, the character can take more time to move from one vertex to another vertex in the graph.

- The terrain (the map) can be loaded from a text file, where characters represent the different elements to be displayed on the map.
- You will provide 3 different terrains.

CONTROLS

- Select the character in the console by providing its coordinate or its name.
- Select the coordinate of a target. The character then moves toward the target.
  - Press the space bar to make the character move toward the target.
  - You may change the color of each cell that should be visited, to highlight the path that will be taken.

EXAMPLE COST FOR THE EDGES

Row: From, Column: To

From / To      High Mountain   Plain   Forest   Desert   Ocean
High Mountain       2            1        1        1       10
Plain               5            1        3        2        2
Forest              6            2        3        2        5
Desert             10            2        3        2        3
Ocean              10            3        3        3        1

You can adjust the cost matrix so it works for each character.
Example: it costs 10 points to go from a high mountain to the ocean.

DISPLAY IN THE CONSOLE

- Monkey: M
- Bird: B
- Fish: F
- Frog: G

Terrain:
1. High mountain: ^ (caret)
2. Desert: . (period)
3. Forest: " (double quotes)
4. Plain: (space)
5. Water: ~ (tilde)

CODE CONSTRAINT

Your code must not contain any break or continue inside loops.

PROVISIONAL RUBRIC / MARKING SCHEME

1. The project is submitted with a readme file that explains what it contains, who did the project, and how to use the files.
2. The project compiles.
3. The project is commented (e.g., a header comment on each function).
4. The project runs, and it is possible to test the application.
5. Programming:
   1. The project works as it should.
   2. The project contains classes:
      - A class Map for the map
      - A class Character (for the monkey, bird, fish, and frog)
   3. Main functions:
      - Display a maze based on the values from a matrix
      - Load a terrain from a text file
      - Shortest-path functions to move a character to a target destination:
        - Implementation of a data structure for a graph
        - Implementation of a priority queue
        - Algorithm for the shortest path (Dijkstra)
      - User control to select a character and move it to a destination
6. A 1-page report explaining how to use the application.
7. Effort in creating the map to show how the characters move.
8. Possibility of selecting different maps.
9. Possibility of loading levels from a file.
10. Ability to explain the project during the presentation (not optional). All students must be present during the presentation.

---

README OUTLINE (DRAFT)

The rubric (items 1 and 6) asks for a readme that covers these three things:

1. What the project contains
   - List of source files and what each one does (Map, Character, graph, priority queue, Dijkstra, main, etc.)
   - Terrain/level files included (the 3 terrains, plus any level files)

2. Who did the project
   - Both group members' names

3. How to use the files
   - How to compile (exact command or steps)
   - How to run the program
   - Controls: selecting a character by coordinate or name, choosing a target, pressing space to move
   - How to choose a different map or load a level file
   - Note that the 1-page usage report has the detailed walkthrough
