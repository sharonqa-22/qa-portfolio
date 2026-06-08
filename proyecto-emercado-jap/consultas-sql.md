# Consultas SQL — Proyecto e-Mercado JAP

## Contexto

Durante la Etapa 2 y Etapa 3 del proyecto, se ejecutaron consultas SQL directamente
sobre la base de datos de e-Mercado para validar la integridad de los datos y
verificar el comportamiento del sistema más allá de la interfaz web.

**Base de datos:** MySQL  
**Tablas principales:** Usuario, Categorias, Articulos, Ventas, MetodoEnvio, FormaPago, CarritoDeCompras, Compras

---

## Consultas de validación

### 1. Verificar usuarios registrados

```sql
SELECT * FROM Usuario;
```

Propósito: confirmar que los usuarios creados desde la interfaz web se persisten
correctamente en la base de datos.

---

### 2. Verificar integridad de artículos publicados

```sql
SELECT id_articulo, nombre, precio, stock, id_usuario
FROM Articulos
ORDER BY id_articulo ASC;
```

Propósito: validar que los artículos publicados por vendedores contienen datos
completos y que el stock no presenta valores negativos ni nulos.

---

### 3. Verificar categorías disponibles

```sql
SELECT * FROM Categorias
ORDER BY nombre ASC;
```

Propósito: confirmar el orden alfabético de las categorías y detectar posibles
duplicados o registros vacíos.

---

### 4. Verificar artículos en el carrito de compras

```sql
SELECT c.id_carrito, c.id_usuario, c.id_articulo, a.nombre, a.precio
FROM CarritoDeCompras c
JOIN Articulos a ON c.id_articulo = a.id_articulo;
```

Propósito: validar que los artículos agregados al carrito se asocian correctamente
al usuario y que los precios coinciden con los registrados en la tabla Articulos.

---

### 5. Verificar ventas registradas

```sql
SELECT v.id_venta, v.id_usuario_comprador, v.id_articulo, v.fecha, v.total
FROM Ventas v
ORDER BY v.fecha DESC;
```

Propósito: confirmar que las ventas completadas quedan registradas con los datos
correctos de usuario, artículo, fecha y monto total.

---

### 6. Verificar métodos de envío disponibles

```sql
SELECT * FROM MetodoEnvio;
```

Propósito: validar que los métodos de envío configurados en la base de datos
coinciden con las opciones mostradas en la interfaz web.

---

### 7. Verificar formas de pago disponibles

```sql
SELECT * FROM FormaPago;
```

Propósito: confirmar que las formas de pago registradas son coherentes con las
opciones habilitadas en el flujo de checkout.

---

### 8. Verificar stock positivo antes de una venta

```sql
SELECT id_articulo, nombre, stock
FROM Articulos
WHERE stock <= 0;
```

Propósito: detectar artículos con stock en cero o negativo que no deberían estar
disponibles para la compra. Este caso fue identificado como defecto crítico:
el sistema procesaba ventas sin validar el stock disponible.

---

## Hallazgos relevantes

- La base de datos no estaba vinculada a la interfaz web durante la Etapa 2,
  lo que impidió ejecutar el 34,6% de los casos de prueba.
- Se detectó que el sistema no validaba stock disponible al momento de procesar
  una venta — defecto de severidad crítica.
- Los datos de usuario registrados desde la interfaz no siempre se persistían
  correctamente en la tabla Usuario.
- Las tablas de Ventas y Compras presentaban registros incompletos debido a
  fallos en el flujo de checkout.

---

## Herramientas utilizadas

- Motor de base de datos: MySQL
- Consultas ejecutadas por: Fernando Galasso (Asesor Técnico) y equipo
- Documentación de sentencias: Google Docs / Google Sheets
