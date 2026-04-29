# Ex.No: 3  Basic movements in Unity 
### DATE:29-04-2026                                                                            
### REGISTER NUMBER : 212223240169
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

public class NewMonoBehaviourScript : MonoBehaviour
{
    // Start is called once before the first execution of Update after the MonoBehaviour is created
    public Transform ob1;
    public Transform ob2;
    public Transform ob3;
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyUp(KeyCode.X))
        {
            ob1.Translate(0.2f,0,0);
        }
        if (Input.GetKeyUp(KeyCode.Y))
        {
            ob2.localScale+=new Vector3(2f,2f,2f);
        }
        if (Input.GetKeyUp(KeyCode.Z))
        {
            ob3.Rotate(0,20f,0);
        }
    }
}

```
### Output:

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/3fb5f02c-f924-4086-808a-c754eee693be" />


<img width="1918" height="1079" alt="image" src="https://github.com/user-attachments/assets/360f36fa-93d9-4238-a8f4-0fa27f5b8b1c" />





### Result:
Thus the basic movement is learned through scripting


