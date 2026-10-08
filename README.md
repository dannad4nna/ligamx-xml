# Diseño y validación de resultados de Liga MX con XML y DTD

## 1. Proposito

Esta practica tiene como proposito diseñar un un formato XML para representar informacion estructurada de partidos de futbol 

## 2. Analisis de la informacion 

| Pregunta | Respuesta |

| Cual deberia ser el elemento raiz? |liga mx  |
| Una jornada puede contener varios partidos? |Si |
| Cada partido debe contener exactamente dos equipos? |Si, uno local y otro visitante |
| Como distinguir al equipo local del visitante? |Elementos distintos equipoLocal y equipoVisitante |
| El marcador es un solo dato o se separan los goles? |Separado|
| Las estadisticas pertenecen al partido o a cada equipo? |De cada equipo |
| Que datos son obligatorios? |id, fecha, numero de jornada, equipos, marcador |
| Cuales son opcionales? |estadio, estadidisticas  |

## 3. Modelo jerarquico 


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




## 4. Elemento o atributo

| Informacion | Elemento/Atributo | Justificacion |
| Jornada |Atributo | |
| Fecha | |Atributo |Es una propiedad directa del partido |
| ID del partido |Atributo |Es el identificador unico |
| Equipo local |Elemento | Representa una entidad compleja que suele contener sub-elementos|
| Equipo visitante |Elemento |Igual que el equipo local, es una estructura que contiene mas informacion |
| Goles | Elemento|Puede contener estructura detallada (minuto, quien metio gol) |
| Estadio |Elemento |es un objeto  independiente que puede incluir atributos  |
| Estado del partido |Atributo |Simple dato de estado |
| Posesion | Atributo |dato estadistico numerico o porcentaje |
| Tarjetas |Elemento | es una lista repetitiva de eventos|


Determine las cardinalidades y completar la siguiente tabla:

|Regla                               | Expresion DTD
Una liga contiene una o mas jornadas | + 
Una jornada contiene uno o mas partidos| +
Un partido tiene exactamente un  local | ?
Un partido tiene exactamente un visitante | ?
Una estadistica opcional | *
Puede haber cero o mas tarjetas | *