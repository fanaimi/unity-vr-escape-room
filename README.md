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