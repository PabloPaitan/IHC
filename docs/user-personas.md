# Historias de Usuario (User Stories) - SafeSound

A continuación se detallan las historias de usuario clave para el desarrollo del sistema de conciencia situacional auditiva:

## Epica: Registro e Inicio de Sesión
### US01: Crear Cuenta / Registrarse
* **Como:** Usuario nuevo.
* **Quiero:** Registrarme en la aplicación ingresando mi correo electrónico y una contraseña segura.
* **Para:** Poder acceder a las funcionalidades personalizadas de SafeSound y guardar mi historial de alertas.

#### Criterios de Aceptación:
* **Escenario 01:** Registro exitoso con datos válidos.
  * **Dado que** el usuario se encuentra en la pantalla de registro.
  * **Cuando** ingresa un correo electrónico válido, una contraseña que cumpla con los requisitos de seguridad y presiona el botón "Registrarse".
  * **Entonces** el sistema crea la cuenta, envía un correo de confirmación y lo redirige a la pantalla de inicio.
* **Escenario 02:** Registro fallido por correo duplicado.
  * **Dado que** el usuario intenta registrarse.
  * **Cuando** ingresa un correo electrónico que ya se encuentra registrado en el sistema.
  * **Entonces** el sistema muestra un mensaje de error indicando que el correo ya está en uso.

---

## Epica: Detección y Alertas Inteligentes
### US02: Detección de Sonidos de Riesgo mediante IA
* **Como:** Usuario peatón (especialmente si usa audífonos o tiene distracción visual).
* **Quiero:** Que la aplicación use el micrófono en segundo plano e identifique sonidos peligrosos (bocinas, ambulancias, frenazos).
* **Para:** Recibir una alerta visual y táctil inmediata que me permita reaccionar a tiempo y evitar un accidente vial.

#### Criterios de Aceptación:
* **Escenario 01:** Identificación correcta de sonido de emergencia.
  * **Dado que** la aplicación está activa ejecutándose en segundo plano.
  * **Cuando** el micrófono capta el sonido de una sirena de ambulancia cercano.
  * **Entonces** el sistema procesa el audio con el modelo de IA y activa una vibración intensa junto con una notificación emergente en pantalla.
