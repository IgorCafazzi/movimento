# movimento

using System.Collections;
using System.Collections.Generic;
using UnityEditor.SceneManagement;
using UnityEngine;

public class movimento : MonoBehaviour
{
    Vector3 posicao;

    // Start is called before the first frame update

    void Start()
    {
        posicao = new Vector3(0f, 2.5f, 2.5f);
        transform.position = posicao;
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKey(KeyCode.A))
        {
            posicao.x = 0.05f;
            posicao.y = 0.0f;
            posicao.z = 0.0f;
            transform.Translate(posicao);
        }
    }
}
