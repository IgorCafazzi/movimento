using System.Collections;

using System.Collections.Generic;

using UnityEngine;

using UnityEngine.Animations;

using UnityEngine.UIElements;

public class Move : MonoBehaviour
{

    // Start is called before the first frame update


    public Vector3 escala, giragira, posicao;

    void Start()
    {


        posicao = new Vector3(0, 0, 0);

        giragira = new Vector3(0, 0, 0);

        escala.x = 5f;
        escala.z = 5f;
        escala.y = 5f;
        transform.localScale = escala;
    }

    // Update is called once per frame


    void Update()
    {


        if (Input.GetKey(KeyCode.E))
        {
            giragira.y = -0.05f;

        }


        if (Input.GetKey(KeyCode.Q))
        {
            giragira.y = 0.05f;
        }

        if (Input.GetKey(KeyCode.W))

        {

            if (transform.position.z < 34)
            {

                posicao.z = 0.01f;

            }
        }



        if (Input.GetKey(KeyCode.S))
        {

            if (transform.position.z > -34)

            {

                posicao.z = -0.01f;
            }
        }

        if (Input.GetKey(KeyCode.G))
        {
            posicao.x = 0.0f;
            posicao.y = 0.03f;
            posicao.z = 0.0f;
            transform.Translate(posicao);
        }

        if (Input.GetKey(KeyCode.A))

        {

            if (transform.position.x > -34)

            {
                posicao.x = -0.01f;

            }
        }


        if (Input.GetKey(KeyCode.D))
        {

            if (transform.position.x < 34)

            {
                posicao.x = 0.01f;
            }
        }

        if((Input.GetKey(KeyCode.Y))) {
            escala.x = Random.Range(2f, 10f);
            escala.y = Random.Range(2f, 10f);
            escala.z = Random.Range(2f, 10f);
            transform.localScale = escala;
        }


        transform.Translate(posicao);

        transform.Rotate(giragira);


        posicao.x = 0;

        posicao.y = 0;

        posicao.z = 0;

        giragira.y = 0;

    }
}
