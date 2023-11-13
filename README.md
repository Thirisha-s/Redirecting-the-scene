# Redirecting-the-scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
### Step 1:
To open the unity engine.

### Step 2:
Create a new plane and create a cube and give color for the cube.

### Step 3:
Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

### Step 4:
Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

### Step 5:
Create the C# script file in the Assets and write the Coding for the Redirecting to the page2 after hit the sphere to cube.

### Step 6:
Next Create a another new scene named as page2.

### Step 7
In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.

### Step 8:
Click the Build and run button in the Build settings and run the scene.

### Step 9:
The Sphere after touching the cube it will disappeared and Press the key [R] the redircting to the new scene that is page2.

## Program:

NAME: THIRISHA S
REG NO: 212222230160

```python
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class player : MonoBehaviour
{

    public GameObject WinText;

    Rigidbody rb;

    public void start()
    {
        rb = GetComponent<Rigidbody>();
    }
    public void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
            SceneManager.LoadScene("scene");
    }
    private void OnMouseDown()
    {
        Destroy(gameObject);
    }
    public void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "sphere")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);

        }
    }
}


```

## Output:

![image](https://github.com/Thirisha-s/Redirecting-the-scene/assets/120380280/b882c4e4-66e5-4146-a1dd-ce3b7627fa3d)



## Result:
The above C# coding is successfully redirecting the scene in the unity engine.
