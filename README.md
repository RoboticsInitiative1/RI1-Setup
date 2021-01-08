# RI1-Setup
System setup instructions for RI1 community.

## Preliminary installations
> 1. Install terminator `sudo apt install terminator`
> 2. Install Git CLI `sudo apt install git-all`
> 3. Setup [ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH) command shell 
> 3. Configure [Git user info](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration) `git config --global user.name "User Name" && git config --global user.email email@example.com`
> 4. Install [GithubCLI](https://github.com/cli/cli/blob/trunk/docs/install_linux.md) (Optional)
> 5. Install [vscode](https://code.visualstudio.com/)
> 6. Put ```export EDITOR="code --wait"``` into your `~/.zshrc` file.


## ROS2 Setup
> Source based linux(Ubuntu20.04) installation:- [ROS2](https://index.ros.org/doc/ros2/Installation/Rolling/Linux-Development-Setup/#linux-latest)

> Add ros2 source in your zsh environment `~/.zshrc` 
```shell
# add ros2 to envionment
echo "source /home/<user-name>/<ros2-directory>/install/setup.zsh" >> ~/.zshrc
```

## Gazebo11 
> Use [default installer](http://gazebosim.org/tutorials?tut=install_ubuntu#Defaultinstallation:one-liner) for gazebo11

```shell
# add gazebo 
echo "source /usr/share/gazebo/setup.sh" >> ~/.zshrc
```

## Gazebo Ros packages
```shell
cd
mkdir -p gazebo_ros/src && cd gazebo_ros/src
git clone https://github.com/ros-simulation/gazebo_ros_pkgs.git --branch ros2
cd .. && colcon build
```
> Add gazebo-ros-pkgs to your environment `~/.zshrc`
```shell
# add gazebo ros packages
echo "source /home/<user-name>/gazebo_ros/install/setup.zsh" >> ~/.zshrc
```

[comment]: <> (## Other Important Ros packages)

[comment]: <> (```shell)

[comment]: <> (mkdir -p ros2_ertra/src && cd ros2_ertra/src)

[comment]: <> (git clone https://github.com/ros-perception/perception_pcl.git)

[comment]: <> (git clone )

[comment]: <> (```)