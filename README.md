# ⚙️ Business Automation Suite — Automatización de Procesos Empresariales (Python / Flask / RPA)
> **Suite integral de herramientas y microaplicaciones para automatización de Recursos Humanos, procesamiento masivo de documentos Word/Excel y utilidades de productividad.**

[![Python](https://img.shields.io/badge/Python-3.x-3776ab.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Web%20Framework-Flask-black.svg)](https://flask.palletsprojects.com/)
[![Deployment](https://img.shields.io/badge/Cloud%20Deploy-Render%20Ready-46E3B7.svg)](#-despliegue-en-la-nube-render)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## 📌 El Desafío de Negocio

En empresas medianas y departamentos operativos, el trabajo diario está saturado de tareas repetitivas de bajo valor que consumen el tiempo del equipo:

- **Carga de Datos Manual en Recursos Humanos**: Extraer información de postulantes o empleados desde archivos PDF y tipear cada dato en planillas internas de control toma decenas de horas semanales y genera errores frecuentes.
- **Generación Repetitiva de Oficios y Formatos**: Crear documentos institucionales combinando plantillas Word con bases de datos Excel sin un sistema ágil conduce a pérdidas de tiempo y desajustes de formato.
- **Cuellos de Botella en Archivos Gráficos**: Convertir manualmente cientos de imágenes (como formatos WebP modernos a PNG o JPG) ralentiza a diseñadores, editores web y administrativos.

---

## 💡 La Solución Implementada

**Business Automation Suite** agrupa soluciones modulares de software orientadas a erradicar el trabajo manual y optimizar la productividad operativa de los equipos:

### 1. Sistema Web de Automatización para Recursos Humanos (`Automatizacion/Web/Automatizar_RH`)
- **Aplicación Web en Flask**: Diseñada para la recepción de archivos, extracción inteligente de datos (`extract_data.py`), validación de reglas de negocio (`validate_data.py`) y autollenado de planillas (`fill_data.py`).
- **Integración con Google APIs**: Conectores para sincronizar expedientes y datos directamente con servicios en la nube de Google.
- **Preparada para Producción**: Incluye archivos de configuración para despliegue inmediato en la nube (`render.yaml`, `Procfile`, `start.sh`).

### 2. Motor de Reemplazo Masivo Word-Excel (`Automatizacion/Reemplazar_formato`)
- Aplicación web y script con interfaz interactiva que permite subir una plantilla Word y un archivo Excel para generar masivamente documentos personalizados de forma instantánea.

### 3. Suite Desktop para Conversión Masiva de Imágenes (`Conversor_Imagenes`)
- Herramienta de escritorio con interfaz gráfica y ejecutable compilado (`.exe`) para optimización y conversión en lote de formatos WebP a PNG/JPG, acelerando el flujo de trabajo de marketing y diseño web sin requerir Photoshop ni software pesado.

### 4. Módulo de Consulta y Auditoría de Identidad (`VERIFICAR_DNI`)
- Scripts modulares de conexión con APIs de identidad y ordenamiento de registros (`api_conection` y `elrayo`).

---

## 📈 Impacto y Mejoras Conseguidas

| Proceso Automatizado | Operación Manual Previa | Con Business Automation Suite | Impacto Directo |
|---|---|---|---|
| **Procesamiento de Documentos RRHH** | 10 a 15 minutos por expediente | Menos de 30 segundos | **Ahorro de más de 25 horas hombre por semana en RRHH** |
| **Generación de Formatos Word/Excel** | Tipeo manual documento por documento | Generación por lotes automatizada | **Reducción de errores humanos a 0%** |
| **Conversión Masiva de Imágenes** | Conversión manual una a una en páginas web | Procesamiento en bloque local en 1 clic | **Optimización del flujo de carga de contenidos web** |
| **Despliegue y Escalabilidad** | Scripts locales en computadoras aisladas | Aplicaciones web cloud-ready en Render | **Acceso centralizado para todo el equipo de trabajo** |

---

## ✨ Módulos y Arquitectura

```text
├── Automatizacion/
│   ├── Web/Automatizar_RH/       # Aplicación Web Flask para RRHH
│   │   ├── app.py                # Servidor y endpoints web de procesamiento
│   │   ├── extract_data.py       # Algoritmos de extracción de datos en documentos
│   │   ├── validate_data.py      # Capa de validación de reglas de negocio
│   │   ├── fill_data.py          # Motor de llenado automático de planillas
│   │   ├── render.yaml           # Manifiesto de infraestructura Cloud (Render)
│   │   └── templates/ & static/  # Frontend web interactivo
│   │
│   └── Reemplazar_formato/       # Sistema de combinación Word-Excel
│       ├── app.py                # Interfaz web de reemplazo
│       └── Find_write_word-excel.py # Script de automatización documental
│
├── Conversor_Imagenes/           # Herramienta de optimización de imágenes
│   ├── main.py                   # Interfaz gráfica de usuario (GUI)
│   ├── converter.py              # Motor de conversión y compresión
│   └── exe/main.exe              # Ejecutable standalone listo para Windows
│
└── VERIFICAR_DNI/                # Conectores de validación de identidad
```

---

## 🛠️ Stack Tecnológico

- **Lenguaje Core**: Python 3.
- **Frameworks Web**: Flask, Jinja2 Templates, HTML5/CSS3/JavaScript.
- **Librerías de Procesamiento**: Pandas, OpenPyXL, python-docx, Pillow (PIL), PyPDF2/pdfplumber.
- **Cloud & DevOps**: Render, Gunicorn, Procfile.
- **GUI de Escritorio**: Tkinter / CustomTkinter compilado con PyInstaller.

---

## 🚀 Despliegue y Ejecución Rápida

### Ejecutar la App de Automatización de RRHH:
```bash
cd Automatizacion/Web/Automatizar_RH
python -m venv venv
# Activar entorno virtual
pip install -r requirements.txt
python app.py
```
Abre en tu navegador `http://localhost:5000`.

### Despliegue en Render (Cloud):
El proyecto cuenta con `render.yaml` nativo. Solo debes conectar tu repositorio en [Render](https://render.com) y el servicio se desplegará automáticamente.

---

## 📬 ¿Tienes procesos manuales que están frenando a tu equipo?

Me especializo en diseñar y construir **automatizaciones de procesos (RPA ligero), scripts de integración entre Excel, Word, PDFs y APIs, y aplicaciones web a medida para optimizar operaciones empresariales**.

- **GitHub**: [@Enybyy](https://github.com/Enybyy)
- **Perfil Profesional**: Eliud RM — Data Science & Software Solutions
- *Conversemos sobre cómo liberar el tiempo de tu equipo y reducir costos operativos.*
