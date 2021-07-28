# Definition:

Minimax is a type of adversarial search algorithm for generating and exploring game trees.
It is mostly used to solve 2 Player zero-sum games (meaning where one side’s gain is equivalent to other side’s loss, so adding all gains and subtracting all losses end up being zero).
Game examples: Tic-Tac-Toe, Chess, Go, etc.\
\
A backtracking algorithm is being used to find the optimal move for a player, assuming that your opponent also plays optimally.
The Minimax algorithm keeps playing the turns of both player and the opponent  until it reaches a terminal state resulting in a draw, a win, or a loss.\
In Minimax the two players are called maximizer and minimizer. The maximizer tries to get the highest score possible while the minimizer tries to do the opposite and get the lowest score possible.\
\
The example below shows a game tree with 4 final states (leaf notes) and paths to reach final state:\
![alt_text](https://media.geeksforgeeks.org/wp-content/uploads/minmax1.png)\
Since this is a backtracking based algorithm, it tries all possible moves, then backtracks and makes a decision.
- On the minimizers turn: Left side it has the choice between 3 and 5, therefore it picks 3. Right side it has the choice between 2 and 9, therefore it picks 2.
- On the maximizers turn: It can chose between left = 3 or right = 2. Therefore it goes left.

# 
