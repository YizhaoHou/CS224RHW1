# CS224RHW1
YizhaoHou/CS224RHW1


# CS224R Homework 1: Behavior Cloning and DAgger

This project implements **Behavior Cloning (BC)** and **DAgger** for imitation learning on Mujoco environments using expert data and policies.




##  How to Run

### ➤ Behavior Cloning (BC) P1.1

#### Ant
```bash
python cs224r/scripts/run_hw1.py --expert_policy_file cs224r/policies/experts/Ant.pkl --env_name Ant-v4 --exp_name bc_ant --n_iter 1 --expert_data cs224r/expert_data/expert_data_Ant-v4.pkl --video_log_freq -1 --ep_len 1000 --num_agent_train_steps_per_iter 5000 --eval_batch_size 5000 --n_layers 2 --size 128 --learning_rate 1e-3 --train_batch_size 128
```

#### Hopper
```bash
python cs224r/scripts/run_hw1.py --expert_policy_file cs224r/policies/experts/Hopper.pkl --env_name Hopper-v4 --exp_name bc_hopper --n_iter 1 --expert_data cs224r/expert_data/expert_data_Hopper-v4.pkl --video_log_freq -1 --ep_len 1000 --num_agent_train_steps_per_iter 5000 --eval_batch_size 5000 --n_layers 2 --size 128 --learning_rate 1e-3 --train_batch_size 128
```

#### Walker2d
```bash
python cs224r/scripts/run_hw1.py --expert_policy_file cs224r/policies/experts/Walker2d.pkl --env_name Walker2d-v4 --exp_name bc_walker2d --n_iter 1 --expert_data cs224r/expert_data/expert_data_Walker2d-v4.pkl --video_log_freq -1 --ep_len 1000 --num_agent_train_steps_per_iter 10000 --eval_batch_size 5000 --n_layers 2 --size 128 --learning_rate 1e-3 --train_batch_size 128
```

### ➤ Behavior Cloning (BC) P1.2
```bash
python cs224r/scripts/run_hw1.py --expert_policy_file cs224r/policies/experts/Ant.pkl --env_name Ant-v4 --exp_name bc_ant --n_iter 1 --expert_data cs224r/expert_data/expert_data_Ant-v4.pkl --video_log_freq -1 --ep_len 1000 --num_agent_train_steps_per_iter 10000 --eval_batch_size 5000 --n_layers 2 --size 128 --learning_rate 1e-3 --train_batch_size 128
```
Change the --num_agent_train_steps_per_iter to test different training steps.

### ➤ DAgger P2
#### Ant
```bash
python cs224r/scripts/run_hw1.py --expert_policy_file cs224r/policies/experts/Ant.pkl --env_name Ant-v4 --exp_name dagger_ant --n_iter 10 --do_dagger --expert_data cs224r/expert_data/expert_data_Ant-v4.pkl --video_log_freq -1 --ep_len 1000 --eval_batch_size 5000 --n_layers 2 --size 128 --learning_rate 1e-3 --train_batch_size 128 --num_agent_train_steps_per_iter 5000
```

#### Hopper
```bash
python cs224r/scripts/run_hw1.py --expert_policy_file cs224r/policies/experts/Hopper.pkl --env_name Hopper-v4 --exp_name dagger_hopper --n_iter 10 --do_dagger --expert_data cs224r/expert_data/expert_data_Hopper-v4.pkl --video_log_freq -1 --ep_len 1000 --num_agent_train_steps_per_iter 5000 --eval_batch_size 5000 --n_layers 2 --size 128 --learning_rate 1e-3 --train_batch_size 128
```


