# Creando nuestra primera imagen con docker


1. Creamos un directorio de trabajo

`mkdir docker && mkdir docker/nginx`

2. Creamos un dichero index.html y creamos un template de html5

`touch index.html`

3. Creamos un dockerfile 

`touch dockerfile`

4. Añadimos a nuestro dockerfile la configuración de la imagen que vamos a crear.

```
FROM nginx
COPY .*html /usr/share/nginx/html/
```
  
5. Compilamos la imagen

`docker build -t libro-docker/ejemplo1 .`

6. Levantamos el contenedor
   
`docker run -it -p 8000:80 --rm libro-docker/ejemplo2` 

- `-it` - para modo interactivo y consola
- `p` - para indicar el puerto destino y el puerto origen
- `rm` - elimina el contenedir si encuentra uno con el mismo nombre, sino asigna ese nuevo tag