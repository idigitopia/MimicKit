
<!-- G1 Steering  -->
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/home/ayubi/miniconda3/envs/mkit/lib/

<!-- Train (warmstart from output/model.pt, save to new_model.pt) -->
python mimickit/run.py --arg_file args/amp_steering_g1_args.txt --mode train --visualize false --model_file output/model.pt

<!-- Test -->
python mimickit/run.py --arg_file args/amp_steering_g1_args.txt --mode test --visualize true --num_envs 4 --model_file output/model.pt
