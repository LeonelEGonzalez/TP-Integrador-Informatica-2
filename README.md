# TP Integrador Informática 2

> Alumno: Gonzalez Leonel Ezequiel

> FSM: Control de protección de sobretensión

## Memoria descriptiva:
Este sistema representa un control de protección frente a situaciones de sobretensión, cuyo propósito es verificar continuamente el nivel de tensión de la red y proteger la carga ante situaciones que puedan afectar su integridad.

En tal caso, el sistema se encargará de aislar y reestablecer la carga una vez que la red se encuentre en un rango seguro. Además, se utilizan tiempos de control y verificación para determinar la persistencia de la condición y así evitar cambios instantaneos entre estados. 

<img width="825" height="733" alt="image" src="https://github.com/user-attachments/assets/f2f33205-4c43-45c4-9678-115f512ac3a6" />

- __Normal__ : operación segura, la tensión se encuentra dentro del rango nominal permitido.
- __Alerta Sobretension__ : detecta y alerta si la tension supera el umbral maximo. Si persiste durante un tiempo establecido, pasa al estado 'Disparo'.
- __Disparo__ : desconecta la carga hasta que la tensión vuelva a un estado seguro.
- __Recuperacion__ : verifica y valida que la tensión haya vuelto a condiciones seguras durante un breve período tiempo, caso contrario, vuelve al estado 'Disparo'.
