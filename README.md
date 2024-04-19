# search
Question 1: 
This first question is slove using Depth First Search (DFS), in this problem, we used stack. 
In the code, it first initialize the stack with start sate and it has a empty set to store the states thats being visited. It then have a while loop to check and run the code while stack is not empty. In the while loop, we will pop the state, which is the node and move from the stack and if the goal state is met, we would return the moves, which is the answer to this problem. Else it would continue visiting the path from the current node. In the for loop, we use _ to ignore the thrid element "stepCost" which we don't care about in this case. The for loop to expore all the successor and check if there is any node that hasn't been visit yet, if so, it would add it to the stack for the next visit. 

Question 2:
In this question, a queue is being used to slove for BFS
Similar to DFS, excpted that we store the start state to the visited before moving into the while loop. This is important because if we don't do this, the code will not work due to the start state could be add into the queue mutiple times. One more different is instead of adding the visited node before loop to successor, we do it in the if statement inside of the loop. 

Question 3:
In this question, a priority queue is being used to solve for uniform cost search
Similar to DFS and BFS but instead of stack and queue we initialize the priority queue to store the node we are going to visist. The priority queue will have two argument: a pair (node,move) and the cost of moving. 

Question 4:
