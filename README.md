# 🏛️ Proyecto: Museo Casa Azul Interactivo

Este proyecto es una simulación interactiva en 3D del **Museo Casa Azul de Frida Kahlo**, desarrollada en C++ y OpenGL. La aplicación permite a los usuarios explorar una recreación del museo y sus jardines, visualizar obras de arte y experimentar animaciones dinámicas.

---

## ✨ Características Principales

* **Exploración 3D:** Recorrido libre por la escena utilizando una cámara en primera persona.
* **Renderizado de Modelos:** Carga y renderiza modelos 3D complejos en formato `.obj` (estáticos) y `.dae` (animados).
* **Sistema de Animación por Keyframes:**
    * Una animación principal compleja para un **caballete** que se desensambla, muestra la pintura en rotación y se vuelve a ensamblar.
    * Animaciones secundarias cíclicas para una **silla mecedora** y un **pincel** que simula pintar sobre un lienzo.
* **Entorno Dinámico:**
    * Un **enjambre de mariposas** que vuela por el jardín con movimiento aleatorio y fluido.
    * Un **foco de luz (spotlight)** animado con una intensidad que simula un pulso.
* **Iluminación Avanzada:** Implementación de luz direccional (sol) y luces de foco (lámparas) que afectan a los objetos.
* **Skybox Cúbico:** Un entorno de 360° que utiliza un mapa cúbico de Coyoacán para simular el cielo y los alrededores.
* **Audio de Fondo:** Reproducción de música en bucle (`la_bruja_son_jarocho.mp3`) utilizando la biblioteca `miniaudio`.
* **Vistas Rápidas (Marcadores):** Teclas predefinidas para teletransportar la cámara a puntos de interés clave del museo.

---

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** C++
* **API Gráfica:** OpenGL (cargado con GLAD)
* **Gestión de Ventana y Entradas:** GLFW
* **Matemáticas para Gráficos:** GLM
* **Carga de Modelos:** Assimp (implícito por las clases `model.h` y `modelAnim.h` para cargar `.obj` y `.dae`)
* **Carga de Texturas:** `stb_image`
* **Reproducción de Audio:** `miniaudio`
* **Control de Tiempo (Framerate):** SDL3 (para `SDL_GetTicks`)

---

## 🚀 Instalación y Compilación

Para compilar este proyecto, necesitarás un compilador de C++ (como el de Visual Studio, g++, o Clang) y las siguientes bibliotecas:

1.  **GLAD** (Generado desde el [servicio web](https://glad.dav1d.de/))
2.  **GLFW**
3.  **GLM**
4.  **Assimp** (para carga de modelos)
5.  **SDL3** (o reemplazar `SDL_GetTicks` por una alternativa)
6.  Las cabeceras `stb_image.h` y `miniaudio.h`

Se recomienda configurar el proyecto usando un sistema de compilación como **CMake** o configurar manualmente las rutas de inclusión (`Include`) y enlace (`Linker`) en tu IDE (ej. Visual Studio).

Asegúrate de que las bibliotecas (`.lib` o `.a`) estén enlazadas correctamente y que los archivos DLL (en Windows) estén en el directorio de ejecución.

---

## 🎮 Controles

### Movimiento de la Cámara

| Tecla | Acción |
| :--- | :--- |
| **W, A, S, D** | Mover la cámara (Adelante, Izquierda, Atrás, Derecha) |
| **Ratón** | Girar la vista de la cámara |
| **Rueda del Ratón** | Hacer zoom (acercar/alejar) |

### Activación de Animaciones

| Tecla | Acción |
| :--- | :--- |
| **Z** | Iniciar / Detener la animación principal del **caballete** |
| **E** | Iniciar / Detener la animación de la **silla mecedora** |
| **Q** | Iniciar / Detener la animación del **pincel** y el cambio de lienzo |

### Vistas Rápidas (Marcadores)

| Tecla | Ubicación de la Vista |
| :--- | :--- |
| **F** | Vista general inicial (lejana) |
| **I** | Vista de la entrada |
| **1** | Sala 1 (Silla mecedora) |
| **2** | Sala 2 (Caballete animado) |
| **3** | Sala 3 (Lámpara y foco) |
| **4** | Sala 4 (Pincel y lienzo) |
| **5** | Vista cenital de las mariposas |
| **B** | Vista de la banca con personajes |
| **J** | Vista general del jardín |
| **V** | Vista de una vitrina |
| **P** | Vista de la pintura "Frida y Diego" |

### Otros

| Tecla | Acción |
| :--- | :--- |
| **ESC** | Cerrar la aplicación |

