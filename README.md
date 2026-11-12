# AA1-TUIA-Ibarbia-Colombo-Ayala

Repositorio para los Trabajos Prácticos obligatorios de la materia Aprendizaje Automático I (FCEIA - UNR, 2026 C2).

## Estructura del repositorio

```
AA1-TUIA-Ibarbia-Colombo-Ayala/
├── house-prices-tp.csv                        # Dataset del TP 1
├── weatherAUS_2026C2.csv                      # Dataset del TP 2
├── 2026C2 - TrabajoPrácticoClasificacionAA1.pdf   # Enunciado del TP 2
├── TP_1/
│   └── TP-regresion-AA1.ipynb                 # Trabajo Práctico 1: Regresión Lineal
└── TP_2/
    ├── TP-clasificacion-AA1.ipynb             # Trabajo Práctico 2: Clasificación
    └── requirements.txt                       # Entorno para correr el notebook del TP 2
```

## Cómo correr los notebooks

### Requisitos previos

Es necesario tener instalado **Python 3.8+** y los siguientes paquetes:

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Entorno del TP 2

El notebook del TP 2 usa PyCaret 3.3.2, que solo funciona con Python 3.9 a 3.11 y necesita versiones anteriores de pandas, numpy y scikit-learn. Por eso se corre en un entorno aparte, con las versiones fijadas en `TP_2/requirements.txt`. Conviene crear el entorno en una ruta corta y fuera del repositorio: en Windows, las rutas largas hacen fallar la instalación.

```bash
py -3.10 -m venv C:\venvs\tp-aa1
C:\venvs\tp-aa1\Scripts\python.exe -m pip install -r TP_2/requirements.txt
```

Después hay que elegir `C:\venvs\tp-aa1\Scripts\python.exe` como kernel del notebook en VS Code. Se puede usar cualquier otra ruta corta, por ejemplo en el disco D.

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
