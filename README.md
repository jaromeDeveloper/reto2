Master DevSecOps en Lite Thinking
Reto 2. Clúster de Kubernetes Local
Consultor: Jorge Valente Fragoso Mora 
Alumno: Jorge Alberto Rodriguez Mendez
Correo: jarome.developer@gmail.com

1. Instalación de MicroK8s en Windows (30 puntos) 
• Instale Multipass 
Se va al a pagina oficial y se descarga el aplicativo





Se le da aceptar a los terminos y condiciones de uso



Se le da click en siguiente

Se selecciona la opción Finish




Se ejecuta el aplicativo

Se quedo pasmado


Instale Microk8S en WSL de Windows

El primer comando dentro de la WSL es verificar si el [boot], la variable systemd=true



Actualizamos los paquetes


Se instala el gestor de paquetes snap para poder descargar microK8s


se ejecuta el comando sudo snap install microk8s


Se añade con el comando sudo usermod -a -G microk8 $USER para la ejecución de MicroK8s


Se instala IP TABLES



2. Exploración del cluster de Kubernetes (30 puntos)



 • Lista los nodos que se están ejecutando en el cluster

• Lista los servicios de todos los espacios de nombre

 3. Instalación de NGINX en el cluster (20 puntos) 

• Crea un deployment para implementar una imagen de Nginx

 • Lista los deployments 

• Lista los Pods



• Obten la IP del nodo y accede al sitio web desde linea de comando con wget 




Se utiliza un proxy para redireccionar por el puerto 8080 el trafico de nginx


4. Escalado de Instancias (20 puntos) o Escala a 5 replicas el pod de nginx. 



Se escala a 5 replicas


Se listan los 5 pods



Se reducen los dos pods

Se listan los pods

EXTRA
Aplicando los conceptos aprendidos he agregado esto extra al reto:


Se escala a 5 Replicas

Se ejecutara esto en una terminal for i in {1..10}; do curl -s localhost:8080 | grep title; done
para generar trafico.



Cambiar la imagen por una más visual como nginxMaster/hello

Se genera la imagen nginxMaster


microk8s enable dashboard



Se instala el dashboard





En el proceso de instalación




Se muestra la configuración, se requiere pegar el token para que muestre el tablero de Kubernetes


Se muestra el tablero de Kubernetes


Nos muestra opciones que podemos hacer de manera visual de kubernetes




Se agrega un ConfigMap


El mensaje de configMap creado


Se muestran conceptos de configuración, entorno y debugging de contenedores


Se muestra la observabilidad


Los eventos en los pods

Para mas pruebas, se instala una herramienta de bechMarking



Se realiza la petición a un pod con el siguiente comando:
hey -z 10s -c 5 http://localhost:8080

En logs se puede apreciar la cantidad de peticiones


Tambien nos muestra la metrica el uso




Muchas gracias, Maestro, por su tiempo y por compartir con nosotros su experiencia. El Master me ha gustado mucho y realmente valoro sus enseñanzas y me inspiro a seguir buscando y aprender de este mundo.



