# search
Question 1: 
This first question is slove using Depth First Search (DFS), in this problem, we used stack. 
In the code, it first initialize the stack with start sate and it has a empty set to store the states thats being visited. It then have a while loop to check and run the code while stack is not empty. In the while loop, we will pop the state, which is the node and move from the stack and if the goal state is met, we would return the moves, which is the answer to this problem. Else it would continue visiting the path from the current node. In the for loop, we use _ to ignore the thrid element "stepCost" which we don't care about in this case. The for loop to expore all the successor and check if there is any node that hasn't been visit yet, if so, it would add it to the stack for the next visit. 

Question 2:
In this question, a queue is being used to slove for BFS
Similar to DFS, excpted that we store the start state to the visited before moving into the while loop. This is important because if we don't do this, the code will not work due to the start state could be add into the queue mutiple times. One more different is instead of adding the visited node before loop to successor, we do it in the if statement inside of the loop. 

Question 3:
In this question, a priority queue is being used to solve for uniform cost search
Similar to DFS and BFS but instead of stack and queue we initialize the priority queue to store the node we are going to visist. The priority queue will have two argument: a pair (node,move) and the cost of moving. In this case, we do care about the step cost so we added into the for loop. If the node is not in visited set, it adds to it and loops throught the successor. For each successor, it calculate the new moves and the cost of the moves. It then push the successor and the new move into the priority queue with the equal cost. 

Question 4:
In this question, a priority queue is being used to solve for aStart Search
Similar uniform cost search, we have a priority queue to store the node we are going to visist. The priority queue will have two argument: a pair (node,move) and the cost of moving. If there is a node that has not yet been visited, it adds it to the set and the successor will add to the priority queue. THe diffrence is in this case, we will need to calculate the new cost of each moves which is the sum of the cost to reach to the current node and calclate the cost to reach the goal from the current node. 

Question 5:
In this question, we need to visit all 4 corners so we need to keep track of which corners have been visited and which one have not. 
In getStartState(self) function, we have return a boolean indicating there is no corners have been visited yet. 
In isGoalState(self, state), we would return any state where all four corners have been visited.
In getSuccessors(self, state), we have a if statement to check if the wall is being hit yet or not, if not, it calculate the next position and then checks each corner to see if the next position is a corner that has not been visited yet, if that's the case, it marks the corner as visited. We have a tuple containing the next posistion which updats the corners visiting status and the action will be taken to reach the next position to the successor list. This will not end until all the successors of the current state has been visited. When its done, the successor list will return which will contain all the valid next state from the current state. 

Question 6:
In this question, we want to find a path that would visit all four corner of the maze. To do this, we first need to define the state which is a combination of the current postion and a tuple indicate which corner have been visited. If all the corner have already been visited, it would return 0 indicate the goal has been completed. If not, it would use the function manhattanDistance() to calculate the minimum distance from the current position to each corner that has not yet been visited. If there is more than one corner that has not been visit yet, it will pop the conrner that is the cloest to the current position. The heurisitc will be update by adding the minimum manhattan distance from the corner, it will be repeat until there is only one unvisited corner left. The function return the calcluated heuristic which is the cost from the current state to the goal. 


Question 7:
For this question, we want to eat all the foods in the maze. To do that, we can use the mazeDistance function that already done for us. We first initialize the distance to 0 and store all the food in a foodGrid list. For each food in that's in the list, we will calculate the maze distance from our current position. We will return the maximum distance as heuristic estimate the cast to reach the goal state from the current state. 

Question 8:
The key function that's missing in the findPathToClosestDot(self, gameState) is a serach method use to find the closest dot. BFS will be a good choice here to find the closest dot since BFS always finds the shortest path.
In isGoalState(self, state) checks if the current state has food or not, which we would just have to return the current food state with the position. 