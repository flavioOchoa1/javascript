# Iconos SVG: Uso y Consideraciones

## ¿Cómo usar los iconos SVG?

Puedes usar tus iconos SVG de dos formas principales:

### 1. SVG incrustado en HTML

Permite cambiar el color y aplicar animaciones o efectos con CSS y JavaScript.

```html
<div class="icon-container icon-hover">
    <svg class="icon-x" viewBox="4 4 24 24" fill="none">
        <line class="x-line" x1="8" y1="8" x2="24" y2="24"/>
        <line class="x-line" x1="24" y1="8" x2="8" y2="24"/>
    </svg>
</div>
```

**Ventajas:**  
- Puedes cambiar el color de la X con CSS, por ejemplo al pasar el mouse (`:hover`).
- Permite animaciones y manipulación con JavaScript.

### 2. SVG como archivo externo (`<img src="...">`)

```html
<div class="icon-container icon-hover">
    <img src="icons/x.svg" alt="Icono X" class="icon-x" width="32" height="32">
</div>
```

**Limitaciones:**  
- No puedes cambiar el color del contenido del SVG con CSS externo ni con `:hover`.
- Solo puedes cambiar el tamaño con `width` y `height`.

---

## Resumen

- **¿Quieres cambiar el color o animar el icono?**  
  Usa el SVG incrustado en el HTML.
- **¿Solo necesitas mostrar el icono y cambiar su tamaño?**  
  Usa el SVG como archivo externo con `<img>`.

Esto es una limitación de cómo los navegadores manejan los SVG externos:  
El contenido de un SVG cargado con `<img>` es independiente del DOM y no puede ser manipulado con CSS externo.

---