# 🚠 SIMTELE-RISK: Sistema de Simulación y Gestión de Riesgos

**Materia:** Métodos Numéricos — Desafío Integrador Final  
**Contexto:** Sistema de transporte por cable urbano (inspirado en Mi Teleférico, La Paz).

> ⚠️ **Aviso Importante:** Este sistema es estrictamente educativo. Utiliza datos sintéticos y parámetros hipotéticos. No tiene conexión con equipos de control reales ni describe fallas verificadas de la empresa.

## 📖 Descripción del Proyecto
SIMTELE-RISK es una aplicación web integrada que resuelve cuatro casos de estudio de ingeniería utilizando métodos numéricos. Cada módulo permite simular escenarios **NORMAL**, **ESTRÉS** y **MAL CONDICIONADO**, calculando errores, mostrando tablas de iteración, gráficos interactivos y guardando los resultados en una base de datos en la nube.

## 🧩 Módulos Implementados
1. **Detención de Emergencia:** EDO (RK2, RK4), Integración (Trapecio, Simpson, Romberg) y Raíces (Bisección, Newton, Secante).
2. **Deterioro Mecánico:** Raíces para umbral de mantenimiento y Sistemas Lineales (Jacobi, Gauss-Seidel, LU, Gradiente Conjugado).
3. **Oscilaciones por Viento:** Resolución de EDOs para sistemas masa-resorte y cálculo de energía acumulada.
4. **Reconstrucción de Sensores:** Interpolación (Lagrange, Newton, Splines Cúbicos) para recuperar señales perdidas y evaluar el Fenómeno de Runge.

## 🛠️ Stack Tecnológico
- **Frontend:** React 19 + Vite
- **Estilos:** Vanilla CSS (Dark Mode, Glassmorphism, Gradientes Mesh) + Framer Motion (Animaciones)
- **Gráficos:** Chart.js (react-chartjs-2)
- **Fórmulas Matemáticas:** MathJax (mathjax-2025)
- **Persistencia:** Supabase (PostgreSQL)
- **Despliegue:** Vercel

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

## 🔗 Enlaces de Interés
- Aplicación Desplegada: https://proyectometodosnumericosi.vercel.app/
- Repositorio GitHub: https://github.com/javierLuna66/DesafioIntFinal.git

## 👥 Autores
- Luna Rojas Javier
- Quispe Espinal Cristian Alexander
