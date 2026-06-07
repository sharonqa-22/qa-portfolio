# Reporte de Bugs — DemoQA — Formularios

**Aplicación:** https://demoqa.com/automation-practice-form  
**Tester:** Sharon Pereira  
**Fecha:** 07/06/2026  

---

| ID | Titulo | Modulo | Severidad | Prioridad | Pasos para reproducir | Resultado esperado | Resultado obtenido | Estado |
|---|---|---|---|---|---|---|---|---|
| BUG-001 | El campo Mobile acepta letras sin mostrar error inmediato | Practice Form | Media | Media | 1. Ingresar letras en el campo Mobile 2. Clic en Submit | El campo rechaza caracteres no numericos en tiempo real | El campo acepta letras y solo muestra error al hacer Submit | Abierto |
| BUG-002 | El modal de confirmacion no tiene opcion de cerrar con teclado | Practice Form | Baja | Baja | 1. Completar formulario correctamente 2. Clic en Submit 3. Intentar cerrar el modal con la tecla Escape | El modal se cierra con Escape | El modal no responde a la tecla Escape | Abierto |
| BUG-003 | El campo Subject no sugiere opciones al ingresar texto invalido | Practice Form | Baja | Baja | 1. Ingresar texto aleatorio en el campo Subjects 2. Observar comportamiento | El campo muestra mensaje indicando que no hay coincidencias | El campo no muestra ninguna indicacion al usuario | Abierto |

---

## Escala de severidad utilizada

| Severidad | Descripcion |
|---|---|
| Critica | El sistema no funciona, bloquea el flujo principal |
| Alta | Funcionalidad importante afectada |
| Media | Funcionalidad afectada pero con alternativa |
| Baja | Problema menor, no afecta el flujo principal |
