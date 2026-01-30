---
{"dg-publish":true,"permalink":"/10-inbox/ims-213-sp-2026-unreal-intro/","tags":["IMS213","tutorial"],"created":"2026-01-30T15:37:11.009-05:00","updated":"2026-01-30T18:41:27.461-05:00"}
---


## Agenda

Unreal is a challenging environment: Our goal is to begin to master the environment.

This does not mean that you'll produce masterpieces from WITHIN the environment. It means that you'll begin to understand how portions of this environment work together.

Today will be a lot for some folks. That's OK. We'll proceed slowly; grab my attention if you're falling behind right away, and we'll help you get caught up.

PLEASE PAY ATTENTION and don't wander off doing your own thing unless you already know what is happening. If you know what you're doing, take this time to build and refine your skills but don't distract people. OR if you like, hang out and help people as they run into trouble.

Everything we'll do in these tutorials is carefully sequenced, one new thing after another, each new thing depends on you having done the last successfully. So if you head off in your own direction and get lost, and then need help, that's OK, we'll get you back into the fold, but please stick with us so we don't have to backtrack too much.

But this is complicated, and people are going to get lost. When you realize something isn't going according to plan just let us know and we'll get you caught up.

---

One thing to encourage (although it is new to me): Experiment with the Developer AI that Epic has in beta. Since it is trained on the documentation, it could be really useful.

https://dev.epicgames.com/community/assistant/unreal-engine

From the LAUNCHER
My suggestions....
Go into SETTINGS
* run in background
X when PC starts
* hide game library
X Enable cloud saves

The LIBRARY tab is where you'll find the projects you're building.

They get HUGE; even a small experiment can become 5GB in size quickly, so you need to keep track of them.

At the bottom of Library tab is your QUIXEL BRIDGE and FAB library. We'll worry about those later, but they'll eventually be VERY IMPORTANT.

### Versions

You can also see the versions of unreal you have installed.

They get updated frequently. You may have 5.7.1 or 5.7.2. Minor point updates are generally bug fixes. FOR THE MOST PART, DO NOT UPDATE UNREAL UNLESS YOU NEED TO, especially in the middle of a project in the middle of the semester.

You can launch from the PROJECT itself or from the LAUNCH button. Let's use the Launch button.

LOTS OF STUFF, most of it is very new. TRY IT! Experiment! That's the only way you'll really learn.

For us:
Click NEW PROJECT on LEFT.
Click THIRD PERSON.

### Where Things Are Stored

NOW:

Let's look at where this stuff is stored.

Project LOCATION at bottom.
Open that up, then create a shortcut and put it on your desktop.

We'll come back

Give proj meaningful name. No spaces, always letter first, always short. I go with dates in my names

IMS213FirstDemoJan29
Create, it'll compile as it launches Unreal Engine 5.7

### Customizing Details in the Viewport

This is the viewport.
These are Viewport Buttons.

Start with SCALABILITY button
REDUCE IT to MIDDLE (or even LOW). Makes life easier.
Now the button is orange to alert you.

### Camera Bookmarks

Start by storing camera position (VERY IMPORTANT)
CTRL1 you'll see a note
VeRY EASY TO GET LOST in 3D, you NEED these camera bookmarks.

### Moving Around

Move around in VIEWPORT.
RIGHT MOUSE BUTTON
MOVE MOUSE
Look around

#### Back to Camera 1

Now jump back to CAM1 pos
hit 1 on keyboard

### More Movement

NOW WITHOUT moving mouse
RIGHT button + WASD
RIGHT button + Q down
RIGHT button + E up

#### Back to Cam 1

NOW go back to 1

### Complex Movement

NOW, like this is a 1st person shooter,
RIGHT BUTTON + mouse move + WASD

### Give This a Try

Now go to hover above each corner of playground face center and set a camera bookmark. 2,3,4,and 5.

Don't like where you're at, just reposition and CTRL-n again overwrites.

THAT'S a LOT of what you'll do all semester long.

NOW let's deal with the STUFF we have in front of us.

These things, grey, green, are what we call STATIC MESHES. 95% of the time this semester, you will be dealing with STATIC MESHES. Some systems call them PRIMS or PRIMITIVES. They're basic shapes which makes them CHEAP to create and render.

Let's look at one closely.



Now select the cylinder in center
Yellow outline means it is selected.

Look in your outliner to see it selected
Look in DETAILS to see its details.
Press F to FOCUS in on it.
Use mouse wheel to zoom in out
Get a bit away from it.
hold ALT + LEFT mouse button + Mouse left-right to orbit. Reposition if necessary. Click F again, then orbit.

Go back to 1, pick something, zoom in out orbit orbit it.

Go back to 3 pick something zoom in out orbit.


OK

Let's use the outliner
FIRST 
Things are often going to get messed up
OK
SO bring the outliner panel out, make it big
That can be useful
Sometimes you may even want to get rid of it, or might do it accidentally

Close Outliner, stretch details panel
OK
Go to WINDOW > Load Layout > DEFAULT
Remember that, you'll NEED IT.


From cam pos 1
In outliner
Close up the LIGHTING 
Under PLAYGROUND
double click on FLOOR
this is the same as FOCUSING
Orbit around the floor

Double click on a few other things
see how camera snaps to them?
Orbit

Now back to double click on FLOOR

Let's rename it to MYFLOOR
naming things and ordering them in the OUTLINER REALLY IMPORTANT
To RENAME: either RightClick > EDIT > RENAME or F2 or select it then click again

