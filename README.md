# README -- MahjongAI

### Mahjong is a four-player strategy game with imperfect information. The main challenges of developing an intelligent Mahjong agent are for example the complicated game rules, the immense search space, multiple opponents and imperfect information. Several existing works have attempted to tackle these problems through Monte Carlo tree simulation, utility function fitting by supervised learning or opponents' model by regression algorithms. Nevertheless, the performance of intelligent Mahjong playing agents is still far away from that of the best human players. Based on statistical analysis for the Mahjong game and human expert knowledge, an intelligent Mahjong agent was proposed in this work. To tackle the problems of the state-of-the-art work, heuristics technologies and an enhanced opponents model achieved by adopting bagging of multilayer perceptron's were applied to this work. The experiments show that the proposed agent outperforms the state-of-the-art agent, and the applied opponents model has a significant positive effect on the performance of the agent. Furthermore, several interesting points can be discerned from the experiments, which are pretty meaningful for future work.
We introduced global reward prediction in Suphx. In the current system, the reward predictor takes limited information as its input. That is, game difficulty should be taken into consideration while designing reward signals. 
We are investing how to leverage prefect information (e.g., by comparing the private initial hands of different players) to measure the difficulty of a round/game and then boost the reward predictor. • We introduced the concept of oracle guiding and instantiated this concept using the gradual transition from an oracle agent to a normal agent by means of perfect feature dropout.
For run-time policy adaptation, in the current system of Suphx, we did 22 simulations at the beginning of each round when private tiles were dealt to our agent. That is, instead of only adapting the policy to the initial hands, we can continue the adaptation as the game goes on and more and more information becomes observable. Doing so should be able to further improve the performance of our policy. 
![image](https://user-images.githubusercontent.com/103657230/205228408-a656ce15-6317-4ad1-86c8-e8e6404b1bdf.png)

![image](https://user-images.githubusercontent.com/103657230/205228364-32f85504-9892-45e8-b5ee-39dc295e9462.png)


