# TP_AA1_Ibarbia_Colombo_Ayala

Repositorio para los Trabajos Prácticos obligatorios de la materia Aprendizaje Automático I (FIUBA - 2026 C2).

## Estructura del repositorio

```
TP_AA1_Ibarbia_Colombo_Ayala/
├── house-prices-tp.csv       # Dataset del TP 1
├── TP_1/
│   └── TP-regresion-AA1.ipynb   # Trabajo Práctico 1: Regresión Lineal
└── TP_2/
    └── TP-clasificacion-AA1.ipynb   # Trabajo Práctico 2: Clasificación
```

## Cómo correr los notebooks

### Requisitos previos

Es necesario tener instalado **Python 3.8+** y los siguientes paquetes:

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Opción A: Ejecutar con VSCode (recomendado)

1. Instalar la extensión **Jupyter** en VSCode (buscar "Jupyter" en el marketplace).
2. Abrir la carpeta del repositorio en VSCode: `File > Open Folder`.
3. Abrir el notebook `TP_1/TP-regresion-AA1.ipynb`.
4. Seleccionar un intérprete/kernel de Python 3.8 o superior.
5. Si VSCode solicita paquetes, instalarlos en ese mismo intérprete con el comando de requisitos previo.
6. Hacer click en **"Run All"** (botón de doble flecha arriba) para ejecutar todas las celdas.

> **Nota:** El notebook busca automáticamente `house-prices-tp.csv` en el directorio actual,
> en la raíz del repositorio y en la carpeta superior. El dataset ya está incluido en la raíz,
> por lo que no requiere conexión a internet.

### Opción B: Ejecutar con Jupyter Notebook en terminal

```bash
# Desde la raíz del repositorio
jupyter notebook TP_1/TP-regresion-AA1.ipynb
```

### Opción C: Ejecutar desde terminal (sin interfaz gráfica)

```bash
# Instalar nbconvert para ejecutar notebooks desde terminal
pip install nbconvert

# Ejecutar el notebook TP1 y generar una copia con resultados
jupyter nbconvert --to notebook --execute TP_1/TP-regresion-AA1.ipynb --output TP_1/TP-regresion-AA1-ejecutado.ipynb
```

### Datos

El dataset `house-prices-tp.csv` está disponible en la raíz del repositorio. La carga local es la opción
principal para que el trabajo sea reproducible; la URL de GitHub queda únicamente como respaldo si se
ejecuta el notebook fuera del repositorio.

### Entrega

- La dirección del repositorio debe indicarse en la actividad *Entrega* del campus virtual.
- Las entregas hasta 2 días posteriores a la fecha tienen disminución de nota.
- Vencido ese plazo, la instancia se cierra automáticamente.

## Consideraciones importantes

- El código está comentado línea por línea para su comprensión.
- Los comentarios justifican las decisiones metodológicas adoptadas.
- La calificación es individual y surge del trabajo entregado junto con la defensa oral.
- Los turnos de defensa se asignan según el orden de entrega.
