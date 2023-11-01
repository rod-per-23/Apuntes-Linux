Volver al [README](../README.md)

Aquí va información relacionada a los Dockers y WSL. Para el caso de los Dockers, se piensa en un sistema Windows.
# Dockers

## Instalar Docker

Simplemente ir a la página de [Docker](https://www.docker.com/products/docker-desktop/) y descargar el instalador para Windows.

## Descargar una imagen

Hay varias formas, se puede buscar directamente desde la GUI del programa, o a través del mismo PowerShell, por ejemplo, para instalar una imagen de [ArchLinux](../Distribuciones/ArchLinux/ArchLinux.md) se puede usar el comando:

```shell
docker run -it archlinux
```

## Inicializar un contenedor desde PowerShell

```shell
# Para inicializar el contenedor
docker container start NOMBRE_CONTENEDOR

# Para ver los contenedores activos
docker container ls

# Para ver las imágenes que tienes en los dockers
docker images

# Para entrar al bash del contenedor desde el powershell
# Dependiendo del terminal que tengas puede ser otro,
# por ejemplo, Nix se usa /bin/sh
docker exec -it NOMBRE_CONTENEDOR /bin/bash
```

# WSL

WSL es básicamente una máquina virtual de Linux dentro del PowerShell de Windows.

## Instalar WSL

Si es que no está instalado, se puede hacer desde el PowerShell con el  siguiente comando:

```shell
wsl --install
```

El comando anterior va a instalar WSL y la distribución por defecto que es Ubuntu.

## Instalar otras distribuciones

Se pueden instalar distribuciones de varias formas, por ejemplo, a través del mismo PowerShell se pueden ver qué otras opciones hay:

```shell
# Lista de distribuciones disponibles
wsl --list --online

# Instalar una distribución de alguna de las de la lista de arriba
wsl --install -d nombreDistribucion
```


Si por ejemplo, se quiere instalar [ArchLinux](../Distribuciones/ArchLinux/ArchLinux.md), se puede hacer por medio de [ArchWSL](https://github.com/yuk7/ArchWSL) 
## Inicializar WSL

Para inicializar una distribución, se debe abrir el PowerShell y escribir `wsl`, sin embargo, esto inicia la distribución por defecto que haya, para cambiarla, se puede hacer lo siguiente:

```shell
# Lista de todas las distribuciones instaladas
wsl -l

# Cambiar distribución por defecto
wsl --setdefault nombreDistribución

```
## Desinstalar una Distribución

Para desinstalar una distribución instalada, se puede hacer de la siguiente forma:

```shell
# Lista de todas las distribuciones instaladas
wsl -l

# Borrar una distribución 
wsl --unregister nombreDistribución
```

Volver a [README](../README.md) 