*🌌 Plan2Explore: Chasing Rewards in Latent Realms*

“Pg 66 of the Rosetta Stone of the mind says: We understand the context of experience, but fail to record it. Thus, relations fade before they form. In RL, too, we modeled dreams, but always kept them in reality’s shape. Plan2Explore dares to go further—it dreams in latent space.”

**🌟 Overview**

Plan2Explore is a curiosity-driven reinforcement learning (RL) algorithm that thrives in sparse-reward environments by learning world dynamics in latent space. Unlike traditional agents (like MBPO) which operate in observation space for both real and imagined experiences, Plan2Explore transitions to latent representations—enhancing generalization and exploration.

This project is not just a reinforcement learning algorithm—it’s a philosophical shift from chasing rewards to understanding the unknown. Inspired by human curiosity, Plan2Explore updates the agent through surprise and predictive disagreement in a learned world model.

**🚀 Motivation**

Model-based RL has long aimed to reduce sample inefficiency, but often struggles with high-dimensional raw inputs and sparse feedback. While MBPO grounded its learning in real-world rollouts, Plan2Explore explores—literally—by imagining futures in a compact latent space and rewarding itself for being surprised.

**🧠 Architecture**

Plan2Explore's design blends structure and surprise:

    Encoder – Converts raw observations into latent representations.
    
    GRU World Model – Predicts future latent states through recurrent dynamics.
    
    Ensemble Module – A disagreement-driven module for intrinsic reward.
    
    World Loss – Joint reconstruction and forward prediction losses for stable world learning.
    
    Feature Extractor – Processes latent dynamics into meaningful features.
    
    Actor & Critic – Policy and value functions operating in latent space.
    
    Target Networks – For soft target updates and stability.
    
    Two Buffers – Real and imagined transitions (sac_buffer + imagination_buffer).
    
    Mixed Batch Logic – Balanced sampling from both buffers to update SAC.
    
    Intrinsic Reward Generator – Based on ensemble disagreement.
    
    Training Loop – Integrates SAC and world updates in a unified flow.

 **🧪 Key Techniques & Skills Used**

    ✅ Reinforcement Learning (Soft Actor-Critic)
    
    ✅ Recurrent Models (GRU-based Dynamics)
    
    ✅ Latent Space Modeling
    
    ✅ Curiosity-Driven Exploration (Intrinsic Motivation)
    
    ✅ Ensemble Modeling for Uncertainty
    
    ✅ World Models
    
    ✅ Mixed Buffer Sampling
    
    ✅ Advanced PyTorch
    
    ✅ Gradient Clipping, Scheduling, and Target Updates
    
    ✅ Shape mismatch Strategy

**📈 Sample Logs**


    Episode: 1386 | Intrinsic Reward: 0.383
    Reward: 109.10  | Actor Loss: 3.70 | Critic Loss: 2.59 | Alpha: 0.2752
    World Loss: 0.0396
    
🛠️ Installation

git clone https://github.com/your_username/Plan2Explore.git
cd Plan2Explore
pip install -r requirements.txt

**📦 Important Code Snippets**

intrinsic_reward_function(![code](https://github.com/user-attachments/assets/2ada54a6-fed5-43f5-b35f-ed96bfbc9d82)
)

GRUWorldModel.forward(![code_1](https://github.com/user-attachments/assets/1990d22e-feed-4ce3-83fb-d0638245fddb)
)

MixBatch.sample(![code_2](https://github.com/user-attachments/assets/9407e948-9801-4cc9-9eab-460aefb40a1c)
)

Agent.update(![code_3](https://github.com/user-attachments/assets/21fc081a-cd15-4c7b-b120-8ec82ca79075)
)


**🔭 Future Directions**

**The next leap is a return to roots—a return to model-free RL with a deep understanding of latent dynamics. The goal: TRPO-based exploration that blends curiosity with structure, with zero reliance on learned world models.**


**❤️ Author's Note**

This project is part of a greater journey toward AI that dreams, wonders, and learns like us. Built during long nights of silence, Plan2Explore is a tribute to solitude, obsession, and the joy of learning from the unknown.

“I do not chase rewards—I chase the reason for them.”
