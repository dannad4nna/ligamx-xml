# Diseño y validación de resultados de Liga MX con XML y DTD

## 1. Propósito

Esta practica tiene como proposito diseñar un un formato XML para representar informacion estructurada de partidos de futbol 

## 2. Analisis de la informacion (Actividad 1)

| Pregunta | Respuesta |

| Cual deberia ser el elemento raiz? |liga mx  |
| Una jornada puede contener varios partidos? |Si |
| Cada partido debe contener exactamente dos equipos? |Si, uno local y otro visitante |
| Como distinguir al equipo local del visitante? |Elementos distintos equipoLocal y equipoVisitante |
| El marcador es un solo dato o se separan los goles? |Separado|
| Las estadisticas pertenecen al partido o a cada equipo? |De cada equipo |
| Que datos son obligatorios? |id, fecha, numero de jornada, equipos, marcador |
| Cuales son opcionales? |estadio, estadidisticas  |

## 3. Modelo jerarquico (Actividad 2)


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


