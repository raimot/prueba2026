---
name: commiter
description: commit changes to the repository in a structured way
---

# Instrucciones para el Commit

Eres responsable de analizar los cambios en el código y crear un mensaje de commit que siga estrictamente la especificación de **Conventional Commits**, pero añadiendo siempre un emoji al inicio.

## Reglas Obligatorias:

1. **Título (Subject Line)**:
   - **Emoji y Tipo**: Debes colocar un emoji al inicio que represente el tipo de commit. Guíate por la siguiente convención:
     - ✨ `feat`: Nueva funcionalidad
     - 🐛 `fix`: Corrección de errores
     - 📚 `docs`: Actualizaciones de documentación
     - 💎 `style`: Formateo de código, corrección de estilos visuales
     - ♻️  `refactor`: Refactorización de código sin añadir funcionalidades ni corregir errores
     - 🚀 `perf`: Mejoras de rendimiento
     - 🚨 `test`: Añadir o corregir tests
     - 🛠  `build`: Cambios de dependencias o del sistema de constucción
     - ⚙️  `ci`: Cambios en la integración continua
     - 🧹 `chore`: Mantenimiento general, limpieza de código
     - ⏪ `revert`: Reversión de cambios anteriores
   - **Alcance (Opcional)**: En minúsculas y entre paréntesis inmediatamente después del tipo (ej. `✨ feat(parser): ...`).
   - **Límite de Longitud**: El título completo (incluyendo el emoji, el tipo, el alcance y la descripción de una línea) **NO DEBE superar los 50 caracteres**.
   - **Formato**: Usa el modo imperativo para el mensaje ("add" en lugar de "added" o "adds"). No uses mayúscula inicial ni punto al final.

2. **Cuerpo del Mensaje de Commit (Descripción Extensa)**:
   - Deja siempre **una línea en blanco** entre el título y el cuerpo del mensaje.
   - Debes proporcionar una **descripción extensa y detallada** explicando el contexto de los cambios, el motivo (el "por qué" y "para qué") y no solo la traducción del código.
   - Justifica las decisiones de diseño si las hubiera.
   - Trata de que las líneas no superen los 72 caracteres de ancho.

3. **Pie del Mensaje (Footer) (Opcional)**:
   - Referencia problemas vinculados (ej. `Fixes #123`) o cambios que rompen la compatibilidad (`BREAKING CHANGE: ...`).

## Ejemplos de Salida Esperada:

### Ejemplo 1: Nueva funcionalidad
```text
✨ feat(api): add validation to payload

Se implementa una nueva validación en el middleware
de la API para asegurar que todos los campos 
obligatorios estén presentes antes de procesar la 
solicitud. Esto evitará las caídas registradas 
en base de datos debidas a datos incompletos.
```

### Ejemplo 2: Corrección de error
```text
🐛 fix(ui): center login button on mobile

Anteriormente, el botón de inicio de sesión se 
desplazaba a la izquierda en pantallas menores 
a 400px debido a un margen mal calculado por 
flexbox. Se corrige aplicando márgenes auto para 
mantener la consistencia visual.
```