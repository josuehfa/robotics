For all documents in that repository you'll need a ROS Kinetic installed.
> Para todos os documentos nesse repositório, você precisará do ROS Kinetic instalado.
----
## Ubuntu install of ROS Kinetic
> Instalação do ROS Kinetic no Ubuntu

### Installation
> Instalação

ROS Kinetic  **ONLY**  supports Wily (Ubuntu 15.10), Xenial (Ubuntu 16.04) and Jessie (Debian 8) for debian packages.
> ROS Kinetic suporta SOMENTE as seguintes versões: Wily (Ubuntu 15.10), Xenial (Ubuntu 16.04) e Jessie (Debian 8) para pacotes debian.

#### Setup your sources.list
> Configure sua "sources.list"

Setup your computer to accept software from packages.ros.org.
> Configure seu computador para aceitar softwares de packages.ros.org.

```
  'sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
#### Set up your keys
> Configure suas chaves
```
 sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
```    
#### Installation of ROS Kinetic
> Instalação do ROS Kinetic

First, make sure your Debian package index is up-to-date:
> Inicialmente, tenha certeza que o índice de seus pacotes Debian está atualizado: 
```
sudo apt-get update
 ``` 
There are many different libraries and tools in ROS. We provided four default configurations to get you started. You can also install ROS packages individually.
> Existem muitas bibliotecas e ferramentos no ROS. Nos providenciamos quatro configurações padrões para você começar. Além disso, você pode instalar pacotes ROS individualmente.

-   ***Desktop-Full Install: (Recommended)***  : ROS,  [rqt](http://wiki.ros.org/rqt),  [rviz](http://wiki.ros.org/rviz), robot-generic libraries, 2D/3D simulators, navigation and 2D/3D perception.

 `
sudo apt-get install ros-kinetic-desktop-full
`        

   > ***Instalação Completa no Computador:(Recomendada):*** ROS, [rqt](http://wiki.ros.org/rqt), [rviz](http://wiki.ros.org/rviz), bibliotecas genericas de robôs, simuladores 2D/3D, navegação e percepção 2D/3D.    
   
   - ***Desktop Install:*** ROS,  [rqt](http://wiki.ros.org/rqt),  [rviz](http://wiki.ros.org/rviz), and robot-generic libraries
   
    `
       sudo apt-get install ros-kinetic-desktop
    `
    
   > ***Instalação no Computador:*** ROS, [rqt](http://wiki.ros.org/rqt), [rviz](http://wiki.ros.org/rviz) e bibliotecas genericas de robôs.
        
    
 - ***ROS-Base: (Bare Bones)***  ROS package, build, and communication libraries. No GUI tools.
 
  `	
sudo apt-get install ros-kinetic-ros-base
    `    
      > ***Base ROS:(Esqueleto do sistema):*** Pacote ROS, construtor e bibliotecas de comunicação. Sem ferramentas GUI.
    
  
  - ***Individual Package:***  You can also install a specific ROS package (replace underscores with dashes of the package name):
  
    `
      sudo apt-get install ros-kinetic-<NAME-OF-PACKAGE>
      `  
      
	> ***Pacotes Individuais:*** Além disso, você pode instalar pacores especificos do ROS (Substitua o < NAME-OF-PACKAGE > pelo nome do pacote a ser instalado.
	
	To find available packages, use:
	
`
	apt-cache search ros-kinetic
`
      > Para achar pacotes disponiveis, use:
#### Initialize rosdep
> Inicializando o rosdep

Before you can use ROS, you will need to initialize  rosdep.  rosdep  enables you to easily install system dependencies for source you want to compile and is required to run some core components in ROS.
> Antes de você poder usar o ROS, necessitará de inicializar o rosdep. Rosdep permite instalar facilmente as dependências do sistema para o código-fonte que deseja compilar, ele é necessário para executar alguns dos principais componentes do ROS.

`
sudo rosdep init
`

`
rosdep update
`

#### Environment setup
> Configuração de ambiente
 
It's convenient if the ROS environment variables are automatically added to your bash session every time a new shell is launched:
> É conveniente se as variaveis de ambiente do ROS são automaticamente adicionadas na sua seção bash toda vez que você inicializa um novo terminal.

` 
echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
`

`
source ~/.bashrc
`

If you just want to change the environment of your current shell, instead of the above you can type:
>Se você quiser somente mudar o ambiente do seu terminal atual, digite apenas:

```
source /opt/ros/kinetic/setup.bash
```
#### Dependencies for building packages
> Dependências para contruir pacotes

Up to now you have installed what you need to run the core ROS packages. To create and manage your own ROS workspaces, there are various tools and requirements that are distributed separately. For example,  [rosinstall](http://wiki.ros.org/rosinstall)  is a frequently used command-line tool that enables you to easily download many source trees for ROS packages with one command.
> Agora como você já instalou o que precisa pra rodar os pacotes ROS. Para criar e gerir o seu proprio espaço de trabalho ROS, existe muitas ferramentas e requisitos que são distribuídos separadamente. Por exemplo,  [rosinstall](http://wiki.ros.org/rosinstall), que é uma ferramente de linha de comando fequentemente usada para permitir downloads de muitas árvores-raiz de pacotes ROS com apenas um comando.

To install this tool and other dependencies for building ROS packages, run:
> Para instalar essa ferramenta e outras dependências para a contrução de pacotes ROS, rode:

```
  sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential
```
### Tutorials

Now, to test your installation, please proceed to the  [ROS Tutorials](http://wiki.ros.org/ROS/Tutorials).
> Agora, para testar sua instalação, por favor, realize os [Tutoriais do ROS](http://wiki.ros.org/ROS/Tutorials).


You can see that tutorial of installation in the [ROS web site](http://wiki.ros.org/kinetic/Installation/Ubuntu).
>Você pode vê esse tutorial de instalação no [site do ROS](http://wiki.ros.org/kinetic/Installation/Ubuntu).
