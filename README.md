# Comunidad Solidaria — EMAL Nº 2702 (Rawson)

Plataforma social diseñada para conectar la solidaridad de los vecinos de Rawson, Chubut. Este es un proyecto de la **Escuela Municipal de Aprendizaje Laboral (EMAL) Nº 2702**, enfocado en facilitar el intercambio de donaciones y la asistencia comunitaria.

![Portada de Comunidad Solidaria](screenshot_home.png)

## 🔴 El Problema
En nuestra comunidad, muchas familias tienen objetos en buen estado que ya no usan (ropa, muebles, herramientas), mientras que otras familias los necesitan urgentemente. Sin embargo, existe una **barrera de comunicación**:
*   No hay un lugar centralizado para publicar donaciones.
*   Muchas familias no tienen acceso a internet o no saben usar redes sociales para pedir ayuda.
*   Las donaciones a veces se pierden por falta de logística o coordinación.

## 🟢 La Solución
**Comunidad Solidaria** funciona como un puente inteligente. No es solo una página web, es una red humana asistida por tecnología:
1.  **Plataforma de Match**: Un sistema simple donde se registran las ofertas y las necesidades.
2.  **Los Conectores**: Alumnos y docentes de la EMAL actúan como voluntarios. Ellos visitan a los vecinos sin internet, relevan lo que necesitan y lo cargan en el sistema.
3.  **Gestión Transparente**: La escuela coordina el nexo final para asegurar que las cosas lleguen a quien realmente las necesita.

## 📋 Caso de Uso: El camino de una donación
Así es como el sistema transforma una intención en una realidad:

1.  **Tengo una cama ortopédica**: Un vecino decide donar un objeto importante.
2.  **La publico**: Registra los datos y fotos en la WebApp en segundos.
3.  **Una familia la necesita**: El sistema detecta que hay un pedido previo de una familia en el Barrio 3 de Abril.
4.  **La solicita**: El Conector a cargo recibe la alerta de "Match".
5.  **Coordina el retiro**: Se ponen en contacto donante y receptor para organizar el traslado.

## 🏗️ Arquitectura (Cómo funciona por dentro)
Hemos diseñado una arquitectura **"Serverless-lite"** para que el proyecto no tenga costos de mantenimiento y sea fácil de administrar por cualquier docente:

*   **Frontend**: Una Web App liviana (HTML/JS) que vuela en cualquier celular.
*   **Entrada de Datos**: Conectada directamente a **Google Forms** para asegurar que la información llegue de forma estructurada.
*   **Base de Datos**: Todo se gestiona desde un **Google Sheet** (planilla de cálculo). Los profes pueden editar o borrar registros desde una herramienta que ya conocen.
*   **Sincronización**: La app lee los datos en tiempo real mediante archivos CSV públicos de Google, permitiendo que la información esté siempre al día en el Panel de Match.

![Esquema de Arquitectura Comunitaria](screenshot_architecture.png)

## 📸 Un vistazo a la App

![Formulario de donación](screenshot_form.png)
*Interfaz de registro: Simple, directa y sin complicaciones.*

![Panel de Match para Conectores](screenshot_admin.png)
*El centro de control donde ocurre la magia de la conexión.*

---
**EMAL Nº 2702 — Rawson, Chubut**  
*Transformando la tecnología en una herramienta de cambio social.*
