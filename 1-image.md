# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**
docker pull hello-world

**¿Qué es nginx**
Nginx es un servidor web que también sirve como proxy inverso y balanceador de carga. Se usa para mostrar páginas web, manejar muchas conexiones al mismo tiempo y repartir el tráfico entre varios servidores de forma rápida y eficiente.

Descargar la imagen  **nginx** en la versión **alpine**
docker pull nginx:alpine
# COMPLETAR

### Listar imágenes

```
docker images
```
<img width="619" height="90" alt="image" src="https://github.com/user-attachments/assets/60f45d2a-2c68-4818-a154-3f0e748c0388" />

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
# COMPLETAR
<img width="886" height="897" alt="image" src="https://github.com/user-attachments/assets/24808aee-7b96-4911-ac27-a25bd1dc23c6" />

<img width="850" height="973" alt="image" src="https://github.com/user-attachments/assets/2264eeeb-bf76-4396-a972-f1a861d49c91" />

**¿Con qué algoritmo se está generando el ID de la imagen**
# COMPLETAR
Con el algoritmo SHA-256 (Secure Hash Algorithm 256 bits) al contenido de la imagen.

### Filtrar imágenes

```
docker images | grep <termino a buscar>
<img width="577" height="67" alt="image" src="https://github.com/user-attachments/assets/29ec9f19-7f83-493d-b6bf-8024f377ce67" />
```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 
# COMPLETAR
<img width="851" height="74" alt="image" src="https://github.com/user-attachments/assets/e839786a-8a7e-4e98-b240-886397b943b8" />

-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
