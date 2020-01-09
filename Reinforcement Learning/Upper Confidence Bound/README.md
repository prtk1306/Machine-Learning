## Upper Confidence Bound Reinforcement Learning Method

Upper Confidence Bound
Upper Confidence Bound (UCB) is the most widely used solution method for multi-armed bandit problems. This algorithm is based on the principle of optimism in the face of uncertainty.

In other words, the more uncertain we are about an arm, the more important it becomes to explore that arm.

<img src="https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2018/09/im_18-768x289.jpg"
     style="float: center; margin-right: 10px;" />

Distribution of action-value functions for 3 different arms a1, a2 and a3 after several trials is shown in the figure above. This distribution shows that the action value for a1 has the highest variance and hence maximum uncertainty.
UCB says that we should choose the arm a1 and receive a reward making us less uncertain about its action-value. For the next trial/timestep, if we still are very uncertain about a1, we will choose it again until the uncertainty is reduced below a threshold.
The intuitive reason this works is that when acting optimistically in this way, one of two things happen:

optimism is justified and we get a positive reward which is the objective ultimately
the optimism was not justified. In this case, we play an arm that we believed might give a large reward when in fact it does not. If this happens sufficiently often, then we will learn what is the true payoff of this action and not choose it in the future.
UCB is actually a family of algorithms. Here, we will discuss UCB1.

Steps involved in UCB1:

Play each of the K actions once, giving initial values for mean rewards corresponding to each action at
For each round t = K:
Let Nt(a) represent the number of times action a was played so far
Play the action at maximising the following expression:

<img src="https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2018/09/im_19.jpg"
     style="float: center; margin-right: 10px;" />


Observe the reward and update the mean reward or expected payoff for the chosen action
We will not go into the mathematical proof for UCB. However, it is important to understand the expression that corresponds to our selected action. Remember, in the random exploration we just had Q(a) to maximise, while here we have two terms. First is the action value function, while the second is the confidence term.

Each time a is selected, the uncertainty is presumably reduced: Nt(a) increments, and, as it appears in the denominator, the uncertainty term decreases.

<img src="https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2018/09/im_20-300x105.jpg"
     style="float: center; margin-right: 10px;" />


On the other hand, each time an action other than a is selected, t increases, but Nt(a) does not; because t appears in the numerator, the uncertainty estimate increases.

<img src="https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2018/09/im_21-300x90.jpg"
     style="float: center; margin-right: 10px;" />


The use of the natural logarithm means that the increases get smaller over time; all actions will eventually be selected, but actions with lower value estimates, or that have already been selected frequently, will be selected with decreasing frequency over time.
This will ultimately lead to the optimal action being selected repeatedly in the end.

**Case study:** The Manager of a grocery store in the south of France wanted to optimize the sales of their products using Association Rule Learning to know exactly where to place the products in the store. Use the Apriori Association Learning Rule to solve the case study. 

Please find the dataset attached!

![alt text](https://github.com/prtk1306/MachineLearning/blob/master/ML%20Logo.PNG "Machine Learning")

Citation: https://www.udemy.com/, https://en.wikipedia.org/