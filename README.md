# LABORATORIO1-bloque2

# Sistema de Turnos Digital – Banco KAY

Problemática planteada:
El Banco KAY enfrenta desafíos operativos críticos en su sistema de gestión de flujo de clientes en sucursales físicas. El modelo actual basado en tickets de papel térmico ha generado una serie de ineficiencias que afectan tanto la experiencia del usuario como la sostenibilidad institucional. La pérdida o deterioro de los boletos físicos provoca constantes confusiones en el orden de atención, derivando en adelantos indebidos o retrasos significativos que alteran la cronología de los turnos. El uso masivo de papel no reciclable contraviene las políticas de responsabilidad ambiental y genera un gasto operativo constante en insumos de impresión.Para mitigar estos conflictos, se identifica la necesidad de una transición digital que centralice la asignación de turnos a través de una plataforma web accesible desde dispositivos móviles o terminales táctiles en el sitio. 

Los sectores enfocados:
La situación problemática actual se centra en los siguientes 3 sectores:

1- El sector Financiero: Para la optimización de la eficiencia operativa y mejora en los indicadores de servicio al cliente (CSAT).

2- El sector Tecnológico (Desarrollo Web): Implementación de sistemas de gestión de colas (Queue Management Systems) basados en arquitectura web.

3- El sector Ambiental (Sostenibilidad): Reducción directa de la huella de carbono mediante la eliminación de residuos de papel (Cero Papel).

Descripción de función de la solución web:
Al llegar al banco, el usuario utiliza terminal táctil para ingresar sus datos básicos (nombre y numero de cuenta). El sistema genera un ticket digital único,
eliminando la necesidad de impresoras térmicas. Mediante el uso de estados en la aplicación web, el usuario podrá visualizar cuántas personas tiene por delante.
El sistema actualizará automáticamente el estado del turno (ej: "Su turno es el próximo"), permitiendo al cliente esperar de forma más cómoda sin temor a perder su lugar.
os empleados del banco dispondrán de una interfaz sencilla para "Llamar siguiente", "Marcar como ausente" o "Reasignar turno", lo que garantiza un flujo de trabajo ordenado
y auditable, resolviendo el problema de los saltos de turno manuales.

---

# Tecnologías utilizadas

* **Vue.js**
* **HTML**
* **CSS**
* **JavaScript**

---

# Preguntas del laboratorio

## ¿Qué es Vue.js y cuál es su función dentro de la página web desarrollada?

Vue.js es un framework de JavaScript que se utiliza para crear interfaces web interactivas. Permite conectar los datos del sistema con los elementos visuales de la página para que la información se actualice automáticamente sin necesidad de recargar la página.

En este proyecto Vue.js se utiliza para manejar los turnos del banco, registrar clientes, actualizar la cola de espera y mostrar la posición del usuario dentro de la fila en tiempo real.

---

## ¿Qué variables reactivas utilizó en su aplicación y cuál es la función de cada una?

Las variables reactivas utilizadas en el proyecto son:

**cola**
Almacena todos los turnos de los clientes que están esperando ser atendidos.

**miTicket**
Guarda el turno asignado al usuario que está utilizando la aplicación.

**contadorId**
Se utiliza para generar automáticamente el número de turno para cada cliente.

**form**
Almacena los datos que el usuario ingresa en el formulario, como su nombre y número de cuenta.

**formValido**
Se utiliza para verificar si los datos ingresados cumplen con los requisitos mínimos antes de generar el turno.

**posicionEnCola**
Calcula cuántas personas están delante del usuario dentro de la cola de espera.

---

## Explique la diferencia entre las directivas v-bind y v-model

La directiva **v-model** se utiliza para conectar los campos de entrada con las variables del sistema. Esto permite que cuando el usuario escriba en un input, el valor se guarde automáticamente en la variable correspondiente.

La directiva **v-bind** se utiliza para enlazar atributos de HTML con datos dinámicos del sistema. En este proyecto se utiliza para habilitar o deshabilitar botones dependiendo de ciertas condiciones.

---

## Mencione al menos un ejemplo de evento utilizado dentro de su aplicación

Un ejemplo de evento utilizado es el evento **click** en los botones.

Por ejemplo, cuando el usuario presiona el botón para generar su turno se ejecuta una función que registra el turno dentro de la cola de espera.

---

# Explique para qué utilizó la directiva v-for dentro de su aplicación

La directiva **v-for** se utiliza para recorrer la lista de turnos que están en la cola de espera. Gracias a esta directiva se pueden mostrar todos los clientes que están esperando ser atendidos dentro de una tabla en la interfaz.

---

# Describa en qué situación utilizó v-if y qué problema resuelve dentro de su interfaz

La directiva **v-if** se utiliza para mostrar diferentes elementos dependiendo del estado de la aplicación.

Por ejemplo, cuando el usuario todavía no tiene turno se muestra el formulario para registrar sus datos. Cuando el usuario ya tiene un turno asignado se muestra su ticket digital con su número de turno y la cantidad de personas que están delante de él.

Esto ayuda a que la interfaz sea más clara y evita que el usuario genere múltiples turnos al mismo tiempo.

---

# Explique cómo se realiza la validación de datos en su aplicación

La validación de datos se realiza verificando que el nombre del cliente tenga más de tres caracteres y que el número de cuenta tenga más de cuatro caracteres.

Si los datos ingresados no cumplen con estas condiciones, el botón para generar el turno permanece deshabilitado y no permite registrar un turno.

La validación es importante porque evita que el sistema almacene información incompleta o incorrecta.
