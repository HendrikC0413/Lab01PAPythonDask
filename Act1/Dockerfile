# Utiliza la imagen oficial de Python como base
FROM python:3.8

# Actualiza el sistema y asegúrate de que las herramientas necesarias estén instaladas
RUN apt-get update && apt-get install -y \
    build-essential \
    libcurl4-openssl-dev \
    graphviz

# Instala Dask, Jupyter Notebook y otras bibliotecas que puedas necesitar
RUN pip install dask jupyter graphviz

# Crea un directorio de trabajo en el contenedor
WORKDIR /app

# Expone el puerto 8888 para Jupyter Notebook
EXPOSE 8888

# Comando para iniciar Jupyter Notebook
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]