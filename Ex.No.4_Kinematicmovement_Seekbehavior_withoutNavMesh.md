# Ex.No: 4  Implementation of Kinematic movement -seek and Flee behavior in Unity
### DATE: 11-05-2026                                                                 
### REGISTER NUMBER : 212223240169
### AIM: 
To write a program to simulate the process of seek and Flee behavior in Unity without NavigationMeshAgent. 
### Algorithm:
1. Create a New Unity Project by Open the  Unity Hub and create a new 3D Project,Name the project (e.g., SeekBehaviorDemo).
2. Create the Moving Object
   In the Hierarchy, right-click → 3D Object → Cube (or Sphere).
   Rename it to Seeker and Reset its position:Select the Seeker, go to Inspector → Transform → Set Position to (0,0,0).
3. Create the Target Object
   Right-click in the Hierarchy → 3D Object → Sphere (or any other shape).
   Rename it to Target. Move it away from Seeker, e.g., set Position to (5, 0, 5).
   Select the Target, add a Material, and change the color. (if needed) 
4. Adding the Seek Behavior Script
   Create the Script-In the Project Window, go to the Assets folder.
   Right-click → Create → C# Script.
5. Write a script for seek behavior and save it
6. Attach the Script
   Select Seeker in the Hierarchy - Drag & Drop the SeekBehavior script onto the Inspector Panel.
   Drag & Drop the Target from the Hierarchy into the "Target" field in the script component.
12.  Write a script for flee behavior and attach it to target
13.  Run the game
14. Stop the program
    
### Program:
```
using UnityEngine;

public class NewMonoBehaviourScript : MonoBehaviour
{
    // Start is called once before the first execution of Update after the MonoBehaviour is created
  public Transform o1;
  public Transform target;    
  public Transform o3;
  public float speed;
  void Start()
  {
      
  }
  public void seeker()
  {
      Vector3 dir = (target.position - o1.position).normalized;
      o1.position += dir * speed * Time.deltaTime;
  }
  public void fleer()
  {
      Vector3 dir = (o3.position - target.position).normalized;
      o3.position += dir * speed * Time.deltaTime;
  }
  // Update is called once per frame
  void Update()
  {
      seeker();
      fleer();
  }
}
```
### Output:

<img width="1915" height="1072" alt="image" src="https://github.com/user-attachments/assets/eb8ef8a8-0a3e-42ab-a66e-358b089e0dbc" />

<img width="1916" height="1079" alt="image" src="https://github.com/user-attachments/assets/ee576221-c53d-4fa9-aa09-18efd392bbf9" />


### Result:
Thus the simple seek behavior was implemented successfully.
