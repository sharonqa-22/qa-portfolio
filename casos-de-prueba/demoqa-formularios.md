# Casos de Prueba — DemoQA — Módulo Formularios

**Aplicación:** https://demoqa.com/automation-practice-form  
**Módulo:** Practice Form  
**Tester:** Sharon Pereira  
**Fecha:** 07/06/2026  

---

| ID | Descripcion | Pasos | Resultado esperado | Resultado obtenido | Estado |
|---|---|---|---|---|---|
| TC-001 | Envio de formulario con todos los campos obligatorios completos | 1. Ingresar First Name: Sharon 2. Ingresar Last Name: Pereira 3. Seleccionar Gender: Female 4. Ingresar Mobile: 0956981610 5. Clic en Submit | Se muestra modal de confirmacion con los datos ingresados | Se muestra modal con tabla de datos correctos | PASS |
| TC-002 | Envio de formulario sin completar campos obligatorios | 1. Dejar First Name vacio 2. Dejar Last Name vacio 3. No seleccionar Gender 4. Clic en Submit | Los campos obligatorios se marcan en rojo | Los campos First Name, Last Name y Gender se resaltan en rojo | PASS |
| TC-003 | Campo Mobile con menos de 10 digitos | 1. Ingresar First Name: Sharon 2. Ingresar Last Name: Pereira 3. Seleccionar Gender: Female 4. Ingresar Mobile: 12345 5. Clic en Submit | El campo Mobile se marca como invalido | El campo Mobile se resalta en rojo | PASS |
| TC-004 | Seleccion de fecha de nacimiento | 1. Completar campos obligatorios 2. Clic en el campo Date of Birth 3. Seleccionar mes, año y dia 4. Clic en Submit | La fecha seleccionada aparece en el modal de confirmacion | La fecha se muestra correctamente en el modal | PASS |
| TC-005 | Carga de imagen en el formulario | 1. Completar campos obligatorios 2. En el campo Picture clic en Choose File 3. Seleccionar una imagen del equipo 4. Clic en Submit | El nombre del archivo aparece junto al campo y se registra en el modal | El nombre del archivo se muestra correctamente | PASS |
| TC-006 | Campo de texto libre Current Address | 1. Completar campos obligatorios 2. Ingresar texto largo en Current Address 3. Clic en Submit | El texto completo aparece en el modal de confirmacion | El texto se muestra completo en el modal | PASS |
