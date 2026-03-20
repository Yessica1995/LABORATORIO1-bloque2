# LABORATORIO1-bloque2

# Sistema de Turnos Digital – Banco KAY

## Descripción del Proyecto

Este proyecto consiste en una aplicación web desarrollada con **Vue.js** que permite gestionar turnos de atención dentro de una sucursal del **Banco KAY**.

La aplicación permite a los usuarios registrar su turno digital ingresando su nombre y número de cuenta, evitando así el uso de tickets impresos en papel. También incluye un panel de gestión que permite visualizar la cola de espera y llamar al siguiente cliente.

---

# Problemática planteada

El Banco KAY enfrenta desafíos operativos en su sistema actual de gestión de turnos dentro de sus sucursales físicas. Actualmente se utilizan tickets impresos en papel térmico para asignar turnos a los clientes. Este sistema presenta varios problemas.

Uno de los principales inconvenientes es que los clientes pueden perder o dañar su ticket, lo que genera confusión en el orden de atención. Esto provoca adelantos o retrasos en los turnos y genera inconformidad entre los usuarios.

Además, el uso constante de papel térmico produce residuos que afectan el medio ambiente y generan gastos adicionales en insumos de impresión.

Para solucionar este problema se propone desarrollar una aplicación web que permita generar **tickets digitales**, eliminar el uso de papel y mejorar la organización de la cola de atención dentro del banco.

---

# Sectores enfocados

La solución propuesta está enfocada en los siguientes sectores:

### Sector Financiero

Permite mejorar la organización del flujo de clientes dentro de las sucursales del banco, optimizando el tiempo de atención y mejorando la experiencia del usuario.

### Sector Tecnológico (Desarrollo Web)

La aplicación utiliza tecnologías modernas como **Vue.js** para implementar un sistema digital de gestión de turnos que permite actualizar la información en tiempo real.

### Sector Ambiental

Al eliminar el uso de tickets impresos, se reduce el consumo de papel térmico y se contribuye a una política institucional de **cero papel**, favoreciendo la sostenibilidad ambiental.

---

# Descripción de la solución web

La solución consiste en una aplicación web que permite a los clientes obtener un turno digital al ingresar al banco.

El usuario ingresa su nombre y número de cuenta en un formulario dentro de una terminal digital. Al presionar el botón para generar el turno, el sistema crea automáticamente un número de turno único y lo agrega a la cola de espera.

El sistema también muestra cuántas personas están antes en la fila y permite visualizar cuándo es el turno del usuario.

Adicionalmente, el sistema incluye un panel de gestión donde el personal del banco puede llamar al siguiente cliente o eliminar turnos de la lista en caso de ser necesario.

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

## Explique para qué utilizó la directiva v-for dentro de su aplicación

La directiva **v-for** se utiliza para recorrer la lista de turnos que están en la cola de espera. Gracias a esta directiva se pueden mostrar todos los clientes que están esperando ser atendidos dentro de una tabla en la interfaz.

---

## Describa en qué situación utilizó v-if y qué problema resuelve dentro de su interfaz

La directiva **v-if** se utiliza para mostrar diferentes elementos dependiendo del estado de la aplicación.

Por ejemplo, cuando el usuario todavía no tiene turno se muestra el formulario para registrar sus datos. Cuando el usuario ya tiene un turno asignado se muestra su ticket digital con su número de turno y la cantidad de personas que están delante de él.

Esto ayuda a que la interfaz sea más clara y evita que el usuario genere múltiples turnos al mismo tiempo.

---

## Explique cómo se realiza la validación de datos en su aplicación

La validación de datos se realiza verificando que el nombre del cliente tenga más de tres caracteres y que el número de cuenta tenga más de cuatro caracteres.

Si los datos ingresados no cumplen con estas condiciones, el botón para generar el turno permanece deshabilitado y no permite registrar un turno.

La validación es importante porque evita que el sistema almacene información incompleta o incorrecta.
