## Creación del Clúster




### Configuración Básica del Clúster

#### Pre configuración
- Crear un par de claves para poder acceder al Clúster mediante SSH
- Crear un Bucket en S3 para guardar los notebooks del clúster 

#### Creación
- Ir a EMR en la cónsola 
- Seleccionar la versión 6.3.1 de Amazon
- seleccionar los paquetes: **Hadoop 3.2.1, JupyterHub 1.2.0, Hive 3.1.2, Sqoop 1.4.7, Zeppelin 0.9.0, Tez 0.9.2, JupyterEnterpriseGateway 2.1.0, Hue 4.9.0, Livy 0.7.0** y **HCatalog 3.1.2**
![image](https://user-images.githubusercontent.com/53226911/171077521-c5d291df-bf0c-46a8-8450-077eff63b7ba.png)
- Activar las utilidades de AWS de Hiva y Spark

![image](https://user-images.githubusercontent.com/53226911/171077471-c030f9b5-191d-499b-bf1a-a98dc06ae6a7.png)

- Ahora hay que añadir la configuración para asegurar la persistencia en S3.

      [
          {
              "Classification": "jupyter-s3-conf",
              "Properties": {
                  "s3.persistence.enabled": "true",
                  "s3.persistence.bucket": "<Bucket name>"
              }
          }
      ]

**Nota:** Remplazar el texto <Bucket name>, con el nombre del bucket creado en S3.
  

- habilitar la opción 'Clusters enters waiting state' y clicker next

![image](https://user-images.githubusercontent.com/53226911/171079102-1e2f1be1-2daa-4eaf-97cb-b2d446cd31cd.png)


- Cambiar el tipo de intancia de los nodos maestro y esclavos de **m5.xlarge** a **m4.xlarge** y cambiar la configuración de Purchasing option de **On-demand** a **Spot**.
  
  ![image](https://user-images.githubusercontent.com/53226911/171079391-e64b6d2c-6e56-4cb5-86ed-3066f63db2ac.png)

- Si se quiere se puede port que la instancia se termine después de no usarse después de un tiempo y clicke en Next con el resto de opciónes por defecto.

  ![image](https://user-images.githubusercontent.com/53226911/171079523-c02f321f-ff65-4838-a6ca-a4cb33a27c98.png)

- Poner un nombre al Clúster y click en next con el resto de opciones por defecto.

- seleccionar el par de claves que se crearon antes de comenzar la creación del clúster y finalizar creando la isntancia con el resto de valores predeterminados.
  

  
  

