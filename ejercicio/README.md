# Sistema Interactivo: Dispensador Automático de Alimento para Perro

## Estudiantes: 
Carolina Rodríguez, 
Noemí Vargas

## a. Nombre del sistema

**Dispensador Automático de Comida para Perros**

## b. Descripción general

Este sistema interactivo dispensa automáticamente una porción de alimento para perro cuando detecta que el recipiente está vacío. El objetivo es facilitar la alimentación de la mascota, mantener horarios constantes y ayudar a dueños con rutinas ocupadas.

El sistema usa un sensor para detectar el nivel de alimento en el plato y un microcontrolador que procesa la información para activar un motor que libera comida.

## c. Usuario objetivo

* Dueños de perros
* Personas con horarios ocupados
* Hogares con mascotas
* Personas que desean automatizar el cuidado de sus animales

## d. Entradas

### Sensor

* **Sensor ultrasónico o sensor infrarrojo** para detectar si el plato tiene alimento

### Tipo de señal

* **Digital o analógica** (según el sensor)
* Señal de distancia o presencia de alimento

### Función de la entrada

El sensor detecta si el plato está vacío o con poco alimento. 

## e. Salidas

### Actuador

* **Servo motor o motor DC**

### Tipo de señal

* **PWM / Digital**

### Función de la salida

El motor gira una compuerta o mecanismo que libera una cantidad definida de alimento seco hacia el plato.

## f. Lógica de funcionamiento

El sistema opera en un ciclo continuo con los siguientes estados:

1. **Espera**: El sensor monitorea el plato cada 10 segundos.
2. **Detección**: Si el sensor detecta ausencia de alimento, envía señal al microcontrolador.
3. **Dispensado**: El microcontrolador activa el motor durante 5 segundos para liberar una porción de alimento.
4. **Verificación**: El sensor confirma que el alimento fue dispensado correctamente.
5. **Reposo**: El sistema vuelve al estado de espera.

> En caso de fallo (plato no detectado después de 3 intentos), el sistema emite una alerta sonora.

## g. Componentes del sistema

| Componente | Descripción | Cantidad |
|---|---|---|
| Microcontrolador (Arduino Uno / ESP32) | Procesa señales y controla actuadores | 1 |
| Sensor ultrasónico HC-SR04 | Detecta nivel de alimento en el plato | 1 |
| Servo motor SG90 | Abre/cierra la compuerta del dispensador | 1 |
| Buzzer pasivo | Emite alerta sonora en caso de fallo | 1 |
| Fuente de alimentación 5V | Alimenta el circuito | 1 |
| Contenedor de alimento (recipiente) | Almacena el alimento seco | 1 |

---

