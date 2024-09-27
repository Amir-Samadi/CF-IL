# Good Data Is All Imitation Learning Needs

This is the repository for CF-Driver, the codebase for our paper "Good Data Is All Imitation Learning Needs", which can be seen [here](https://arxiv.org/abs/2302.12689 'Huber paper'). This repository contains all necessary resources to reproduce the experiments presented in the paper and apply Counterfactual Explanations (CFEs) for Autonomous/Automated Driving Systems (ADS).

## Prerequisites
Carla version: 0.9.10.1

If you haven't installed the environment of `leaderboard` or `scenario_runner` before:
```bash
cd /path/to/DOS
pip install -r leaderboard/requirements.txt
pip install -r scenario_runner/requirements.txt
```

## Setup
To use this benchmark for data collection or agent evaluation based on an existing project (like [InterFuser](https://github.com/opendilab/InterFuser), [LAV](https://github.com/dotchen/LAV)), you only need to follow these four steps:
1. Clone the repository using Git.
2. Go to your project directory and make a backup of your leaderboard and scenario_runner folders.
3. Move the DOS_benchmark folder to your project directory, and replace the existing leaderboard and scenario_runner folders with the ones provided in this repository.
4. Update leaderboard/scripts/run_evaluation.sh by setting ROUTES to DOS_benchmark/DOS_0X_town05.xml, SCENARIOS to DOS_benchmark/DOS_0X_town05.json (where X is the scenario id), and ensuring that TEAM_CONFIG, TEAM_AGENT, and CARLA_ROOT are correctly configured.



## 📖 Citation
If you use CF-Driver in your research or find our repo useful, please cite our paper:
```bibtex
@misc{samadi2024gooddataimitationlearning,
      title={Good Data Is All Imitation Learning Needs}, 
      author={Amir Samadi and Konstantinos Koufos and Kurt Debattista and Mehrdad Dianati},
      year={2024},
      eprint={2409.17605},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2409.17605}, 
}
```
