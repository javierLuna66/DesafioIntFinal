# 🚠 SIMTELE-RISK — Plataforma de Simulación y Análisis de Riesgos

**Materia:** Métodos Numéricos — Desafío Integrador Final  
**Contexto:** Sistema de transporte por cable urbano (inspirado en Mi Teleférico, La Paz).

> ⚠️ **Aviso Importante:** Este sistema es estrictamente educativo. Utiliza datos sintéticos y parámetros hipotéticos. No tiene conexión con equipos de control reales ni describe fallas verificadas de la empresa.

## 📖 Descripción del Proyecto
SIMTELE-RISK es una aplicación web integrada desarrollada para resolver cuatro casos de estudio de ingeniería utilizando métodos numéricos. El sistema permite simular escenarios **NORMAL**, **ESTRÉS** y **MAL CONDICIONADO**, calculando errores, mostrando tablas de iteración, gráficos interactivos y guardando los resultados en una base de datos relacional en la nube. 

## 🧩 Módulos y Cobertura Matemática
La aplicación cubre las 5 familias de métodos exigidas:
1. **Detención de Emergencia (Módulo 1):** EDO (RK2, RK4), Integración (Trapecio, Simpson, Romberg) y Raíces (Bisección, Newton, Secante) para predecir distancia y tiempo de frenado.
2. **Deterioro Mecánico (Módulo 2):** Raíces para umbral de mantenimiento y Sistemas Lineales (\(A x = b\), \(n \ge 4\)) usando Jacobi, Gauss-Seidel, LU y Gradiente Conjugado.
3. **Oscilaciones por Viento (Módulo 3):** Resolución de sistemas de EDOs masa-resorte y cálculo de energía acumulada mediante integración de \(x(t)^2\).
4. **Reconstrucción de Sensores (Módulo 4):** Interpolación (Lagrange, Newton y Splines Cúbicos) para recuperar señales perdidas y evaluación del Fenómeno de Runge.

## 📊 Teoría de Errores Transversal
En cumplimiento con la consigna, cada módulo integra el análisis de:
- Error absoluto, relativo y porcentual.
- Norma euclidiana del residuo (\(\|r\|_2\)).
- Análisis de mal condicionamiento mediante el número de condición \(\kappa_2(A)\).
- Comparación de estabilidad asintótica y sensibilidad bajo perturbaciones (Escenarios de Estrés y Mal Condicionado).

## 🛠️ Stack Tecnológico
- **Frontend:** React 19 + Vite
- **Estilos:** Vanilla CSS (Dark Mode, Glassmorphism, Gradientes Mesh) + Framer Motion
- **Gráficos:** Chart.js
- **Fórmulas Matemáticas:** MathJax (`mathjax-2025`)
- **Persistencia:** PostgreSQL en la nube (Supabase) con API REST autogenerada.
- **Despliegue:** Netlify

Plataforma interactiva de métodos numéricos aplicada al modelado computacional de sistemas de transporte por cable urbano (inspirada en la infraestructura y topografía de Mi Teleférico, La Paz).
## 🚀 Cómo Ejecutar el Proyecto Localmente
1. Clona el repositorio:
   git clone "https://github.com/javierLuna66/DesafioIntFinal.git"  
   cd frontend  
   
2. Instala las dependencias:
   npm install  
(Nota: Si hay conflictos de dependencias por versiones antiguas de React, usa npm install --legacy-peer-deps).  

3. Configura las variables de entorno:
Crea un archivo .env.local en la carpeta frontend/ y agrega tus credenciales de Supabase:  
  VITE_SUPABASE_URL=https://tu-proyecto.supabase.co  
  VITE_SUPABASE_ANON_KEY=tu_clave_anon_aqui  

4. Ejecuta el servidor de desarrollo:  
  npm run dev  
La aplicación estará disponible en http://localhost:5173.  

## 🗄️ Persistencia y Base de Datos
El sistema cuenta con un modelo relacional (6 tablas: caso_estudio, escenario, simulacion, ejecucion_metodo, iteracion_resultado, resultado_resumen) alojado en Supabase.  
Prueba de recuperación: Al guardar una simulación, es posible cerrar sesión, reiniciar el navegador y recuperar los parámetros exactos, los resultados y el historial desde la pestaña "Historial" de la plataforma.

## 🔗 Enlaces de Interés
- Aplicación Desplegada: https://metodosnumericosproyecto.netlify.app/
- Repositorio GitHub: https://github.com/javierLuna66/DesafioIntFinal.git

## 👥 Autores
- Luna Rojas Javier
- Quispe Espinal Cristian Alexander
