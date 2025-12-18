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


## Scripts Provided By Unity
using UnityEngine;

### DoorOpener with animation    
    public class DoorOpener : MonoBehaviour
    {
       private Animator doorAnimator;
    
       void Start()
       {
           // Get the Animator component attached to the same GameObject as this script
           doorAnimator = GetComponent<Animator>();
       }
    
       private void OnTriggerEnter(Collider other)
       {
           // Check if the object entering the trigger is the player (or another specified object)
           if (other.CompareTag("Player")) // Make sure the player GameObject has the tag "Player"
           {
               if (doorAnimator != null)
               {
                   // Trigger the Door_Open animation
                   doorAnimator.SetTrigger("Door_Open");
               }
           }
       }
    }




# 2D Development
Use the 2D Button at the top-rigth of the Scene View for optimized 2D Development.

3D Models are "called" __2D Sprites__
Gracity Scale 0 -> makes the player stay on Screen and not fall through the bottom

## Game View Aspect
Can be changed while in Play mode (16:9, 16:10, ...)

## Order in Layer
Sprite Renderer Component -> Order in Layer on Same Level as Player if its an obstacle

Objects slide like on Ice : Linear Damping 5-10
Objects rotate on the Spot: Angular Damping 5-10

## Sprite Editor
Used for animating 2D Assets 
-> Sprite Mode Multiple 















