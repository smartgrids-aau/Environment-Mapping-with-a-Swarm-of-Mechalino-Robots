# Environment-Mapping-with-a-Swarm-of-Mechalino-Robots
Swarm Robotics • Environment Mapping • Occupancy Grid Mapping • Neural Networks • Bayesian Sensor Fusion

Exploration and mapping of unknown environments is an important capability for multi-robot systems used in inspection, monitoring, and search tasks. The Mechalino platform provides a low-cost swarm robotics system equipped with eight infrared distance sensors arranged at 45 degree intervals around the robot, enabling obstacle perception in all directions. Reliable environment mapping requires that the raw IR sensor readings, which are prone to reflection artifacts and offsets, first be converted into an accurate occupancy representation of the environment.

This repository documents work on constructing occupancy grid maps from Mechalino IR sensor readings, using a single robot as the basis for the underlying sensor processing pipeline before extending it to a full swarm setting. Sensor readings are processed with a neural network that learns to distinguish real object reflections from wall/free-space reflection behavior, fused into occupancy probabilities using a Bayesian sensor fusion approach, and further refined with a second neural network that evaluates local spatial plausibility across neighboring grid cells.

Experiments were conducted in the Mechalino Arena, which consists of one or more Mechalino robots, an overhead observer camera for global localization via ArUco markers, and a ROS2-based framework for robot communication, data collection, and experiment monitoring. This setup allows robots to operate in a controlled physical environment while enabling the recording and analysis of exploration and mapping behavior.

The longer-term objective is to extend this single-robot sensor processing and mapping pipeline toward decentralized exploration and collaborative occupancy mapping with a full swarm of Mechalino robots.

## Research Questions
* How can noisy, reflection-prone IR sensor readings be converted into reliable occupancy probability estimates?
* Can a neural network learn to distinguish real-object reflections from wall/free-space reflection behavior, and how much does this improve the resulting occupancy map?
* Does incorporating local spatial neighborhood information further improve occupancy grid quality?
* (Follow-up) Can a swarm of Mechalino robots construct a consistent map of an unknown environment using decentralized exploration, and how can local observations from multiple robots be combined into a shared map representation?

## Focus Areas
* Sensor-to-occupancy-probability pipeline: reflection-aware neural classification, empirical probabilistic sensor modeling, and Bayesian sensor fusion.
* Spatial neural network for local plausibility correction of fused occupancy grid cells.
* Use of the Mechalino Arena infrastructure (observer camera, ArUco-based localization, ROS2 framework) for experiment control and data collection.
* Evaluation against ground-truth occupancy maps using classification metrics (Precision, Recall, F1, FPR) and a Balanced Brier Score.
* (Future work) Extension to decentralized multi-robot exploration and collaborative mapping.

## Contributors
* Lisa-Sophie Baier-Pichler — Bachelor thesis: *Investigation of Occupancy Maps and Their Possible Improvement with Neural Network Models*, AAU Klagenfurt, 2026.
* Supervision: Wilfried Elmenreich, Khalil Youssefi

## Dataset
Collected IR sensor / occupancy datasets from the experiments in this repository are made available at: *[link to be added]*

## Reading List
Khalil Al-rahman Youssefi and Wilfried Elmenreich, Coverage exploration of unknown obstacle-cluttered environments using a swarm of ground robots, Applied Soft Computing, Volume 185, 2025, 113964.

W. Elmenreich, Constructing dependable certainty grids from unreliable sensor data, Robotics and Autonomous Systems, 56(12):1094–1101, 2008.
