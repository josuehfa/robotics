# Jackal Simulator Install
> Instalação do simulador do Jackal

Jackal simulator was not installed by default on *ROS Kinetic*. To use it, you must install dependencies and compile git code.
> O Jackal não é instalado automaticamente no ROS Kinetic. Para usá-lo você deverar instalar as dependências e compilar o código do git. 


### Install dependencies :
> Instalando dependências
 
This is *manual* way to install necessary packages :
> Esta é a maneira manual de instalar os pacotes necessários:

```
sudo apt-get install ros-kinetic-robot-localization ros-kinetic-controller-manager ros-kinetic-joint-state-controller ros-kinetic-diff-drive-controller ros-kinetic-gazebo-ros ros-kinetic-gazebo-ros-control ros-kinetic-gazebo-plugins ros-kinetic-lms1xx ros-kinetic-pointgrey-camera-description ros-kinetic-roslint ros-kinetic-amcl ros-kinetic-gmapping ros-kinetic-map-server ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro ros-kinetic-message-runtime ros-kinetic-topic-tools ros-kinetic-teleop-twist-joy ros-kinetic-teleop-twist-keyboard
```
If you want to use `rosdep` and install all dependencies (for example for doc generation etc), skip this step.
> Se você preferir usar o *rosdep* e instalar todas as dependencias, execute os comandos abaixo:
 
`
rosdep install jackal_control
`

`
rosdep install jackal_description
`

`
rosdep install jackal_navigation
`

`
sudo apt-get install ros-kinetic-ros-control ros-kinetic-ros-controllers ros-kinetic-gazebo-ros-control
`


### Create a workspace 
> Criando espaço de trabalho
 
`
mkdir -p jackal_robot/src
`

`cd jackal_robot/src
`

`catkin_init_workspace
`
### Clone sources
> Clonando os codigos do git

`
git clone https://github.com/jackal/jackal.git
`

`
git clone https://github.com/jackal/jackal_simulator.git
`

`
git clone https://github.com/jackal/jackal_desktop.git
`

`
git clone https://github.com/jackal/jackal_robot.git
`

`
git clone https://github.com/ros-visualization/interactive_marker_twist_server.git
`

*Install dependencies with* `rosdep` : 
> Instalando dependências com o *rosdep* que possam ter surgido.

`
cd jackal_robot
`

` 
rosdep install --from-paths . --ignore-src --rosdistro=kinetic
`
### Build and Environment setup
>Construindo e ambientando as variáveis do ROS

`
cd jackal_robot
`

`
catkin_make
`

`
source devel/setup.bash
`
### Start simulation : 
> Iniciando a simulação

In terminal 1 :
> No primeiro terminal: 

```
roslaunch jackal_gazebo jackal_world.launch config:=front_laser
```
In terminal 2 :
> No segundo terminal:

```
roslaunch jackal_viz view_robot.launch
```
and follow the [tutorial](http://docs.ros.org/indigo/api/jackal_tutorials/html/simulation.html)
> e, continue executando esse [tutorial](http://docs.ros.org/indigo/api/jackal_tutorials/html/simulation.html).

### Control:
> Controle:

To teleoperate using a joystick:
> Para a teleoperação usando um joystick:

`
roslaunch teleop_twist_joy teleop.launch joy_dev:=/dev/input/js1
`

To teleoperate using the keyboard:
> Para a teleoperação usando o teclado:

`
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
`


----

You can follow that tutorial in the [*Clearpath Robotics website*](http://www.clearpathrobotics.com/assets/guides/jackal).
> Você pode seguir esse tutorial no [*website da Clearpath Robotics*](http://www.clearpathrobotics.com/assets/guides/jackal).

----
