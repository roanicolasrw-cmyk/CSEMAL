# Comunidad Solidaria - Proyecto EMAL 2702

Este es el repositorio de la plataforma **Comunidad Solidaria**, un proyecto nacido en la **Escuela Municipal de Aprendizaje Laboral (EMAL) Nº 2702** de Rawson, Chubut. 

La idea es simple: usar la tecnología para que los vecinos que tienen algo para donar se encuentren con los que lo necesitan, sin vueltas y sin costo.

![Portada de Comunidad Solidaria](screenshot_home.png)

## 💡 Sobre el proyecto

El proyecto surgió al ver que mucha gente en Rawson quería ayudar pero no sabía cómo llegar a las familias que realmente lo necesitaban. Creamos esta herramienta para centralizar esos pedidos y donaciones.

Un pilar fundamental son los **Conectores**. Son alumnos y profes de la EMAL que salen al barrio a hablar con los vecinos que no tienen internet o no se llevan bien con la tecnología, cargando sus pedidos en la app por ellos.

## 🛠️ Cómo está armado (Arquitectura)

Para que esto fuera sostenible y gratuito para la escuela, decidimos no usar servidores complicados ni bases de datos pagas. Todo funciona integrado con **Google Workspace**.

*   **Frontend**: Una interfaz sencilla en HTML, CSS y JavaScript que corre en cualquier celular.
*   **Formularios**: Usamos Google Forms para que la carga de datos sea segura y fácil de configurar.
*   **Base de datos**: Todo se guarda en un Google Sheet (una planilla de cálculo), lo que permite a los profes gestionar todo desde una interfaz que ya conocen.
*   **El "Match"**: El sistema cruza automáticamente los datos de donaciones y pedidos por categoría y barrio, facilitando la logística.

![Esquema de funcionamiento del sistema](screenshot_architecture.png)

## 🚀 Instalación y Setup

Si querés probarlo o instalarlo para otra institución:

1. Cloná el repo.
2. Abrí el `index.html` en un navegador.
3. Para que guarde datos de verdad, vas a tener que crear tus propios formularios en Google y poner los IDs en la configuración del archivo principal.

## 📸 Capturas de la App

A continuación se muestran algunas pantallas del sistema en funcionamiento:

![Formulario de donación](screenshot_form.png)
*Formulario simple para que los vecinos registren sus aportes.*

![Panel de Match para Conectores](screenshot_admin.png)
*El panel donde los voluntarios de la EMAL coordinan las entregas.*

---
Hecho con ❤️ por la comunidad de la **EMAL 2702 - Rawson**.
