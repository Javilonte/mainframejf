# Entorno de Desarrollo Mainframe + Java(Todavía no está lista esta parte) + Frontend

Este proyecto levanta un entorno completo de Mainframe (MVS 3.8j) usando Docker.
## Requisitos
1. Docker Desktop instalado.
2. Un emulador TN3270 (x3270, TN3270 X, Brownie).
(Tengo un short en mi canal para instalar x3270 en mac m1+)

## Instalación (Paso a paso)

1. **Clonar este repositorio:**
   git clone <https://github.com/Javilonte/mainframejf>
   cd mi-proyecto

2. **Descargar el Sistema Operativo (TK4-):**
   - Descarga el zip de: http://wotho.ethz.ch/tk4-/tk4-_v1.00_current.zip
   - Descomprímelo DENTRO de la carpeta `mainframe/`.
   - **Importante:** Renombra la carpeta descomprimida a `mvs_data`.
   
   La estructura debe quedar así:
   /mainframe
      /mvs_data
         /conf
         /dasd
         ...

3. **Arrancar:**
   Ejecuta en tu terminal:
   docker-compose up --build

4. **Conectar:**
   - Abre tu emulador TN3270.
   - Conecta a: `localhost` Puerto: `3270`.
   - Usuario: `HERC01` / Password: `CUL8TR`.

## Arquitectura
- **Mainframe:** Corre sobre Hercules en un contenedor Ubuntu.
- **Volúmenes:** Los datos persisten en la carpeta local `mainframe/mvs_data`.