
This is taken from https://huggingface.co/learn/llm-course/chapter12/5, with some changes to fix things which are broken in the link.
I used RunPod for GPU access. More to come

# Figures

The loss increases because it contains Kullback-Leibler divergence contribution and reinforcement learning contribution. As the model's weights change
to increase the reward it gets, the Kullback-Leibler divergence increases as the weights stray from the optimal weights it was originally trained on.

![image](https://github.com/dwight-nwaigwe/finetune-LLM-with-RL/blob/main/loss.png)


Reinforcement learning rewards good behavior, and penalizes bad. Successful finetuning with RL requires that our rewards increase with time.

![image](https://github.com/dwight-nwaigwe/finetune-LLM-with-RL/blob/main/reward.png)


