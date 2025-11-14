# R2D2robot

1-mkdir -p ros2_ws/src

2-cd ros2_ws/src

3-#thise step for install the urdf_tutorial r2d2 that i already published it (you can used it directly)

(ros2 pkg create --build-type ament_python --license Apache-2.0 urdf_tutorial_r2d2 --dependencies rclpy)

4-cd ros2_ws

5-colcon build --symlink-install --packages-select urdf_tutorial_r2d2

6-source install/setup.bash

#Launch the package

7-ros2 launch urdf_tutorial_r2d2 demo.launch.py

#Open a new terminal, the run Rviz using

8-rviz2 -d `ros2 pkg prefix urdf_tutorial_r2d2 --share`/r2d2.rviz
