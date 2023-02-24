https://github.com/ros2/teleop_twist_keyboard.git
sudo apt-get install ros-foxy-joint-state-publisher-gui
sudo apt install ros-foxy-slam-toolbox
sudo apt install ros-foxy-twist-mux



run slam:
ros2 launch slam_toolbox online_async_launch.py params_file:=./src/coffee_bot/config/mapper_params_online_async.yaml use_sim_time:=true


