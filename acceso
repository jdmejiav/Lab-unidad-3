# Configuración de Acceso a las instancias del Clúster

Por defecto las instancias del clúster se crean con un security group con los puertos bloqueados, por lo que no se puede acceder al clúster mediante ssh
ni mediante http a los notebooks.

Crear una regla en los security groups para poder acceder a Spark,  los puertos 8888, 9443, 8890 y en caso de la conexión por ssh dar error de timeout, 
también crear una regla parael acceso mediate ssh


## Pasos

- ir a ec2 en la consola
- Editar los Security Group del maestro y los esclavos para añadir las siguientes reglas.
![image](https://user-images.githubusercontent.com/53226911/171086863-9f712f59-d084-4ab6-8acf-0e9f85721c9f.png)
- En la configuración de EMR habilitar los puertos 8888, 9443, 8890 y 22 para que no se bloqueen o cabmiar la configuración de **Block public Access** a **Off**.
- ![image](https://user-images.githubusercontent.com/53226911/171087035-e737a203-5351-41e6-9f36-9bf22be20fad.png)
