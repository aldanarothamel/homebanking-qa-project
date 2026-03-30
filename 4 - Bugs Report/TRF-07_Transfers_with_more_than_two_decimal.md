ID TRF-07
Title: System allows transfers with more than two decimal places under certain values, bypassing amount format validation
Type: Functional Bug – Data Validation
Severity: High
Priority: Medium-High

Environment:
Application: Home Banking Web
Documented Version: v3.0
Browser: Chrome
Persistence: localStorage (mock)
Detection Date: 04/03/2026

Description:
The amount field in the Transfers module appears to correctly validate entries with a maximum of two decimal places. 
However, when entering values with multiple decimals (more than 2), the system allows the transfer to execute in certain cases.
An inconsistent behavior is observed where:
Some values with multiple decimals are correctly rejected.
Other values with higher decimal precision (e.g., 1.000000001) are accepted and processed.
This indicates incomplete or inconsistent validation of the numerical format.

Preconditions:
User is authenticated.
Access to the Transfers module.
Account has sufficient balance.

Steps to Reproduce:
1-Access the Transfers module.
2-Select source and destination accounts.
3-Enter an amount with more than two decimal places, for example: 1.000000001.
4-Confirm the operation.

Actual Result:
The system allows entering values with more than two decimals in certain cases.
The transfer executes successfully.
No validation error is displayed.
Behavior is inconsistent across different values with multiple decimals.

Expected Result:
The system should:
Allow only values with up to two decimal places.
Reject any value with more than two decimals.
Display a clear validation message.
Example: “The amount must have a maximum of two decimal places.”

Impact:
Non-compliance with monetary formatting rules.
Potential inconsistencies in financial calculations.
Unpredictable behavior depending on the entered value.
Reduces system reliability/trustworthiness.

Status: Reported – Pending Analysis

---------------------------------------------------------------------------------------------------------------------------------------

ID TRF-07
Título: El sistema permite transferencias con más de dos decimales bajo ciertos valores, incumpliendo la validación de formato de monto
Tipo: Bug Funcional – Validación de Datos
Severidad: Alta
Prioridad: Media-Alta

Ambiente:
Aplicación: Home Banking Web
Versión documentada: v3.0
Navegador: Chrome
Persistencia: localStorage (mock)
Fecha detección: 04/03/2026

Descripción:
El campo de monto en el módulo de Transferencias aparenta validar correctamente el ingreso de valores con un máximo de dos decimales. 
Sin embargo, al ingresar valores con múltiples decimales (más de 2), el sistema permite la ejecución de la transferencia en ciertos casos.
Se observa un comportamiento inconsistente donde:
Algunos valores con múltiples decimales son rechazados correctamente
Otros valores con mayor precisión decimal (ej: 1,000000001) son aceptados y procesados
Esto indica una validación incompleta o inconsistente del formato numérico.

Precondiciones:
Usuario autenticado
Acceso al módulo Transferencias
Cuenta con saldo suficiente

Pasos para Reproducir:
1-Acceder al módulo Transferencias
2-Seleccionar cuenta de origen y destino
3-Ingresar un monto con más de dos decimales, por ejemplo: 1,000000001
4-Confirmar la operación

Resultado Actual:
El sistema permite ingresar valores con más de dos decimales en ciertos casos
La transferencia se ejecuta exitosamente
No se muestra error de validación
El comportamiento no es consistente para todos los valores con múltiples decimales

Resultado Esperado:
El sistema debería:
Permitir únicamente valores con hasta dos decimales
Rechazar cualquier valor con más de dos decimales
Mostrar mensaje de validación claro
Ejemplo:
“El monto debe tener como máximo dos decimales”

Impacto:
Incumplimiento de reglas de formato monetario
Posibles inconsistencias en cálculos financieros
Comportamiento impredecible según el valor ingresado
Reduce la confiabilidad del sistema

Estado: Reportado – Pendiente de análisis
