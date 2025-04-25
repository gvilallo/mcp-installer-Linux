# Guía de instalación de MCP Installer para Linux
by gvilallo

A continuación, te presento una guía paso a paso para instalar y publicar el adaptador MCP Installer para Linux.
Instalación del MCP Installer en Linux
## Requisitos previos
Node.js versión 20 o superior
npm (incluido con Node.js)
Git
## Pasos de instalación
Actualizar Node.js (si tu versión es inferior a 20)
 bash
# Instalar n (gestor de versiones de Node.js)
sudo npm install -g n

# Instalar la última versión estable
sudo n stable

# Verificar la versión instalada
node --version


## Clonar el repositorio
 bash
git clone https://github.com/gvilallo/mcp-installer-linux.git
cd mcp-installer-linux


## Instalar el paquete globalmente
 bash
npm install -g .


## Verificar la instalación
 bash
which mcp-installer
  Debería mostrar algo como: /usr/local/bin/mcp-installer


## Configurar Claude Desktop
Abrir o crear el archivo de configuración:
 bash
mkdir -p ~/.config/Claude
nano ~/.config/Claude/claude_desktop_config.json


## Añadir la configuración del MCP:
 json
{
  "mcpServers": {
    "mcp-installer-linux": {
      "command": "/usr/local/bin/mcp-installer",
      "args": []
    }
  }
}


## Reiniciar Claude Desktop
Cierra completamente Claude Desktop
Abre nuevamente la aplicación

