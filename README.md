# ros-env
Ros-env is a script that allows both for the user to quickly switch between
different ROS distributions and new user to quickly set up the initial
distribution. So far this have only ben tested on Archlinux.
## How to use
In your `.bashrc` write this on the bottom.
```bash
git clone https://github.com/byteofsoren/ros-env.git ~/.ros-env/
echo "source ~/.ros-env/.rosrc" > ~/.bashrc
```
To then start the ROS distribution, in the terminal write:
```bash
$ ros-env [distrobution]
```
i.e
```
$ ros-env lunar
```

## Version history
2018-04-17:001
   Fixed a bug in the script that made 2 if statmest un executible.
   Added alpa suport for debug levels by using `$DEBUG_LEVEL=5`
   Removed depricated if statments.
