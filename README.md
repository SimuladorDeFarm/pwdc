# pwdc

## Descripción rápida

`pwdc` ("pwd + copy") muestra en pantalla la ruta absoluta del directorio actual (o de la ruta que le indiques) y la copia automáticamente al portapapeles, detectando la herramienta de clipboard disponible en tu sistema.

## Requisitos

- Bash
- Linux con alguna de estas herramientas de portapapeles (basta con una):
  - `wl-clipboard` (Wayland)
  - `xclip` o `xsel` (X11)
- También funciona en macOS (`pbcopy`), WSL (`clip.exe`) y Termux (`termux-clipboard-set`).

## Instalación

```bash
git clone https://github.com/SimuladorDeFarm/pwdc.git
cd pwdc
chmod +x pwdc
```

### Mover al PATH para ejecutar desde cualquier lugar

**Opción 1 (recomendada): `~/.local/bin`**

```bash
mkdir -p ~/.local/bin
mv pwdc ~/.local/bin/
```

Asegúrate de que `~/.local/bin` esté en tu `PATH` (agrega esto a tu `~/.bashrc` o `~/.zshrc` si no lo está):

```bash
export PATH="$HOME/.local/bin:$PATH"
```

**Opción 2: `/usr/local/bin` (requiere sudo)**

```bash
sudo mv pwdc /usr/local/bin/
```

## Guía de uso

```bash
pwdc              # copia y muestra el directorio actual
pwdc /ruta/dir    # copia y muestra la ruta absoluta de /ruta/dir
pwdc archivo.txt  # copia y muestra la ruta absoluta de un archivo
pwdc -h           # ayuda
pwdc -v           # versión
```
