# Ex.No: 3  Basic movements in Unity 
                                                                         
### REGISTER NUMBER : 212225240085
### AIM: 
 To learn the basic movements translation,scaling and rotation of game objects through code.
### Procedure:
1. Setup the Scene
2. Open Unity and create a 3D Scene.
3. Add three objects:Cube → Rename to Object1 (for movement),Sphere → Rename to Object2 (for rotation).Capsule → Rename to Object3 (for scaling).
4. Add the Script,Create a C# Script → Name it TransformOperations.cs.
5. Write the code for translation,scaling and rotation,save and close the script
6. Save the script
7. Select any empty GameObject (or create one: GameObject → Create Empty).
8. Attach the TransformOperations script to it.
9. In the Inspector, assign Object1 → Drag the Cube,Object2 → Drag the Sphere.Object3 → Drag the Capsule.
10. Run the Scene Press Play ▶️ in Unity
11. Stop the program.
### Program 
```
using UnityEngine;

public class TransformOperations : MonoBehaviour
{
    public Transform object1;
    public Transform object2;
    public Transform object3;

    public float moveSpeed = 2f;
    public float rotateSpeed = 50f;
    public float scaleSpeed = 0.5f;

    void Update()
    {
        // Translation
        if (object1 != null)
        {
            object1.Translate(
                Vector3.right * moveSpeed * Time.deltaTime,
                Space.World
            );
        }

        // Rotation
        if (object2 != null)
        {
            object2.Rotate(
                Vector3.up * rotateSpeed * Time.deltaTime
            );
        }

        // Scaling
        if (object3 != null)
        {
            float scaleChange =
                1f + Mathf.PingPong(Time.time * scaleSpeed, 1f);

            object3.localScale = new Vector3(
                scaleChange,
                scaleChange,
                scaleChange
            );
        }
    }
}
```
### Output:

<img width="1920" height="1200" alt="Screenshot 2026-11-03 135546" src="https://github.com/user-attachments/assets/7870ffb3-aa15-4b3a-bda9-91d463d88de9" />


<img width="1920" height="1200" alt="Screenshot 2026-11-03 135558" src="https://github.com/user-attachments/assets/d73bdffb-acb5-4c12-8fc8-4273c1c69e26" />





### Result:
Thus the basic movement is learned through scripting


