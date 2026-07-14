# Dotfiles

Configuración personal administrada con Chezmoi.

## Requisitos

- Git
- Curl

## Instalación

> [!WARNING]
> `--apply` instala inmediatamente todos los archivos administrados y puede
> reemplazar configuraciones existentes en el directorio personal. Revisa o
> respalda tus archivos actuales antes de continuar.

Instala Chezmoi, clona este repositorio y aplica toda la configuración:

```bash
sh -c "$(curl -fsLS https://get.chezmoi.io)" -- \
  init --apply https://github.com/vanhertz/dotfiles.git
```

Si Chezmoi ya está instalado:

```bash
chezmoi init --apply https://github.com/vanhertz/dotfiles.git
```

La URL identifica el repositorio remoto, no el usuario local. Chezmoi aplica
los archivos en el directorio personal de quien ejecuta el comando. Para usar
un fork, reemplaza la URL por la del repositorio correspondiente.

Para descargar y aplicar cambios posteriores:

```bash
chezmoi update
```

## Contenido

- Git
- Bash
- Fish
- Kitty
- Ghostty
- Fastfetch
- Btop
- Neovim
- KDE Plasma
- Starship

## Licencia

GLP-3.0
