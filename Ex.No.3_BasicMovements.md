# Ex.No: 3  Basic movements in Unity 
### DATE:                                                                            
### REGISTER NUMBER : 212223240037
## AIM: 
To learn the basic movements translation,scaling and rotation of game objects through code.
## Procedure:
1. Setup the Scene
2. Open Unity and create a 3D Scene.
3. Add three objects:Sphere → Rename to Object1 (for movement),Cylinder → Rename to Object2 (for rotation).Capsule → Rename to Object3 (for scaling).
4. Add the Script,Create a C# Script → Name it TransformController.cs.
5. Write the code for translation,scaling and rotation,save and close the script
6. Save the script
7. Select any empty GameObject (or create one: GameObject → Create Empty).
8. Attach the TransformController script to it.
9. In the Inspector, assign Object1 → Drag the Sphere,Object2 → Drag the Cylinder, Object3 → Drag the Capsule.
10. Run the Scene Press Play ▶️ in Unity
11. Stop the program.
## Program 
```
using UnityEngine;

public class TransformController : MonoBehaviour
{
    public Transform object1; // Object for translation
    public Transform object2; // Object for rotation
    public Transform object3; // Object for scaling

    public float moveSpeed = 0.9f;     // Speed of translation
    public float rotateSpeed = 50f;  // Speed of rotation
    public float scaleSpeed = 0.5f;  // Speed of scaling

    void Update()
    {
        // Move object1 along the X-axis
        if (object1 != null)
        {
            object1.Translate(Vector3.right * moveSpeed * Time.deltaTime);
        }

        // Rotate object2 around the Y-axis
        if (object2 != null)
        {
            object2.Rotate(Vector3.forward * rotateSpeed * Time.deltaTime);
        }

        // Scale object3 gradually
        if (object3 != null)
        {
            object3.localScale += new Vector3(0.02f, 0.02f, 0f);
        }
    }
}

```
## Output:
### Before Running:
<img width="1215" height="681" alt="image" src="https://github.com/user-attachments/assets/c2ddf8a4-429b-4b2c-a1e5-f34b591c5a98" />

### After Running:

<img width="1216" height="679" alt="image" src="https://github.com/user-attachments/assets/40af5735-48a1-4e7c-ba64-51c34bad31a5" />



## Result:
Thus the basic movement is learned through scripting


