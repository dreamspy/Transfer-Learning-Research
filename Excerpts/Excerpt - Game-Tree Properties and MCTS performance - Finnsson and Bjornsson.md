
#EXCERPT: Game-Tree Properties and MCTS Performance


## Main idea
Measure the effect of high level game properties on the effectiveness of using MCTS, compared f.x. to $\alpha\beta$ search. Done using specially designed games that exploit the given properties.

**From Abstract:** In here we identify some general properties that are encountered in game trees and measure how these properties affect the success of MCTS. We do this by running it on custom-made games that allow us to parameterize various game properties in order for trends to be discovered. Our experiments show how MCTS can favor either deep, wide or balanced game trees. They also show how the level of game progression relates to playing strength and how disruptive Optimistic Move can be.

#### Game-Tree Properties
- Tree Depth vs Branching factor 
- Optimistic moves
	- Optimistic moves is a name we have given moves that achieve very good result for its player assuming that the opponent does not realize that this seemingly excellent move can be refuted right away. The refutation is usually accomplished by capturing a piece that MCTS thinks is on its way to ensure victory for the player.In the worst case this causes the player to actually play the optimistic move and lose its piece for nothing. Given enough simulations MCTS eventually becomes vice to the fact that this move is not a good idea, but at the cost of running many simulations to rule out this move as an interesting one.
- Progression

## Conclusion
### Tree Depth vs Branching factor
To summarize MCTS does not have a deﬁnite favorite when it comes to depth and branching factor and its strength cannot be predicted from those properties only. It appears to be dependent on the rules of the game being played. We show that games can have big branching factors that pose no problem for MCTS. Still with very simple alterations to our abstract game we can see how MCTS does worse with increasing branching factor and can even prefer a balance between it and the tree depth.

### Progression
The above results show that progression is an important property for MCTS, however, what is somewhat surprising is how quickly MCTS’s performance improves as the percentage of simulations ending at true terminal states goes up.

This game property of winning only by committing to any single out of many possible good strategies, is clearly important in the context of MCTS. We suspect that in games with this property MCTS might be more prone to switching strategies than traditional ↵" search, because of the inherent variance in simulation-based move evaluation. Although we did not set out to investigate this now apparently important game property, it clearly deservers further investigation in future work.

### Optimistic Moves

The setup showcases that optimistic moves are indeed a big problem for MCTS. Even at 50,000,000 node expansions the player faced with the biggest branching factor still erroneously believes that he must block the opponent’s piece on the right wing before it is moved forward (the opponent’s optimistic move).

Two general method of doing so are the MAST (Finnsson and Bjornsson 2008) and RAVE (Gelly and Silver 2007) techniques, but much bigger improvements could be made if these moves could be identiﬁed when they are ﬁrst encountered and from then on completely ignored.

### Final conclusion from article

In this paper we tried to gain insight into factors that inﬂuence MCTS performance by investigating how three different general game-tree properties inﬂuence its strength.

We found that it depends on the game itself whether MCTS prefers deep trees, big branching factor, or a balance between the two. Apparently small nuances in game rules and scoring systems, may alter the preferred game-tree structure. Consequently it is hard to generalize much about MCTS performance based on game tree depth and width. Progression is important to MCTS. However, our results suggests that MCTS may also be applied successfully in slow progressing games, as long as a relatively small percentage of the simulations provide useful outcomes. In GGP games one could potentially take advantage of how low ratio of real outcomes are needed, by curtailing potentially fruitless simulations early, thus increasing simulation through-put. Hints of MCTS having difﬁculty in committing to a strategy when faced with many good ones were also discov-ered. Optimistic Moves are a real problem for MCTS that escalates with an increased branching factor.

For future work we want to come up with methods for MCTS that help it in identifying these properties on the ﬂy and take measures that either exploit or counteract what is discovered. This could be in the form new extensions, pruning techniques or even parameter tuning of known extension. Also more research needs to be done regarding the possible MCTS strategy commitment issues.