##Introdution
----------------------

This project named Jarvis which is an inspiration from Iron Man aims at controlling your LINUX system using hand motion, gestures using Jarvis. This was part of my learning during Human Computer Interaction course.  


##Requirements
------------------------

1. Python
2. pygtk
3. python-opencv
4. xprop,xwit,xdotool


##Install and configure
-----------------------------

1. ./install
2. Configuration file exists in ~/.jarvis/config.py  
3. To Add/Edit/Remove gestures Go to Jarvis. File>settings


##Uninstall
------------------------

> ~/.jarvis/uninstall<


##Things u can do using Jarvis:
------------------------------------

1. The first thing you can do using Jarvis is control your mouse. You just need a colored object (preferably has color different from its background).

2. The second thing is that you can assign any gesture which is a combination of Left->Right, Right->Left, Top->Bottom, Bottom->Top to any command. So using this you can literally perform anything!!! The following are the things you can do by default:

Minimize current window
Maximize current window
Close current window
Go next and forward in ppt presentation
Page up and Page down
Switch window (Alt+tab)
Take screenshot
Shutdown system
Suspend system
Mute and unmute
Open Calculator, File manager, Gedit

You can practically add anything else also. All you need to know is the command which does that and the equivalent of the gesture which you want to assign in the combination of Left->Right, Right->Left, Top->Bottom, Bottom->Top.

##Running:
----------------------------------

1. Now simply open Jarvis from your Applications menu
OR
Do this:
$ cd ~/.jarvis
$ python main.py
Now click on Start Jarvis 

2. Add new gesture:
   
   2.1 Go to settings from the File menu
   2.2 Click on Add gesture from the File menu of settings 

3. Suppose say that you want to add a gesture which opens terminal.
Say the gesture you wish to give is (Left to Right)->(Right to Left)->(Top to Bottom)->(Bottom to Top)
The command corresponding to open gnome terminal is 'gnome-terminal'

4. Fill the details and save it.

##How to use?
---------------------------------

We need two different colored objects which are required to run. One the tracker and the other one is the flag!

If the flag is not exposed then the gesture is disabled and Jarvis works as a mouse controller.
When both tracker and flag are exposed the gesture begins. Perform the gesture using the tracker. Once the gesture is complete hide the flag. Jarvis then processes and analyses the gesture performed and checks for any matches from the existing database. If there is a match then it executes it!.

Customizing Tracker and Flag color:
By default the tracker is yellow color and flag is blue color.
You can change it by editing the config.py file

$ gedit ~/.jarvis/config.py

Change the min and max values of TRACKER_COLOR and GESTURE_COLOR corresponding to the HSV values of the color intended

By default these are the values:
TRACKER_COLOR={'MIN':[20,100,100],'MAX':[30,255,255]}
GESTURE_COLOR={'MIN': [108.0, 100, 10],'MAX': [118.0, 255, 255]}

Thanks for reading this much. Please improve as there is a lot of scope for improvement.

# To do
-----------------

1. Add support for more gestures.
2. Add more functionalities to control system.
3. Make this product more interactive by adding Speech-Recognition to it side by side with Gesture Control.
