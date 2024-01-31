# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Gradle documentation](https://docs.gradle.org)
* [Spring Boot Gradle Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/3.3.0-SNAPSHOT/gradle-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/3.3.0-SNAPSHOT/gradle-plugin/reference/html/#build-image)
* [Spring Web](https://docs.spring.io/spring-boot/docs/3.3.0-SNAPSHOT/reference/htmlsingle/index.html#web)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/rest/)

### Additional Links
These additional references should also help you:

* [Gradle Build Scans – insights for your project's build](https://scans.gradle.com#gradle)


kubectl logs -f -p POD -c spring-boot-k8s-d9d6dc5bd-g2qlc

kubectl logs --tail=50 spring-boot-k8s-d9d6dc5bd-g2qlc


Comandos para generar conexion minikube + docker + kubernates

minikube status *para saber si esta corriendo o no*
minikube start *en el caso de que no este corriendo*

eval $(minikube docker-env)  *No estoy seguro para que funciona esto*

docker build -t demo:1.0 . *para crear la imagen de docker, el "demo" es dinamico dependiendo del nombre que quieras darle*

docker images *para ver las imagenes creadas*

kubectl apply -f deployment.yaml *para ejecutaar configuracion del deployment del ms, el nombre "deployment" debe ser el mismo del archivo en el ms*

kubectl get deploy *para ver los deployments*

kubectl get pods *para ver los pods creados, es importante ver que esten 1/1 ready*

kubectl logs --tail=50 spring-boot-k8s-d9d6dc5bd-g2qlc *para ver los logs de un pod especifico*

kubectl apply -f service.yaml *para desplegar la config del server*

kubectl get svc *para ver los service creados, de aca deberia obtenerse el port de la url 8080:{PORT/TCP}*

kubectl get nodes -o wide *en el caso de tener un service tipo nodeport con este comando se puede ver la internal IP*

minikube ip *para obtener la misma ip que encuentras con el comando anterior*

la url para poder pegarle a tu api deberia ser construida asi: http://{nodeIp}:{PORT}/{API URL}

http://127.0.0.1:9518/dummy

PARA OBTENER LA URL REAL DEL POD ES MEJOR USAR EL SIGUIENTE COMANDO:

minikube service springboot-k8s-svc

con ese comando deberia mostrate la url en el navegador y con esa completas tu api para probarla

http://127.0.0.1:9601/

video de youtube seguido:
https://www.youtube.com/watch?v=7o7e8OAAWyg