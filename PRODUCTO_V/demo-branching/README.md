# Demo práctica: GitFlow vs. Trunk-Based Development

**Pregunta 2 — Unidad 5 · Team Pixel & Code**

**Ponente: Génesis Varguillas (V-24.848.424)**

Esta carpeta contiene la evidencia práctica de la comparación entre los modelos
de ramificación GitFlow y Trunk-Based Development, usada como apoyo para la
exposición. El árbol de commits completo puede verse con:

git log --all --graph --oneline --decorate

## 1. Demo GitFlow

Simulación del flujo completo: `develop` → `feature/reporte-mensual` → merge a
`develop` → `release/1.0` → merge a `main` con etiqueta de versión.

- `README.md` — base de la rama `develop`
- `reporte.js` — cambio de la rama `feature/reporte-mensual`
- `VERSION` — archivo de la rama `release/1.0`
- Tag: `v1.0.0`

Resultado: un árbol ramificado, con varias líneas paralelas antes de llegar a `main`.

## 2. Demo Trunk-Based Development

Simulación de tres ciclos de integración corta directo sobre `main`, cada uno
con una rama que vivió solo minutos:

- `boton-exportar.js` — rama `feature/boton-exportar`, protegida por un feature flag
- `validacion.js` — cambio pequeño integrado directo a `main`
- Ajuste en `reporte.js` — rama `feature/ajuste-texto`

Resultado: una línea de historial casi recta, con integraciones frecuentes y
pequeñas, respaldada conceptualmente por un pipeline de CI con 3 Quality Gates
(pruebas, análisis estático, auditoría de dependencias).

## Referencia

Ver la presentación completa (láminas 9 y 10) para las capturas de este
historial y la explicación de cada paso.
