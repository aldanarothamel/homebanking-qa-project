ID AUTH-06
Title: Checkbox “Remember Me” does not persist the session after closing the browser
Type: Functional Bug
Severity: Low
Priority: Medium

Environment:

* Application: Home Banking Web
* Documented version: v3.0 (Functional Specification)
* Browser: Chrome (latest version)
* Environment type: Web – Mock with localStorage
* Detection date: 03/03/2026

Description:
When selecting the “Remember me” option during login and completely closing the browser, the session does not remain active upon re-entering the application.
The functionality does not generate any visible behavior or additional persistence compared to a login without selecting this option.

Preconditions:
* Valid user available (demo / demo123).
* Application accessible from a browser.

Steps to Reproduce:
1. Go to the Login screen.
2. Enter valid credentials:
   * User: demo
   * Password: demo123
3. Check the “Remember me” box.
4. Click on "Login".
5. Verify correct access to the Dashboard.
6. Completely close the browser.
7. Reopen the browser.
8. Access the application URL again.

Expected Result:
If the "Remember me" option is enabled, the system should: 
* Keep the session active automatically
  or
* At least remember the previously entered user
  or
* Persist the session token according to the functionally defined behavior.

Actual Result:
* The system redirects to the Login screen.
* Does not keep the session active.
* Does not remember the user.
* There is no difference in behavior compared to not selecting the option.

Impact:
* Does not affect financial operations.
* May cause possible confusion in the user experience.
* Could be considered incomplete or inconsistent functionality regarding the presence of the checkbox in the UI. 

Observations The Functional Specification does not detail the expected behavior of the "Remember me" checkbox, which could indicate: Omission in documentation or Incomplete implementation It is recommended to validate with Functional Analysis / Product Owner. 

Reported Status – Pending analysis

------------------------------------------------------------------------------------------------------------------------------------------

ID AUTH-06
Título: Checkbox “Recordarme” no persiste la sesión luego de cerrar el navegador
Tipo: Bug Funcional
Severidad: Baja
Prioridad: Media

Ambiente:
* Aplicación: Home Banking Web
* Versión documentada: v3.0 (Especificación Funcional)
* Navegador: Chrome (última versión)
* Tipo de entorno: Web – Mock con localStorage
* Fecha de detección: 03/03/2026

Descripción:
Al seleccionar la opción “Recordarme” durante el inicio de sesión y cerrar completamente el navegador, la sesión no se mantiene activa al volver a ingresar a la aplicación.
La funcionalidad no genera ningún comportamiento visible ni persistencia adicional respecto a un login sin marcar dicha opción.

Precondiciones:
* Usuario válido disponible (demo / demo123).
* Aplicación accesible desde navegador.

Pasos para Reproducir:
1. Ingresar a la pantalla de Login.
2. Ingresar credenciales válidas:
   * Usuario: demo
   * Contraseña: demo123
3. Marcar la casilla “Recordarme”.
4. Hacer clic en "Ingresar".
5. Verificar acceso correcto al Dashboard.
6. Cerrar completamente el navegador.
7. Volver a abrir el navegador.
8. Acceder nuevamente a la URL de la aplicación.

Resultado Esperado:
Si la opción “Recordarme” está activada, el sistema debería:
* Mantener la sesión activa automáticamente
  o
* Recordar al menos el usuario previamente ingresado
  o
* Persistir el token de sesión según comportamiento definido funcionalmente

Resultado Actual:
* El sistema redirige a la pantalla de Login.
* No mantiene sesión activa.
* No recuerda usuario.
* No existe diferencia de comportamiento respecto a no marcar la opción.


Impacto:
* No afecta operaciones financieras.
* Genera posible confusión en la experiencia de usuario.
* Puede considerarse funcionalidad incompleta o inconsistente respecto a la presencia del checkbox en UI.

Observaciones:
La Especificación Funcional no detalla el comportamiento esperado del checkbox “Recordarme”, lo que podría indicar:
* Omisión en documentación
  o
* Implementación incompleta
Se recomienda validación con Análisis Funcional / Product Owner.

Estado:
Reportado – Pendiente de análisis

¿Seguimos con un bug más interesante o avanzamos con diseño de casos críticos de Transferencias?

