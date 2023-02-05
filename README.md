# FPS Equipment
A example module that implements various FPS-style weapons. Implements first-person specific viewmodels and animations with integrations for more generic
third person animations on whatever player model. It also implements the datablocks for the ShapeImages as well as accompianing scripts to implement shooting
and other weapon states. 
 
# Usage and Instructions
### Installation
Copy entire FPSEquipment folder into the Torque3D project's data/ folder, restart the project if it's running and it'll be integrated.

### ShapeBaseImage/Data
These datablocks are the primary driver for the weapons/usable equipment. They contain the fields for setting up the state machine that drives the equipment behavior.
They are mounted to a Shapebase-derived object class like Player or Vehicle. 
The state machine not only provides the rules for how to transition between states, such as noAmmo, or onFire, but also describes what animation to play, sound to make, particles to emit, and any script functions.
Additionally sets the first and third person models for use when the item is mounted and active as well as defining a prefix string. The prefix string is used to integrate back to the mounted object(such as a player) to tell it what animation to play when a state sequence playes. This allows the image's state, eg the Reload state, to not only play the first person model animation, but inform the player to also play a matching third person animation.
