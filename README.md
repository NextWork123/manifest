<div align="center">
<hr>
<img src="https://github.com/SpiceOS/xda_template/blob/12.1/Banner/header.png?raw=true">
<br>
<br>
<strong><i>Just a spiced up AOSP ROM ;)</i></strong>
<br>
<br>
<hr>
</div>

Credits
===========
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**CrDroid**](https://github.com/crdroidandroid)
 * [**PixysOS**](https://github.com/PixysOS)
 * [**Superior OS**](https://github.com/SuperiorOS)
 * [**Arrow OS**](https://github.com/ArrowOS)

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](https://source.android.com/source/using-repo.html).

1.Set up your environment

    sudo apt-get install git-core
    git clone https://github.com/akhilnarang/scripts
    cd scripts
    bash setup/android_build_env.sh

2.Then run these commands to get git all working:

     git config --global user.email "you@example.com"
     git config --global user.name "Your Name"

3.Then Create a folder for SpiceOS and open it

    mkdir spiceos
    cd spiceos

4.To initialize your local repository using the SpiceOS-Beta trees, use a command like this:

    repo init -u git@github.com:SpiceOS/manifest.git -b 13 --depth=1

5.Then to sync up:

    repo sync -c -f --force-sync

OR, for those with limited bandwidth/storage:

    repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

6.To start the build once everything is ready , Run to prepare our devices list

    . build/envsetup.sh

7.Now build

    lunch spiceos_device_userdebug
    make bacon
