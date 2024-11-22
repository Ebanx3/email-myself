# email-myself

## Descripción
Este servidor backend permite recibir mensajes a través de un endpoint, y lo autoenvía hacia el correo asociado.

## Funcionalidad
- **Recepción de datos**: El servidor recibe datos a través de un endpoint POST.
- **Reenvío de correos**: Utiliza Nodemailer para enviar los correos electrónicos recibidos a la dirección especificada.

## Instalación
1. Clona el repositorio:
    ```sh
    git clone https://github.com/yourusername/email-reenviador-api.git
    ```
2. Instala las dependencias:
    ```sh
    cd email-reenviador-api
    npm install
    ```
3. Configura las variables de entorno:
    ```env
    EMAIL_SERVICE=smtp.example.com
    EMAIL_PORT=587
    EMAIL_USER=your-email@example.com
    EMAIL_PASS=your-email-password
    ```

## Uso
1. **Iniciar el servidor**:
    ```sh
    npm start
    ```
2. **Enviar datos**:
    ```sh
    curl -X POST -H "Content-Type: application/json" -d '{"message": "Hola", "email": "destinatario@example.com"}' http://localhost:3000/send-email
    ```
