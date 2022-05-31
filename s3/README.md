# Configuración S3

Ir a la pestaña de S3 en el Dashboard de HUE

![1](https://user-images.githubusercontent.com/53226911/171091788-af4a8952-2bff-46aa-8c36-adb0ab9d77a5.png)

- Seleccionar el Bucket que asociamos a este cluster.

![image](https://user-images.githubusercontent.com/53226911/171091874-08551c8d-964f-428f-b69b-facc29b9174c.png)


- Crear un directorio para los datasets /datasets/onu

![image](https://user-images.githubusercontent.com/53226911/171092074-d06799c1-0f0c-4006-879a-2a669db8baf8.png)


-Subir los datasets

![image](https://user-images.githubusercontent.com/53226911/171092254-188b8256-9fa4-418e-ada0-f5161f84a1d6.png)



# Subir a S3 utilizando HDFS

Desde la isntancia subir los datasets a S3.

      hadoop distcp hdfs:/user/hadoop/datasets s3a://jdmejiavbucket/datasets/hdfs

![image](https://user-images.githubusercontent.com/53226911/171092835-0aaa8ff2-676e-4df5-b655-5610ca855e15.png)


- Verificar que se hayan subido los datasets en S3, para esto en la consola, ir a S3 y seleccionar el bucket asociado al clúster

![image](https://user-images.githubusercontent.com/53226911/171093008-5b97fe37-3ad0-4981-980a-df514cbcf488.png)
