# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
# COMPLETAR
<img width="605" height="49" alt="image" src="https://github.com/user-attachments/assets/8704b825-3e0f-4f5c-bf96-d88fa3d4c355" />


Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
# COMPLETAR
docker create hello-world:latest

<img width="618" height="45" alt="image" src="https://github.com/user-attachments/assets/495f989f-ab88-42e5-b6f8-204a04db9e79" />


### Listar los contenedores ejecutándose o no

```
docker ps -a
```
<img width="932" height="82" alt="image" src="https://github.com/user-attachments/assets/28d154a2-9e0c-40a4-8014-611c7e8e093e" />


### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
# COMPLETAR
docker start srv-web


### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```
<img width="832" height="56" alt="image" src="https://github.com/user-attachments/assets/fd420adb-988c-4850-9ffa-8ae699b7604e" />



### Para detener un contenedor

```
docker stop <nombre contenedor>
```
docker stop srv-web


### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
# COMPLETAR
docker run --name srv-web2 nginx:alpine


**¿Qué sucede luego de la ejecución del comando?**
# COMPLETAR  
El contenedor se ejecuta en primer plano y captura la entrada de la terminal, mostrando directamente los mensajes de Nginx. Mientras corre, la terminal queda ocupada por el contenedor.


Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
# COMPLETAR
docker run -d --name srv-web3 nginx:alpine
<img width="481" height="37" alt="image" src="https://github.com/user-attachments/assets/5054a916-93f9-4490-83e3-09b72c9c365b" />


### Para eliminar un contenedor
```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
# COMPLETAR
<img width="318" height="35" alt="image" src="https://github.com/user-attachments/assets/eca0e889-2fcd-4584-b679-e1d3675d9420" />


Verificar que el contenedor que se eliminó
# COMPLETAR
<img width="893" height="95" alt="image" src="https://github.com/user-attachments/assets/efdf1562-6d25-4e92-a02c-ce841f6d33fb" />


### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
# COMPLETAR
docker rm -f srv-web3

Verificar que el contenedor que se eliminó
# COMPLETAR
<img width="898" height="82" alt="image" src="https://github.com/user-attachments/assets/29922ebb-3909-43af-b0a4-d38ffd658c8b" />


### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
# COMPLETAR
docker inspect srv-web
<img width="946" height="973" alt="image" src="https://github.com/user-attachments/assets/547a651f-e810-465b-971b-0115b58d0d51" />

