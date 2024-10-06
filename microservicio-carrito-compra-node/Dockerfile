# Usa una imagen base de Node.js
FROM node:18-alpine

# Establece el directorio de trabajo en el contenedor
WORKDIR /usr/src/app

# Copia los archivos package.json y package-lock.json al contenedor desde el subdirectorio 'carrito-compra'
COPY carrito-compra/package.json carrito-compra/package-lock.json ./

# Instala las dependencias
RUN npm install

# Copia el resto de los archivos de la aplicación al contenedor
COPY carrito-compra .

# Expone el puerto que usará tu aplicación
EXPOSE 3000

# Comando para ejecutar la aplicación
CMD ["npm", "start"]
