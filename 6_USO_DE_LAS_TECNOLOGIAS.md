# 6. Uso de las tecnologías

## 6.1. Lenguaje

Existen una inmensa variedad de lenguajes de programación que podemos elegir para satisfacer distintas necesidades. Si bien es cierto que muchos de ellos se pueden utilizar en diferentes ámbitos, siempre suele haber algún lenguaje que destaque entre los demás para dicha área.

Siempre es bueno hacer uso de un framework para desarrollar bajo el paradigma de la programación orientada a objetos y/o usando un patrón de arquitectura.

Algunos ejemplos de frameworks que soportan este paradigma en diversos lenguajes son: Spring Boot, Laravel, Symfony, Flask, Django etc.

## 6.2. Almacenamiento

Para la gestión de datos, tanto relacionales como no relacionales, se debe considerar que las bases de datos deben estar instaladas en modo clúster para no relacionales y gestor de base de datos para las relacionales, por ello, se deben tomar las precauciones necesarias al momento de crear las consultas y realizar conexiones seguras al hacer empleo de las mismas.

**En el caso de las bases de datos relacionales, se debe considerar:**

* Tiempo de respuesta por parte del servidor.
* No tener referencias circulares.
* Aplicar las tres formas normales.
* Uso de disparadores y procedimientos almacenados.
* Creación consciente de los usuarios.
* Segmentar la información en tablas concretas y bien definidas para reducir al mínimo información redundante.

**Para las bases de datos no relacionales:**

* Tiempo de respuesta de los clústers.
* Asegurarse de tener las tres zonas de disponibilidad brindadas por el gestor.
* Limitar la conexión de IP al clúster.

## 6.3. Formateo de código

El formateo del código debe considerarse una parte esencial para mantener un código limpio. Se debe elegir un conjunto de reglas para que actúe como reglas de formato de código y se aplique de manera consistente. Así mismo, llegar a un acuerdo con el equipo de desarrollo para aplicar dichas normas y aplicar las diferentes revisiones y correcciones pertinentes.

El formateo de código es una herramienta de suma importancia, ya que impone una comunicación fundamental con los programadores y proporciona un ambiente profesional por lo que el estilo y legibilidad del código son precedentes que definirán la mantenibilidad y extensibilidad.
