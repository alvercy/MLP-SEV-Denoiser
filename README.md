# MLP-SEV1D-Denoiser

Este repositorio contiene un flujo de trabajo completo para generar datos sintéticos de sondeo eléctrico vertical (SEV) 1D, contaminarlos con ruido gaussiano y entrenar un perceptrón multicapa (MLP) para eliminar el ruido de las curvas de resistividad aparente.

El flujo de trabajo está organizado en tres notebooks:

1. **`CLEAN_DATASET.ipynb`**: genera modelos sintéticos de tierra estratificada y sus curvas limpias de resistividad aparente tipo Schlumberger.
2. **`CORRUPT_DATASET.ipynb`**: construye un conjunto de datos para desruido agregando ruido gaussiano a diferentes niveles de ruido sobre las curvas limpias.
3. **`DENOISING_TRAINING.ipynb`**: entrena y evalúa un MLP que aprende a mapear curvas ruidosas a curvas limpias.

Los datasets en formato `.npz` se almacenan en una carpeta llamada **`DATASETS/`**.

---

## Estructura del repositorio

```bash
.
├── CLEAN_DATASET.ipynb
├── CORRUPT_DATASET.ipynb
├── DENOISING_TRAINING.ipynb
├── DATASETS/
│   ├── dataset_1d_variable_models_variable_ab2.npz
│   └── dataset_denoising_gaussian.npz
└── README.md
