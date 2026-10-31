# Tag of Flag
Proposing Tag of Flag as a game with 12-DOF quadrupeds carrying a 6-DOF arm. The goal of the game is to capture the flag on the back of the quadruped of the opponent team.

With the recent CD-07B update ([GitHub](https://github.com/SphericalCowww/CubicDoggo_07B)) suggesting a low-budget 12-DOF quadruped can carry more than 1 kg of payload, and a recent ROS2 Jazzy implementation ([GitHub](https://github.com/adoodevv/so101_ros2)) of the SO-101 arm of roughly 700g ([HuggingFace](https://huggingface.co/docs/lerobot/en/so101)), I think this make the following game challenge possible. 

The following are some suggestive rules just to have a starting point.

## Goal

The goal of the game is very simple: 2 players each control a quadruped that starts with a standardized flag on the robot's back. If the player can capture the opponent's flag with the arm or if the opponent exits the arena on all landed feet, the player wins.

## Robot requirements

  * 4x3-DOF quadruped with a 6-DOF arm using 12V ST-3215 servos. The budget should be controlled to < 1000 EUR
  * Printed with PLA or its variants for all its support parts, but otherwise completely free to design any parts (will need restriction on shielding around the flag eventually). Bolts+nuts, heat set inserts, and glue are all allowed on the PLA
  * Controlled by ROS, but gait, automation, and reinforcement learning stack are completely free to optimize
  * Sensors up to 200 EUR are allowed, but watch out for potential damages
  * No wheels for now

## Arena/Flag

  * The arena is a 160 cm x 180 cm fire blancket (for example, [Amazon](https://www.amazon.de/Extra-Large-Fire-Blanket-Extinguisher/dp/B0FX38NKM7))
  * The robots start from opposite ends of the arena facing each other
  * Flag insert standard, not decided. Maybe a survey flag with an 8 cm insert (for example, [Amazon](https://www.amazon.de/dp/B0FBKQ2F62)), probably too big though

## Potential strategies

  * Use PLA shielding to protect the flag surround, or hook structure on the arm (maybe hook structure should be avoided too)
  * Just control better to bypass the opponent's arm, made possible if the gait is nicely written
  * Use Nav to circle the opponent
  * Use RL to compensate for the arm extension imbalance

## References:

- CubicDoggo 07B: Homemade 12-DOF 4-Legged Robot Recipe ([GitHub](https://github.com/SphericalCowww/CubicDoggo_07B))
- adoodevv, so101_ros2 ([GitHub](https://github.com/adoodevv/so101_ros2))
- LeRobot, SO-101 ([HuggingFace](https://huggingface.co/docs/lerobot/en/so101))


