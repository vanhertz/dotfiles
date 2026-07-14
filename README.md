# Dotfiles

Configuración personal administrada con Chezmoi.

## Requisitos

### Esenciales

- Linux
- Git, para clonar el repositorio y los plugins de Zsh
- Curl, para ejecutar el instalador de Chezmoi
- Zsh 5.1 o posterior
- Locale `es_CL.UTF-8` disponible en el sistema
- Conexión a Internet durante la instalación y el primer inicio de Zsh

### Integraciones de la configuración

- Kitty con una sesión Wayland
- Powerlevel10k instalado en `~/.powerlevel10k`
- `wl-clipboard`, utilizado para copiar selecciones de la línea de Zsh
- FZF, necesario para la integración interactiva; su ausencia no impide
  iniciar Zsh

La configuración también establece Vim, Neovim, Firefox y Kitty como
aplicaciones preferidas, y contiene alias para Wget, Plocate y lf. Estas
aplicaciones solo son necesarias al utilizar sus funciones correspondientes.

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

- Configuración básica de Bash
- Entorno compartido de shell con rutas XDG, locale y aplicaciones preferidas
- Alias compartidos para comandos y aplicaciones
- Configuración completa de Zsh:
  - Entorno mediante `ZDOTDIR`
  - Historial y autocompletado
  - Navegación, selección, borrado, copia y pegado de texto
  - Integración con FZF
  - Gestor ligero de plugins
  - z.lua
  - zsh-vi-mode
  - zsh-defer
  - zsh-autosuggestions
  - fast-syntax-highlighting
  - dotbare
- Powerlevel10k y su configuración de prompt
- Kitty con tema Catppuccin, backend Wayland y atajos integrados con Zsh

## Licencia

GLP-3.0
