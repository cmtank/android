# LineageOS 12.1 (CM12.1)
To get started with Android/LineageOS, you'll need to get familiar with [Git](https://services.github.com/on-demand/downloads/github-git-cheat-sheet/) and [Repo](http://source.android.com/source/using-repo.html).


## Set up build environment
On the [LineageOS Wiki](https://wiki.lineageos.org), you will find additional useful information. (Just pick any device to find build instructions, but consider the device-specific statements not applicable). To build LineageOS 12.1, you need **OpenJDK 1.7**, which however is not part of the standard package repositories in a modern Linux distribution. See the Ask Ubuntu question [How do I install openjdk 7 on Ubuntu 16.04 or higher?](https://askubuntu.com/questions/761127/how-do-i-install-openjdk-7-on-ubuntu-16-04-or-higher). **Skip** the "PPA" suggestion even if it is the most upvoted and implement one of the next options.


## How to initially set up your build tree:
```Shell session
repo init -u https://github.com/cmtank/android.git -b cm-12.1 --groups=all,-notdefault,-darwin,-x86,-mips
repo sync --no-tags
```
Note: If you use a MAC to build, omit the `-darwin` in above `repo init` statement.

## How launch a cm-12.1 build:
```Shell session
make clean  
repo sync --no-tags 
source build/envsetup.sh  
brunch tank  
```

## How to contribute
Contributions (i.e. pull requests) are always welcome.
- We have an own [Thread on XDA](https://forum.xda-developers.com/t/rom-unlocked-tank-lineageos-12-1.3961110/)

