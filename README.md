# Implementation of Value Iteration and Maximum Entropy Value Iteration
## Setup
The code is written in python 3. In order to install the requiriments,refer to the requirements.txt and use pip3 install to install them.

Before running the code make sure to set the `PYTHONPATH` to be the project folder. You can do that by running 
the following command:

`export PYTHONPATH=path_to_folder/`

The data and logging for all the parts experiments will be saved in the folders `data/part1/`. This will contain
the final value function contour (if the state space is of dimension lower or equal than 2), the learning curve of the
run, a csv file with the returns per iteration, and a json file with the parameters of the run. If the experiments are
 run rendering the progress (by using the flag `-r` or `--render`), then it will save two videos with the learning
 progess, one for the contours and another with the rollouts.
 
 
To visualize data of combined experiments you can use the command `python viskit/frontend 
path_to_the_experiments_folder`. You will be able to visualize the learning curves split by any parameter that you 
decide or we ask in the report.

Each part folder has its own run script named `part1/run_part1.py` that will run all the environments we ask for.
You will have to modify the arguments of the run script to answer the different questions, you can see what each
command means by running `python part1/run_part1.py --help`. In all the run scripts you can run visualize the 
rollouts by adding the flag `--render` or `-r` ,i.e., `python part1/run_part1.py -r`.

The functions are documented to explain all the inputs, returns, and the utilities needed to solve each question.


## Part 1: Value Iteration
### Question (a): Implement value iteration for a deterministic policy
You will need to fill the code in `part1/tabular_value_iteration.py`
 below the lines `if self.policy_type == 'deterministic'`. Run `python part1/run_part1.py `
to run the code that will generate the plots and loggings.

### Question (b): Implement value iteration for a maximum entropy policy
You will need to fill the code in `part1/tabular_value_iteration.py`
 below the lines `if self.policy_type == 'max_ent'`. Run `python part1/run_part1.py -p max_ent -t TEMPERATURE `
to run value iteration with a maximum entropy policy and different temperature values.



