### What is Maze Runner?
I decided to expand my solution to Check Point Security Academy 2020 - Amaze_me Challenge.  
The challenge required me to navigate a 250X250 unknown maze and figure out where the treasure is hidden.   
Once close enough, I received distance from treasure in order to calculate it's coordinates.

### ![Maze](https://github.com/iRusek/Maze_Runner/blob/master/media/Full_Maze.PNG?raw=true)
![#000000](https://placehold.it/15/000000/000000?text=+) Undiscovered, ![#ff0000](https://placehold.it/15/ff0000/000000?text=+) Blocked, ![#ffff00](https://placehold.it/15/ffff00/000000?text=+) Dead-End, ![#00ff00](https://placehold.it/15/00ff00/000000?text=+) Path Un-Exhausted

### What's so special about this project?
Knowing where the treasure is hidden wasn't enough for me, I had to reach it!  
I used Openpyxl in order to create a maze visualized by colors, to better understand the automated Maze Runner while it was communicating with Check Point's server.

### How is the challenge solved?
Each cell in the maze is a location dictionary.  
Maze Runner will start running to paths yet undiscovered, using the Wall Follower algorythm.  
Once getting close enough (45 cells) he will receive distance hints, and after 3 of those he can calculate the treasure location.  
From now on Maze Runner will run toward the treasure, still using the Wall Follower algorythm, "changing hands" in order to reach the target and avoid different obstacles.
