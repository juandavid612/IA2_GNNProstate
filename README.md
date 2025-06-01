# Clasificación de Cáncer de Próstata con Redes Orientadas a Grafos

## 👥 Autores

**Juan David Paipa Jaimes**, **Juan Manuel Ortiz Pabón**

## 🚩 Banner

![imagen](https://github.com/user-attachments/assets/851fb5ef-a2af-4591-b561-7229428a13a6)




## 🎯 Objetivo

Desarrollar una red orientada a grafos que permita la clasificación de lesiones de cáncer de próstata.

## 🧠 Modelos Utilizados

### 🏗️ Extracción de Características

Se emplearon las siguientes **redes preentrenadas** para extraer características de las imágenes:

- `ResNet34`
- `ResNet100`
- `EfficientNet_b0`
- `VGG19`

### 🧩 Redes de Clasificación Basadas en Grafos

Se exploraron varias arquitecturas orientadas a grafos:

- **GCN (Graph Convolutional Network)**: Realiza operaciones de convolución sobre el grafo, capturando características de los nodos vecinos.
- **GraphSAGE**: Agrega información de un número fijo de vecinos mediante funciones de agregación.
- **GAT (Graph Attention Network)**: Introduce mecanismos de atención para ponderar la influencia de cada vecino.
- **GIN (Graph Isomorphism Network)**: Utiliza capas fully-connected para aprender funciones de agregación más potentes.

## 🔗 Enlaces

- 📈 **Diapositivas**:
  [https://www.canva.com/design/DAGo4NlIXqI/jwmngl2Bm7tya8zJGd_4qg/edit?utm_content=DAGo4NlIXqI&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton](https://www.canva.com/design/DAGo4NlIXqI/jwmngl2Bm7tya8zJGd_4qg/edit?utm_content=DAGo4NlIXqI&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
- 📹 **Video**: -
- 📁 **Carpeta Google Drive**:
  [https://drive.google.com/drive/folders/1KVk8y6Z24sh3nGK-sL6-UG8F5mxr6AV2?usp=sharing](https://drive.google.com/drive/folders/1KVk8y6Z24sh3nGK-sL6-UG8F5mxr6AV2?usp=sharing)
- :octocat: **Repositorio**:
  [https://github.com/juandavid612/IA2_GNNProstate](https://github.com/juandavid612/IA2_GNNProstate)

## 📊 Dataset

### 📂 Descripción del Dataset

El dataset **PICAI_Consolidado** contiene información de **1067 pacientes**, cada uno con secuencias de resonancia magnética: **T2W**, **ADC** y **DWI**.

- 🧠 Se identifican un total de **1083 lesiones** (ya que un paciente puede presentar múltiples).
- 📍 Cada lesión cuenta con su respectivo **centroide**.
- 🏷️ Las etiquetas originales del dataset son: `0`, `2`, `3`, `4` y `5`.
  - `0` ➜ No hay cáncer.
  - `2` a `5` ➜ Niveles crecientes de malignidad.
- 🔄 Para este proyecto, se transformó en una **clasificación binaria**:
  - `0` ➜ No hay cáncer
  - `1` ➜ Presencia de cáncer

### ➡️ Acceso al Dataset

Dentro de la carpeta de Google Drive se encuentra los notebooks y el dataset:

**📁 Link a la carpeta de Google Drive:**  
[https://drive.google.com/drive/folders/1KVk8y6Z24sh3nGK-sL6-UG8F5mxr6AV2?usp=sharing](https://drive.google.com/drive/folders/1KVk8y6Z24sh3nGK-sL6-UG8F5mxr6AV2?usp=sharing)

> ⚠️ **Importante:** Dentro de la carpeta de Google Drive, acceder al subdirectorio llamado **`Dataset`** para encontrar los archivos necesarios.

> 💡 **Recomendación:**  
> Para ejecutar los notebooks en Google Colab, se recomienda crear un **acceso directo** al subdirectorio `Dataset` dentro de su propio Google Drive. Posteriormente, modifique las rutas de acceso a los archivos en los notebooks, justo debajo del texto en color **magenta**, para que apunten correctamente a dicho acceso directo.

---

## 📓 Descripción de los Notebooks

- **`IA2_Generación_del_Grafo.ipynb`**  
  Visualiza la ubicación espacial de los nodos según el ID de la lesión correspondiente.

- **`IA2_Grafos_PICAI_(5kfold).ipynb`**  
  A partir del dataset de imágenes, se genera el dataset de grafos.

- **`IA2_GNN_PICAI_(5kfold).ipynb`**  
  Entrenamiento y validación de modelos de GNN utilizando el dataset de grafos con validación cruzada 5-fold.

---

## 📂 Contenido de la Carpeta `Dataset`

- **`IA2_Copia_de_Consolidado_`**  
  Carpeta con las imágenes correspondientes a todas las secuencias de cada paciente.

- **`IA2_8x64x64-CIspheres.json`**  
  Archivo `.json` que contiene información clave de cada lesión, incluyendo etiquetas y coordenadas del centroide.

- **`IA2_DatasetGrafos_PICAI_Consolidado`**  
  Dataset de grafos generado a partir de imágenes procesadas con una red preentrenada ResNet34.

- **`IA2_picai_patches_splits_5kf.json`**  
  Archivo `.json` con los IDs de las lesiones organizados en 5 folds para aplicar validación cruzada 5-fold.

---

