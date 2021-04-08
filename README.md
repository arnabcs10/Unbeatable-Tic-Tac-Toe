# Unbeatable Tic-Tac-Toe
An implementation of Minimax AI Algorithm on Tic-Tac-Toe (or Noughts and Crosses) game. Try it: [Unbeatable Tic-Tac-Toe](https://unbeatable-tic-tac-toe-game.netlify.app/)

<p align="center">
	<img src="preview/sample.png"></img>
</p>

## Introduction
To solve games using AI, we will introduce the concept of a game tree followed by minimax algorithm. The different states of the game are represented by nodes in the game tree, very similar to the above planning problems. The idea is just slightly different. In the game tree, the nodes are arranged in levels that correspond to each player's turns in the game so that the “root” node of the tree (usually depicted at the top of the diagram) is the beginning position in the game. In tic-tac-toe, this would be the empty grid with no Xs or Os played yet. Under root, on the second level, there are the possible states that can result from the first player’s moves, be it X or O. We call these nodes the “children” of the root node.

Each node on the second level, would further have as its children nodes the states that can be reached from it by the opposing player's moves. This is continued, level by level, until reaching states where the game is over. In tic-tac-toe, this means that either one of the players gets a line of three and wins, or the board is full and the game ends in a tie.

## What is Minimax?
Minimax is a artificial intelligence applied in two player games, such as tic-tac-toe, checkers, chess and go. This games are known as zero-sum games, because in a mathematical representation: one player wins (+1) and other player loses (-1) or both of anyone not to win (0).

## How does it works?
The algorithm search, recursively, the best move that leads the *Max* player to win or not lose (draw). It consider the current state of the game and the available moves at that state, then for each valid move it plays (alternating *min* and *max*) until it finds a terminal state (win, draw or lose).

## Understanding the Algorithm
The algorithm was studied by the book Algorithms in a Nutshell (George Heineman; Gary Pollice; Stanley Selkow, 2009). Pseudocode (adapted):

```
minimax(state, depth, player)

	if (player = max) then
		best = [null, -infinity]
	else
		best = [null, +infinity]

	if (depth = 0 or gameover) then
		score = evaluate this state for player
		return [null, score]

	for each valid move m for player in state s do
		execute move m on s
		[move, score] = minimax(s, depth - 1, -player)
		undo move m on s

		if (player = max) then
			if score > best.score then best = [move, score]
		else
			if score < best.score then best = [move, score]

	return best
end
```
## Getting Started

### Installing

* Fork and clone this repository in your system
* Go to the required directory and run 
```
git clone https://github.com/arnabcs10/Unbeatable-Tic-Tac-Toe.git
```

### Executing program
Follow the instructions to get started with the project on your local machine 🚀

* In your terminal run `cd tic-tac-toe-ai/`
* Run `index.html` to view the project.

## Authors

@arnabcs10

## Version History

* 0.1
    * First Release - An implementation of Minimax AI Algorithm on Tic-Tac-Toe (or Noughts and Crosses) game.


