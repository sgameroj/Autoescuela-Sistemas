# 📚 Autoescuela de Sistemas 3 AVA

Una aplicación web interactiva para evaluar y mejorar conocimientos sobre **hardware, sistemas operativos, redes e infraestructura**. Este proyecto demuestra la aplicación profesional de metodología Memory Bank para el desarrollo guiado por IA.

## 🎯 Objetivo del Proyecto

Crear un **programa de tests online** con preguntas relacionadas con:
- 🪟 Comandos Windows
- 🐧 Comandos Linux  
- 💻 Hardware
- 🌐 Redes IP
- 🐳 Contenedores (Docker)

El foco principal es **demostrar la capacidad de dirigir una IA siguiendo especificaciones técnicas estrictas**, aplicando la metodología profesional **Memory Bank**.

---

## ✨ Características Principales

✅ **25+ preguntas** divididas en 5 categorías  
✅ **Interfaz interactiva** con feedback visual en tiempo real  
✅ **Puntuación por categoría** para análisis detallado  
✅ **Barra de progreso** que muestra el avance del test  
✅ **Sistema de reinicio** para practicar múltiples veces  
✅ **Arquitectura modular** con componentes reutilizables  
✅ **Código limpio y documentado** siguiendo buenas prácticas  

---

## 📁 Estructura del Proyecto

```
Autoescuela-Sistemas/
├── index.html                 # Página principal HTML
├── style.css                  # Estilos de la aplicación
├── app.js                     # Lógica principal y orquestación
├── components.js              # Funciones puras para renderización
├── questions.js               # Base de datos de preguntas
├── memoria-bank/              # Memory Bank del proyecto
│   ├── productContext.md      # Visión del proyecto
│   ├── systemPatterns.md      # Reglas técnicas y arquitectura
│   ├── activeContext.md       # Contexto actual de desarrollo
│   └── progress.md            # Progreso y tareas pendientes
├── mensajes_prompts.txt       # Historial de prompts usados
└── README.md                  # Este archivo
```

---

## 🏗️ Arquitectura

### Patrón Implementado

El proyecto sigue una **arquitectura separada en dos capas**:

#### 📄 **components.js** - Componentes Puros
Funciones que reciben datos y devuelven **HTML strings** sin efectos secundarios:
- `createWelcomeScreen()` - Pantalla de bienvenida
- `createQuestionCard()` - Tarjeta de pregunta
- `createResultsPanel()` - Panel de resultados
- `createProgressBar()` - Barra de progreso

#### ⚙️ **app.js** - Lógica Principal
Maneja la **orquestación, estado y eventos**:
- Estado centralizado en `appState`
- Event delegation para interactividad
- Gestión de flujo del test
- Cálculo de puntuaciones

### Flujo de Datos

```
questions.js → app.js (State) → components.js (Rendering) → index.html
```

---

## 🚀 Cómo Usar

### 1. **Abrir en el navegador**
```bash
# Simplemente abre index.html en tu navegador
open index.html
# O usa un servidor local
python -m http.server 8000
```

### 2. **Tomar el test**
- Haz clic en "Comenzar Test"
- Responde cada pregunta seleccionando una opción
- Verás la respuesta correcta resaltada en verde
- Al finalizar, recibirás tu puntuación y estadísticas por categoría

### 3. **Reiniciar**
- Haz clic en "Reiniciar Test" para comenzar nuevamente
- Las preguntas se mezclarán en un nuevo orden

---

## 📊 Base de Datos de Preguntas

El proyecto contiene **25 preguntas** distribuidas así:

| Categoría | Cantidad | Temas |
|-----------|----------|-------|
| 🪟 Comandos Windows | 5 | ipconfig, netstat, ping, tasklist, format |
| 🐧 Comandos Linux | 5 | ls, chmod, find, pwd, ps |
| 💻 Hardware | 5 | CPU, RAM, ROM, Disco duro, GPU |
| 🌐 Redes IP | 5 | IPv4, DNS, DHCP, Clases IP, Máscaras |
| 🐳 Contenedores | 5 | Docker, docker run, Dockerfile, docker-compose |

---

## 🎓 Metodología Memory Bank

Este proyecto demuestra el uso profesional de **Memory Bank** con los siguientes archivos:

### 📋 **memory-bank/productContext.md**
Define la visión del proyecto: Una autoescuela para aprender sistemas de forma interactiva.

### 🔧 **memory-bank/systemPatterns.md**
Especifica las reglas técnicas:
- Funciones puras en `components.js`
- Lógica centralizada en `app.js`
- Separación clara de responsabilidades

### 🔄 **memory-bank/activeContext.md**
Indica la tarea actual en desarrollo para mantener el contexto con la IA.

### ✅ **memory-bank/progress.md**
Lista lo completado y lo pendiente en el proyecto.

---

## 📝 Historial de Prompts

Todos los prompts utilizados para generar el código están documentados en `mensajes_prompts.txt`:

1. **PROMPT 1**: Creación del Memory Bank
2. **PROMPT 2**: Creación del banco de preguntas
3. **PROMPT 3**: Creación de componentes visuales
4. **PROMPT 4**: Lógica principal y orquestación
5. **PROMPT 5**: Estilos y estructura HTML

---

## 💻 Tecnologías Utilizadas

- **HTML5** - Estructura
- **CSS3** - Estilos y responsive design
- **JavaScript (Vanilla)** - Lógica sin dependencias
- **Sin frameworks** - Código limpio y eficiente

---

## 🎨 Interfaz

### Pantalla de Bienvenida
Presenta el objetivo del test y botón para comenzar.

### Tarjeta de Pregunta
- Categoría de la pregunta
- Enunciado de la pregunta
- 4 opciones de respuesta
- Barra de progreso

### Panel de Resultados
- Puntuación total
- Porcentaje de aciertos
- Estadísticas por categoría
- Botón para reiniciar

---

## 📈 Estadísticas

Al finalizar el test, recibirás:
- **Puntuación global** (X/25)
- **Porcentaje** de aciertos
- **Desglose por categoría** con aciertos/total
- **Mensaje personalizado** según desempeño (≥60% = aprobado)

---

## 🔧 Extensiones Futuras

Posibles mejoras del proyecto:
- [ ] Agregar más preguntas (100+)
- [ ] Sistema de dificultad (Fácil, Medio, Difícil)
- [ ] Guardar progreso en localStorage
- [ ] Exportar resultados en PDF
- [ ] Modo de estudio con explicaciones
- [ ] Sistema de badges/logros
- [ ] Leaderboard local

---

## 📚 Recursos

- [Cline Memory Bank Documentation](https://docs.cline.bot/features/memory-bank)
- [Cline Bot Guide](https://docs.cline.bot/home)

---

## 👥 Autores

Proyecto realizado por: **sgameroj**  
Asignatura: **Sistemas 3 AVA**  
Fecha: **2026**

---

## 📄 Licencia

Este proyecto es de código abierto. Úsalo libremente para aprender y mejorar.

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para cambios importantes:
1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

---

**¡Bienvenido a la Autoescuela de Sistemas! 🚀**
