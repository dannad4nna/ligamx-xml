# Diseño y validación de resultados de Liga MX con XML y DTD

## 1. Propósito

<!-- Describe en 2 o 3 líneas qué hace este proyecto y qué se representa en el XML. -->

## 2. Análisis de la información (Actividad 1)

| Pregunta | Respuesta |
|---|---|
| ¿Cuál debería ser el elemento raíz? | |
| ¿Una jornada puede contener varios partidos? | |
| ¿Cada partido debe contener exactamente dos equipos? | |
| ¿Cómo distinguir al equipo local del visitante? | |
| ¿El marcador es un solo dato o se separan los goles? | |
| ¿Las estadísticas pertenecen al partido o a cada equipo? | |
| ¿Qué datos son obligatorios? | |
| ¿Cuáles son opcionales? | |

## 3. Modelo jerárquico (Actividad 2)

```text
liga
│
└── jornada
    │
    ├── partido
    │   ├── equipoLocal
    │   ├── equipoVisitante
    │   ├── marcador
    │   └── estadisticas
    ├── partido
    └── partido
```

<!-- Amplía este árbol con tu diseño final. -->

## 4. Elemento o atributo (Actividad 2)

| Información | Elemento/Atributo | Justificación |
|---|---|---|
| Jornada | | |
| Fecha | | |
| ID del partido | | |
| Equipo local | | |
| Equipo visitante | | |
| Goles | | |
| Estadio | | |
| Estado del partido | | |
| Posesión | | |
| Tarjetas | | |

## 5. Estadísticas seleccionadas (Actividad 4)

| Estadística | Elemento/Atributo | Obligatoria u opcional |
|---|---|---|
| Posesión | | |
| Tiros | | |
| Tiros a puerta | | |
| Faltas | | |
| Tarjetas | | |
| Tiros de esquina | | |

### Decisión de diseño

Opción elegida:

<!-- Estadísticas dentro de cada equipo, dentro del partido, u otra. -->

| Criterio | Justificación |
|---|---|
| Comprensibilidad | |
| Reducción de duplicación | |
| Facilidad de procesamiento | |
| Posibilidad de agregar estadísticas | |

## 6. Cardinalidades del DTD (Actividad 5)

| Regla | Expresión DTD |
|---|---|
| Una liga contiene una o más jornadas | |
| Una jornada contiene uno o más partidos | |
| Un partido tiene exactamente un local | |
| Un partido tiene exactamente un visitante | |
| Una estadística opcional | |
| Puede haber cero o más tarjetas | |

## 7. Atributos (Actividad 6)

| Elemento | Atributo | Tipo | Obligatorio (`#REQUIRED`/`#IMPLIED`) |
|---|---|---|---|
| | | | |
| | | | |
| | | | |
| | | | |

**Pregunta:** si cada partido tiene un identificador `P001`, `P002`, etc., ¿qué ventaja tiene declararlo como `ID` en lugar de `CDATA`?

Respuesta:

## 8. Asociación XML y DTD (Actividad 7)

Ruta relativa del XML al DTD:

```text

```

Declaración utilizada:

```xml

```

## 9. Instrucciones de validación

<!-- Indica cómo validar el XML: comando, herramienta y resultado esperado. -->

```powershell

```

## 10. Pruebas negativas (Actividad 8)

| Prueba | ¿Bien formado? | ¿Válido? | Error detectado |
|---|---|---|---|
| Falta visitante | | | |
| Dos locales | | | |
| Orden incorrecto | | | |
| Falta atributo obligatorio | | | |
| ID duplicado | | | |
| Elemento desconocido | | | |

> XML bien formado ≠ XML válido

Conclusión:

## 11. Jornada del domingo 27 de septiembre de 2026 (Actividad 9)

| Partido | Local | Marcador | Visitante |
|---|---|---|---|
| P001 | | | |
| P002 | | | |
| P003 | | | |
| P004 | | | |
| P005 | | | |

## 12. Decisiones ante el cambio de requisitos

| Información nueva | ¿Es un requisito legítimo? | Decisión | ¿Se modificó el DTD? |
|---|---|---|---|
| | | | |
| | | | |

## 13. Estructura del repositorio

```text
liga-mx-xml/
├── README.md
├── xml/
│   ├── resultados.xml
│   └── resultados-invalido.xml
└── dtd/
    └── resultados.dtd
```

## 14. Enlace al repositorio

<!-- https://github.com/TU_USUARIO/liga-mx-xml -->
