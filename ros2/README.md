ref: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04
0. update existing packages
$ sudo apt update
1. let apt use packages in HTTPS
$ sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
2. Add GPG key for official Docker repo into our system
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -


ref: http://pyrasis.com/book/DockerForTheReallyImpatient/Chapter02


1. Installing docker in wsl
$ sudo apt-get update
$ sudo apt-get install docker.io
$ sudo ln -sf /usr/bin/docker.io /usr/local/bin/docker

$ docker pull ubuntu:16.04
Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?
--> means docker service not executed
// check service status
$sudo systemctl status docker
System has not been booted with systemd as init system (PID 1). Can't operate.
Failed to connect to bus: Host is down

$sudo /etc/init.d/docker start

ref: https://index.ros.org/doc/ros2/Installation/Foxy/Linux-Install-Binary/

1. Add the ROS 2 apt repository
// You will need to add the ROS 2 apt repositories to your system.
// authorize our GPG key with apt
$ sudo apt update && sudo apt install curl gnupg2 lsb-release

$ curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
gpg: can't connect to the agent: IPC connect call failed

	apt remove gpg ( follow the instructions)
	apt install gnupg1 (follow the instructions)

	Option 2.

	sudo apt remove gpg
	sudo apt-get update -y
	sudo apt-get install -y gnupg1 

$ curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
OK

// add the repository to your sources list
$sudo sh -c 'echo "deb http://packages.ros.org/ros2/ubuntu `lsb_release -cs` main" > /etc/apt/sources.list.d/ros2-latest.list'

2. Downloading ROS 2
// Update your apt repository caches after setting up the repositories.
$ sudo apt update
// Desktop Install (Recommended): ROS, RViz, demos, tutorials.
$ sudo apt install ros-foxy-desktop

3. Env setup
$ source /opt/ros/foxy/setup.bash
// help auto ccomplete (optional)
$ sudo apt install python3-argcomplete

4. ROS1 (melodic) bridge
$ sudo apt update
$ sudo apt install ros-foxy-ros1-bridge

5. TEST
// terminal 1
$ source /opt/ros/foxy/setup.bash
$ ros2 run demo_nodes_cpp talker
// terminal 2
$ source /opt/ros/foxy/setup.bash
$ ros2 run demo_nodes_py listener

