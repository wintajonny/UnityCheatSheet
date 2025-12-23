# Whatever i want to write down and have to paste somewhere else


## ShortCuts
in Hierarchy Window:
### F2 - Rename

## Character Controller Unity
Instead of Rigidbody on Player Character

## IsTrigger
GameObject acts like a 'cloud'
- Collider Component with IsTrigger acts as a trigger instead of a physical collider - will no longer have a solid barrier - but can still detect entry by the player or another GameObject


#Programming
Public variables are changeable in the Inspector Window of Unity
Using statements link the Script to the necessary libraries
- so when you enter something like 'Rigidbody' the script knows what that means

Monobehaviour is a required class for all GameObjects in Unity.
- This bit of code is what allows you to add your script as a component to a GameObject.



## Snapping 
with Ctrl - Moves on the Grid

# Deleting a GameObject
Destroy(gameObject)

# Instantiating
means creating a copy of an object during runtime

        Instantiate(prefab /*onCollectEffect*/ , transform.position, transform.rotation);

# Visual Effects (VFX)
You can use __Particle Systems__ to simulate complex visual effects. (e.g. Fire, smoke, bursts of sparks)



## Functions in Unity 
#### Start 
Executes exactly once at the beginning of the game
#### Update 
Runs once per Frame
### OnTriggerEnter
Runs when a GameObject with a Rigidbody component collides with another (that has isTrigger?)

# Publishing

## Build number
File > Build Profiles (Ctrl + Shift + B)
Scene Lift on the left (Platforms Panel) -> Drag and Drop Scenes in there

## Player Settings
Set Company Name and Product Name
Select Default Icon

## Publish to WebGL
Build Profiles > Platforms: Web > Switch Platform
Build






