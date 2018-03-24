# hector_quadrotor_robot
Start with Hector Quadrotor robot
			HECTOR_QUADROTOR
		      --------------------
mkdir ~/catkin_mv
cd ~/catkin_mv
wstool init src https://raw.github.com/tu-darmstadt-ros-pkg/hector_quadrotor/kinetic-devel/tutorials.rosinstall
cd src
git clone https://github.com/ros-simulation/gazebo_ros_pkgs.git
sudo apt-get install libgazebo7 
cd ..
catkin_make
source devel/setup.bash
roslaunch hector_quadrotor_demo outdoor_flight_gazebo.launch
-- Novo terminal --
cd catkin_mv
source devel/setup.bash
cd src/hector_quadrotor/hector_quadrotor_teleop/launch
roslaunch hector_quadrotor_teleop logitech_gamepad.launch
