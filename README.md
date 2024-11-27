# email-myself

## Descripción
Este servidor backend permite recibir mensajes a través de un endpoint, y lo autoenvía hacia el correo asociado.

## Funcionalidad
- **Recepción de datos**: El servidor recibe datos a través de un endpoint POST.
- **Reenvío de correos**: Utiliza Nodemailer para enviar los correos electrónicos recibidos a la dirección especificada.

## Instalación
1. Clona el repositorio:
    ```sh
    git clone https://github.com/Ebanx3/email-myself.git
    ```
2. Instala las dependencias:
    ```sh
    cd email-myself
    npm install
    ```
3. Configura las variables de entorno:
    ```env
    EMAIL_SERVICE=smtp.example.com
    EMAIL_PORT=587
    EMAIL_ADDRESS=your-email@example.com
    EMAIL_APP_PASSWORD=your-email-password
    ```

## Uso
1. **Iniciar el servidor**:
    ```sh
    node --run start
    ```

## Endpoints
Este servidor ofrece dos endpoints principales:

1. **`/status`**
   - **Descripción**: Endpoint para verificar si el servidor está activo.
   - **Método**: `GET`
   - **Respuesta**: Retorna un mensaje indicando el estado del servidor.

2. **`/redirectEmail`**
   - **Descripción**: Endpoint para recibir y redirigir correos electrónicos.
   - **Método**: `POST`
   - **Body**: Debe incluir los siguientes campos en formato JSON:
     ```json
     {
       "email": "destinatario@example.com",
       "message": "Este es el contenido del mensaje."
     }
     ```

## Guía para uso con gmail
* Acceder al enlace [gmail](https://myaccount.google.com/signinoptions/twosv) y activar la verificación en dos pasos.
* En la misma página, al final, acceder a Contraseñas de aplicación.
<img src="https://res.cloudinary.com/dupcvyc8l/image/upload/v1732673654/email-myself/imagen_2024-11-26_231411361_ysozm3.png" style="width:60%;height:auto;margin:auto;"/>
<img src="https://res.cloudinary.com/dupcvyc8l/image/upload/v1732673771/email-myself/imagen_2024-11-26_231609781_gtilqf.png" style="width:60%;height:auto;margin:auto;"/>
* Copiar la contraseña que aparece a continuación
<img src="https://res.cloudinary.com/dupcvyc8l/image/upload/v1732673859/email-myself/imagen_2024-11-26_231737151_ap8e3e.png" style="width:60%;height:auto;margin:auto;"/>

* Una vez clonado, completa las variables de entorno:
```env
    EMAIL_ADDRESS=<el email con el que creaste la aplicación>
    EMAIL_APP_PASSWORD=<la contraseña copiada anteriormente>
    EMAIL_SERVICE=smtp.gmail.com
    EMAIL_PORT=465
```

* Una vez colocadas las variables de entorno, ejecutar en local o hacer deploy y debería estar funcionando.