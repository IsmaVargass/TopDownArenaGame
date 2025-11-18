# TopDownArenaGame

¡Bienvenido al repositorio de TopDownArenaGame!  
Este es un juego de acción top-down de ritmo rápido ambientado en una arena, donde la supervivencia y la habilidad son clave.

---

## 🔗 Descarga del Juego

El juego completo **no se incluye** dentro de este repositorio.  
Puedes descargar la última versión ejecutable desde el siguiente enlace de Google Drive:

👉 [Descargar TopDownArenaGame (Google Drive)](https://drive.google.com/drive/folders/129EZn1P5Xh1N2QNFpG2frk5kK_efjzxo?usp=sharing)

---

## 🕹️ Controles

La jugabilidad se centra en un esquema de control sencillo e intuitivo pensado para acción continua:

| Acción        | Control              | Descripción                                      |
|---------------|----------------------|--------------------------------------------------|
| Movimiento    | `W`, `A`, `S`, `D`   | Mueve al personaje en la dirección deseada.      |
| Disparo       | Clic izquierdo       | Dispara el arma principal.                       |
| Dash / Evasión| Shift izquierdo      | Realiza una esquiva rápida para evitar daño.     |
| Pausa         | ESC                  | Abre el menú de pausa.                           |

---

## 🚀 Cómo Ejecutar el Juego (Windows)

1. Descarga el archivo ZIP desde el enlace de Google Drive.  
2. Descomprime el ZIP en la carpeta que prefieras.  
3. Navega a la carpeta del juego:

```
TopDownArenaGame/Game
```

4. Ejecuta el archivo:

```
TopDownArenaGame.exe
```

El juego se iniciará inmediatamente.

---

## ⚙️ Estructura del Proyecto y Decisiones de Desarrollo

El juego se ha desarrollado con un enfoque simple, eficiente y centralizado, utilizando una única escena principal para todo el gameplay.

### 🎮 Jerarquía de la Escena Única (`SCENEBUENA`)

Toda la lógica del juego se concentra en una sola escena llamada SCENEBUENA, lo que:

- Minimiza tiempos de carga.  
- Simplifica la comunicación entre sistemas.  
- Facilita el mantenimiento y la depuración.

La escena está organizada en varios bloques:

### 🧩 Objetos Fundamentales (globales)

- Main Camera, Directional Light, Global Volume — elementos base de renderizado e iluminación.  
- Arena — contenedor del escenario donde ocurre la acción.  
- Player, EnemySpawner — componentes clave del gameplay.

### 🛠️ Sistemas de Juego (managers)

- SystemPause — controla el estado de pausa.  
- UIManagerObject, EventSystem — gestión de interfaz e inputs.  
- GameManager — control central de lógica (puntuación, estados del juego).  
- EnemyShooter — comportamiento de disparo enemigo.  
- music, SimpleVolumeManager — gestión de audio y volúmenes.

### 🖥️ Interfaz de Usuario (Canvas)

El Canvas contiene toda la UI, organizada en paneles que se activan o desactivan según el estado del juego:

- MenuPause, BtnPause  
- BackgroundDash  
- GameOverPanel  
- MenuOpciones, MainMenu  
- DamageOverlayPanel

---

## 🧠 Razón de la Escena Única y Múltiples Scripts

### Centralización con una sola escena
Permite comunicación directa entre managers, jugador y UI sin necesidad de sistemas persistentes ni cargas adicionales.

### Separación de responsabilidades
En lugar de un único "Mega-Script":

- Se utiliza una arquitectura de muchos scripts pequeños.  
- Cada uno tiene una sola responsabilidad.  
- El código es más modular, claro, fácil de depurar y escalable.

Ejemplos: SystemPause, EnemyShooter, SimpleVolumeManager, etc.

---

## 📸 Capturas (añadir imágenes)

```markdown
![Captura 1](screenshots/screenshot1.png)
![Captura 2](screenshots/screenshot2.png)
```

Consejo: sube las capturas al repositorio (no al build) y referencia la ruta `screenshots/` para que se muestren en GitHub.

---

## 🛠️ Tecnologías usadas

- Motor de juego: Unity  
- Lenguaje de programación: C#

---

Gracias por revisar el proyecto. Si tienes sugerencias o encuentras algún error, abre un issue o contacta.
