
# Excerpt: DeepChess- End-to-End Deep Neural Network for Automatic Learning in Chess


## Main idea
- Tabula rasa DNN learning of chess. 
- No handcrated features.
- Compares two chess states and decides which is better
- "Supervised learning", using a dataset from www.computerchess.org
- On pair with state of the art grandmaster chess engines
- First end-to-end ML algorithm to achive GM results

### Difference from AZC
*We presented the first successful end-to-end application of machine learning in com- puter chess. Similarly to human chess masters, DeepChess does not assign numeral evaluation values to different positions, but rather, compares different positions that may arise, and opts for the most promising continuation.*

## Details
### Three stages in training
- 	deep unsupervised neural network for pretraining
-  supervised network to select preferable position out of two input positions, using alpha beta search
-  compress the network for speed

###	Dataset
*Dataset: We employed the games dataset of CCRL (www.computerchess.org. uk/ccrl), which contains 640,000 chess games, out of which White won 221,695 games and Black won 164,387 games, the remaining games ended in a draw. Our experiments show that the inclusion of games that ended in a draw is not beneficial, so we only use games which ended in a win.*


## Previous work
**Has detailed info about previous work**

Quote: 

* *Chess-playing programs have been improved significantly over the past several decades. While the first chess programs could not pose a challenge to even a novice player, the current advanced chess programs have been outperforming the strongest hu- man players, as the recent man vs. machine matches clearly indicate. Despite these achievements, a glaring deficiency of today’s top chess programs is their severe lack of a learning capability (except in most negligible ways, e.g., “learning” not to play an opening that resulted in a loss, etc.). During more than fifty years of research in the area of computer games, many learning methods have been employed in several games. Reinforcement learning has been successfully applied in backgammon [16] and checkers [13]. Although reinforce- ment learning has also been applied to chess [1,10], the resulting programs exhibit a playing strength at a human master level at best, which is substantially lower than the grandmaster-level state-of-the-art chess programs. These experimental results confirm Wiering’s [17] formal arguments for the failure of reinforcement learning in rather complex games such as chess. Very recently, a combination of a Monte-Carlo search and deep learning resulted in a huge improvement in the game of Go [15]. However, Monte-Carlo search is not applicable to chess, since it is much more tac- tical than Go, e.g., in a certain position, all but one of the moves by the opponent may result in a favorable result, but one refutation is sufficient to render the position unfavorable.
* In our previous works, we demonstrated how genetic algorithms (GA’s) could be applied successfully to the problem of automatic evaluation function tuning when the features are initialized randomly [3,4,5,6]. Although to the best of our knowledge, these works are the only successful automatic learning methods to have resulted in grandmaster-level performance in computer chess, they do not involve learning the features themselves from scratch. Rather, they rely on the existence of a manually created evaluation function, which consists already of all the required features (e.g., queen value, rook value, king safety, pawn structure evaluation, and many other hand crafted features). Thus, GAs are used in this context for optimization of the weights of existing features, rather than for feature learning from scratch.
*
## Evalutaion function
* *The evaluation function is the most important component of a chess program. It receives a chess position as an input, and provides a score as an output. This score represents how good the given position is (typically from White’s perspective). For example, a drawish position would have a score close to 0, a position in which white has two pawns more than black would have a score of +2, and a position in which black has a rook more than white, would be scored around −5. A good evaluation function considers typically a large number (i.e., on the order of hundreds and even thousands) of properties in addition to various piece-related parameters, such as king safety, passed pawns, doubled pawns, piece centrality, etc. The resulting score is a linear combination of all the selected features. The more accurately these features and their associated values capture the inherent properties of the position, the stronger the corresponding chess program becomes.
In this paper, we are interested in developing such an evaluation function from scratch, i.e., with absolutely no a priori knowledge. As a result, we do not provide our evaluation function with any features, including any knowledge about the rules of chess. Thus, for our training purposes, we are limited to observing databases of chess games with access only to the results of the games (i.e., either a win for White or Black, or a draw).
*	
	

## Conclusion

* On similar level as FALCON, a GM level program.
* 
### Final conclusion from article

