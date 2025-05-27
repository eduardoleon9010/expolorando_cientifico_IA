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

```bash
conda create -n ai_scientist python=3.11
conda activate ai_scientist
# Instalar pdflatex
sudo apt-get install texlive-full

# Instalar requisitos PyPI
pip install -r requirements.txt
