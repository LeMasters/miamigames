---
{"dg-publish":true,"permalink":"/10-inbox/ims-213-sp-2026-agenda-feb-5/","tags":["IMS213","agenda"],"created":"2026-02-05T06:26:23.551-05:00","updated":"2026-02-05T20:39:29.871-05:00"}
---


# Agenda

SO MANY THINGS TO DO!
* return to create a new material
* see how Material Instances work
* get a "goal" artifact from FAB.COM
* Put it into a dynamic Blueprint + animate
* Light it up
* Collision box <-- writing our first UE5 code (conditionals)

Make note of this:
Brick texture via freepik.com (no author given)
Sand texture via bgfons.com (no author given)
We need this data for our README

YOU ARE ETHICALLY OBLIGED TO GIVE CREDIT
I WILL PENALIZE ANY PROJECT WITHOUT CREDITS

---

STEPS
* make sure everything is working
	* create a backup for safety
* create brick wall material
* ![M_BrickWall.png](/img/user/90_Assets/M_BrickWall.png)
	* Note it isn't perfect on all planes: Some are very scrunched up! It's an approach to tiling meshes that was common in the 1990's and early 2000's. There are "newer" ways to do this, but they are more complex, and this approach is often good enough.
* Create Instanced Materials for flexibility
	* From the Material itself, choose "Create Child"
	* Name the instance "MI_BrickWall_Long"
	* Open up the instance:
		* See how simplified the interior of MI is?
	* Instances save MEMORY and CYCLES. Try to use instanced materials when you can.
	* Apply new MI_BrickWall_Long to our big 16m wall
	* Back inside MI_B... adjust our parameters and take a look
	* Adjust parameters further as necessary
* Create another instanced material, MI_BrickWall_Medium etc
	* Repeat as necessary on your own
	* Your goal: Don't use the M_Brickwall, only INSTANCES
* OK? Take a moment and save your file.
	* Good progress!
* Go to FAB and find a heart artifact (our player's goal)
* Jot down the source of the heart -- this needs to go in your README later
* Rename it and move the file to a better place
* Put that mesh into scene to see if we like it
	* Note that we won't leave it here!
	* SM_Heart is INERT, we want dynamic
	* That means we want a BLUEPRINT
* NOW create a blueprints folder
* Create BP_Heart
	* Have a look around!
	* Put BP_Heart into the BP Viewport
	* Go ahead and RESIZE IT X2
* Put the blueprint into the world
* Put it on a Plinth
* Back to BP: Add ROTATION component
	* ![BP_Heart_COMPONENTSPanel.png](/img/user/90_Assets/BP_Heart_COMPONENTSPanel.png)
	* Check on it in world
* Let's add illumination with SPOTLIGHT
	* Check on it in world
* GREAT
* Now let's fix up a collision
	* This is the first real CODE we're writing
	* Basically a CONDITIONAL
* Go to BP_Heart
	* Add collision sphere
	* Add behavior from details
	* ![BP_Heart_Collision_Capsule.png](/img/user/90_Assets/BP_Heart_Collision_Capsule.png)
	* Use PRINT STRING to reveal outcome
		* PRINT STRING is your new best friend. Commit it to memory: You will use it ALL THE TIME.
	* Test it in-world
	* Why misfiring? B/C it detects everything (Plinth)
	* So we do a safety check
		* Cast to BP_ThirdPersonCharacter
		* Then print
	* FINALLY, add COMMENTS to our code.

For Tuesday (your job)
* create as many BRICK TEXTURE INSTANCES as necessary
* create a sand floor and apply to our floor
* catch up on the rest of the work we've done to this point
* polish as necessary -- there won't be time to polish later!
	* This ALWAYS MEANS TESTING. Open things in PIE, and run around and around and around. Test every corner, every corridor. Approach the goal artifact from many angles. A broken game will break your Valentine's heart. And mine.

On Tuesday, we will:
* Add soundtrack
* Add sound effect
* Add messages (Start, End) using BP_Widgets
