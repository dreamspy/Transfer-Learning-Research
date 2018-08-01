
#EXCERPT: General Game Learning using Knowledge Transfer


## Main idea
Transfering knowledge from one game to another by means of automatic feature detection which is implemented by coalescing subtrees with terminal states (depth 2). Q-values from source game from a specific feature is used to initialize the Q-values of the corresponding feature in the target game (same feature = same Q-value). 

**From Abstract:** *"We use the technique of value-function transfer where general features are extracted from the state space of a previous game and matched with the completely different state space of a new game. To capture the underlying similarity of vastly disparate state spaces arising from different games, we use a game-tree lookahead structure for features. We show that such feature-based value function transfer learns superior policies faster than a reinforcement learning agent that does not use knowledge transfer. Furthermore, knowledge transfer using lookahead features can capture opponent-speciﬁc value-functions, i.e. can exploit an opponent’s weaknesses to learn faster than a reinforcement learner that uses lookahead with minimax (pes-simistic) search against the same opponent."*

##Dots
- Suitable for 2 player alternate move complete information games.
- Uses TD($\lambda$)

## Conclusion
### stuff


### Final conclusion from article

transfer and nontransfer are compared with minimax-lookahead which assumes perfect play of the opponent

minimax lookahead looks x steps ahead, and then applies a heuristic if it has not reached a terminal state.

these are pitteded against good and bad players, epsylon greedy playing good, and then some playing badly (random and weak). 

transfer was always better than non-transfer

minimax was better than others when playing against "intelligent" players like epsylon greedy, but worse when playing against bad players. This makes sense since minimax assumes perfectly playing opponent


