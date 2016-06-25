Implementation of two reinforcement learning methods in OpenAI gym

First is an evolutionary algorithm that fits a multivariate gaussian distribution to the parameter of a parameterized policy. It then picks a top small percentage of parameters that lead to the biggest game reward. It then re-fits a multivariate gaussian to the selected parameters and continues iterating on the distribution of the parameter. Finally at test time, it uses gaussian mean as the parameter to pick policy action ( evaluated on CartPole-v0 task )

Second is a gradient based algorthm to find the parameter of the policy that maximizes the log-likelihood of the policy that leads to good rewards. It evaluates the advantage of policy by subtracting a baseline which is the average reward obtained at a particular state. It then evaluates the derivative of expected advantage with respect to the policy parameter to come up with the policy gradient. It then uses gradient descent to update the parameter ( evaluated on Acrobot-v0 task )

My lab solution for Berkeley deep RL class 
