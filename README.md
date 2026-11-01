# Tag of Flag
Proposing Tag of Flag as a game with 12-DOF quadrupeds carrying a 6-DOF arm. The goal is to capture the flag on the opponent team's quadruped's back.

With the recent CD-07B update ([GitHub](https://github.com/SphericalCowww/CubicDoggo_07B)) suggesting a low-budget 12-DOF quadruped can carry more than 1 kg of payload, and a recent ROS2 Jazzy implementation ([GitHub](https://github.com/adoodevv/so101_ros2)) of the SO-101 arm of roughly 700g ([HuggingFace](https://huggingface.co/docs/lerobot/en/so101)), I think this make the following game challenge possible. 

In developing the winning strategies, this game could enforce multiple engineering disciplines that are beneficial to the robotics community. I believe this game has the potential to be **a long-term educational and research platform and a worthwhile benchmark** to aim for.

The following are some suggestive rules just to have a starting point.

## V0 Rules

### Goal

The goal of the game is very simple: 2 players each control a quadruped that starts with a standardized flag on the robot's back. The player wins when the opponent's flag leaves the flag-mount in any way or if the opponent exits the arena on all landed feet.

### Arena/Flag

  * Arena: 160 cm x 180 cm fire blanket (for example, [Amazon](https://www.amazon.de/Extra-Large-Fire-Blanket-Extinguisher/dp/B0FX38NKM7))
  * Start position: opposite ends of the arena facing each other
  * Height baseline: the top of the battery pack
  * Flag standard: a survey flag (for example, [Amazon](https://www.amazon.de/dp/B0FBKQ2F62)), should be pretty lightweight
  * Flag-mount standard: 3D-printed 8 cm height block, any shape within 3 cm diameter, as long as there is an 8 cm tall loose insert facing up. The bottom of the flag-mount should be within 4 cm in height of the height baseline

Additional rule:

  * Deliberate damage to the electronics and other robot components is not allowed, so no tripping legs
  * Potential timeout 

### Robot requirements

  * 4x3-DOF quadruped with a 6-DOF arm using 12V ST-3215 servos. The budget should be controlled to < 1000 EUR
  * Printed with PLA or its variants for all its support parts, but otherwise free to design any parts 
    - bolts+nuts+washers, heat set inserts, and glue are all allowed, but only for connections
    - also allow bearings, and the linkages are allowed to be non-PLA materials, but again only for connections
    - considering the shielding dimension, the CAD should not be built to be taller than the flag-mount when mounted. The only exception will be the moving parts of the arm
    - no hook structure on the arm 
  * Controlled by ROS, but gait, automation, and reinforcement learning stack are completely free to optimize
  * Sensors up to 200 EUR are allowed, but watch out for potential damages
  * Untethered using batteries
  * No wheels by default
  * No projectiles
  * No controller interference

### Potential tactics

  * Use PLA shielding to protect the flag surround
  * Control better manually to bypass the opponent's arm using the leader arm, made possible if the gait is nicely written
  * Use Nav to circle around the opponent
  * Use RL to compensate for the arm extension imbalance

Depending on the actual performance when improved to the ST3215's limits, the game probably resembles less of a dogfight, but a naval duel that some type of anchor-mode is needed to maximally extend the arm

  * Note that no rule says the belly cannot contact the ground
  * Even if the leg is broken, the player is still in the game if the flag is still safe


### Team idea

  * Perhaps a team of 4, with one as the ace that is allowed to have wheels
    - robot with flag taken is out of commission
    - 10 min game. The team with the most flags left wins
    - can be played under different terrains
  * Perhaps allow multi-robot coordination codes
  * Perhaps allow CAD linkage between robots

## References:

- CubicDoggo 07B: Homemade 12-DOF 4-Legged Robot Recipe ([GitHub](https://github.com/SphericalCowww/CubicDoggo_07B))
- adoodevv, so101_ros2 ([GitHub](https://github.com/adoodevv/so101_ros2))
- LeRobot, SO-101 ([HuggingFace](https://huggingface.co/docs/lerobot/en/so101))


