# 🌟 STELLARGEN - Discord Generator Bot

<div align="center">
  <p>🚀 Un bot de Discord potente para la generación de cuentas y servicios.</p>
  <p>🌐 <i>A powerful Discord bot for account and service generation.</i></p>
</div>

---

## 📋 Índice / Table of Contents

- [Español (ES)](#-español-es)
  - [Descripción](#descripción)
  - [Características](#características)
  - [Requisitos](#requisitos)
  - [Instalación](#instalación)
  - [Configuración](#configuración)
  - [Comandos](#comandos)
- [English (EN)](#-english-en)
  - [Description](#description)
  - [Features](#features)
  - [Requirements](#requirements)
  - [Installation](#installation)
  - [Configuration](#configuration)
  - [Commands](#commands)

---

## 🇪🇸 Español (ES)

### Descripción
**STELLARGEN** es un bot de Discord diseñado para automatizar la entrega de cuentas y servicios. Utiliza una estructura modular de comandos y un sistema de archivos para gestionar el stock de forma sencilla.

### Características
- ⚡ **Generación Instantánea**: Entrega de cuentas directamente por mensaje privado.
- 📦 **Sistema de Stock**: Fácil gestión de cuentas mediante archivos `.txt`.
- 🛠️ **Arquitectura Modular**: Comandos organizados en carpetas para facilitar la expansión.
- 🌐 **Express Integration**: Incluye un servidor web básico para mantener el bot activo (Keep-Alive).

### Requisitos
- [Node.js](https://nodejs.org/) v12 o superior.
- Una cuenta de Discord y un Token de Bot (obtenido en [Discord Developer Portal](https://discord.com/developers/applications)).

### Instalación
1. Clona este repositorio o descarga los archivos.
2. Abre la terminal en la carpeta del proyecto.
3. Instala las dependencias:
   ```bash
   npm install
   ```

### Configuración
Edita el archivo `config.json` con tus credenciales:
```json
{
    "TOKEN": "TU_TOKEN_AQUÍ",
    "PREFIX": "$",
    "COOLDOWN": "5"
}
```

### Comandos
| Comando | Descripción |
| --- | --- |
| `$help` | Muestra la lista de comandos disponibles. |
| `$ping` | Comprueba la latencia del bot. |
| `$stock` | Muestra la cantidad de cuentas disponibles en cada categoría. |
| `$gen-[servicio]` | Genera una cuenta del servicio especificado (ej: `$gen-disney`). |

---

## 🇺🇸 English (EN)

### Description
**STELLARGEN** is a Discord bot designed to automate the delivery of accounts and services. It uses a modular command structure and a file-based system to manage stock easily.

### Features
- ⚡ **Instant Generation**: Delivers accounts directly via private message.
- 📦 **Stock System**: Easy account management using `.txt` files.
- 🛠️ **Modular Architecture**: Commands organized into folders for easy expansion.
- 🌐 **Express Integration**: Includes a basic web server to keep the bot active (Keep-Alive).

### Requirements
- [Node.js](https://nodejs.org/) v12 or higher.
- A Discord account and a Bot Token (obtained from the [Discord Developer Portal](https://discord.com/developers/applications)).

### Installation
1. Clone this repository or download the files.
2. Open the terminal in the project folder.
3. Install the dependencies:
   ```bash
   npm install
   ```

### Configuration
Edit the `config.json` file with your credentials:
```json
{
    "TOKEN": "YOUR_TOKEN_HERE",
    "PREFIX": "$",
    "COOLDOWN": "5"
}
```

### Commands
| Command | Description |
| --- | --- |
| `$help` | Shows the list of available commands. |
| `$ping` | Checks the bot's latency. |
| `$stock` | Shows the amount of available accounts in each category. |
| `$gen-[service]` | Generates an account for the specified service (e.g., `$gen-disney`). |

---

<div align="center">
  <p>Generador creado por <b>$MartoBossX#7777</b></p>
</div>