now go back to 1
Pick cylinder in center
See it in OUTLINER
Now delete it
Gone from VIEWPORT
Gone from Outliner
Gone from your game

Did you do that accidentally,
CTRL - Z to undo, will bring it back.

But delete it again,
delete everything in the center
If you accidentally delete floor,
Bring it back.

so everything from the middle is gone
GREAT
Let's SAVE the project

Look on tab
LvL_ThirdPerson ASTERISK
An asterisk next to something always means UNSAVED
But LvL_ThirdPerson wasn't the name we assigned our PROJECT.
Project name is on upper right hand side
LEVEL name, is on the TAB

Your games will typically have several levels, this is just the default

SO LET'S SAVE EVERYTHING SAVE ALL
Quit UNREAL.
Go to PROJECTS
Open that directory
When things break, we'll often have to come back here to fix things.
.uproject is MAIN FILE
SAVED folder is where your screenshots will go
INTERMEDIATE and DATACACHE are processing files and are generally disposable
CONFIG is where your project config files are stored
CONTENT is the MAIN MAGIC FOLDER
It is where your assets are stored
It is shaped by you, but as we go, we'll talk about the standards that you need to adhere to.
Open content, choose Third Person
There is Lvl_ThirdPerson.umap
That is the level we were editing.

NOW:
We can see these files, rename them, delete them, add files, etc.

For the most part, don't do that. Leave these files alone. ONLY MAKE CHANGES from within UNREAL's file browser, not from within YOUR file browser, OK?

But let's do ONE THING before we go.

Go up to the project level and right click on project file and create a zip. Rename it BACKUP DAY ONE.zip. Now if you get in trouble, you have this perfect copy of your project that you can come back to.

Go back to launcher, open project by double-clicking it.

Everything just like you left it
Check camera positions

Let's actually make something now.
PLACE ACTORS
actors are things in your level; they are like objects
Place a SHAPE > CUBE
FOCUS in on it
Orbit it
See the GIZMO in the CENTER
That is how we TRANSFORM the INSTANCE of the STATIC MESH
MOVE IT AROUND
UP DOWN FORWARD BACK
Orbit around it a bit
Move it around some more

See how location data changes on right
type in location data
or put mouse in window LMB mouse move

Reset it to 0,0,0 with tiny back arrow icon
TWO OTHER TRANSFORMS
Upper lefthand of viewport buttons
CHOOSE ROTATE
Experiment with rotation
See how the numbers change
Reset it
NOW
CHOOSE SCALE, the last TRANSFORM
Scale it up and down
Can always CTRLZ
OR reset in the details panel

GRAB the MIDDLE of the SCALE GIZMO
in order to scale things uniformly
reset it

LOCATION GIZMO
DRAG Cube above floor
Now press END to seat it perfectly on floor
It aligns the faces
On Mac FN RIGHT ARROW

Now lets create duplicates and place them
To keep track tho let's rename the cube
Go to the OUTLINER
Rename (F2) to SM_MyCube
ALWAYS ALWAYS ALWAYS SM_name
SM stands for static mesh
You will have hundreds and hundreds of different actors in your outliner YOU NEED TO BE ABLE TO LOOK AT THEM AND KNOW IN AN INSTANT, AH, that's a mesh, that's a blueprint, that's a widget, that's a light. YOU MUST ADOPT THIS HABIT.


Select myCube
Select move gizmo
HOLD ALT and drag along axis (mac OPT)
Release
Select again
HOLD ALT and drag
So create four cubes next to each other

Now MULTI SELECT holding SHIFT while you choose them

Then with all selected, go to gizmo, ALT and drag

Now add a sphere
Roughly place on top of cube
so it is higher but generally aligned
rename it to MYSPHERE so it doesn't get lost

OK.

Last thing.

the viewport is a miraculous place -- if you've used cad software or blender this will be very familiar.

Go to viewports view button on upper righthand of viewport click it

In outliner double-click on sm_mysphere
all the windows will focus on it.
TOP FRONT RIGHT PERSPECTIVE
Hover over window you can MOUSEWHEEL zoom IN OUT
RIGHT CLICK in window you can move around
click on sphere (hard to do).
BUT
Using the different window points of view
try to get your sphere exactly over top of one of the cubes
work in one window at a time
THIS CAN BE HARD TO FIGURE OUT AT FIRST.
Then use ALT-DRAG to duplicate sphere
Put it over top of another cube.
When we're done, go back to VIEWPORT WINDOWS button and maximize our PERSPECTIVE VIEWPORT view.

They should be almost perfectly placed!

Let's grab screenshot
First position your camera at perfect angle
Save it to a bookmark

Go back to PERFORMANCE SCALABILITY BUTTON
(ORANGE probably)
Click to set it to EPIC or CINEMATIC
That's important here.
go to our COMMAND LINE BOX

type HIGHRESSHOT 2
Make sure you get both S's
Space between word and 2
It'll take a moment, you should see notifying popups

NOW click on the output log button
Scroll to bottom,
You'll see all the stuff happening in background
It will tell you it saved

(This data is ugly but you'll have to get used to it!)

Now minimize UE
open up our project DIR
Go to project, then to SAVED
Then to SCREENSHOTS
It should be in there somewhere.

Great
Go back to UE
Change the scalability setting back to MEDIUM
Save all
close out 
You are done

FOR TUESDAY
Using the shapes and techniques we've talked about
BUILD SOMETHING
Some MODERN ART
Use at least a dozen different static meshes
