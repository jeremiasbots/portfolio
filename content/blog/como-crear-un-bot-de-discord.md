+++
title = "¿Cómo crear un bot de Discord?"
author = "jeremiasbots/devep"
date = "2024-12-30"
description = "Creación de bot en Discord"
tags = [
    "discord",
    "javascript",
    "bot"
]
+++

Hola, hoy vamos a crear un bot de Discord usando JavaScript, para esto tenemos que asegurarnos de tener instalado Git en nuestra computadora y por supuesto Node.js.

## Creación del bot

Primero iremos a nuestra carpeta de proyectos y crearemos un nuevo directorio llamado bot:

```sh
mkdir bot
```

Después de haber creado el directorio, usaremos `cd bot` para ubicarnos allí e iniciaremos el proyecto con `npm init -y`, una vez hecho todo esto, podremos instalar discord.js y dotenv:

```sh
npm i dotenv discord.js
```

Una vez instalados `dotenv` y `discord.js`, crearemos un archivo index.js con el siguiente código:

```js
require("dotenv").config();
const { Client } = require("discord.js");
const client = new Client({ intents: 3276799 });

client.on("ready", () => {
  console.log("🤖 | Bot encendido");
});
```

Y crearemos un archivo `.env` en la misma ruta con el `"TOKEN"` de nuestro bot, atentos que el `"TOKEN"` se saca en https://discord.dev/ y ahí tendremos que crear el bot y después irnos a la sección que dice `Bot` y activar los tres intentos privilegiados. Una vez hecho eso, podremos crear nuestro archivo `.env` donde hay que reemplazar `<token del bot>` por nuestro token sacado de esa página.

```env
TOKEN=<token del bot>
```

¡Ya tenemos finaliziado nuestro bot de Discord y sólo nos falta usar `node index.js`! 🥳🎈

## Dudas

No se preocupe si no ha entendido cómo mantenerlo activo 24/7 o cómo sacar el `"TOKEN"`, pronto actualizaré este artículo para ser más detallado.
