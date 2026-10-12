Ejercicio 1: El botón reutilizable
¿Por qué el nombre de una etiqueta propia debe llevar guion?

R: Para evitar conflictos con futuras etiquetas oficiales de HTML. El estándar de la W3C exige incluir un guion como el <mi-boton> para que el navegador identifique de inmediato que es un componente creado por ti y no un elemento nativo.

Ejercicio 2: La tarjeta de producto
1. Manejo de tipos en los atributos:

Ya que el DOM siempre lee los atributos HTML como texto (string), es obligatorio convertir manualmente los valores numéricos (como precio o existencia) usando métodos como Number() o parseFloat() antes de realizar cálculos dentro del componente.

2. Propagación de eventos personalizados y Shadow DOM:

Los eventos personalizados creados dentro de un Shadow DOM no salen al exterior por sí solos. Para que el evento "agregar" cruce esa barrera y llegue hasta el contenedor principal, debes emitirlo activando { bubbles: true, composed: true }. Sin el parámetro composed: true, el evento se queda atrapado en la tarjeta de forma silenciosa, evitando que el contador reaccione.