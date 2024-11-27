<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>email-myself</title>
    <style>
        img {
            max-width: 100%; /* Ajuste automático del tamaño de las imágenes */
            height: auto;
        }
    </style>
</head>
<body>
    <h1>email-myself</h1>

    <h2>Descripción</h2>
    <p>Este servidor backend permite recibir mensajes a través de un endpoint, y lo autoenvía hacia el correo asociado.</p>

    <h2>Funcionalidad</h2>
    <ul>
        <li><strong>Recepción de datos</strong>: El servidor recibe datos a través de un endpoint POST.</li>
        <li><strong>Reenvío de correos</strong>: Utiliza Nodemailer para enviar los correos electrónicos recibidos a la dirección especificada.</li>
    </ul>

    <h2>Instalación</h2>
    <ol>
        <li>Clona el repositorio:
            <pre><code>git clone https://github.com/Ebanx3/email-myself.git</code></pre>
        </li>
        <li>Instala las dependencias:
            <pre><code>cd email-myself
npm install</code></pre>
        </li>
        <li>Configura las variables de entorno:
            <pre><code>EMAIL_SERVICE=smtp.example.com
EMAIL_PORT=587
EMAIL_USER=your-email@example.com
EMAIL_PASS=your-email-password</code></pre>
        </li>
    </ol>

    <h2>Uso</h2>
    <ol>
        <li><strong>Iniciar el servidor</strong>:
            <pre><code>node --run start</code></pre>
        </li>
    </ol>

    <h2>Endpoints</h2>
    <p>Este servidor ofrece dos endpoints principales:</p>
    <ol>
        <li><strong>/status</strong>
            <ul>
                <li><strong>Descripción</strong>: Endpoint para verificar si el servidor está activo.</li>
                <li><strong>Método</strong>: <code>GET</code></li>
                <li><strong>Respuesta</strong>: Retorna un mensaje indicando el estado del servidor.</li>
            </ul>
        </li>
        <li><strong>/redirectEmail</strong>
            <ul>
                <li><strong>Descripción</strong>: Endpoint para recibir y redirigir correos electrónicos.</li>
                <li><strong>Método</strong>: <code>POST</code></li>
                <li><strong>Body</strong>: Debe incluir los siguientes campos en formato JSON:
                    <pre><code>{
    "email": "destinatario@example.com",
    "message": "Este es el contenido del mensaje."
}</code></pre>
                </li>
            </ul>
        </li>
    </ol>

    <h2>Guía para uso con gmail</h2>
    <ul>
        <li>Acceder al enlace <a href="https://myaccount.google.com/signinoptions/twosv">gmail</a> y activar la verificación en dos password.</li>
        <li>En la misma página, al final, acceder a Contraseñas de aplicación.</li>
        <li><img src="https://res.cloudinary.com/dupcvyc8l/image/upload/v1732673654/email-myself/imagen_2024-11-26_231411361_ysozm3.png" alt="contraseñas de aplicacion"></li>
        <li><img src="https://res.cloudinary.com/dupcvyc8l/image/upload/v1732673771/email-myself/imagen_2024-11-26_231609781_gtilqf.png" alt="nombre aplicación"></li>
        <li>Copiar la contraseña que aparece a continuación.</li>
        <li><img src="https://res.cloudinary.com/dupcvyc8l/image/upload/v1732673859/email-myself/imagen_2024-11-26_231737151_ap8e3e.png" alt="contraseña"></li>
        <li>Una vez clonado completar las variables de entorno:
            <pre><code>EMAIL_ADDRESS=&lt;el email con el que creaste la aplicación&gt;
EMAIL_APP_PASSWORD=&lt;la contraseña copiada anteriormente&gt;
EMAIL_SERVICE=smtp.gmail.com
EMAIL_PORT=465</code></pre>
        </li>
        <li>Una ves colocadas las variables de entorno ejecutar en local o hacer deploy y debería estár funcionando.</li>
    </ul>
</body>
</html>
