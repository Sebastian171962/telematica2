# Instalando la imagen de Ubuntu
FROM ubuntu:20.04

# EJECUCION DE COMANDOS
ENV TZ=America/Bogota
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Actualizar
RUN apt update

# Instalación de npm 
RUN apt install -y npm

# Creando carpeta de almacenamiento
RUN mkdir /root/node-web

# Copiar los archivos de la página web
COPY Node /root/node-web

# Estableciendo el directorio de trabajo
WORKDIR /root/node-web

# Instalando dependencias
RUN npm install

# Abriendo puertos para la imagen
EXPOSE 3000

# CMD se usa para proporcionar valores predeterminados para una ejecución de contenedor
CMD ["npm", "start"]
