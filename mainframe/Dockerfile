# 1. Usamos Ubuntu como base
FROM ubuntu:22.04

# Evitamos preguntas de configuración durante la instalación
ENV DEBIAN_FRONTEND=noninteractive

# 2. INSTALACIÓN (Esta es la parte que te faltaba)
# Actualizamos e instalamos hercules y unzip
RUN apt-get update && apt-get install -y \
    hercules \
    unzip \
    && rm -rf /var/lib/apt/lists/*

# 3. Configuramos la carpeta de trabajo
WORKDIR /mvs

# 4. Exponemos los puertos
EXPOSE 3270 8038

# 5. Comando de arranque
# Apuntamos a la configuración que viene dentro de la carpeta que descargaste (tk4-)
CMD ["hercules", "-f", "conf/tk4-.cnf"]