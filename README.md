# Explorando AI-Scientist 🧠🤖

Este repositorio es una copia basada en el proyecto original [AI-Scientist](https://github.com/SakanaAI/AI-Scientist) desarrollado por **SakanaAI**.

Este espacio tiene fines de aprendizaje, documentación, y posible extensión del proyecto original, con respeto por la autoría y cumpliendo con la [Licencia Apache 2.0](LICENSE).

## 📁 Contenido original

El código original ha sido mantenido sin modificaciones en esta versión. Para más información técnica, consulta la documentación original o visita [SakanaAI](https://github.com/SakanaAI/AI-Scientist).

## ✍️ Créditos

Créditos al equipo de SakanaAI por su contribución al campo de la inteligencia artificial.

---
<h1 align="center">
  <a href="https://github.com/SakanaAI/AI-Scientist/blob/main/docs/logo_2.png">
    <img src="docs/logo_2.png" width="215" /></a><br>
  <b>El Científico de IA: Hacia un Descubrimiento Científico</b><br>
  <b>Completamente Automatizado y Abierto 🧑‍🔬</b><br>
</h1>

<p align="center">
  📚 <a href="https://arxiv.org/abs/2408.06292">[Artículo]</a> |
  📝 <a href="https://sakana.ai/ai-scientist/">[Entrada de Blog]</a> |
  📂 <a href="https://drive.google.com/drive/folders/1G7A0wTqfXVa-cpexjk0oaXakaSJwffEt">[Carpeta Drive]</a>
</p>

Uno de los grandes desafíos de la inteligencia artificial es desarrollar agentes capaces de realizar investigación científica y descubrir nuevos conocimientos. Aunque ya se han utilizado modelos de vanguardia para ayudar a científicos humanos —por ejemplo, para generar ideas o escribir código—, todavía requieren supervisión manual extensa o están fuertemente limitados a tareas específicas.

Nos entusiasma presentar **El Científico de IA**, el primer sistema integral para el descubrimiento científico totalmente automático, que permite que modelos fundamentales como los Grandes Modelos de Lenguaje (LLMs) realicen investigaciones de manera independiente.

Proveemos todas las ejecuciones y datos de nuestro artículo [aquí](https://drive.google.com/drive/folders/1G7A0wTqfXVa-cpexjk0oaXakaSJwffEt?usp=sharing), donde ejecutamos cada modelo base en cada plantilla con aproximadamente 50 ideas. Recomendamos *encarecidamente* leer algunos de los [artículos de Claude](https://drive.google.com/drive/folders/1Mmpz6M1FK4q8e-SewgZcUzdeD0Q2zC39?usp=sharing) para entender las fortalezas y debilidades del sistema. Aquí algunos ejemplos de artículos generados por **El Científico de IA** 📝:

1. [DualScale Diffusion: Equilibrio Adaptativo de Características para Modelos Generativos de Baja Dimensionalidad](https://github.com/SakanaAI/AI-Scientist/blob/main/example_papers/adaptive_dual_scale_denoising.pdf)
2. [Adaptación Multi-escala de Ruido en Grillas: Mejorando Modelos de Difusión para Datos de Baja Dimensión](https://github.com/SakanaAI/AI-Scientist/blob/main/example_papers/grid_based_noise_adaptation.pdf)
3. [Difusión Mejorada con GAN: Impulsando Calidad y Diversidad de Muestras](https://github.com/SakanaAI/AI-Scientist/blob/main/example_papers/gan_diffusion.pdf)
4. [DualDiff: Mejorando la Captura de Modos en Modelos de Difusión de Baja Dimensión mediante Desenfoque Dual-Experto](https://github.com/SakanaAI/AI-Scientist/tree/main/example_papers/dual_expert_denoiser.pdf) 
5. [StyleFusion: Generación Multi-estilo Adaptativa en Modelos de Lenguaje a Nivel de Caracteres](https://github.com/SakanaAI/AI-Scientist/blob/main/example_papers/multi_style_adapter.pdf)
6. [Tasas de Aprendizaje Adaptativas para Transformers mediante Q-Learning](https://github.com/SakanaAI/AI-Scientist/tree/main/example_papers/rl_lr_adaptation.pdf)
7. [Desbloqueando Grokking: Estudio Comparativo de Estrategias de Inicialización de Pesos en Modelos Transformer](https://github.com/SakanaAI/AI-Scientist/tree/main/example_papers/weight_initialization_grokking.pdf)
8. [Grokking Acelerado: Tasas de Aprendizaje por Capa para la Generalización en Transformers](https://github.com/SakanaAI/AI-Scientist/tree/main/example_papers/layerwise_lr_grokking.pdf)
9. [Grokking a través de la Compresión: Revelando la Generalización Súbita mediante la Longitud Mínima de Descripción](https://github.com/SakanaAI/AI-Scientist/tree/main/example_papers/mdl_grokking_correlation.pdf)
10. [Acelerando la Intuición Matemática: Impulsando Grokking mediante Aumento Estratégico de Datos](https://github.com/SakanaAI/AI-Scientist/tree/main/example_papers/data_augmentation_grokking.pdf)

> **Nota:**  
> **¡Precaución!** Esta base de código ejecutará código generado por LLM. Existen diversos riesgos y desafíos asociados con esta autonomía, incluyendo el uso de paquetes potencialmente peligrosos, acceso a la web y la posible creación de procesos. Utilice bajo su propia responsabilidad. Asegúrese de [usar contenedores](#containerization) y restringir el acceso web apropiadamente.

<p align="center">
  <a href="https://github.com/SakanaAI/AI-Scientist/blob/main/example_papers/adaptive_dual_scale_denoising/adaptive_dual_scale_denoising.pdf"><img src="https://github.com/SakanaAI/AI-Scientist/blob/main/docs/anim-ai-scientist.gif" alt="Adaptive Dual Scale Denoising" width="80%" />
</a></p>

## Tabla de Contenidos

1. [Introducción](#introduction)
2. [Requisitos](#requirements)
   - [Instalación](#installation)
   - [Modelos soportados y claves API](#supported-models-and-api-keys)
3. [Configuración de las Plantillas](#setting-up-the-templates)
   - [Plantilla NanoGPT](#nanogpt-template)
   - [Plantilla Difusión 2D](#2d-diffusion-template)
   - [Plantilla Grokking](#grokking-template)
4. [Ejecutar Experimentos de Generación de Artículos con AI Scientist](#run-ai-scientist-paper-generation-experiments)
5. [Obtener una Revisión de Artículo Generado por LLM](#getting-an-llm-generated-paper-review)
6. [Crear Tu Propia Plantilla](#making-your-own-template)
   - [Plantillas Contribuidas por la Comunidad](#community-contributed-templates)
7. [Recursos de Plantillas](#template-resources)
8. [Cómo Citar El Científico de IA](#citing-the-ai-scientist)
9. [Preguntas Frecuentes](#frequently-asked-questions)
10. [Contenerización](#containerization)

## Introducción

Proveemos tres plantillas usadas en nuestro artículo, que cubren los siguientes dominios: **NanoGPT**, **Difusión 2D** y **Grokking**. Estas plantillas permiten que El Científico de IA genere ideas y realice experimentos en estas áreas. Aceptamos contribuciones de nuevas plantillas por parte de la comunidad, pero tenga en cuenta que no son mantenidas por nosotros. Todas las demás plantillas, más allá de las tres proporcionadas, son contribuciones comunitarias.

## Requisitos

Este código está diseñado para ejecutarse en Linux con GPUs NVIDIA usando CUDA y PyTorch. El soporte para otras arquitecturas GPU puede ser posible siguiendo las [guías de PyTorch](https://pytorch.org/get-started/locally/). Las plantillas actuales probablemente tomen un tiempo inviable en máquinas sin GPU. Ejecutarlo en otros sistemas operativos puede requerir ajustes significativos.

### Instalación

```
conda create -n ai_scientist python=3.11
conda activate ai_scientist
# Instalar pdflatex
sudo apt-get install texlive-full

# Instalar requisitos PyPI
pip install -r requirements.txt
```
**Note:** Installing `texlive-full` can take a long time. You may need to [hold Enter](https://askubuntu.com/questions/956006/pregenerating-context-markiv-format-this-may-take-some-time-takes-forever) during the installation.

### Modelos Soportados y Claves API
Soportamos una gran variedad de modelos, incluyendo modelos de código abierto y aquellos accesibles solo vía API. En general, recomendamos utilizar únicamente modelos de frontera con capacidad superior a la del GPT-4 original. Para ver una lista completa de modelos soportados, consulta aquí.

**API de OpenAI (GPT-4o, GPT-4o-mini, modelos o1)**
Por defecto, utiliza la variable de entorno OPENAI_API_KEY.

**API de Anthropic (Claude Sonnet 3.5)**
Por defecto, utiliza la variable de entorno ANTHROPIC_API_KEY.

**Modelos Claude vía Bedrock**
Para los modelos Claude proporcionados por Amazon Bedrock, instala estos paquetes adicionales:
```
pip install anthropic[bedrock]
```
Luego, especifica un conjunto de credenciales válidas de AWS y la región objetivo:

Establece las variables de entorno: AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY, AWS_REGION_NAME.

**Modelos Claude vía Vertex AI**
Para los modelos Claude disponibles en Vertex AI Model Garden, instala estos paquetes adicionales:
```
pip install google-cloud-aiplatform
pip install anthropic[vertex]
```
Luego, configura la autenticación para un proyecto en Google Cloud, por ejemplo especificando la región y el ID del proyecto:
```
export CLOUD_ML_REGION="REGIÓN"             # para llamada a Model Garden
export ANTHROPIC_VERTEX_PROJECT_ID="ID_PROYECTO"  # para llamada a Model Garden
export VERTEXAI_LOCATION="REGIÓN"           # para llamada Aider/LiteLLM
export VERTEXAI_PROJECT="ID_PROYECTO"       # para llamada Aider/LiteLLM
```
**API de DeepSeek (deepseek-chat, deepseek-reasoner)**
Por defecto, utiliza la variable de entorno DEEPSEEK_API_KEY.

**API de OpenRouter (Llama3.1)**
Por defecto, utiliza la variable de entorno OPENROUTER_API_KEY.

**Google Gemini**
Soportamos modelos Gemini de Google (por ejemplo, "gemini-1.5-flash", "gemini-1.5-pro") mediante la librería Python google-generativeai. Por defecto, se utiliza la variable de entorno:
```
export GEMINI_API_KEY="TU CLAVE GEMINI"
```
**API de Semantic Scholar (Búsqueda de Literatura)**
Nuestro código puede utilizar opcionalmente una clave API de Semantic Scholar (S2_API_KEY) para una mayor capacidad de búsqueda si tienes una, aunque en principio debería funcionar sin ella. Si tienes problemas con Semantic Scholar, puedes omitir las fases de búsqueda y citación durante la generación de artículos.

Asegúrate de proporcionar la clave para el modelo que uses en tus ejecuciones, por ejemplo:
```
export OPENAI_API_KEY="TU CLAVE AQUÍ"
export S2_API_KEY="TU CLAVE AQUÍ"
```
**API de OpenAlex (Alternativa de Búsqueda de Literatura)**
La API de OpenAlex puede usarse como alternativa si no tienes una clave de Semantic Scholar. OpenAlex no requiere clave de API.
```
pip install pyalex
export OPENALEX_MAIL_ADDRESS="TU CORREO ELECTRÓNICO"
```
Y especifica --engine openalex al ejecutar el código de AI Scientist.

Ten en cuenta que esto es experimental para quienes no tienen una clave de Semantic Scholar.

## Configuración de las plantillas

### Plantilla NanoGPT

La plantilla **NanoGPT** genera artículos científicos a partir de tareas de lenguaje en miniatura con modelos de lenguaje. Utiliza código personalizado para NanoGPT y recopila métricas durante el entrenamiento y la evaluación.

### Plantilla de Difusión 2D

Esta plantilla emplea modelos de difusión simples en 2D para generar artículos científicos. Incluye múltiples variantes de entrenamiento y configuraciones para explorar cómo los modelos de difusión pueden optimizarse para datos de baja dimensión.

### Plantilla Grokking

La plantilla **Grokking** está diseñada para explorar el fenómeno del "grokking", donde un modelo muestra una súbita generalización tras un periodo de sobreajuste. Esta plantilla permite investigar configuraciones de redes neuronales que ilustran este fenómeno.

## Ejecutar Experimentos de Generación de Artículos con AI Scientist

Puedes ejecutar la generación de artículos científicos utilizando los modelos base seleccionados en las plantillas proporcionadas. Por ejemplo, para ejecutar la plantilla de NanoGPT, usa el siguiente comando:

```
python ai_scientist/run_ai_scientist.py \
  --template nanogpt \
  --engine gpt-4o \
  --num_ideas 20
```
Este código generará artículos completos y almacenará todos los resultados, incluyendo los resúmenes, ideas generadas, código ejecutado, resultados experimentales y el PDF final.

#### Obtener una Revisión de Artículo Generado por LLM
También puedes usar AI Scientist para obtener una revisión de los artículos generados. El revisor AI proporciona sugerencias para mejorar el contenido, la organización y la claridad del artículo:
```
python ai_scientist/review_ai_scientist.py \
  --input_path path/to/generated/paper
```
**Crear tu propia plantilla**
Puedes diseñar tus propias plantillas para generar artículos científicos en dominios personalizados. Solo necesitas crear un archivo Python siguiendo el formato de las plantillas existentes e integrarlo al sistema.

**Plantillas contribuidas por la comunidad**
Aceptamos nuevas plantillas por parte de la comunidad. Estas plantillas deben incluir instrucciones claras sobre su funcionamiento, dependencias y dominios de aplicación.

  ***⚠️ Nota: No damos soporte a las plantillas comunitarias.***

**Recursos de plantillas**
En el directorio ai_scientist/templates/, encontrarás ejemplos de cómo están estructuradas las plantillas. Cada plantilla incluye:

- Archivos para generación de ideas
- Código para experimentación
- Código para análisis y visualización
- Código para generar el PDF final

##Cómo Citar AI Scientist
Si utilizas este trabajo en tu investigación, por favor cita nuestro artículo:

> AI Scientist: LLMs can generate scientific papers from arbitrary experimental results  
> Tianjun Zhang, Saurav Kadavath, Andy Zou, Kunjal Kshirsagar, Laria Reynolds, Arka Sadhu, Shinnosuke Saito, Sharon Zhou, Xiangning Chen, Pieter Abbeel, Joseph Gonzalez, Ludwig Schmidt  
> [https://arxiv.org/abs/2405.17711](https://arxiv.org/abs/2405.17711)

**BibTeX:**

```
@article{zhang2024ai,
  title={AI Scientist: LLMs can generate scientific papers from arbitrary experimental results},
  author={Zhang, Tianjun and Kadavath, Saurav and Zou, Andy and Kshirsagar, Kunjal and Reynolds, Laria and Sadhu, Arka and Saito, Shinnosuke and Zhou, Sharon and Chen, Xiangning and Abbeel, Pieter and others},
  journal={arXiv preprint arXiv:2405.17711},
  year={2024}
}
```

## Preguntas frecuentes

Te recomendamos leer nuestro artículo antes de consultar esta sección, ya que ahí respondemos muchas de las preguntas más comunes sobre *The AI Scientist*.

**¿Por qué me faltan archivos al ejecutar The AI Scientist?**

Asegúrate de haber completado todos los pasos de configuración y preparación antes de ejecutar el script principal del experimento.

**¿Por qué no se ha generado un PDF o una revisión?**

*The AI Scientist* completa una idea con una tasa de éxito que depende de la plantilla utilizada, el modelo base empleado y la complejidad de la idea. Te sugerimos consultar nuestro artículo principal. Las tasas de éxito más altas se observan con Claude Sonnet 3.5. Las revisiones funcionan mejor con GPT-4o; los demás modelos tienden a presentar sesgos de positividad o fallan al cumplir con el formato requerido.

**¿Cuál es el costo de generar cada idea?**

Generalmente, menos de 15 USD por artículo utilizando Claude Sonnet 3.5. Recomendamos DeepSeek Coder V2 como una alternativa más económica. Puedes consultar el [ranking de Aider](https://aider.chat/docs/leaderboards/) para descubrir nuevos modelos recomendados.

**¿Cómo cambio el formato base del artículo generado?**

Debes modificar el archivo `template.tex` correspondiente dentro de cada plantilla.

**¿Cómo ejecuto The AI Scientist para diferentes áreas temáticas?**

Consulta las instrucciones específicas para cada plantilla. En esta versión actual, está restringido a ideas que se pueden expresar en código. ¡Sin embargo, eliminar esta restricción sería un trabajo futuro muy interesante! :)

**¿Cómo agrego soporte para un nuevo modelo base?**

Puedes modificar `ai_scientist/llm.py` para agregar soporte para un nuevo modelo base. No recomendamos usar modelos que sean significativamente menos potentes que GPT-4 para **The AI Scientist**.

**¿Por qué necesito ejecutar las pruebas base (baseline) yo mismo?**

Estas pruebas aparecen como `run_0` y deben ejecutarse en cada máquina donde corras **The AI Scientist** para obtener comparaciones de tiempo de ejecución precisas, debido a las diferencias de hardware.

**¿Qué hago si tengo problemas para acceder a la API de Semantic Scholar?**

Usamos la API de Semantic Scholar para verificar la novedad de las ideas y recopilar citas para la redacción del artículo. Puedes omitir estas fases si no tienes una clave API o si la API es lenta o inaccesible.

## Contenerización (Containerization)

Incluimos una imagen Docker [contribuida por la comunidad](https://github.com/SakanaAI/AI-Scientist/pull/21) que puede ayudarte con la contenerización, disponible en `experimental/Dockerfile`.

Puedes usar esta imagen así:

```
# Script de endpoint
docker run -e OPENAI_API_KEY=$OPENAI_API_KEY -v `pwd`/templates:/app/AI-Scientist/templates <AI_SCIENTIST_IMAGE> \
  --model gpt-4o-2024-05-13 \
  --experiment 2d_diffusion \
  --num-ideas 2
```
```
# Modo interactivo
docker run -it -e OPENAI_API_KEY=$OPENAI_API_KEY \
  --entrypoint /bin/bash \
  <AI_SCIENTIST_IMAGE>
```

### Historia de las estrellas (Star History)
[![Gráfico de la historia de las estrellas](https://api.star-history.com/svg?repos=SakanaAI/AI-Scientist&type=Date)](https://star-history.com/#SakanaAI/AI-Scientist&Date)
