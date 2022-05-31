# Hdfs

Para configurar el sistema de archivos con los recursos necesarios es necesario acceder el clúster via SSH.

- En la consola de AWS seleccionar el Clúster y copiar el comando que nos muestra en pantalla cuando le damos a conectar a nodo maestro con SSH

![image](https://user-images.githubusercontent.com/53226911/171088541-fe0ec228-5362-40a8-be42-5bb274ae4a22.png)

     ssh -i ~/cluster.pem hadoop@ec2-44-205-15-93.compute-1.amazonaws.com
     
![image](https://user-images.githubusercontent.com/53226911/171088608-7d8f1ba9-f92d-4abf-b928-cb9553502fa3.png)

- Cambiar de usuario a hadoop


      sudo su hadoop
      
- Crear el directorio HDFS
  
  hdfs dfs -mkdir /user/hadoop/datasets
  
- Subir los datasets utilizando SSH

      scp -r -i .\cluster.pem ".\Documents\telematica\st0263-2022-1-main\Big Data\datasets\" hadoop@ec2-44-205-15-93.compute-1.amazonaws.com:~/.
      
- Subir los datasets a HDFS
      
      hdfs dfs -copyFromLocal datasets/* /user/hadoop/datasets/

- Verificar si los archivos se guardaron

      hdfs dfs -ls /user/hadoop/datasets/gutenberg-small/
      
 
 ## HUE
 
 Conectarse a HUE mediante el navegador usando el DNS que nos arroja AWS
 
 ![image](https://user-images.githubusercontent.com/53226911/171090686-0c90303e-209d-483c-b7c3-dfec078f6e16.png)


Se debe crear un usuario y una contraseña en la pestaña

![image](https://user-images.githubusercontent.com/53226911/171090754-4bed5a99-2f9a-474b-916a-fa8e79afefb7.png)


- Ir a Files y verificar que en la ruta /users/hadoop/datasets/onu estén los Datasets, sino es el caso, crear el directorio y subir los archivos

![image](https://user-images.githubusercontent.com/53226911/171091336-544c35d0-963a-46f5-8336-9ca28506b0bf.png)


