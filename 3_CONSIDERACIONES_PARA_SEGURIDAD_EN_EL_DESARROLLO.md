# 3. Consideraciones para seguridad en el desarrollo

## 3.1. Uso de librerías y frameworks de seguridad

Para un desarrollo seguro es necesario seleccionar librerías y frameworks confiables, teniendo en cuenta que tiene un desarrollo y mantenimiento activo, para que sean ampliamente utilizadas por los programadores, es importante tener un control sobre las librerías y frameworks con la intención de tener las versiones más actualizadas o en su defecto las más estables. 

La mayoría de frameworks nos indican ciertos puntos sobre cómo solucionar algún problema en específico que ya había ocurrido anteriormente en el desarrollo de software. Por lo regular se recurre a optar por el uso de frameworks que se enfocan en atender distintas áreas como la seguridad como el control de acceso, el cifrado y la validación de entradas, etc.

## 3.2. Consultas seguras a las bases de datos

Las vulnerabilidades pueden llegar hacer por una inyección SQL qué ocurre cuando datos no confiables son insertados en una consulta SQL. Este tipo de ataques permite al enemigo extraer, modificar o eliminar información desde la base de datos, e incluso llegar a tomar el control del sistema.

Para prevenir este tipo de ataques se deben tomar ciertas medidas de protección a la información que ayuden a:

### 3.2.**1.** **Limitar el acceso a la base de datos:**

Cuando muchas personas tienen intervención, el resultado no puede ser positivo, esto ocurre con los accesos a las bases de datos, por eso cuanto más acotados los permisos y privilegios, se tiene un mejor control.

### 3.2.**2.** **Identifica los datos sensibles:**

Antes de pensar en utilizar alguna técnica o herramienta de protección, es necesario saber cuál es la información importante que se debe proteger. Así que es importante entender la lógica para poder definir una buena base de datos, y llegar a poder determinar dónde y cómo podemos almacenar los datos sensibles. La única forma de tener una buena administración es tener conocimiento de la base de datos que se desarrolla. 

### 3.2.**3.** **Monitorear la actividad de la base de datos:**

Estar atento es importante para poder registrar las acciones y movimientos que se realizan sobre los datos para saber quién ha manipulado la información. Tener un historial de las operaciones va a ayudar a comprender todo lo que se realiza, modifica en la base de datos y así se podrá evitar robo de información, cambios malintencionados y ****detectar acciones sospechosas.

### 3.2.**4.** **Cifrar la información:**

Una vez que se identifican los datos sensibles y/o la información confidencial, una buena práctica es utilizar métodos que puedan cifrar estos datos.

Cuando un atacante encuentra alguna vulnerabilidad y logra tener acceso al sistema, se sabe que a lo primero a lo que él accede es a la base de datos, ya que se tiene mucha información importante, la mejor manera de cuidar estos datos es volverla ilegible para cualquier persona. 

### 3.2.**5.** **Soluciones de seguridad:**

Un buen análisis puede ayudar a detectar las vulnerabilidades que se tienen en el sistema, encontrando así los riesgos y poder establecer un plan de prevención y un plan de recuperación de la información ante desastres que el atacante pueda llegar hacer, por lo que el administrador de la base de datos debe mantener y asegurar la información.

## 3.3. Codificar y escapar los datos

Estas llegan hacer técnicas que evitan ataques de terceros, pues esta consiste en transformar algunos caracteres especiales en otros caracteres equivalentes que puedan ser entendidos fácilmente para el intérprete.

Escapar caracteres también llega hacer muy parecido a codificar los datos, con la diferencia de que en lugar de reemplazar un carácter por otro, se añade un carácter antes del dato a escapar, para evitar una mal interpretación.

Se debe tomar en cuenta que se debe considerar como inseguros los datos que se ingresen fuera de la aplicación, así como también los datos que provienen desde la base de datos todo esto por si algún atacante hizo alguna modificación de los datos, por eso deben ser correctamente codificados y escapados los datos.

## 3.4. Validación de datos

La validación de datos ayuda a garantizar que todos los datos que se ingresen en la aplicación sean correctos, es decir que sean, precisos, seguros y consistentes. Esto se logra a través de funciones que realizan las debidas validaciones para las entradas de datos.

Es una buena práctica asegurar que solo los datos que se ingresaron correctamente podrán se registren en la aplicación. Por ejemplo, si se espera que en un campo se puedan ingresar solo dígitos numéricos, no se deben aceptar cualquier otro tipo de caracteres.

Algunos de los tipos de validación de datos incluyen:

- Validación de código
- Validación de tipo de datos
- Validación del rango de datos
- Validación de restricciones

## 3.5. Implementar mecanismos de autenticación seguros

Para poder proteger la identidad de los usuarios cuando se realice alguna acción, se debe identificarse, autenticarse y estar autorizado, haciendo uso de algún método donde pueda registrarse. Se debe saber que:

- **La autenticación:**

Se define como aquel proceso mediante el cual un usuario obtiene acceso a los recursos de un sistema a través de una identificación.

- **La autorización**

