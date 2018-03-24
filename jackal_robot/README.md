# jackal_robot

			JACKAL ROBOT
		     -----------------
cd ~/catkin_mv/src
git clone https://github.com/jackal/jackal.git
git clone https://github.com/jackal/jackal_desktop.git
git clone https://github.com/jackal/jackal_simulator.git
git clone https://github.com/jackal/jackal_robot.git
source devel/setup.bash
rosdep install jackal_control
rosdep install jackal_description
rosdep install jackal_navigation
sudo apt-get install ros-kinetic-ros-control ros-kinetic-ros-controllers
sudo apt-get install ros-kinetic-gazebo-ros-control
