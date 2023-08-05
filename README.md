# Kubernetes_ejemplo

Configurar un clúster Kubernetes con Minikube es una forma sencilla de crear un entorno Kubernetes local en su máquina. Minikube es ideal para fines de desarrollo y pruebas. A continuación te explicamos cómo puedes configurar Minikube:

1. Instalar Requisitos previos:
   Antes de instalar Minikube, asegúrese de tener instalados los siguientes prerrequisitos:
   - VirtualBox (u otro hipervisor compatible): Minikube ejecuta nodos Kubernetes como máquinas virtuales, y VirtualBox es un hipervisor comúnmente utilizado para este propósito. Puede encontrarlo en https://www.virtualbox.org/.
   - kubectl: Asegúrese de que tiene kubectl instalado en su sistema. Puede seguir las instrucciones en https://kubernetes.io/docs/tasks/tools/install-kubectl/ para instalar kubectl.

2. Instale Minikube:
   - Visite el repositorio oficial de Minikube en https://github.com/kubernetes/minikube/releases y descargue la versión adecuada para su sistema operativo.
   - Instale Minikube siguiendo las instrucciones para su sistema operativo.
3. Inicie Minikube:
   - Abra su terminal o símbolo del sistema e inicie Minikube:

minikube start

4. Verifique el estado de Minikube:
   - Verifique el estado de su cluster Minikube:

minikube status

5. Interactúe con el cluster Kubernetes:
   - Con Minikube en ejecución, kubectl debería utilizar automáticamente el contexto del clúster Minikube.
   - Verifique que kubectl está utilizando Minikube:

kubectl config current-context

De aqui usaremos VCS para tener nuestro archivos yaml. Que tendremos dos.
Una vez hecho la actualizacion y configuracion de minikube como cluster. Se detecta el uso de docker desktop. Esto creara el contenedor con el servicio. 
![image](https://github.com/xavinavi545/Kubernetes_ejemplo/assets/115561829/7e1ba479-59ff-4da6-a8cd-19b925d57eb8)
Gracias a Minikube. Que es un cluster local nos permite hacer la mayoría de las instalaciones de forma automática en Docker desktop.

![image](https://github.com/xavinavi545/Kubernetes_ejemplo/assets/115561829/f94ec5ed-17be-419a-8438-f6e632f25ba3)

Usaremos este comando y tendremos una confirmacion.
![image](https://github.com/xavinavi545/Kubernetes_ejemplo/assets/115561829/94be8f8f-fb12-477d-9f28-ff6e2c8c050d)

Ahora iremos a VSC y haremos los yaml. 
Guarda ambos archivos y, desde tu terminal, apunta a la carpeta donde los tienes guardados.

Ejecuta los siguientes comandos para desplegar la aplicación en tu clúster de Kubernetes:

kubectl apply -f nginx-deployment.yaml
kubectl apply -f nginx-service.yaml

Verifica el estado del despliegue y el servicio:

kubectl get pods
kubectl get services

Una vez que los pods estén en estado "Running" y el servicio tenga una dirección IP asignada (en el caso del tipo "LoadBalancer"), podrás acceder a la aplicación web de Nginx a través de esa dirección IP.
minikube service nginx-service


TIP:
Mientras todo el proceso se haga no cerrar el terminal donde se inicie el comando de minikube.

