# TP Integrador Informática 2

> Alumno: Gonzalez Leonel Ezequiel

> FSM: Control de protección de sobretensión

## Memoria descriptiva:
Este sistema representa un control de protección frente a situaciones de sobretensión, cuyo propósito es verificar continuamente el nivel de tensión de la red y proteger la carga ante situaciones que puedan afectar su integridad.

Ante una sobretensión, el sistema se encargará de aislar la carga y reestablecerla una vez que la red se encuentre dentro de un rango seguro. Además, se utilizan tiempos de control y verificación para determinar la persistencia de la condición, y así, evitar cambios instantáneos entre estados ante variaciones momentáneas en la tensión. 

## Diagrama de la máquina de estado:

<img width="825" height="733" alt="image" src="https://github.com/user-attachments/assets/f2f33205-4c43-45c4-9678-115f512ac3a6" />

- __Normal__ : operación segura del sistema, la tensión se encuentra dentro del rango nominal permitido.
- __Alerta Sobretension__ : detecta y alerta si la tensión supera el umbral máximo permitido. Si persiste durante un tiempo establecido, pasa al estado 'Disparo'.
- __Disparo__ : desconecta la carga y la mantiene aislada hasta que la tensión vuelva a un rango seguro.
- __Recuperacion__ : verifica y valida que la tensión haya vuelto a condiciones seguras durante un breve período tiempo, caso contrario, vuelve al estado 'Disparo'.
