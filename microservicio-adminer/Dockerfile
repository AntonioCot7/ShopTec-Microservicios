# Usa una imagen oficial de Python como base
FROM python:3.9-slim

# Establece el directorio de trabajo en /app
WORKDIR /app

# Copia solo el archivo de requerimientos primero, para aprovechar la caché de Docker
COPY requirements.txt /app/

# Instala las dependencias definidas en requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Ahora copia el resto de los archivos de la aplicación
COPY . /app

# Exponemos el puerto 5000, que es donde Flask corre por defecto
EXPOSE 5000

# Define el comando para correr la aplicación Flask
CMD ["python", "app.py"]
