# Power-Benchmark: Benchmarking RL-agents for Power Grids

Master's thesis by **Giulio Maximilian Pazzi**  
University of Kassel — Department of Electrical Engineering / Computer Science  
Department of Intelligent Embedded Systems  
Submitted: September 2026

## About

The increasing complexity of power grids and the growing use of reinforcement learning
agents and other automated control strategies create a need for reliable methods to
evaluate and compare agents for power grid operation.

Existing benchmarks often rely primarily on aggregated measures such as cumulative
reward. While these measures allow agents to be ranked, they provide limited insight
into their individual strengths, weaknesses, and behaviour.

This thesis presents **Power Benchmark**, a configurable benchmarking tool for agents
in power grid operation. The benchmark combines quantitative scoring with detailed
diagnostic feedback and evaluates agents across configurable scenarios with different
power grids, profiles, and grid modifications.

Agent performance is measured using multiple grid-operation metrics. These metrics are
normalised and hierarchically aggregated into category, scenario, and overall benchmark
scores. In addition to numerical evaluation, Power Benchmark provides textual and visual
result presentations as well as replay functionality for analysing agent actions and the
resulting grid states over time.

The benchmark is evaluated experimentally using a do-nothing agent, a greedy agent,
and a PPO agent with a graph neural network policy encoder. The experiments demonstrate
that the evaluation of power-grid agents should not be reduced to a single aggregated
score or a single scenario. Analysing multiple metrics across diverse operating conditions
provides substantially more information about agent behaviour and can reveal undesirable
strategies that would otherwise remain hidden.

## Research Question

> How can a benchmarking tool be designed to quantitatively and qualitatively evaluate
> and compare agents for power grid operation, providing both an overall performance
> score and detailed feedback on their strengths and weaknesses across different operating
> scenarios?

## Main Contributions

The thesis introduces:

- a configurable benchmark for evaluating reinforcement learning agents in power-grid
  operation
- a hierarchical scoring system based on normalised grid-operation metrics
- configurable scenarios using different grids, profiles, and grid modifications
- evaluation categories covering overload mitigation, voltage violation mitigation,
  survival, operational costs, and computational performance
- textual and visual result analysis
- replay functionality for inspecting agent actions and grid states over time
- support for baseline agents and custom trainable reinforcement learning agents
- an experimental comparison of do-nothing, greedy, and PPO-based control strategies

## Repository Contents

This repository contains the material associated with the Master's thesis, including:

- the thesis source files
- the final thesis PDF
- experiment configurations
- experiment and training results (see next section)

### Experiment and Training Results

Due to their size, the complete experiment and training artifacts are not stored directly in this repository.

They are available through the repository's **GitHub Releases**:

[View experiment and training results in GitHub Releases](https://github.com/Giulcoo/power-benchmark-thesis/releases/tag/results)

The release assets include:

- experiment results
- for the PPO:
  - hyperparameter tuning results
  - training checkpoints
  - training logs

These files correspond to the experiments presented in the thesis and can be used to inspect or reproduce the reported results.

### Reproducing the Experiment

First the [Power Benchmark](https://github.com/Giulcoo/power-benchmark) project needs to downloaded and correctly setup as described in the tool's wiki. 
Then the configs and scenarios folder should be copied into the power-benchmark project folder to use the same configurations.
Follow the wiki in [Power Benchmark](https://github.com/Giulcoo/power-benchmark) to run the config afterwards.

For the **PPO Perf** experiment (computational performance test), the corresponding trained PPO checkpoint must be copied into the `PPO Perf` experiment folder before running the experiment.

The checkpoint is provided in the GitHub Release together with the other training artifacts.

After downloading the release assets, copy the PPO performance checkpoint into the respective `PPO Perf` folder so that the agent can load the trained model when recreating the performance experiment.

## Power Benchmark

The implementation of **Power Benchmark** is maintained in a separate repository:

[Power Benchmark](https://github.com/Giulcoo/power-benchmark)

The software repository contains the benchmark implementation, installation and usage
instructions, agent integration, configuration examples, and additional documentation in
its GitHub Wiki.

## Citation

If you use this work in academic research, please cite the Master's thesis:

```text
@mastersthesis{pazzi2026powerbenchmark,
  author  = {Giulio Pazzi},
  title   = {Power-Benchmark: Benchmarking RL-agents for Power Grids},
  school  = {University of Kassel},
  year    = {2026},
  type    = {Master's Thesis},
  address = {Kassel, Germany},
  month   = sep
}
```

## License

**Power-Benchmark: Benchmarking RL-agents for Power Grids © 2026 by Giulio Maximilian Pazzi is licensed under CC BY 4.0.**

To view a copy of this license, visit:

https://creativecommons.org/licenses/by/4.0/

Unless otherwise noted, this license applies to the contents of this repository, including the thesis text, thesis PDF, original figures, tables, experiment results, and related research materials.

Third-party materials remain subject to their respective copyright and licensing terms.

See the [`LICENSE`](LICENSE) file for further information.