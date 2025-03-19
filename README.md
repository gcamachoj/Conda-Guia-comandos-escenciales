# 📘 Guía Completa de Comandos Conda

## 📌 Introducción
**Conda** es un gestor de paquetes y entornos que facilita la administración de bibliotecas en **Python** y otras tecnologías. Es ampliamente utilizado en **Data Science**, **Machine Learning** y **desarrollo de software**.

Esta guía cubre los comandos esenciales para gestionar entornos, instalar paquetes y mantener un sistema organizado.

---

## 🔹 1. Instalación de Conda
Antes de empezar, asegúrate de tener **Anaconda** o **Miniconda** instalado:

- **Descargar Anaconda:** [https://www.anaconda.com/download](https://www.anaconda.com/download)
- **Descargar Miniconda:** [https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html)

Verifica la instalación con:
```bash
conda --version
```
---

## 🔹 2. Gestionar Entornos
Primero para activar el prompt de conda debes buscarlo en inicio como  "Anaconda Prompt" para SO Windows.
### 📂 2.1 Ver entornos disponibles
```bash
conda info --envs
```
El entorno activo está marcado con un **asterisco** `*`.

### 🏗 2.2 Crear un nuevo entorno
```bash
conda create --name <mi_entorno> python=<versión>
```
Ejemplo:
```bash
conda create --name entorno_ds python=3.9
```

### ✅ 2.3 Activar un entorno
```bash
conda activate <mi_entorno>
```
Ejemplo:
```bash
conda activate entorno_ds
```

### ❌ 2.4 Desactivar un entorno
```bash
conda deactivate
```

### 🗑 2.5 Eliminar un entorno
Antes de eliminar un entorno, asegúrate de no estar dentro de él (`conda deactivate`). Luego, ejecuta:
```bash
conda env remove --name <mi_entorno>
```
Ejemplo:
```bash
conda env remove --name entorno_ds
```
Verifica con:
```bash
conda info --envs
```

---

## 🔹 3. Gestionar Paquetes

### 📦 3.1 Instalar paquetes
**Usando Conda:**
```bash
conda install <nombre_paquete>
```
Ejemplo:
```bash
conda install numpy pandas
```

**Usando pip (dentro del entorno):**
```bash
pip install <nombre_paquete>
```
Ejemplo:
```bash
pip install matplotlib
```

### 📌 3.2 Ver paquetes instalados
```bash
conda list
```

### 🔄 3.3 Actualizar paquetes
Actualizar **Conda**:
```bash
conda update conda
```
Actualizar **todos los paquetes** en el entorno:
```bash
conda update --all
```

### ❌ 3.4 Eliminar paquetes
```bash
conda remove <nombre_paquete>
```
Ejemplo:
```bash
conda remove scipy
```

---

## 🔹 4. Gestionar Entornos en Power BI
Si deseas usar Conda en **Power BI**, configura la ruta del entorno en:

📍 `Opciones > Opciones Avanzadas > Python scripting`

Ubica la carpeta del entorno y agrégala como interprete de Python en Power BI.

---

## 🔹 5. Exportar e Importar Entornos

### 📥 5.1 Exportar un entorno
Guarda la configuración del entorno en un archivo:
```bash
conda env export > entorno.yml
```

### 📤 5.2 Importar un entorno desde un archivo
```bash
conda env create -f entorno.yml
```

---

## 🎯 Conclusión
Conda es una herramienta esencial para gestionar entornos y paquetes de manera eficiente. Con esta guía, puedes administrar entornos de desarrollo sin conflictos de dependencias.

🚀 **¡Usa esta guía como referencia y optimiza tu flujo de trabajo con Conda!**

