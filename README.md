# Game-Dev-Code

# Scale Controller code

using UnityEngine;

public class ScaleController : MonoBehaviour
{
    public Transform modelTransform;
    public float scaleFactor = 1.2f; // Scale factor for scaling the model

    private void Start()
    {
        if (modelTransform == null)
        {
            modelTransform = transform; // Use the transform of this GameObject if not assigned
        }
    }

    public void ScaleUp()
    {
        modelTransform.localScale *= scaleFactor;
    }

    public void ScaleDown()
    {
        modelTransform.localScale /= scaleFactor;
    }
}
