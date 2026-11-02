# 🏫 Sistema Escolar - Introducción a JSON

Implementación de un laboratorio interactivo para comprender la serialización y deserialización de datos usando el formato JSON en JavaScript.

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![JSON](https://img.shields.io/badge/Format-JSON-orange)
![Status](https://img.shields.io/badge/status-completado-success)

---

## 📌 Descripción

En esta actividad se agregó un **Laboratorio JSON** al proyecto. El objetivo es comprender cómo viajan los datos entre el frontend y el backend (o el almacenamiento local), convirtiendo Objetos de JavaScript en cadenas de texto (JSON) y viceversa.

Todo ocurre en el navegador; el servidor en C++ solo se encarga de entregar el archivo HTML.

---

## ✨ Características

- 🔄 **Serialización:** Uso de `JSON.stringify()` para convertir objetos JS a texto.
- 📥 **Deserialización:** Uso de `JSON.parse()` para reconstruir objetos JS desde texto.
- 🕵️ **Visualización clara:** Muestra en pantalla el objeto original, el JSON string y el objeto parseado.
- 💾 **Persistencia local:** Guarda el JSON en `localStorage`.
- 🧩 **Mini-reto incluido:** Demostración de serialización con un arreglo (array) de 3 alumnos.

---

## 🛠️ Tecnologías

| Tecnología | Uso |
|------------|-----|
| HTML5 | Estructura de la página del laboratorio |
| CSS3 | Estilos visuales para las cajas de código |
| JavaScript (ES6+) | Lógica de conversión y manejo del DOM |

---

## 🧠 Conceptos aplicados

### Objeto JavaScript vs. JSON

| Aspecto | Objeto JS | JSON (String) |
|---------|-----------|---------------|
| **Naturaleza** | Estructura en memoria | Texto plano |
| **Claves** | Sin comillas (ej. `nombre`) | Con comillas dobles (ej. `"nombre"`) |
| **Funciones** | Permitidas | ❌ Prohibidas |
| **Comentarios** | Permitidos | ❌ Prohibidos |
| **`undefined`** | Permitido | ❌ Prohibido |
| **Fechas** | Objeto `Date` | String en formato ISO |

### Funciones Clave
- **`JSON.stringify(objeto)`**: Convierte a texto. *Pierde las funciones, los `undefined` y la identidad del objeto.*
- **`JSON.parse(texto)`**: Convierte de texto a objeto. *Devuelve un objeto plano (no instancias de clases).*
- **`localStorage`**: Solo guarda strings, por lo que siempre requiere usar `stringify` y `parse`.

---

## 🚀 Cómo probarlo

1. Asegúrate de tener tu servidor C++ corriendo:
   ```bash
   ./servidor
   ```
2. Abre tu navegador y visita:
   ```text
   http://localhost:8080/json-lab.html
   ```
3. Haz clic en el botón **"Ejecutar Pruebas"**.
4. Verás en pantalla las tres cajas de texto con el objeto original, el JSON y el objeto parseado.
5. Abre las herramientas de desarrollador (**F12** → Consola) para ver los logs de comparación y el resultado del mini-reto (el arreglo de 3 alumnos).

---

## 📁 Estructura del proyecto

```text
Sistema-Escolar/
├── servidor.cpp       <-- Servidor web en C++
├── README.md
└── Public/
    ├── index.html
    ├── registro.html
    ├── json-lab.html  <-- NUEVO: Laboratorio de la Actividad 25
    ├── styless.css
    ├── app.js
    └── img/
```

---

## 📄 Licencia

MIT License
