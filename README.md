# Redireccionador de emails

Servidor hecho con nodejs, cors, express, resend y redis.

## Funcionalidad:
- Primer paso registrar email y url de la frontend desde la cual se desean enviar los emails en []()

    Recibe emails desde el frontend registrado, teniendo en el cuerpo de la petición (body), de la forma =>
    ~~~
        {
            from: string,
            subject: string,
            html: string o html
        }
    ~~~
    y los redirecciona a el email registrado
