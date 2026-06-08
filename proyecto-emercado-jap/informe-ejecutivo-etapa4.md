# Informe Ejecutivo — Etapa 4: Evaluación

## Proyecto e-Mercado JAP | Grupo 280 — Equipo 4 | 2023

**Autora:** Sharon Pereira — Coordinadora de Retroalimentación / Líder de Documentación

---

## Resumen ejecutivo

Este informe resume las conclusiones y resultados del proceso de testing llevado a cabo
a lo largo del proyecto e-Mercado. El objetivo principal fue evaluar la calidad del
software, su funcionalidad, seguridad, rendimiento y usabilidad. A lo largo de las
distintas fases, el equipo trabajó para identificar y documentar cualquier problema que
pudiera afectar la integridad y operación del sistema.

---

## Conclusiones generales

### Calidad del software

Se reconoce estabilidad en algunas áreas, pero la presencia de errores críticos indica
deficiencias en la calidad general. Las pruebas de regresión no confirmaron que las
nuevas implementaciones estuvieran libres de problemas, lo que indica la necesidad de
una revisión exhaustiva antes de pasar a producción.

### Funcionalidad

Persisten problemas críticos en funciones clave del sistema:

- Incapacidad para agregar artículos al carrito de compras
- Deficiencias en la identificación de campos obligatorios
- Falta de actualización de precios al modificar la cantidad de productos
- Eliminación de la opción de compra en la versión 2.0, bloqueando la funcionalidad principal

### Seguridad

Se superaron algunas pruebas de seguridad, pero persisten vulnerabilidades que no fueron
abordadas de manera efectiva. Se recomienda implementar medidas adicionales para
fortalecer la seguridad del sistema, en particular en los módulos de registro y
autenticación de usuarios.

### Rendimiento

Los tiempos de respuesta se mantuvieron por debajo de 1 segundo en condiciones normales.
Sin embargo, se identificaron restricciones de respuesta que requieren optimización para
garantizar una experiencia fluida en todas las plataformas.

### Usabilidad

- El sitio presenta claridad y consistencia visual en escritorio
- Se identificaron problemas de interfaz en dispositivos móviles
- Se recomienda ampliar el tamaño de las secciones para mejorar la accesibilidad

---

## Resultados clave

| Indicador | Resultado |
|---|---|
| Cobertura de pruebas | 100% (funcional, seguridad, rendimiento, usabilidad, APIs) |
| Total de defectos identificados | 27 |
| Defectos corregidos y verificados | 7 |
| Casos bloqueados (sin poder ejecutar) | 50% en etapa individual |
| Tiempo de respuesta promedio | Por debajo de 1 segundo |
| Reducción de vulnerabilidades críticas | 10% respecto al inicio del proyecto |

---

## Observaciones y recomendaciones finales

**Colaboración:** La comunicación efectiva entre los integrantes del equipo fue
fundamental. Se recomienda mantener esta dinámica e incorporar colaboración
interdepartamental entre los equipos de testing y desarrollo en futuros proyectos.

**Documentación:** La documentación detallada de los casos de prueba facilitó la
identificación y resolución de problemas. Se sugiere mantener y mejorar este estándar
en iteraciones futuras.

**Pruebas de usabilidad:** Se recomienda incluir pruebas de usabilidad más detalladas
desde etapas tempranas del proyecto, especialmente para dispositivos móviles.

**Seguridad:** Se sugiere priorizar los casos de seguridad en próximas iteraciones, ya
que afectan directamente la credibilidad y usabilidad del sistema.

---

## Conclusión final

El proyecto e-Mercado ha concluido su ciclo de testing. El software pasó por un proceso
riguroso de cuatro etapas. Se identificaron defectos significativos que aún requieren
atención por parte del equipo de desarrollo, en particular los relacionados con el flujo
de compra y la seguridad en el registro de usuarios. El equipo queda a disposición para
consultas adicionales o colaboración futura.
