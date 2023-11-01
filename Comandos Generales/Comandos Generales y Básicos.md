Volver al [README](../README.md)

Aquí irán guías con comandos básicos que deberían ser aplicables para cualquier distribución y que son importante recordar.

# Usuarios y permisos

Para cambiar de un usuario a otro se usa `su nombreUsuario`, por ejemplo: 

```bash
# Cambia el usuario a nekoarcho
su nekoarch

# Cambia el usuario a root
su root
```

Normalmente el usuario `root` tiene todos los permisos, pero no es recomendable hacer cosas con dicho usuario, por eso se utiliza alguno otro, sin embargo, cuando se necesitan permisos especiales se debe utilizar el comando `sudo` al comienzo, por ejemplo, en [ArchLinux](../Distribuciones/ArchLinux/ArchLinux.md) se puede actualizar el sistema completo con `pacman -Syu`, pero si el usuario no tiene permisos tiene que ser `sudo pacman -Syu`.

# Usar un AppImage

Para usar un archivo AppImage, normalmente hay que hacerlo ejecutable antes de ejecutarlo.

```bash
# Darle permisos y hacerlo ejecutable
# Asume que el usuario es distinto al root
sudo chmod +x NombreArchivo.AppImage

# Ejecutar Archivo
./NombreArchivo.AppImage
```
