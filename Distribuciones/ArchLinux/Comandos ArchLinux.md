Volver a [ArchLinux](./ArchLinux.md)

Aquí van a ir comandos útiles e importantes para ArchLinux.

# Pacman

Pacman es el manager de paquetes de Arch Linux.

## Instalar paquetes

Para instalar paquetes con Pacman, se debe usar el siguiente comando:

```bash
# Instala 3 paquetes distintos: neofetch, cowsay y lolcat
# Se asume que se está en un usuario distinto a root
sudo pacman -S neofetch cowsay lolcat
```

Como ejemplo del uso de los paquetes, se obtiene la siguiente imagen.
(Cabe mencionar que el Arch mostrado en la figura es a través de [Comandos Dockers y WSL > WSL](../../Dockers%20y%20WSL/Comandos%20Dockers%20y%20WSL.md#WSL) . 

![WhatsApp Image 2023-10-31 at 10.03.46 PM](../../WhatsApp%20Image%202023-10-31%20at%2010.03.46%20PM.jpeg)

## Actualizar sistema

Arch es conocido por ser una "rolling release distro", es decir, que siempre hay actualizaciones constantemente.

Para actualizar el sistema completo se usa el siguiente comando:

```bash
# Añadir 'sudo' antes si es que no se está en root
pacman -Syu 
```

# AUR

Una de las cosas más atractivas de Arch es la [AUR](https://aur.archlinux.org/) , que es básicamente un repositorio de paquetes de la comunidad de Arch.

> [!NOTE] **¡¡¡IMPORTANTE!!!**
>  RECORDAR QUE LA AUR SON PAQUETES PRODUCIDOS POR LOS MISMOS USUARIOS Y NO SON OFICIALES, POR LO QUE INSTALAR ALGÚN PAQUETE EXTRAÑO PUEDE DESTRUIR TODO EL SISTEMA

Primero se deben instalar unos paquetes importantes, aunque si se siguió la guía [Instalar ArchLinux](./Instalar%20ArchLinux.md) ya deberían estar todos instalados, si no, hay que utilizar el siguiente comando:
```bash
pacman -Syu
pacman -S git base-devel
```

## Usando yay

Se puede utilizar un 'helper' como `yay` para instalar paquetes de la AUR, para instalar `yay` se hace a través del siguiente comando:
```bash
git clone https://aur.archlinux.org/yay.git
```
Una vez instalado, se debe ir al directorio donde se descargó `yay` e iniciar el proceso de construcción del paquete:
```bash
# Ir al directorio de yay
cd yay

# Construir el paquete
makepkg -si
```

Con esto, ya se debe poder utilizar `yay`
```bash
yay -S nombrePaquete
```

## Sin helper

Se pueden instalar paquetes de la [AUR](https://aur.archlinux.org/) sin usar un helper como `yay`, para ello hay que seguir los mismos pasos para instalar `yay`, pero cambiando el URL por el que uno desee.

Como ejemplo, se instala [LibreWolf](https://librewolf.net/).

```bash
# Descarga los archivos de la AUR
git clone https://aur.archlinux.org/packages/librewolf-bin

# Cambia el directorio a donde fue instalado el paquete
cd librewolf-bin

# Instala el paquete
makepkg -si
```


Volver a [ArchLinux](./ArchLinux.md).