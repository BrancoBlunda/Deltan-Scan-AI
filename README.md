# 🦷 DentalScan AI - Sistema de Análisis Dental

![Resultado del análisis](https://brancoblunda.github.io/assets/proyectos/deltan-scan/03-resultados.webp)

| Inicio | Historial |
|---|---|
| ![Inicio](https://brancoblunda.github.io/assets/proyectos/deltan-scan/01-inicio.webp) | ![Historial](https://brancoblunda.github.io/assets/proyectos/deltan-scan/04-historial.webp) |

## Guía de Ejecución

Sistema de análisis de radiografías dentales panorámicas con detección automática de dientes, calibración de medidas y marcado de reparos anatómicos.

---

## Requisitos del Sistema

- **Python**: Versión 3.9 o superior
- **Sistema Operativo**: Windows 10/11, macOS o Linux
- **Memoria RAM**: Mínimo 4 GB (recomendado 8 GB)
- **Navegador web**: Chrome, Firefox, Edge o Safari (actualizado)

---

## Instalación

### Opción 1: Instalación Directa

```bash
# 1. Abrir terminal en la carpeta del proyecto

# 2. Instalar dependencias
pip install -r requirements.txt

# 3. Ejecutar la aplicación
streamlit run app.py
```

### Opción 2: Con Entorno Virtual (Recomendado)

```bash
# 1. Crear entorno virtual
python -m venv venv

# 2. Activar entorno virtual
# En Windows:
venv\Scripts\activate
# En macOS/Linux:
source venv/bin/activate

# 3. Instalar dependencias
pip install -r requirements.txt

# 4. Ejecutar la aplicación
streamlit run app.py
```

---

## Ejecución

Una vez instaladas las dependencias, ejecute:

```bash
streamlit run app.py
```

La aplicación se abrirá automáticamente en su navegador en la dirección:
```
http://localhost:8501
```

---

## Funcionalidades Principales

| Función | Descripción |
|---------|-------------|
| **Carga de Imágenes** | Soporta JPG, PNG y PDF |
| **Detección Automática** | Detección de dientes con IA (YOLO) |
| **Plantilla de 28 Dientes** | Genera dentadura permanente completa |
| **Edición Interactiva** | Mover, redimensionar, rotar y eliminar rectángulos |
| **Reparos Anatómicos** | Marcar Conducto Mentoniano y Seno Maxilar |
| **Calibración** | Convertir píxeles a milímetros |
| **Filtros de Imagen** | CLAHE, detección de bordes, mapa de densidad |
| **Exportación** | Descargar resultados en CSV |

---

## Estructura del Proyecto

```
DentalScan_AI/
├── app.py              # Aplicación principal (interfaz Streamlit)
├── analysis.py         # Lógica de detección y medición
├── utils.py            # Utilidades de procesamiento de imagen
├── requirements.txt    # Dependencias del proyecto
├── README.md           # Este archivo
└── yolov8n.pt          # Modelo YOLO (se descarga automáticamente)
```

---

## Solución de Problemas

### Error: "No module named 'streamlit'"
```bash
pip install streamlit
```

### Error: "No module named 'cv2'"
```bash
pip install opencv-python
```

### El canvas no muestra la imagen de fondo
Asegúrese de tener instalada la versión correcta de streamlit-drawable-canvas:
```bash
pip install streamlit-drawable-canvas --upgrade
```

### La aplicación no abre en el navegador
Abra manualmente: `http://localhost:8501`

---

## Notas Importantes

- **Primera ejecución**: El modelo YOLO (`yolov8n.pt`) se descargará automáticamente la primera vez que use la detección con IA.
- **Rendimiento**: Para mejores resultados, use imágenes de radiografías panorámicas de buena calidad.
- **Calibración**: Para obtener medidas precisas en milímetros, calibre el sistema usando un diente de referencia con medida conocida.

---

## Contacto y Soporte

Este software es un **prototipo MVP** entregado como código fuente.

Desarrollado por Branco Blunda · brancoadrianblunda@gmail.com · https://linkedin.com/in/brancoblunda

Caso completo con capturas en https://brancoblunda.github.io/proyectos/deltan-scan.html

---

*Desarrollado con Streamlit, OpenCV y YOLOv8*
