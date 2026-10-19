
This is taken from https://huggingface.co/learn/llm-course/chapter12/5, with some changes to fix things which are broken in the link. The goal is to become familiar with finetuning LLMs using reinforcement learning. I ran the scripts here using RunPod (for GPU access). 

The original LLM was trained using the usual maximum likelihood/cross-entropy. During any finetuning, we expect that that loss function increases on the original dataset since we are now optimizing the model with respect to a different loss function. This is what we see here. 

![image](https://github.com/dwight-nwaigwe/finetune-LLM-with-RL/blob/main/loss.png)


Reinforcement learning rewards good behavior, and penalizes bad. Successful finetuning with RL requires that our rewards increase with time, which we see here.

![image](https://github.com/dwight-nwaigwe/finetune-LLM-with-RL/blob/main/reward.png)



Output of finetuned model (173 words):

```
The cat is a fascinating and complex creature. Here's a short summary of its history, characteristics, and behaviors:

**History:**

* The earliest known ancestor of the domestic cat is Felis catus, which lived around 7500 BC.
* The earliest known domesticated cat is Felis catus, which lived around 7500 BC.
* The domesticated cat is thought to have originated in the Middle East, where it was domesticated by humans around 7500 BC.

**Characteristics:**

* The domestic cat is a small, carnivorous mammal that belongs to the Felidae family.
* It has a slender, elongated body covered in short, dark brown or black fur.
* The coat is short and smooth, with a distinctive white spot at the base.
* The eyes are large and expressive, with a prominent left eye and a small right eye.
* The ears are small and rounded, with a prominent inner ear.
* The tail is long and muscular, with a distinctive black tip.
* The tail is used for balance and balance.
* The paws are small and adapted for walking on four legs.

**Behavior:**

* The domestic cat
```


Output of original model (175 words):
```
The cat is a fascinating species that has captivated human imagination for centuries. Here's a detailed explanation of its history,
characteristics, behavior, and significance:

**History**

The domestication of the cat dates back to around 7,500 years ago, when humans began to domesticate wild animals. The earliest recorded evidence
of cat domestication comes from the ancient Mesopotamian civilization, around 3000 BC. The earliest known domesticated cat, Felis silvestris lybica,
 was domesticated in the Middle East around 7,500 BC.

**Characteristics**

* **Domestication**: The cat's domestication was gradual, with early humans adopting the cat as a companion animal. Over time, the cat became more
domesticated, and it evolved into a distinct species.
* **Physical Characteristics**: The cat has a slender, elongated body with a short, rounded tail. Its coat is short and dense, with a soft, white
undercoat. The cat's eyes are large, round, and dark, with vertical pupils.
* **Behavior**: The cat is a solitary hunter, but it can be trained to hunt small prey, such as rodents and birds. It has a keen sense of smell and
is capable
```

Our finetuned RL model is barely shorter for this example.
