# Práctica Temática: Propuesta Documentada de Mini Proyecto en Sistemas

## 1) Título de la práctica
**Diseño de Propuesta para Práctica Temática Pequeña**

> Ejemplos de tema que puedes elegir:
> - **Mini Toolkit en ARM64**
> - **Asistente de Estudio en Terminal**
> - **Reporteador de Información del Sistema**
> - **Organizador de Archivos**
> - **Juego de Aprendizaje en Línea de Comandos**

---

## 2) Descripción general
En esta actividad vas a **diseñar y documentar** una propuesta de proyecto pequeño para una práctica temática de arquitectura de computadoras y programación de sistemas.

### Objetivo central
Que construyas una propuesta clara, viable y bien justificada **antes de programar mucho código**.

### Lenguaje principal (elige uno)
- ARM64 Assembly
- C
- Python
- Bash

> **Nota importante para ARM64 Assembly:** se recomienda **solo para programas muy pequeños** (por ejemplo: operaciones básicas, manejo simple de entrada/salida, utilidades mínimas de terminal).

### Alcance esperado
- Proyecto pequeño, realizable en tiempo corto.
- Enfoque en documentación: idea, caso de uso, estructura y plan de pruebas.
- Evita soluciones complejas o de gran escala.

### Restricciones técnicas
Para mantener la actividad accesible (incluyendo uso de IA con límites), **NO** se permite:
- Frameworks grandes.
- APIs pagadas.
- Bases de datos.
- Servicios en la nube.
- Contenedores (Docker, etc.).
- Dependencias complejas o pesadas.

---

## 3) Entregables del estudiante
Tu repositorio debe incluir **como mínimo**:
- `README.md`
- `docs/propuesta.md`
- `docs/caso_de_uso.md`
- `docs/estructura_repositorio.md`
- `docs/plan_de_pruebas.md`

Opcional (si decides incluir código inicial):
- `src/`
- `scripts/`
- `tests/`

---

## 4) Estructura recomendada del repositorio
Usa esta estructura base:

```text
nombre-del-proyecto/
├── README.md
├── docs/
│   ├── propuesta.md
│   ├── caso_de_uso.md
│   ├── estructura_repositorio.md
│   └── plan_de_pruebas.md
├── src/
│   └── main.<ext>
├── scripts/
│   └── run.sh
└── tests/
    └── test_plan.md
```

> `<ext>` depende del lenguaje elegido (`s`, `c`, `py`, `sh`).

---

## 5) Contenido mínimo por archivo

### `README.md`
Debe contener:
1. Nombre del proyecto.
2. Tema elegido.
3. Lenguaje principal y justificación breve.
4. Objetivo general (1 párrafo).
5. Alcance (qué sí incluye y qué no incluye).
6. Estructura del repositorio (resumen).
7. Instrucciones rápidas de ejecución (si ya hay prototipo).

### `docs/propuesta.md`
Incluye:
1. **Planteamiento del problema** (¿qué necesidad atiende?).
2. **Propuesta de solución** (mini herramienta o mini práctica).
3. **Usuarios objetivo** (quién la usaría y en qué contexto).
4. **Requerimientos funcionales** (3 a 6 puntos máximos).
5. **Requerimientos no funcionales** (simplicidad, portabilidad, tiempo de ejecución, etc.).
6. **Alcance técnico limitado** (qué NO vas a implementar).
7. **Justificación del tamaño pequeño** (por viabilidad y recursos).

### `docs/caso_de_uso.md`
Incluye al menos:
1. Nombre del caso de uso principal.
2. Actor principal.
3. Precondiciones.
4. Flujo principal paso a paso (5 a 10 pasos).
5. Flujos alternos (mínimo 1).
6. Resultado esperado.

### `docs/estructura_repositorio.md`
Incluye:
1. Árbol del repositorio actualizado.
2. Explicación breve de cada carpeta y archivo.
3. Convenciones de nombres (archivos, scripts y pruebas).
4. Decisiones de organización (por qué esa estructura y no otra).

### `docs/plan_de_pruebas.md`
Incluye:
1. Estrategia de pruebas manuales (mínimo 5 casos).
2. Para cada caso: objetivo, entrada, pasos, salida esperada.
3. Criterios de aceptación mínimos.
4. Riesgos conocidos y cómo mitigarlos.

---

## 6) Requisitos de calidad de la documentación
- Redacción clara, concreta y técnica.
- Ortografía y formato consistentes en Markdown.
- Coherencia entre propuesta, caso de uso y plan de pruebas.
- El alcance debe ser realista para un mini proyecto.

---

## 7) Sugerencias de temas pequeños (opcional)
Puedes inspirarte en ideas como:
- **Bash/Python:** organizador de archivos por extensión.
- **C:** visor de estadísticas básicas de un archivo de texto.
- **ARM64 Assembly:** calculadora mínima de operaciones enteras.
- **Bash:** asistente de comandos frecuentes con menú de texto.
- **Python:** generador de checklist de estudio en terminal.

---

## 8) Rúbrica sugerida (100 puntos)
1. **Claridad de la propuesta** (20 pts)
2. **Definición del caso de uso** (20 pts)
3. **Estructura y organización del repositorio** (20 pts)
4. **Calidad del plan de pruebas** (20 pts)
5. **Coherencia técnica y alcance realista** (20 pts)

---

## 9) Criterios de aceptación
Se considera entrega válida si:
- Incluye todos los archivos obligatorios.
- La propuesta describe un proyecto pequeño y viable.
- El caso de uso es entendible y comprobable.
- El plan de pruebas permite validar el comportamiento esperado.
- La documentación está completa, ordenada y consistente.

---

## 10) Instrucciones de entrega en GitHub Classroom
1. Crea/usa tu repositorio asignado en GitHub Classroom.
2. Sube la estructura mínima solicitada.
3. Completa los archivos de documentación.
4. Realiza al menos un commit final con mensaje claro, por ejemplo:
   - `docs: propuesta inicial de práctica temática`
5. Verifica que todos los archivos se vean correctamente en GitHub.

---

## 11) Recomendación final del instructor
Primero diseña, luego codifica. Si tu documentación está bien pensada, implementar un prototipo pequeño será mucho más rápido y con menos errores.
