# Actividad2
## Template para Actividad 2

```
docker build -t pw-generator-app .
docker run -p 3000:3000 pw-generator-app

```

## Sobre la actividad

**Restricciones:**

Duración: 90 minutos.

Máximo grupos de tres alumnos.

**Descripción:**

Usted se encuentra dándole mantenimiento a una aplicación la cual tiene como objetivo permitirles hashear contraseñas a múltiples usuarios. La aplicación nace como un front end gratuito donde el usuario digita su contraseña y se le retorna un hash seguro.

Actualmente, debido a su gran potencial, su aplicación es solicitada por una gran empresa en el mercado para ser utilizada en el flujo de registro de usuarios.

Dicha empresa, utiliza el siguiente curl para generar los hash:

curl --location url/create-user' \\

\--header 'Content-Type: application/json' \\

\--data '{

"CI" : 12345,

"Name" : "pepe",

"Password": "MiPwSecr3ta"

}'

Esta empresa reporta que, al empezar a utilizar dicha aplicación en parte de su flujo productivo, muchas de las request fallan o demoran demasiado.


**Consigna:**

Esta entrega no requiere código fuente como entregable por lo cual <mark>se deberá generar un archivo pdf con capturas y respuestas de cada punto el cual debe ser entregado por las aulas</mark>.

**Parte 1: Despliegue y Monitoreo de la Aplicación**

- Despliegue la aplicación dockerizada en Elastic Beanstalk. Adjunte capturas del dashboard de Elastic Beanstalk y los resultados de una solicitud.
- Configure una conexión con New Relic para monitorizar la aplicación y vuelva a desplegarla. Adjunte capturas de la configuración de la conexión y las métricas iniciales obtenidas.
- Seleccione un tipo de prueba de rendimiento adecuado, justificando su elección, y genere un script de K6 para correr sobre la API desde su navegador. La prueba debe validar que el tiempo de respuesta P(95) sea inferior a 2500 ms y que fallen menos del 1% de las solicitudes. Adjunte el script, capturas de los resultados y registros en New Relic.
- Obtenga logs de aplicación utilizando CloudWatch y sugiera mejoras si es necesario. Puede complementarlo con capturas de código ajustadas.

**Parte 2: Optimización de Tiempos de Respuesta**

Su cliente se queja de los tiempos de respuesta que afectan la creación de usuarios. Aunque se ha intentado mejorar el algoritmo de hash, no es posible reducir los tiempos sin comprometer la seguridad, sin escalar verticalmente la aplicación. Proponga una nueva arquitectura que garantice tiempos de respuesta óptimos sin sacrificar la seguridad.