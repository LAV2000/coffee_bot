Install Gazebo: sudo apt install ros-humble-gazebo-ros-pkgs

Install  Xacro: sudo apt install ros-humble-xacro

https://github.com/ros2/teleop_twist_keyboard.git
sudo apt-get install ros-foxy-joint-state-publisher-gui
sudo apt install ros-foxy-slam-toolbox
sudo apt install ros-foxy-twist-mux


run robot:
ros2 launch coffee_bot launch_sim.launch.py world:=src/coffee_bot/worlds/coffee_map.world use_sim_time:=true

run rviz:
rviz2

run slam:
ros2 launch slam_toolbox online_async_launch.py params_file:=./src/coffee_bot/config/mapper_params_online_async.yaml use_sim_time:=true

run twist_mux
ros2 run twist_mux twist_mux --ros-args --params-file ./src/coffee_bot/config/twist_mux.yaml -r cmd_vel_out:=diff_cont/cmd_vel_unstamped

run navigation:
ros2 launch nav2_bringup navigation_launch.py use_sim_time:=true





