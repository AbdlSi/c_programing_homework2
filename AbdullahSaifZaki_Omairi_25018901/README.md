# maze_game_hw

I have completed all parts of the homework as requested in the assignment. Here is what the program does:

* **Map Loading**: It dynamically reads a map layout from an external text file to create the game board
* **Movement Controls**: You navigate through the maze using the 'w', 'a', 's', and 'd' keys
* **Collecting Items**: You collect Silver (S), Gold (g), and Dollars ($) to increase your score
* **Dynamic Walls**: When an item is collected, the program places a wall (#) in your previous position on the next move
* **Path Validation**: The game uses a search algorithm to check if remaining items are still reachable before letting you continue
* **Score Tracking**: It calculates your final score by subtracting the total moves (time) from the points you collected
* **Exit Option**: You can quit the game at any time by pressing the 'e' key

## Notes:

I followed the rules for the assignment such as:

* **Dynamic Memory**: I used malloc and free to handle the 2D map array based on the file size
* **Structs**: I used a Player struct for coordinates and a ScoreBoard struct to track game state
* **DFS Algorithm**: I implemented a Depth First Search with a manual stack to verify item reachability
* **File Output**: The program appends your final results to a "scores.txt" file for record-keeping

## Functions that I used in the Code

* **allocateMap**: Reserves memory for the 2D grid based on the number of rows
* **loadMap**: Opens the text file and populates the grid with characters
* **handleMove**: Manages player positioning, item collection, and wall placement logic
* **hasReachableItem**: Uses a manual stack to perform a DFS to find paths to items
* **saveScoreToFile**: Records the final stats and score into an external file