Consiste en designar los recursos que estarán permitidos al usuario acceder de un sistema, si bien, ya se encuentra autenticado, no significa que tendrá el acceso completo del sistema.

La autenticación hace referencia a la acción de verificar que una persona es quien dice ser. Se pueden utilizar varios mecanismos como lo son: 

- **Contraseñas:**

Las aplicaciones deben exigir al usuario el uso de una buena contraseña, también se deben implementar mecanismos para la recuperación de contraseñas, ya sea utilizando algún medio como un correo electrónico o mensajes.

También se debe implementar algún método donde solo el usuario tenga un límite de intentos de inicio de sesión, ya sea bloqueando las cuentas después de un cierto número de intentos fallidos, y no se debe llegar a bloquear permanentemente las cuentas, ya que podría traer problemas con los usuarios reales de las cuentas donde se quiso ingresar sin su consentimiento. 

- **Multifactor**

Esta es otra manera donde se requiere varios métodos de autenticación para comprobar la identidad de un usuario. Comúnmente se usa una combinación de dos o más factores como lo son: las contraseñas, tokens de seguridad, o mediante el uso de verificación biométrica que permite crear una mejor seguridad que dificulta que un atacante acceda fácilmente al sistema, o una base de datos etc. Si en un factor se logra ingresar, al menos el atacante tendría una o más barreras que romper antes de entrar con éxito en el objetivo.

- **Autenticación criptográfica**

La autenticación con cifrado es la manera donde se puede tener una comunicación segura. Ya que ayuda a garantizar que el origen de donde salen los datos y el destino a donde llegan sean seguras. Esto consiste en codificar la comunicación en el origen y decodificarla cuanto esta llega a su destino. El cifrado impide que los atacantes puedan interceptar cualquier información que sea transmitida.

## 3.6. Implementar mecanismos de manejo de sesión

El manejo de la sesión es uno de los aspectos críticos de la seguridad. Los objetivos principales son: 

- Los usuarios autenticados tengan un mejor control con sus sesiones.
- Se cumplan los medios de autorización cuando se requiera ingresar el usuario.
- Se prevengan los ataques, como lo es ingresar a  sesiones activas que no fueron cerradas correctamente.

**Algunas vulnerabilidades que pueden ocurrir si no se implementan de forma correcta los mecanismos pueden ser:** 

- Fijación de sesión donde el atacante obtiene el identificador de sesión de otra persona y puede ingresar.
- Manejo de la información de sesión errónea, por no implementar un buen control en las sesiones, el atacante puede obtener datos de la sesión de otro usuario.

Para el manejo de las sesiones, se debe considerar al menos lo siguiente:

- Al iniciar sesión el identificador de sesión debe ser único.  ****
- Se deben generar otro identificador de sesión cuando este inicie sesión.
- Se tiene que terminar la sesión del usuario por inactividad.

## 3.7. Datos en reposo

Debemos siempre tratar de proteger la información del usuario, ya que a veces se requieren medios de protección dependiendo el estado en el que se encuentre la información, con esto se refiere a la información que no está siendo accedida, usada y que se encuentra guardada.

Es por eso que se debe evitar, cuando sea posible, el almacenamiento de datos sensibles por
parte de la aplicación. En caso de que no se pueda evitar almacenar datos sensibles, estos deben ser protegidos mediante encriptación, para prevenir la modificación o acceso no autorizado.

## 3.8. Desarrollo orientado a pruebas

El equipo de desarrollo deberá tener un set de datos no válidos, escogido para trabajar y cargar el sitio para efectos de pruebas de integración continua o unitarias. Este set no debe contener información real y la cantidad de datos debe ser reducida, pero suficiente para generar pruebas.

## 3.9. Calidad de código

Algo muy importante dentro del desarrollo de software es la calidad del código; los estándares se encuentran constantemente presentes en la vida cotidiana, son importantes para mantener un orden en las cosas y en el desarrollo no es la excepción. 

Los estándares de código son una serie de reglas definidas para un lenguaje de programación, o bien, un estilo de programación específico. El estilo garantiza que todos los que contribuyen en un proyecto tengan una forma única de diseñar su código, lo que da como resultado una base de código coherente, asegurando una fácil lectura y mantenimiento.

Algunas consideraciones a tomar en cuenta son: 

- Tomar como base estándares oficialmente publicados de las herramientas que se utilizan en cada proyecto.
- Para obtener un código de fácil lectura es necesario poner atención al estilo del mismo como segmentos de código, correcto uso de indentación, longitud de líneas y espacios entre ellas.
- Asignación correcta de nombres en variables, funciones, etc.
- Establecer límites en complejidad o longitud de funciones.

## 3.10. Manejo seguro de errores y excepciones

Se debe desarrollar el sistema, de forma tal, que aplique el principio de “fallar seguro”, es decir:

- No exponer información sensible o privada en los mensajes de error. En particular, nunca olvidar desactivar el modo debug al pasar a producción.
- Asegurarse de que una excepción o fallo no comprometa la seguridad por un error de programación en el sistema. Por ejemplo, causar una denegación de servicio o ejecución de código con privilegios incorrectos.
- Registrar las excepciones adecuadamente en los sistemas que correspondan.