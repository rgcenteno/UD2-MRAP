# Práctica S3 CRR y MRAP

En esta práctica vamos a trabajar con S3 Cross-Region Replication y S3 Multi Region Access Point. 

## S3 Cross-Region Replication (CRR)

**Amazon S3 Cross-Region Replication (CRR)** es una funcionalidad que permite replicar automáticamente objetos de un bucket S3 hacia otro bucket ubicado en una región diferente de AWS. La replicación se realiza de forma asíncrona y puede aplicarse a todo el contenido del bucket o únicamente a determinados prefijos, como ocurre en esta práctica con la carpeta **datos/**. CRR se utiliza habitualmente para mejorar la disponibilidad de los datos, implementar estrategias de recuperación ante desastres (Disaster Recovery), cumplir requisitos normativos relacionados con la ubicación geográfica de la información o acercar copias de los datos a usuarios distribuidos globalmente. [Documentación.](https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication.html)

## S3 Multi-Region Access Point (MRAP)

**Amazon S3 Multi-Region Access Point (MRAP)** proporciona un único endpoint global para acceder a varios buckets S3 ubicados en distintas regiones. En lugar de que las aplicaciones decidan a qué bucket conectarse, todas las peticiones se envían al MRAP y este selecciona automáticamente el bucket con menor latencia y mejor ruta de red para cada solicitud. Su uso principal es simplificar arquitecturas globales, reducir tiempos de acceso para usuarios distribuidos geográficamente y mejorar la resiliencia de las aplicaciones, ya que permite mantener el acceso a los datos incluso cuando una región presenta problemas o deja de estar disponible temporalmente.

En resumen, **CRR se encarga de mantener sincronizados los datos entre regiones**, mientras que **MRAP se encarga de dirigir cada petición al bucket más adecuado** según la ubicación y las condiciones de la red. [Documentación.](https://docs.aws.amazon.com/AmazonS3/latest/userguide/MultiRegionAccessPoints.html)
