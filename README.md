# ros-env
Ros-env is a script that allows both for the user to quickly switch between
different ROS distributions and new user to quickly set up the initial
distribution. So far this have only bin tested on Archlinux.
## How to use
In your `.bashrc` write this on the bottom.
```bash
$ git clone https://github.com/byteofsoren/ros-env.git ~/.ros-env/
$ echo "source ~/.ros-env/.rosrc" >> ~/.bashrc
```
To then start the ROS distribution, in the terminal write:
```bash
$ ros-env [distrobution]
```
i.e
```
$ ros-env lunar
```
But if you want to auto start lunar each time you open a terminal just add run
this:
```
$ echo "ros-env lunar" >> ~/.bashrc
```
## catshit
There are also a new function that helps with the compiler.
Normally you need to stay in `catkin_ws` to be able to compile the ROS packages.
But with `$ catshit` you can stand any ware in the system and it compiles the
ROS packages.

The function also helps with compiling certain packages.
```
$ catshit [PKG0] [PKG1] ...
```
Where PKGx is each package that you want to compile.
If PKGx is left empty `$ catkin_make` compiles all packages.


## Version history
2018-05-02:003 <br />
   Fixed a typo that made a if statement always true.
   Forced `ROS_DISTRO` environmental variable to be set to the desired distro.
   The `catshit` command was given a feature to discover if the target is a real package in `catkin_ws/src/`.
   <br />
2018-04-26:002 <br />
   Fixed a problem with python 2.7 that didn't print out its version number on
   the stdout terminal and the row to add ros-env to the bash rc.
   <br />
2018-04-17:001 <br />
   Fixed a bug in the script that made 2 if statement un executable.
   Added alpha support for debug levels by using `$DEBUG_LEVEL=5`
   Removed deprecated if statement.
