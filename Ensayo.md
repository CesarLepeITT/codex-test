# Ensayo Documental

**Estudiante:** César Lepe Garcia
**Plataforma de Simulación:** Wokwi
**Microcontrolador:** Raspberry Pi Pico W
**Lenguaje:** C++ (Arduino Core / Pico SDK)

## 1. Introducción y Descripción del Proyecto
En esta práctica se desarrolló y documentó un circuito electrónico interactivo utilizando una Raspberry Pi Pico W. El hardware consta de un teclado matricial (membrane keypad) de 4x4 y un arreglo de 12 LEDs (8 azules y 4 rojos) conectados individualmente a los pines GPIO de la placa mediante resistencias de 220 Ω, además de resistencias pull-up de 1 kΩ para el teclado. 

El objetivo principal del firmware (escrito en C++) es mapear las entradas del teclado para controlar los LEDs. Las teclas numéricas del `1` al `8` y las letras de la `A` a la `D` encienden LEDs individuales de forma directa. Además, se implementó control por grupos: la tecla `9` enciende los 8 LEDs azules simultáneamente, mientras que la tecla `0` los apaga. De manera similar, la tecla `*` enciende los 4 LEDs rojos y la tecla `#` los apaga.

## 2. Metodología de Documentación asistida por IA (CODEX)
Para estructurar el repositorio y generar la documentación técnica de este proyecto, se utilizó el agente de Inteligencia Artificial "CODEX", asumiendo el rol de un Ingeniero Principal de Sistemas Embebidos. 

Durante este proceso, se abordaron y resolvieron dos retos principales respecto al uso de la herramienta:

* **Limitación de Visión Artificial (OCR):** Dado que CODEX opera estrictamente como un agente de texto y carece de capacidades de visión por computadora, no era posible simplemente enviarle una captura de pantalla del circuito en Wokwi. Para solucionar esto, se empleó un modelo auxiliar (ChatGPT), al cual se le proporcionó la imagen del diagrama para obtener una descripción interpretativa en texto puro. Esta descripción detallaba qué componentes estaban presentes y cómo interactuaban.
* **Optimización del Idioma (Prompt Engineering):** Siguiendo las mejores prácticas, el "Mega-Prompt" final fue redactado y suministrado a CODEX íntegramente en inglés. Debido a que la mayoría de los Modelos Fundacionales (Foundation Models) son entrenados con corpus de datos predominantemente en inglés, interactuar en este idioma garantizó un resultado mucho más preciso, generando una estructura de directorios técnica y un archivo `README.md` de nivel profesional.

Al prompt se le inyectó el código fuente en C++, el archivo `diagram.json` extraído de Wokwi y la descripción textual del circuito generada previamente.

## 3. Resultados y Conclusión
La IA procesó los datos y estructuró con éxito un repositorio completo sin alterar la lógica de control principal del firmware. CODEX generó un archivo `CMakeLists.txt` para la compilación, ubicó el código en un directorio `src/main.cpp` y, lo más importante, construyó la documentación en una carpeta `docs/` detallando el mapeo de los pines (wiring) y la arquitectura.

**Conclusión:**
Esta práctica demuestra que integrar herramientas como CODEX en el flujo de trabajo de sistemas embebidos automatiza drásticamente la creación de documentación estructurada (scaffolding). El desarrollador humano puede centrarse en la lógica electrónica y de programación en simuladores como Wokwi, mientras que la IA, alimentada con el contexto correcto (JSON y descripciones puente vía ChatGPT), se encarga de estandarizar la entrega del proyecto.

---

## Enlaces de Entrega

* **Simulación en Wokwi:** [(https://wokwi.com/projects/300124198602277389)]
