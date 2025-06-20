Automatización de despliegue visual con GitHub Actions y AWS S3

Este proyecto demuestra un pipeline CI/CD sencillo que automatiza el despliegue de cambios visuales en un sitio web estático almacenado en un bucket de AWS S3.
¿Qué hace?

    Cada vez que haces un push al repositorio, se ejecuta un workflow de GitHub Actions.

    El workflow construye y valida los cambios.

    Luego, se sincronizan los archivos con un bucket S3 configurado para hosting estático.

    Así, cualquier cambio visual queda publicado automáticamente y en tiempo real en el sitio web.

Tecnologías usadas

    GitHub Actions (workflow para CI/CD)

    AWS S3 (bucket para hosting estático)

    AWS IAM (roles y permisos para desplegar con seguridad)

    AWS CLI (comandos para sincronizar archivos con S3)

Requisitos previos

    Tener un bucket S3 configurado para hosting estático.

    Configurar las credenciales AWS con permisos para acceso y despliegue (por ejemplo, mediante secrets en GitHub).

    GitHub Actions configurado en el repositorio.

Cómo funciona el workflow

El archivo .github/workflows/deploy.yml contiene la definición del pipeline que:

    Detecta cambios en la rama principal.

    Ejecuta validaciones necesarias (opcional).

    Usa AWS CLI para sincronizar los archivos locales con el bucket S3.

Uso

    Haz commit y push de los cambios en el repositorio.

    GitHub Actions ejecutará automáticamente el pipeline.

    Los archivos se desplegarán en el bucket S3 y estarán visibles en la URL pública.
