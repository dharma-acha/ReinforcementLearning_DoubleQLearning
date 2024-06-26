# Reinforcement Learning DoubleQLearning

#### Visualization of Reinforcement Learning Grid Environment 
![](images/image1.png)

####  Negative action (loss of reward)
![alt text](images/image2.png)

####  Positive action (Gain of reward)
![alt text](images/image3.png)


####  Goal (High reward)
![alt text](images/image4.png)

### Overview
Double Q-Learning is an enhancement of the traditional Q-Learning algorithm, addressing the issue of overestimation bias in action value estimates. In Q-Learning, the action values (Q-values) are updated based on the maximum Q-value of the next state, which can lead to overestimation, especially in environments with stochastic rewards or noisy observations. Double Q-Learning mitigates this overestimation by decoupling action selection and evaluation, using two separate Q-value estimators.

### Key Concepts
#### 1. Action Selection and Evaluation:

* Double Q-Learning maintains two sets of Q-values Q1 and Q2

* For each state transition, one of the Q-values is used to select the next action, while the other is used to evaluate the chosen action's value.

#### 2. Update Rule:

![](images/image5.png)

* At each step, one of the Q-value estimators is randomly selected to update.
* The update rule for the selected Q-value is similar to the standard Q-Learning update, using the Bellman equation to estimate the value of taking an action in a state.

#### 3. Target Network:

* To stabilize training, a separate target network may be used to calculate the target Q-value.

* The target network is periodically updated with the parameters of the primary Q-value estimator.

#### 4. Benefits
* Reduced Overestimation: By decoupling action selection and evaluation, Double Q-Learning reduces the overestimation bias present in traditional Q-Learning.

* Improved Learning Stability: The use of two Q-value estimators and potentially a target network enhances the stability of learning, leading to more robust performance in noisy environments.

### Contact

If you have any questions or comments, feel free to contact me on [Email](mailto:achadharma333@gmail.com)
