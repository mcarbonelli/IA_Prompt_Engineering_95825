# Identificación Automática de Medidores Eléctricos con IA

# Fast Prompting – Proof of Concept (POC)

## Descripción

Este proyecto implementa una **Proof of Concept (POC)** utilizando la API de OpenAI para demostrar la aplicación de técnicas de **Fast Prompting** en la generación de imágenes.

El objetivo es validar técnicamente que una optimización estructurada de prompts mejora la calidad, precisión y consistencia de los resultados generados por el modelo.

## Objetivos

- Implementar generación de imágenes usando la API de OpenAI.
- Comparar versiones de prompts (V1 vs V2 vs V3).
- Aplicar técnicas de Fast Prompting.
- Validar mejoras en calidad y control del resultado.
- Documentar resultados de manera reproducible.

---

## Concepto de POC

Una **Proof of Concept** demuestra que una idea es técnicamente viable.

Para mi caso:
- Se generan imágenes con diferentes versiones de prompts.
- Se comparan resultados.
- Se evalúa impacto de mejoras estructurales en el prompt.

No es un producto final, sino una validación funcional.

---

## Estructura del Proyecto

├── .venv/                                       # Entorno virtual 
├── .docs/                                       # Pdfs de la presentaciones   
├── imagenes/                                    # Imágenes generadas por la API y muestras/ejemplos de medidores
│   └── guia_capacitacion_medidor.png
├── notebooks/
│   ├── Preentrega1_MauricioCarbonelli.ipynb     # Definición de prompts
│   └── Preentrega2_MauricioCarbonelli.ipynb
├── .env                                         # Se encuentra la API key de OpenAI
├── .gitignore
├── requirements.txt                             # Todo lo necesario para instalar en el entorno virtual
└── README.md                                    # Este documento



## Instalación

### Clonar repositorio

git clone https://github.com/mauricio-carbonelli/IA_Prompt_Engineering_95825.git
cd IA_Prompt_Engineering_95825

### Crear entorno virtual

python -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate     # Windows

### Instalar dependencias

pip install -r requirements.txt