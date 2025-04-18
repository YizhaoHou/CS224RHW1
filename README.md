# CS224RHW1
YizhaoHou/CS224RHW1


# CS224R Homework 1: Behavior Cloning and DAgger

This project implements **Behavior Cloning (BC)** and **DAgger** for imitation learning on Mujoco environments using expert data and policies.




##  How to Run

### ➤ Behavior Cloning (BC) Problem 1


```bash
python cs224r/scripts/run_hw1.py \
--expert_policy_file cs224r/policies/experts/Ant.pkl \
--env_name Ant-v4 \
--expert_data cs224r/expert_data/expert_data_Ant-v4.pkl \
--exp_name bc_ant \
--n_iter 1 \
--video_log_freq -1 \
--ep_len 1000 \
--num_agent_train_steps_per_iter 10000 \
--eval_batch_size 5000 \
--n_layers 2 \
--size 128 \
--learning_rate 1e-3 \
--train_batch_size 128
