De estructura plana a paquetes Python profesionales

🎯 OBJETIVO

💡 Crear una app modular, escalable y profesional, con:

📂 Un paquete principal news_analyzer
⚙️ Un main.py que se ejecute fácil (python main.py)
🧩 Paquetes separados para la lógica y los ejemplos
🪶 Imports ordenados (PEP 8)
🤖 Refactor asistido por Pylance
🏗️ ESTRUCTURA FINAL DEL PROYECTO

.

├── main.py

├── examples/

│   ├── __init__.py

│   ├── ejemplo_1.py

│   └── ejemplo_2.py

└── news_analyzer/

    ├── __init__.py

    ├── api_client.py

    ├── config.py

    ├── exceptions.py

    └── utils.py

📦 Cada carpeta con __init__.py se convierte en un paquete.

🪜 PASOS CLAVE DEL REFACTOR

1️⃣ Crea los paquetes

 ➤ examples/ y news_analyzer/, ambos con __init__.py.

2️⃣ Mueve los módulos

 ➤ api_client, config, exceptions, utils dentro de news_analyzer/.

3️⃣ Deja main.py en el root

 ➤ Facilita la ejecución y mantiene imports simples.

4️⃣ Separa los ejemplos

 ➤ examples/ sirve solo para pruebas, no para lógica de la app.

5️⃣ Revisa los imports

🔹 Dentro del paquete → importación relativa: from .config import API_KEY
🔸 Fuera del paquete → importación absoluta: from news_analyzer import api_client
6️⃣ Ordena imports (PEP 8)

🧱 Estándar
🌍 Terceros
📦 Locales (deja una línea en blanco entre grupos)
7️⃣ Prueba la ejecución

💻 python main.py → sin errores, con artículos mostrados.

🗝️ ¿POR QUÉ main.py EN EL ROOT?

✅ Ejecución directa desde terminal

✅ Evita rutas confusas de imports

✅ Define una entrada clara a la app

⚙️ CÓMO AYUDA PYLANCE

🤖 Te asiste en el refactor:

Actualiza rutas de import automáticamente.
Detecta módulos rotos tras mover archivos.
Reduce errores humanos al renombrar o reubicar código.
💡 Haz los movimientos desde el editor para que Pylance mantenga consistencia.

📦 QUÉ ES UN PAQUETE EN PYTHON

📁 Un paquete es una carpeta con __init__.py, que se ejecuta al importar.

Permite inicializar configuraciones o exponer APIs internas.

Ejemplo mínimo:

# news_analyzer/__init__.py

# Inicialización del paquete principal

🪆 Si hay subcarpetas (paquetes anidados), cada una también necesita su __init__.py.

🔄 IMPORTACIÓN RELATIVA Y ABSOLUTA

Dentro del paquete

# news_analyzer/api_client.py

from .config import API_KEY, BASE_URL

from .exceptions import AppError

Desde fuera del paquete

# main.py

from news_analyzer import api_client, exceptions

⚠️ Si aparece “módulo no encontrado”, revisa si el import debe ser relativo (.) o absoluto.