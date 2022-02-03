# unity-vr-escape-room

## setting up

* install XR interaction toolkit
	* after installation import Samples > Default Input Actions
	
* for teleportation
	* select ground
	* add new layer "Teleportation"
	* apply Teleportation layer to ground
	* still on GROUND, add Component "Teleportation Area"
	
* in hierarchy:
	* new > XR > XR Origin (action based) 
	
* on XR Origin:
	* add component "Input Action Manager"
	* click plus icon under Action Assets
	* from Assets > samples > XR Interaction toolkit > v.v.v-pre-v > Default Input Actions
		* drag XRI Default Input Actions into Element 0
		
	* add component "Locomotion System"
		* drag XR Origin into Locomotion System
		
	
	* from Assets > samples > XR Interaction toolkit > v.v.v-pre-v > Default Input Actions
		* drag XRI Default SNAP TURN into XR Origin inspector to add it as a component
		
	* drag LOCOMOTION SYSTEM component under SNAP TURN PROVIDER > system	
	
* edit > project settings > XR plugin Managment	=> Install XR plugin Managment > check OCULUS

* under XR ORIGIN > inspector > add component > TELEPORTATION PROVIDER 
	* also drag Locomotion system under Teleportation provider > system
	
* ADD actions into LEFT and RIGHT Controller
	* from Assets > samples > XR Interaction toolkit > v.v.v-pre-v > Default Input Actions
		* drag XRI Default Right Controller under XR ORIGIN > Camera Offset > RightHand Controller (inspector)
		* do the same for left controller
		
* Rename XR ORIGIN > Camera Offset > RightHand Controller
	* as RightHand Teleportation Controller
	* do the same for left controller
	
* in hierarchy, under Camera offset: CREATE > new > XR > DIRECT INTERACTOR (Action Based)
	* rename it as "RightHandGrabController"
	* from Assets > samples > XR Interaction toolkit > v.v.v-pre-v > Default Input Actions
		* drag XRI Default Right Controller under XR ORIGIN > Camera Offset > RightHandGrab Controller (inspector)
	* in hierarchy, drag RightHand Teleportation controller as A CHILD OF RightHandGrabController	
		* into RightHand Teleportation controller (inspector) > XR Controller, UNCHECK:
			* Enable Input Tracking
			* Position Action 
			* Rotation Action
	* DO THE SAME FOR LEFT CONTROLLER		
	
* Drag XR Origin from hierarchy into PREFABS folder	