# usv_dynamics_plugin

The gazebo boat simulator uses the usv dynamics plugin, which we have pulled from the px4 sitl_gazebo repo to compile it as a standalone plugin. 

## Installation

### Clone usv_dynamics_plugin

```
cd ~
git clone git@github.com:IcebergASV/usv_dynamics_plugin.git
cd usv_dynamics_plugin/
mkdir build
cd build
cmake ..
make
```

Add these lines to your bashrc:

```
# Set the plugin path so Gazebo finds our plugins
export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:$HOME/usv_dynamics_plugin/build
export SITL_GAZEBO_PATH=$HOME/usv_dynamics_plugin
```
