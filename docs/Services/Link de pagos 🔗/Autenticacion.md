---
stoplight-id: nc0wxf4bfdoc0
---

# Autenticacion

Para interactuar con la API de Link de pagos utiliza una autenticación similar a la de 
[Checkout](https://docs.placetopay.dev/checkout/authentication) para lograr identificar y validar que tus operaciones sean seguras 

## Credenciales

Para lograr autenticarte debes contar con tus credenciales `login` y `secretKey`.

- **login:** Identificador del sitio, puede considerarse público pues viaja como dato plano en las peticiones API.
- **secretKey:** Llave secreta del sitio, debe ser privada, a partir de este dato se generará un nuevo `tranKey` que será enviado en las peticiones.

### Como generar una autenticacion?

Debes conocer y preparar los siguientes datos:

- **login:** Credencial login provista al inicar tu integración. Identificador del sitio.

- **secretKey:** Credencial secretKey provista al iniciar tu integración. Llave secreta del sitio.

- **seed:** Se trata de la fecha en la que se generó la autenticación. La fecha debe estar en formato ISO 8601. `Ejemplo: 2023-06-21T09:56:06-05:00`

- **nonce:** Valor arbitrario que identifica a una petición cómo única. Se genera y se utiliza para otras operaciones. Al momento de enviarlo, debe ser codificado en base 64. `Ejemplo: base64('927342197')`

- **tranKey:** Se genera en cada solicitud de forma programática. Se genera con la siguiente fórmula `Base64(SHA-256(nonce + seed + secretKey))` esta fórmula debe ser traducida según el lenguaje de programación utilizado.