## OpenSpace-VisLink
#### If at the Bell, all clone and setup steps have been done already. Continue to 'Run VisLink'. Unity has already been installed.
<br>

Getting up and running from scratch:
#### Clone this repo
In Git Bash:
```
cd <desired_repo_location>
git clone --recursive https://github.com/OpenSpace-VisLink/OpenSpace.git
```
#### Set up with Cmake
In Git Bash:
```
cd OpenSpace
mkdir build
cd build
cmake-gui ..
```
In the CMake window
- Click Configure 
- Select Visual Studio 2017 and x64 and confirm
- Click 'Grouped' at the top of the CMake window
- Check mark OPENSPACE --> OPENSPACE_MODULE_VISLINK
- Click Configure again
- Click Generate
- Click OpenProject  

Comment out STB_IMAGE_IMPLEMENTATION:
```
OpenSpace/apps/OpenSpace/ext/sgct/src/sgct/image.cpp, line 29
```
Set the 'OpenSpace' module as your startup project and build.
#### Clone VisLinkUnityTest
In Git Bash:
```
cd <desired_repo_location>
git clone https://github.com/OpenSpace-VisLink/VisLinkUnityTest.git
```
#### Run VisLink
Run OpenSpace with the command line arguments:
```
-f <path_to>/vislink.cfg
```
This will automatically load the 'bell.xml' file, but you can change that in the vislink.cfg file.   
Next, open the cloned 'VisLinkUnityTest' project. You will need to install a recent Unity version (tested with 2019.4.xxf1).   
Once OpenSpace is fully loaded (showing planets), click 'Play' in Unity.   
