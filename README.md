# Análisis de Acciones y Automatización de Envío de Correo en Python

## Descripción

Este proyecto fue desarrollado como práctica académica para integrar análisis de datos financieros, visualización gráfica y automatización de tareas en Python.

Se realiza un análisis de la acción de Apple (AAPL) durante los últimos 6 meses y se automatiza el envío de un correo electrónico con los resultados obtenidos.

---

## Tecnologías utilizadas

- Python 3.11
- yfinance
- matplotlib
- pyautogui
- pyperclip
- python-dotenv
- Git & GitHub

---

## Análisis de Datos

Se obtienen los datos históricos de los últimos 6 meses utilizando `yfinance`:

```python
import yfinance

data = yfinance.Ticker("AAPL").history("6mo")
cierre = data.Close
cierre.plot()
```

A partir de estos datos se calculan:

- Cotización máxima  
- Cotización mínima  
- Valor promedio  

Se genera una gráfica del comportamiento de cierre de la acción.

---

## Automatización del Correo

El proyecto automatiza el proceso de envío de correo mediante:

- Apertura automática del navegador  
- Inserción del destinatario  
- Redacción del asunto  
- Pegado del cuerpo del mensaje con los resultados calculados  
- Envío del correo  

Librerías utilizadas:

```python
pyautogui
pyperclip
webbrowser
```

---

## Seguridad y Buenas Prácticas

La información sensible como URLs o destinatarios se maneja mediante variables de entorno y no se incluye en el repositorio.

Recomendaciones:

- Crear un archivo `.env`
- Agregarlo al archivo `.gitignore`
- No subir datos personales al repositorio público

---

## Cómo ejecutar el proyecto

### 1. Clonar el repositorio

```bash
git clone URL_DEL_REPOSITORIO
```

### 2. Instalar dependencias

```bash
pip install yfinance matplotlib pyautogui pyperclip python-dotenv
```

### 3. Configurar variables de entorno

Crear un archivo `.env` con las variables necesarias.

### 4. Ejecutar el proyecto

Ejecutar el notebook o script principal.

---

## Objetivo Académico

Este proyecto tiene como propósito practicar:

- Consumo de datos financieros  
- Visualización con Python  
- Automatización de tareas repetitivas  
- Gestión segura de información  
- Control de versiones con Git  

---

## Autora

**Estefany Ramírez**  
Desarrolladora Backend en formación
