# Environment-Mapping-with-a-Swarm-of-Mechalino-Robots
Swarm Robotics • Environment Mapping • Decentralized Exploration • Multi-Robot Systems

Exploration and mapping of unknown environments is an important capability for multi-robot systems used in inspection, monitoring, and search tasks. The Mechalino platform provides a low-cost swarm robotics system equipped with eight infrared distance sensors arranged at 45 degree intervals around the robot, enabling obstacle perception in all directions. A swarm-based coverage exploration algorithm [37] already exists that enables robots to explore unknown environments with obstacles using decentralized decision-making. In the original formulation of the algorithm, obstacle avoidance relies only on front-facing sensors, although the robot hardware provides sensing capabilities around the entire body.

This project investigates how a swarm of Mechalino robots can construct a map of an unknown environment while performing decentralized exploration. The goal is to adapt the existing coverage exploration approach, or other decentralized swarm exploration strategies, to enable collaborative environment mapping using all available sensors of the robots.

Experiments will be conducted in the Mechalino Arena, which consists of multiple Mechalino robots, an overhead observer camera for global localization, and a ROS2-based framework for robot communication, data collection, and experiment monitoring. This setup allows robots to operate in a controlled physical environment while enabling the recording and analysis of exploration and mapping behavior.

The objective is to study how decentralized swarm exploration combined with distributed sensing can enable robots to collectively construct a map of an unknown environment.

## Research Questions
*	Can a swarm of Mechalino robots construct a consistent map of an unknown environment using decentralized exploration?
*	How can local observations from multiple robots be combined into a shared map representation?
*	How does the number of robots influence mapping speed and map completeness?

## Focus Areas
*	Implement a decentralized exploration and mapping pipeline for Mechalino robots.
*	Use the Mechalino Arena infrastructure with the observer camera and ROS2 framework for experiment control and data collection.
*	Evaluate mapping performance under different swarm sizes and obstacle configurations.

## Reading List
Khalil Al-rahman Youssefi and Wilfried Elmenreich, Coverage exploration of unknown obstacle-cluttered environments using a swarm of ground robots, Applied Soft Computing, Volume 185, 2025, 113964.

