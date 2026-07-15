# Comunidad Solidaria - Proyecto EMAL 2702

Plataforma comunitaria de la **Escuela Municipal de Aprendizaje Laboral (EMAL) Nº 2702** de Rawson, Chubut. Diseñada para facilitar el intercambio de donaciones y la gestión de necesidades en el barrio.

![Portada de Comunidad Solidaria](screenshot_home.png)

## 💡 Propósito del Proyecto

El sistema busca eliminar las barreras entre quienes quieren ayudar y quienes necesitan asistencia. Introducimos el rol de los **Conectores** (alumnos y docentes voluntarios) que actúan como puente para familias que no tienen acceso a dispositivos móviles o internet, asegurando que la solidaridad llegue a todos.

## 🏗️ Arquitectura y Funcionamiento

El proyecto utiliza una arquitectura **"Serverless-lite"** para garantizar costo cero y facilidad de mantenimiento para la escuela.

1.  **Interfaz (Frontend)**: Web App desarrollada en HTML5, CSS3 y Vanilla JavaScript. No requiere servidores pesados y funciona en cualquier navegador móvil.
2.  **Captura de Datos**: Se integra con **Google Forms**. Los registros se envían directamente a formularios institucionales, garantizando seguridad y orden.
3.  **Gestión y Match**: Los datos se almacenan en **Google Sheets**. La aplicación sincroniza esta información en tiempo real para sugerir "Matches" (coincidencias) entre donantes y beneficiarios.
4.  **Logística**: Los Conectores coordinan las entregas directamente, agilizando el proceso mediante vínculos a WhatsApp.

![Esquema de funcionamiento del sistema](screenshot_architecture.png)

## 🛠️ Pasos para la Puesta en Marcha

Para implementar este sistema en la escuela o cualquier otra organización, solo se requiere:

1.  **Repositorio**: Descargar los archivos del proyecto.
2.  **Configuración de Formularios**: 
    *   Crear 3 formularios en Google (Necesidades, Donaciones, Conectores).
    *   Vincular cada formulario a una hoja de cálculo de Google Sheets.
3.  **Vincular la App**: 
    *   Obtener los IDs de campo (`entry.ID`) de los formularios creados.
    *   Actualizar el objeto `GOOGLE_FORMS_CONFIG` en el archivo `index.html`.
4.  **Publicación**: Abrir el archivo `index.html` en un navegador o subirlo a cualquier hosting estático gratuito (como GitHub Pages).

## 📸 Capturas de la App

![Formulario de donación](screenshot_form.png)
*Interfaz de registro de aportes comunitarios.*

![Panel de Match para Conectores](screenshot_admin.png)
*Panel de administración donde se gestionan los cruces y entregas.*

---
Proyecto educativo para la integración comunitaria.  
**EMAL 2702 - Rawson, Chubut.**
