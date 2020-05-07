# Xbot_with_Vins-Mono
Xbot is a good open-source robot package, it has many state-of-the-art algorithms about SLAM and Navigation. 

Simtaneously，Vins-Mono is also a good open-source MONO-SLAM project，out of interest，I integrate them by replacing original SLAM algorithm
of Xbot with vins-mono.

Just by five steps， then you can run：

0. Git clone vins-mono, and cmake.
1. replace the original one of vins-mono with given euroc_config.yaml， it has configured parameters about extrinsic and intrinsic parameters.
2. roslaunch robot_sim_demo robot_spawn.launch
3. rosrun robot_sim_demo robot_keyboard_teleop.py
4. roslaunch vins_estimator euroc.launch
5. roslaunch vins_estimator vins_rviz.launch

However, there are some problems while running. It might running against normal trajectory. The main reason is that the simulating environment has many walls and little good features in MONO camera. I think the more good features there are, the higher quality it will have, so you can try altering the environment.
