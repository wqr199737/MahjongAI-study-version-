# README -- MahjongAI

### Mahjong is a four-player strategy game with imperfect information. The main challenges of developing an intelligent Mahjong agent are for example the complicated game rules, the immense search space, multiple opponents and imperfect information. Several existing works have attempted to tackle these problems through Monte Carlo tree simulation, utility function fitting by supervised learning or opponents' model by regression algorithms. Nevertheless, the performance of intelligent Mahjong playing agents is still far away from that of the best human players. Based on statistical analysis for the Mahjong game and human expert knowledge, an intelligent Mahjong agent was proposed in this work. To tackle the problems of the state-of-the-art work, heuristics technologies and an enhanced opponents model achieved by adopting bagging of multilayer perceptron's were applied to this work. The experiments show that the proposed agent outperforms the state-of-the-art agent, and the applied opponents model has a significant positive effect on the performance of the agent. Furthermore, several interesting points can be discerned from the experiments, which are pretty meaningful for future work.
We introduced global reward prediction in Suphx. In the current system, the reward predictor takes limited information as its input. That is, game difficulty should be taken into consideration while designing reward signals. 
We are investing how to leverage prefect information (e.g., by comparing the private initial hands of different players) to measure the difficulty of a round/game and then boost the reward predictor. • We introduced the concept of oracle guiding and instantiated this concept using the gradual transition from an oracle agent to a normal agent by means of perfect feature dropout.
For run-time policy adaptation, in the current system of Suphx, we did 22 simulations at the beginning of each round when private tiles were dealt to our agent. That is, instead of only adapting the policy to the initial hands, we can continue the adaptation as the game goes on and more and more information becomes observable. Doing so should be able to further improve the performance of our policy. 
Differences between Perfect-Information Games and Imperfect-Information Games. For perfect-information games, basically it`s a search tree with value network.
For imperfect-information games, it`s all about the EV(expecting value). But because the role of mahjong can be very complicated, which will be stated in the next slide, there will be so many relevant factors.
In the picture on the left, the X axis means the points that can be earned if win, Y axis means the time state in the game(turns) and Z axis means the EV of earning those points. This is when a tile is discarded in a particular situation.
![image](https://user-images.githubusercontent.com/103657230/205228636-705ac54c-527a-45e9-84d7-8c9507db29b0.png)
![image](https://user-images.githubusercontent.com/103657230/205228655-f3fe897a-efca-4f7a-8b40-943d0016493a.png)
![image](https://user-images.githubusercontent.com/103657230/205228691-58cca471-51f7-4465-acca-10f1f963d3b7.png)
![image](https://user-images.githubusercontent.com/103657230/205228699-b514d513-8cc4-4667-8139-9d66467def83.png)
The learning of Suphx contains three major steps. First, we train the five models of Suphx by supervised learning, using (state, action) pairs of top human players collected from the Tenhou platform. Second, we improve the supervised models through self-play reinforcement learning (RL), with the models as policy. We adopt the popular policy gradient algorithm (Section 3.1) and introduce global reward prediction (Section 3.2) and oracle guiding (Section 3.3) to handle the unique challenges of Mahjong. Third, during online playing, we employ run-time policy adaptation (Section 3.4) to leverage the new observations on the current round in order to perform even better. 
![image](https://user-images.githubusercontent.com/103657230/205228711-c9ccb29c-ade9-4fd4-ab7b-ff2ce5186bfe.png)
For the version with defense model, 526 games were played, and for the version without defense model, 532 games were played. This is not as many as two related works, but as shown in the figure of the convergence behavior of agent's performance, 526 games are sufficient.
![image](https://user-images.githubusercontent.com/103657230/205228723-8fce09ab-6ef0-4530-8b2b-7ae81d6b75a3.png)
![image](https://user-images.githubusercontent.com/103657230/205228737-42be8184-afc7-4329-a56e-95c66d96e21b.png)
![image](https://user-images.githubusercontent.com/103657230/205228742-614ed9da-045f-4e22-9d3c-1a7157af2514.png)
![image](https://user-images.githubusercontent.com/103657230/205228749-64594566-4232-42fa-8252-cce595776677.png)
[1] My Mahjong agent with defence model
[2] My Mahjong agent without defence model
[3] Mizukami's extended work: Mizukami N., Tsuruoka Y.. Building a computer mahjong player based on monte carlo simulation and opponent models. In: 2015 IEEE Conference on Computational Intelligence and Games (CIG), pp. 275–283. IEEE (2015)
[4] Mizukami et. al.: N. Mizukami, R. Nakahari, A. Ura, M. Miwa, Y. Tsuruoka, and T. Chikayama. Realizing a four-player computer mahjong program by supervised learning with isolated multi-player aspects. Transactions of Information Processing Society of Japan, vol. 55, no. 11, pp. 1–11, 2014, (in Japanese).
![image](https://user-images.githubusercontent.com/103657230/205228757-44d09954-3cbe-4883-b590-7d086f430ce7.png)
Suphx: Mastering Mahjong with Deep Reinforcement Learning. Junjie Li,1 Sotetsu Koyamada,2 Qiwei Ye,1Guoqing Liu,3 Chao Wang,4 Ruihan Yang,5 Li Zhao,1TaJunjie Li,1 Sotetsu Koyamada,2 Qiwei Ye,1Guoqing Liu,3Chao Wang,4 Ruihan Yang,5 Li Zhao,1Tao Qin,1 Tie-Yan Liu,1 Hsiao-Wuen Hon11Microsoft Research Asia2Kyoto University, University of Science and Technology of ChinaTsinghua UniversityNankai University
This work was conducted at Microsoft Research Asia. The 2nd, 4th, 5th, and 6th authors were interns at Microsoft Research Asia then.o Qin,1 Tie-Yan Liu,1 Hsiao-Wuen Hon11Microsoft Research AsiaKyoto UniversityUniversity of Science and Technology of China4Tsinghua UniversityNankai University
This work was conducted at Microsoft Research Asia. The 2nd, 4th, 5th, and 6th authors were interns at Microsoft Research Asia then.
MahjongAI by erreurt, Jianyang Tang (Thomas): jian4yang2.tang1@gmail.com



![image](https://user-images.githubusercontent.com/103657230/205228769-b1c1b35d-bb50-465a-9b41-337591175853.png)





