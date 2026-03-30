ID TRF-06
Title: Account balance does not update in the source selector after making a transfer 
Type: Functional Bug – UI Inconsistency 
Severity: High 
Priority: Medium-High 

Environment: 
*Application: Home Banking Web 
*Documented version: v3.0 
*Browser: Chrome 
*Persistence: localStorage (mock) 
*Detection date: 03/04/2026 

Description: 
After making a successful transfer, the account balance updates correctly in the Dashboard / Products module, 
but does not update in the source account selector within the Transfers module. 
This creates an inconsistency between the values shown in different parts of the interface. 

Preconditions:
 *Authenticated user 
*Available account balance (e.g., $100,000) 

Steps to Reproduce: 
1-Access the Transfers module 
2-Select source account (e.g., Checking Account) 
3-Verify balance displayed in the selector (e.g., $100,000) 
4-Make a transfer of $10,000 
5-Confirm the transaction
6-Check balance on Dashboard
7-Return to the Transfers module
8-Check the balance shown in the account selector

Current Result
*The balance on the Dashboard updates correctly (e.g., $90,000)
*The account selector still shows the previous balance (e.g., $100,000)
*There is no synchronization between components

Expected Result
The account balance should update consistently throughout the application, including:
*Dashboard
*Account selector in Transfers
*Any component that displays balance

Impact:
*Generates visual inconsistency in the application
*Can mislead the user regarding their available balance
*Affects trust in the information shown
*May lead to attempts of invalid operations

Status: Reported – Pending analysis

—----------------------------------------------------------------------------------------------------------

ID TRF-06
Título: El saldo de la cuenta no se actualiza en el selector de origen luego de realizar una transferencia
Tipo: Bug Funcional – Inconsistencia de UI
Severidad: Alta
Prioridad: Media-Alta

Ambiente:
*Aplicación: Home Banking Web
*Versión documentada: v3.0
*Navegador: Chrome
*Persistencia: localStorage (mock)
*Fecha detección: 04/03/2026

Descripción:
Luego de realizar una transferencia exitosa, el saldo de la cuenta se actualiza correctamente en el módulo de Dashboard / productos, 
pero no se actualiza en el selector de cuenta de origen dentro del módulo de Transferencias.
Esto genera una inconsistencia entre los valores mostrados en diferentes partes de la interfaz.

Precondiciones
*Usuario autenticado
*Saldo disponible en cuenta (ej: $100.000)

Pasos para Reproducir
1-Acceder al módulo Transferencias
2-Seleccionar cuenta de origen (ej: Cuenta Corriente)
3-Verificar saldo mostrado en el selector (ej: $100.000)
4-Realizar una transferencia por $10.000
5-Confirmar operación
6-Verificar saldo en Dashboard
7-Volver al módulo Transferencias
8-Verificar saldo mostrado en el selector de cuenta

Resultado Actual
*El saldo en Dashboard se actualiza correctamente (ej: $90.000)
*El selector de cuenta sigue mostrando el saldo anterior (ej: $100.000)
*No hay sincronización entre componentes

Resultado Esperado
El saldo de la cuenta debería actualizarse de forma consistente en toda la aplicación, incluyendo:
*Dashboard
*Selector de cuenta en Transferencias
*Cualquier componente que muestre saldo

Impacto:
*Genera inconsistencia visual en la aplicación
*Puede inducir al usuario a error respecto a su saldo disponible
*Afecta la confianza en la información mostrada
*Puede provocar intentos de operaciones inválidas

Estado: Reportado – Pendiente de análisis
