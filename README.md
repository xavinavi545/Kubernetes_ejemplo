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
