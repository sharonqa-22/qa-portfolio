# Reporte de Bugs — SauceDemo

**Aplicación:** https://www.saucedemo.com  
**Tester:** Sharon Pereira  
**Fecha:** 07/06/2026  

---

| ID | Titulo | Modulo | Severidad | Prioridad | Pasos para reproducir | Resultado esperado | Resultado obtenido | Estado |
|---|---|---|---|---|---|---|---|---|
| BUG-001 | Las imagenes de productos se muestran incorrectas con problem_user | Catalogo | Media | Media | 1. Iniciar sesion con problem_user / secret_sauce 2. Ver catalogo de productos | Las imagenes corresponden a cada producto | Todas las imagenes muestran el mismo producto incorrecto | Abierto |
| BUG-002 | El boton Add to Cart no funciona con problem_user | Carrito | Alta | Alta | 1. Iniciar sesion con problem_user / secret_sauce 2. Clic en Add to Cart en cualquier producto | El producto se agrega al carrito | El boton no responde | Abierto |
| BUG-003 | Usuario bloqueado no recibe mensaje claro al intentar login | Login | Baja | Baja | 1. Ingresar locked_out_user / secret_sauce 2. Clic en Login | Mensaje de error descriptivo y visible | El mensaje aparece pero sin formato destacado | Abierto |

---

## Escala de severidad utilizada

| Severidad | Descripcion |
|---|---|
| Critica | El sistema no funciona, bloquea el flujo principal |
| Alta | Funcionalidad importante afectada |
| Media | Funcionalidad afectada pero con alternativa |
| Baja | Problema menor, no afecta el flujo principal |
