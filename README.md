# STELLARGEN — Bot generador para Discord

[![Node.js](https://img.shields.io/badge/Node.js-12%2B-339933?logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![discord.js](https://img.shields.io/badge/discord.js-bot-5865F2?logo=discord&logoColor=white)](https://discord.js.org/)
[![Express](https://img.shields.io/badge/Express-keep--alive-000000?logo=express&logoColor=white)](https://expressjs.com/)
[![GPL-3.0](https://img.shields.io/badge/Licencia-GPL--3.0-blue)](LICENSE)

[Español](#español) · [English](#english)

---

## Español

### Índice

- [Descripción](#descripción)
- [Características](#características)
- [Requisitos](#requisitos)
- [Instalación](#instalación)
- [Configuración](#configuración)
- [Comandos](#comandos)
- [Estructura del proyecto](#estructura-del-proyecto)
- [Seguridad](#seguridad)
- [Licencia](#licencia)

### Descripción

**STELLARGEN** automatiza la entrega de cuentas y servicios desde Discord. Los comandos están organizados en módulos independientes y el stock vive en archivos de texto, de modo que añadir un servicio nuevo es copiar un comando y crear su `.txt`.

### Características

- **Generación instantánea**: entrega la cuenta por mensaje privado al usuario que ejecuta el comando.
- **Sistema de stock por archivos**: un `.txt` por servicio en `accounts/`.
- **Arquitectura modular**: un archivo por comando en `commands/`, cargados dinámicamente.
- **Keep-alive con Express**: un servidor HTTP mínimo para que el proceso no se duerma en hostings gratuitos.
- **Comprobación de stock** antes de generar, para no prometer lo que no hay.

### Requisitos

- **Node.js 12 o superior**.
- Una cuenta de Discord y un **token de bot** del [Discord Developer Portal](https://discord.com/developers/applications).
- Permisos de **bot** y de envío de mensajes directos en el servidor.

### Instalación

```bash
git clone https://github.com/alberto2005-coder/Discordbot_generador.git
cd Discordbot_generador
npm install
npm start
```

### Configuración

Edita `config.json`:

```json
{
  "TOKEN": "TU_TOKEN_AQUI",
  "PREFIX": "$",
  "COOLDOWN": "5"
}
```

| Clave | Para qué |
|---|---|
| `TOKEN` | Token del bot |
| `PREFIX` | Prefijo de los comandos de texto |
| `COOLDOWN` | Segundos de espera entre generaciones por usuario |

Para añadir un servicio, crea `accounts/<servicio>.txt` con una cuenta por línea y su comando `commands/gen-<servicio>.js` clonando uno existente.

### Comandos

| Comando | Descripción |
|---|---|
| `$help` | Lista los comandos disponibles |
| `$ping` | Comprueba la latencia del bot |
| `$stock` | Muestra las cuentas disponibles por categoría |
| `$gen-<servicio>` | Entrega una cuenta del servicio indicado por MD |

Servicios incluidos como ejemplo: `disney`, `hbo`, `paramount`, `star+`, `crunchyroll`, `funimation`, `duolingo`, `roblox` y `steam`.

### Estructura del proyecto

```text
Discordbot_generador/
├── index.js            # Arranque, carga de comandos y servidor keep-alive
├── config.json         # Token, prefijo y cooldown
├── commands/
│   ├── help.js · ping.js · stock.js
│   └── gen-<servicio>.js
├── accounts/
│   └── <servicio>.txt  # Stock, una cuenta por línea
├── package.json
├── LICENSE
└── README.md
```

### Seguridad

- **Nunca** subas `config.json` con un token real ni archivos de `accounts/` con cuentas válidas: cualquiera con acceso al repositorio puede usarlas. Mantenlos fuera de git (`.gitignore`) y sírvelos desde variables de entorno o un almacén privado.
- Si un token o unas credenciales ya se han publicado, considéralos comprometidos: regenera el token y cambia las contraseñas.
- Limita el comando de generación a roles o canales concretos y registra quién canjea cada cuenta.

### Licencia

**GNU General Public License v3.0 (GPL-3.0)** — consulta [LICENSE](LICENSE).

---

## English

### Table of contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Configuration](#configuration)
- [Commands](#commands)
- [Project structure](#project-structure)
- [Security](#security)
- [License](#license)

### Overview

**STELLARGEN** automates account and service delivery from Discord. Commands live in independent modules and stock lives in text files, so adding a new service means copying a command and dropping in its `.txt`.

### Features

- **Instant delivery**: the account is sent by direct message to whoever runs the command.
- **File-based stock**: one `.txt` per service under `accounts/`.
- **Modular architecture**: one file per command in `commands/`, loaded dynamically.
- **Express keep-alive**: a tiny HTTP server so the process does not sleep on free hosts.
- **Stock check** before generating, so nothing is promised that is not available.

### Requirements

- **Node.js 12 or later**.
- A Discord account and a **bot token** from the [Discord Developer Portal](https://discord.com/developers/applications).
- **bot** scope and permission to send direct messages.

### Installation

```bash
git clone https://github.com/alberto2005-coder/Discordbot_generador.git
cd Discordbot_generador
npm install
npm start
```

### Configuration

Edit `config.json`:

```json
{
  "TOKEN": "YOUR_TOKEN_HERE",
  "PREFIX": "$",
  "COOLDOWN": "5"
}
```

| Key | Purpose |
|---|---|
| `TOKEN` | Bot token |
| `PREFIX` | Text command prefix |
| `COOLDOWN` | Seconds between generations per user |

To add a service, create `accounts/<service>.txt` with one account per line and its `commands/gen-<service>.js` cloned from an existing one.

### Commands

| Command | Description |
|---|---|
| `$help` | Lists the available commands |
| `$ping` | Reports bot latency |
| `$stock` | Shows available accounts per category |
| `$gen-<service>` | Sends one account for that service over DM |

Bundled examples: `disney`, `hbo`, `paramount`, `star+`, `crunchyroll`, `funimation`, `duolingo`, `roblox` and `steam`.

### Project structure

```text
Discordbot_generador/
├── index.js            # Bootstrap, command loading and keep-alive server
├── config.json         # Token, prefix and cooldown
├── commands/
│   ├── help.js · ping.js · stock.js
│   └── gen-<service>.js
├── accounts/
│   └── <service>.txt  # Stock, one account per line
├── package.json
├── LICENSE
└── README.md
```

### Security

- **Never** commit `config.json` with a real token or `accounts/` files with valid credentials: anyone with repository access can use them. Keep them out of git (`.gitignore`) and serve them from environment variables or a private store.
- If a token or credentials were already published, treat them as compromised: regenerate the token and rotate the passwords.
- Restrict the generation command to specific roles or channels and log who redeems each account.

### License

**GNU General Public License v3.0 (GPL-3.0)** — see [LICENSE](LICENSE).
