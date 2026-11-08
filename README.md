# 🏭 Factory Puzzle: Arquitectos del Código

> Juego educativo interactivo para **profundizar el aprendizaje del patrón Abstract Factory** (patrón creacional del catálogo GoF) y afianzar los fundamentos de la **Programación Orientada a Objetos (POO)** mediante la práctica.

![Estado](https://img.shields.io/badge/estado-completo-brightgreen)
![Tecnología](https://img.shields.io/badge/HTML5-CSS3-JS-blue)
![Licencia](https://img.shields.io/badge/licencia-MIT-yellow)
![Nivel](https://img.shields.io/badge/nivel-principiante%20a%20intermedio-orange)

---

## 🎯 Propósito del proyecto

Este juego nace con una intención **pedagógica**: que quien lo juegue no solo *memorice* la teoría del patrón Abstract Factory, sino que **la interiorice resolviendo problemas reales** de diseño de software.

El aprendizaje se profundiza porque cada nivel obliga a **tomar decisiones arquitectónicas**, no a responder un cuestionario. El jugador debe:

- **Clasificar** piezas según su rol en el patrón.
- **Distinguir** entre interfaces abstractas e implementaciones concretas.
- **Armar familias de productos compatibles** sin mezclarlas.
- **Elegir** la fábrica concreta adecuada según el contexto.
- **Conectar** en un diagrama de clases las dependencias correctas.
- **Ordenar** el código Python de una implementación real.
- **Detectar bugs arquitectónicos** que violan el patrón.
- **Construir** un sistema completo desde cero.

Cada acción del jugador recibe **retroalimentación inmediata y explicada**, de modo que el error se convierte en una oportunidad de aprendizaje y no en un callejón sin salida.

---

## 📚 ¿Qué es el patrón Abstract Factory?

> *"Proporciona una interfaz para crear familias de objetos relacionados o dependientes sin especificar sus clases concretas."*
> — Gamma, Helm, Johnson y Vlissides, *Design Patterns* (1994)

### Problema que resuelve

Sin este patrón, el código crea objetos concretos por todas partes:

```python
# ❌ Código acoplado: cambia según el sistema operativo
if sistema == "windows":
    boton = WinButton()
    ventana = WinWindow()
else:
    boton = MacButton()
    ventana = MacWindow()
