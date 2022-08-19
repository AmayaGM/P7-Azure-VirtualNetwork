# Practica 7 con "Virtual Network"

*Conexion de red y maquinas virtuales*

**Paso 1 _Grupo de recursos_**
- Buscar grupo de recursos y elegir dicha opcion
![Paso 1](/imagenes/img_1.png)

- Pulsamos en "crear"
![Paso 1.1](/imagenes/img_1_1.png)

- Posteriormente debemos escoger en:
    - Detalles del proyecto:
      - Suscripcion
      - Nombre para nuestro grp. de recursos
    - Detalles del recurso:
      - La region donde deseamos crearlo
- Una vez elegido todo lo correspondiente, dar en revisar y crear
![Paso 1.2](/imagenes/img_1_2.png)

- A continuacion damos en "crear"
  ![Paso 1.3](/imagenes/img_1_3.png)


**Paso 2 _Red virtual_**
- Buscar y elegir "Redes virtuales"
 ![Paso 2.1](/imagenes/img2_1.png)

- Posteriormente seleccionamos la opcion de crear
 ![Paso 2.2](/imagenes/img2_2.png)

- A continuacion debemos escoger en "Datos basicos":
    - Detalles del proyecto:
      - Suscripcion
      - Y el grp. de recursos realizado en el paso 1
    - Detalles de instancia:
      - Nombre de nuestra virtual network
      - La region donde deseamos crearla
![Paso 2.3](/imagenes/img2_3.png)

- A continuacion debemos escoger en "Direcciones IP":
    - Debelos elegir "Agregar subred"
  ![Paso 2.4](/imagenes/img2_4.png)

       - Es necesario nombrar nuestra subred y elegir el intervalo de direcciones, una vez establecidos los parametros necesarios damos clic en "Agregar"
        ![Paso 2.5](/imagenes/img2_5.png)

- Una vez que finalizamos lo anterior damos clic en "Revisar y crear" y posteriormente en "Crear"
  ![Paso 2.6](/imagenes/img2_6.png)
  ![Paso 2.7](/imagenes/img2_7.png)

- Es necesario crear una segunda red con los mismos pasos anteriores
  ![Paso 2.8](/imagenes/img2_8.png)
  ![Paso 2.9](/imagenes/img2_9.png)
  ![Paso 2.10](/imagenes/img2_6.png)
  ![Paso 2.11](/imagenes/img2_7.png)

**Paso 3 _Maquina virtual_**
- Primero debemos buscar maquinas virtuales y elegir la opcion
![Paso 3.1](/imagenes/img4_1.png)

- Damos en "crear" y elegimos la primera opcion
![Paso 3.2](/imagenes/img4_2.png)

- A continuacion elegimos todos los parametros necesarios para crear una maquina virtual de Linux
  - Primero elegimos los "Datos basicos" tal como vienen en la imagen de abajo
    ![Paso 3.3.1](/imagenes/img4_3_1.png)
    ![Paso 3.3.2](/imagenes/img4_3_2.png)
    ![Paso 3.3.3](/imagenes/img4_3_3.png)
    ![Paso 3.3.4](/imagenes/img4_3_4.png)

  - Despues escogemos las opciones en "Redes" tal como vienen a continuacion y por ultimo en revisar y crear
    ![Paso 3.4.1](/imagenes/img4_4_1.png)
    ![Paso 3.4.2](/imagenes/img4_4_2.png)

  - Finalmente damos en crear
    ![Paso 3.5](/imagenes/img2_7.png)

- Posteriormente crearemos una segunda maquina virtual con las instrucciones antes dadas y segun los parametros dados en las siguientes fotos
  - Datos basicos
    ![Paso 3.6.1](/imagenes/img4_5_1.png)
    ![Paso 3.6.2](/imagenes/img4_5_2.png)
    ![Paso 3.6.3](/imagenes/img4_5_2_1.png)
    ![Paso 3.6.4](/imagenes/img4_5_3.png)

  - Redes
    ![Paso 3.7.1](/imagenes/img4_6_1.png)
    ![Paso 3.7.2](/imagenes/img4_6_2.png)

  - Damos en "revisar y crear", despues en "Crear"
    ![Paso 3.8.1](/imagenes/img2_6.png)
    ![Paso 3.8.2](/imagenes/img2_7.png)

**Paso 4 _Conexion_**
- Ir a MV1
![Paso 4.1](/imagenes/img5_1.png)

- Elegir el apartado de conectar y elegir SSH
  ![Paso 4.2.1](/imagenes/img5_2_1.png)

    - Copia lo marcado en rojo
  ![Paso 4.2.2](/imagenes/img5_2_2.png)

- Dar clic en el Azure Cloud Shell
![Paso 4.3](/imagenes/img5_3.png)

  - Elegir crear almacenamiento
  ![Paso 4.3.1](/imagenes/img5_3_1.png)

  - Ahora teclearemos en la terminal "ssh" Seguido de lo que copiamos anteriormente 
  ![Paso 4.3.2](/imagenes/img5_3_2.png)

  - Nos haran una pregunta a la cual contestaremos de forma afirmativa
  ![Paso 4.3.3](/imagenes/img5_3_3.png)

  - Despues nos pediran el password de la maquina virtual
  ![Paso 4.3.4](/imagenes/img5_3_4.png)

  - Para comprobar nuestra conexion hay que teclear "sudo apt-get moo" y nos aprecera una vaquita de confirmacion
  ![Paso 4.3.5](/imagenes/img5_3_5.png)

- Posteriormente nos iremos a la red virtual 2
  ![Paso 4.4.1](/imagenes/img5_4.png)

    - Luego vamos a dispositivos conectados
  ![Paso 4.4.2](/imagenes/img5_4_2.png)

  - Podremos visualizar nuestra maquina virtual 2
  ![Paso 4.4.3](/imagenes/img5_4_3.png)

- Ahora iremos a la red virtual 1
  ![Paso 4.5.1](/imagenes/img5_5.png)

  - Posteriormente pulsamos en emparejamientos
    ![Paso 4.5.2](/imagenes/img5_5_2.png)

  - Ahora seleccionamos "Agregar"
      ![Paso 4.5.3](/imagenes/img5_5_3.png)

    - Posteriormente rellenamos segun los parametros dados en las siguientes imagenes y finalmente damos en agregar
        ![Paso 4.5.3.1](/imagenes/img5_5_4_1.png)
        ![Paso 4.5.3.2](/imagenes/img5_5_4_2.png)
        ![Paso 4.5.3.3](/imagenes/img5_5_4_3.png)

- Por ultimo copiamos la direccion IP de la red 2 y en la consola tecleamos "ping" seguido de la IP para comprobar nuestra conexion. Podremos observar como se esta llevando una comunicacion de manera exitosa
  ![Paso 4.6](/imagenes/img5_6.png)
  ![Paso 4.7](/imagenes/img5_7.png)

>Nota: Las redes y maquinas deben estar en la misma region


