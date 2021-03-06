# DDK_create_custom_Linux-based_systems(Yocto Project)
 Use the Yocto Project (YP) to create custom Linux-based systems.

# Download the source files of the buildroot
ls  <br/>
cd Desktop/  <br/>
sudo apt install git <br/>
git clone -b fido git://git.yoctoproject.org/poky.git <br/>
cd poky/ <br/>
source oe-init-build-env &nbsp;

![image](https://user-images.githubusercontent.com/67073582/155920483-a3741063-07c1-4afb-97b2-af130b959274.png) &nbsp;

![image](https://user-images.githubusercontent.com/67073582/155920531-6a3c804e-bd81-4397-b5c6-7edb60da357a.png) &nbsp;

# Build images
bitbake core-image-minimal <br/>

WARNING: Host distribution "Ubuntu-20.04" has not been validated with this version of the build system; you may possibly experience unexpected failures. It is recommended that you use a tested distribution. <br/>

|       |   ^~~~~ <br/>
| make[3]: *** [Makefile:1842: freadahead.o] Error 1 <br/>
| make[3]: *** Waiting for unfinished jobs.... <br/>

## Recommended distributions
Ubuntu 16.04 (LTS) <br/>
Ubuntu 18.04 (LTS) <br/>
Ubuntu 19.04 &nbsp;

# Run on QEMU
runqemu qemuarm &nbsp;

# How to add layer?
1.Download the layer <br/>
http://layers.openembedded.org/layerindex/branch/master/layers/ <br/>
 
![image](https://user-images.githubusercontent.com/67073582/155921078-0992ef3d-b0f3-45cf-88b9-e4422a8676fe.png) &nbsp;

2.Add the layer (BBLAYERS ?=) <br/>
/home/parallels/Desktop/poky/build/conf/ bblayers.conf <br/>
 
![image](https://user-images.githubusercontent.com/67073582/155921328-b8101e2f-60fc-4845-9590-4b15edc11a44.png) &nbsp;

3.Test the layer <br/>
bitbake-layers show-layers &nbsp;


