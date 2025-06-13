# Redireccionador de emails

Servidor hecho con nodejs, cors, express, resend y redis.

## Uso
1️⃣ Registro de URL y Email
Visita la ruta / en tu navegador y completa los campos en el formulario HTML.

2️⃣ Enviar Emails
Desde la URL registrada, envía una solicitud POST al servidor con el siguiente formato:

~~~
{
  "from": "Portfolio",
  "subject": "Recibiste un mensaje en tu portfolio",
  "html": "<h2>Recibiste un mensaje de ${email}</h2><br><p>Este es un mensaje desde el formulario de contacto.</p>"
}
~~~

✅ El servidor redireccionará automáticamente este email al correo previamente registrado.


## 🛠 Tecnologías Usadas
- Node.js ⚡
- Express.js 🚀
- Redis 🏃‍♂️
- Sender ✉️