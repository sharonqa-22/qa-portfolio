# Casos de Prueba — SauceDemo — Módulo Login

**Aplicación:** https://www.saucedemo.com  
**Módulo:** Autenticación / Login  
**Tester:** Sharon Pereira  
**Fecha:** 07/06/2026  

---

| ID | Descripcion | Pasos | Resultado esperado | Resultado obtenido | Estado |
|---|---|---|---|---|---|
| TC-001 | Login con credenciales validas | 1. Ingresar usuario: standard_user 2. Ingresar contrasena: secret_sauce 3. Clic en Login | Redirige al catalogo de productos | Redirige al catalogo de productos | PASS |
| TC-002 | Login con usuario bloqueado | 1. Ingresar usuario: locked_out_user 2. Ingresar contrasena: secret_sauce 3. Clic en Login | Muestra mensaje de error | Muestra: "Sorry, this user has been locked out" | PASS |
| TC-003 | Login con contrasena incorrecta | 1. Ingresar usuario: standard_user 2. Ingresar contrasena: 12345 3. Clic en Login | Muestra mensaje de credenciales invalidas | Muestra mensaje de error correspondiente | PASS |
| TC-004 | Login con campos vacios | 1. Dejar ambos campos vacios 2. Clic en Login | Muestra mensaje de error | Muestra: "Username is required" | PASS |
| TC-005 | Contrasena vacia | 1. Ingresar usuario: standard_user 2. Dejar contrasena vacia 3. Clic en Login | Muestra mensaje de error | Muestra: "Password is required" | PASS |
