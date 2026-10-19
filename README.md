
This is taken from https://huggingface.co/learn/llm-course/chapter12/5, with some changes to fix things which are broken in the link. The goal is to become familiar with finetuning LLMs using reinforcement learning. I ran the scripts here using RunPod (for GPU access). 

The original LLM was trained using the usual maximum likelihood/cross-entropy. During any finetuning, we expect that that loss function increases on the original dataset since we are now optimizing the model with respect to a different loss function. This is what we see here. 
![image](https://github.com/dwight-nwaigwe/finetune-LLM-with-RL/blob/main/loss.png)


Reinforcement learning rewards good behavior, and penalizes bad. Successful finetuning with RL requires that our rewards increase with time, which we see here.

![image](https://github.com/dwight-nwaigwe/finetune-LLM-with-RL/blob/main/reward.png)


