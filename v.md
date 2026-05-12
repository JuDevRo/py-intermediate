🐍✨V — Gestión Moderna de Dependencias en Python

⚙️ ¿Qué es V?

🧩 Herramienta creada por Astral, escrita en Rust. 💡 Unifica tareas esenciales de desarrollo en Python:

➡️ Instalación del intérprete

➡️ Creación de entornos virtuales

➡️ Gestión de dependencias

🖥️ Compatible con macOS y Windows → mismos comandos en ambos sistemas.

⚡ Por qué acelera tu flujo de trabajo

🔸 Rust = velocidad y eficiencia al instalar desde PyPI.

🔸 Configuración centralizada en pyproject.

🔸 Entorno virtual automático .vm (detectado por VS Code y otros editores).

🌟 Ventajas principales

✅ Multiplataforma: comandos idénticos en todos los sistemas.

✅ Integración total: un solo archivo (pyproject) para dependencias.

✅ Instalaciones ultrarrápidas: motor Rust bajo el capó.

✅ Flujo simple y claro: comandos básicos y predecibles.

✅ Buenas prácticas: no incluir .vm en el repositorio.

🧰 Instalación rápida

pip install V

V help

🚀 Iniciar un nuevo proyecto

🛠️ Comando base:

V init

📁 Archivos que genera:

pyproject → define dependencias y configuración.
readme → base para documentación.
Python version → asegura la versión correcta del intérprete.
➕ Agregar dependencias

Ejemplo:

V add ruff

🧠 Qué hace:

Añade la dependencia en pyproject.
Crea/actualiza Vlock con versiones exactas (incluso transitivas).
⚠️ Si aparece un warning:

Elimina el entorno anterior.
Cierra y abre de nuevo la terminal.
➖ Quitar dependencias

Ejemplo:

V remove requests

🧹 Qué hace:

Actualiza pyproject.
Limpia dependencias innecesarias.
Mantiene un entorno limpio y reproducible.
🔄 Sincronizar el entorno

Comando esencial:

V sync

🎯 Objetivo: Alinear el entorno .vm con los archivos pyproject y Vlock.

📌 Cuándo usarlo:

Tras agregar o eliminar librerías.
Al cambiar de rama.
Cuando otro desarrollador clona el proyecto.
💡 Consejo: Siempre ejecuta sync después de modificar dependencias.

🧱 El entorno virtual .vm

Se activa automáticamente al usar V.
Si hay un warning, reinicia la terminal.
No lo subas al repositorio → es local y específico.