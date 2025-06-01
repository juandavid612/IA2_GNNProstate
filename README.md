# <font color='magenta'>IA2_GNNProstate</font>

# Acceso al Dataset y Descripción de Notebooks

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
