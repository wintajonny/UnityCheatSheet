# Whatever i want to write down and have to paste somewhere else

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





## Functions in Unity 
#### Start 
Executes exactly once at the beginning of the game
#### Update 
Runs once per Frame

## Scripts Provided By Unity

### PlayerController 
    using UnityEngine;

    // Controls player movement and rotation.
    public class PlayerController : MonoBehaviour
    {
        public float speed = 5.0f; // Set player's movement speed.
        public float rotationSpeed = 120.0f; // Set player's rotation speed.
    
        private Rigidbody rb; // Reference to player's Rigidbody.
    
        // Start is called before the first frame update
        private void Start()
        {
            rb = GetComponent<Rigidbody>(); // Access player's Rigidbody.
        }
    
        // Update is called once per frame
        void Update()
        {
    
        }
    
        // Handle physics-based movement and rotation.
        private void FixedUpdate()
        {
            // Move player based on vertical input.
            float moveVertical = Input.GetAxis("Vertical");
            Vector3 movement = transform.forward * moveVertical * speed * Time.fixedDeltaTime;
            rb.MovePosition(rb.position + movement);
    
            // Rotate player based on horizontal input.
            float turn = Input.GetAxis("Horizontal") * rotationSpeed * Time.fixedDeltaTime;
            Quaternion turnRotation = Quaternion.Euler(0f, turn, 0f);
            rb.MoveRotation(rb.rotation * turnRotation);
        }
    }

