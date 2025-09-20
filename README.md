# RLeste

<img src="https://i.imgur.com/r71ZG9D.gif" alt="RLeste" width="256">

A reinforcement learning implementation to solve [Celeste Classic](https://www.lexaloffle.com/bbs/?tid=2145).
Based on the marvelous [Pyleste](https://github.com/CelesteClassic/Pyleste) emulator.

It currently uses a very simple reward heuristic that's enough for beating the first two levels.
More complex levels (the ones with keys, for instance) would require more fleshed-out heuristics,
the same if one wants to get the strawberries.
The optimization is done through DQN tuned for high exploration,
which should be good throughout the whole game.

Solutions can be visualized with [CelesteTAS](https://github.com/CelesteClassic/ClassicTAS/tree/master/Celeste)
after converting the output to a supported format.

## TODOs
1. Port the solution to [Ray RLib](https://docs.ray.io/en/latest/rllib/index.html) so we can use [action masking](https://github.com/ray-project/ray/blob/3a60beec28c1f9a2d132b6dba40cc5fc5c3aa879/rllib/examples/envs/classes/action_mask_env.py) (only take valid actions at each frame).
2. Improve the reward rule so it's more generalized and (maybe) accomplishes many objectives at once (getting keys, strawberries, etc.).
3. Optimize the time penalty or the time logic as a whole so the agent is faster (learns to speedrun).
4. Strawberries!
