# Identificación Automática de Medidores Eléctricos con IA

# Fast Prompting – Proof of Concept (POC)

## Descripción

Este proyecto implementa una **Proof of Concept (POC)** utilizando la API de OpenAI para demostrar la aplicación de técnicas de **Fast Prompting** en la resolución de problemas técnicos a partir de imágenes. Específicamente, se centra en la identificación de números en medidores de energía eléctrica y en la generación de materiales instruccionales visuales.

El objetivo es validar técnicamente que una optimización estructurada de prompts mejora significativamente la calidad, precisión, y consistencia de los resultados brindados por los modelos de IA.

## Objetivos

- Implementar inferencia de visión y generación de imágenes usando la API de OpenAI (modelos orientados a texto/visión y de generación visual).
- Comparar analíticamente versiones de prompts (Iteraciones V1 vs V2 vs V3).
- Aplicar técnicas avanzadas de Fast Prompting para asegurar resultados confiables y fácilmente integrables.
- Validar las mejoras en calidad y control del resultado, por ejemplo asegurando una estructura de salida en JSON.
- Documentar los resultados y costos (análisis de uso de tokens) de manera reproducible.

---

## Concepto de la POC

Una **Proof of Concept** demuestra que una idea es técnicamente viable.

En este proyecto en particular, la experimentación se divide en dos enfoques:
1. **Imagen-Texto:** Se optimizan las instrucciones a través de distintas versiones de prompts para extraer con alta precisión el número de un medidor desde una fotografía, culminando en un control de respuesta estructurada (JSON).
2. **Texto-Imagen:** Se instruye al modelo para que funcione como un experto en generación de prompts, optimizando la descripción técnica para luego generar un póster o guía de capacitación sobre cómo capturar imágenes de manera correcta y evitar lecturas defectuosas.

Se comparan los resultados a cada paso y se evalúa tanto el impacto técnico como el costo de tokens. No consiste en una aplicación final producida, sino en una sólida validación funcional del concepto y de las directrices a la hora de armar los llamados a la API.

---

## Estructura del Proyecto

El repositorio tiene la siguiente estructura de carpetas y archivos, adaptado a la entrega final:

```text
├── .venv/                                       # Entorno virtual de Python
├── docs/                                        # Documentos PDF y presentaciones del proyecto
├── imagenes/                                    # Imágenes base utilizadas y generadas por la API
│   ├── guia_capacitacion_medidor.png
│   └── medidor-viejo.jpg
├── notebooks/                                   # Notebooks de experimentación de prompts
│   ├── Preentrega1_MauricioCarbonelli.ipynb     # Definición base de prompts
│   ├── Preentrega2_MauricioCarbonelli.ipynb     # Refinamiento y pruebas intermedias
│   └── EntregaFinal_MauricioCarbonelli.ipynb    # Ejecución completa de la POC (Imagen-Texto y Texto-Imagen)
├── .env                                         # Variables de entorno (API key de OpenAI - local)
├── .gitignore                                   # Reglas de exclusión para control de versiones
├── requirements.txt                             # Lista de dependencias del entorno de Python
└── README.md                                    # Este documento de presentación
```

---

## Requisitos Previos

El proyecto se comunica con la API de OpenAI, por lo tanto requerirás tu propia clave de acceso API.  
Debes crear un archivo `.env` en la raíz del directorio con el siguiente contenido:

```env
OPENAI_API_KEY=tu_api_key_aqui
```

## Instalación

### Clonar el repositorio

```bash
git clone https://github.com/mauricio-carbonelli/IA_Prompt_Engineering_95825.git
cd IA_Prompt_Engineering_95825
```

### Crear el entorno virtual

```bash
python -m venv venv
source venv/bin/activate  # En Mac/Linux
venv\Scripts\activate     # En Windows
```

### Instalar dependencias

```bash
pip install -r requirements.txt
```

Tras instalar los requisitos, puedes navegar al directorio `notebooks/` para ejecutar los `.ipynb` (por ejemplo, `EntregaFinal_MauricioCarbonelli.ipynb`) y visualizar las experimentaciones.