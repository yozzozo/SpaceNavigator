#SpaceNavigator
SpaceNavigator driver for Unity3D

This driver lets you fly around your scene and allows you to move stuff around.  
You can also use it at runtime via scripting.  

The default mode is **Fly** mode and when you're flying around, this driver always keeps your horizon horizontal.  
So you don't have to worry about ending up upside down, just go where you want and get some work done.  
To move stuff around, you can use 2 modes: Telekinesis and GrabMove.  
In **Telekinesis** mode, you can move the stuff you selected with the SpaceNavigator, while your camera stays put.  
(this mode can be operated in Camera-, World-, Parent- and Local coordinates)  
In **GrabMove** mode the stuff will be linked to your camera so you can take it with you and position it where you want.  
Translation can be snapped to a grid and rotation can be angle-snapped.  

##Platform support
The driver supports Unity 3 and 4, both Indie and Pro versions.  
At the moment it is windows-only, but the code is right [here](https://github.com/PatHightree/SpaceNavigator). 
Who knows, somebody with a mac might just step in and code the mac implementation. 
I've prepared the code to make this as painless as possible, just subclass the SpaceNavigator class.  

##The goods
- [SpaceNavigator + DemoScenes.unitypackage](http://bit.ly/1gslAEv) import this package into an empty project and play around.
  - Fly around.unity: Fly around with a sphere while knocking over some cubes.
  - Folow curve.unity: Make your torus follow the curve, but don't touch it!
- [SpaceNavigator.unitypackage](http://bit.ly/1cGZMCA) import this package into your project and get to work.
- Source code on [Github](https://github.com/PatHightree/SpaceNavigator)

##Known bugs and limitations
- No mac support
- Grab Mode only works in the camera coordinate system (sorry, I couldn't get my head around the quaternion math of manipulating in one coordinate system while constraining in another)

##Installation
- Install [3DConnexion driver](http://www.3dconnexion.com/service/drivers.html) and make sure it is running
- Import the unitypackage into your project
- Open the SpaceNavigator window from the pull-down menu Window/SpaceNavigator (or hit Alt-S)
- Fly away

### Pro tip
Copy the SpaceNavigator.unitypackage to *Unity/Editor/Standard Packages* directory.  
- SpaceNavigator is added to the packages list in the project creation in wizard.  
- Easy to add later by right-clicking in *Project View* and choosing *Import Package*.  

Credits
-------
- Big thanks to Dave Buchhoffer (@vsaitoo) for testing and development feedback
- Quaternion math by Minahito
  http://sunday-lab.blogspot.nl/2008/04/get-pitch-yaw-roll-from-quaternion.html