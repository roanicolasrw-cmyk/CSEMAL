# Arquitectura del Sistema: Comunidad Solidaria

Este documento explica cómo está armado el sistema de la EMAL 2702. La idea fue hacer algo robusto pero que no dependiera de servidores costosos ni bases de datos complicadas.

## 🛠️ El "Motor" de Datos (Google Workspace)

En lugar de programar un backend desde cero, usamos las herramientas que la escuela ya tiene:

### 1. Captura de datos (Frontend -> Google Forms)
Cuando un usuario completa un formulario en la web, el JavaScript recolecta los campos y los envía mediante un `POST` asíncrono directamente al `formResponse` de un Google Form. 
*   **Ventaja**: No necesitamos un servidor intermedio para procesar datos.
*   **Seguridad**: Los datos quedan guardados en la cuenta institucional de la escuela.

### 2. Almacenamiento (Google Sheets)
Cada Google Form está vinculado a una hoja de cálculo. Esto permite que los directivos o profes puedan ver, editar o borrar registros directamente desde un Excel en la nube, sin entrar a la base de datos.

### 3. Distribución (Google Sheets -> Frontend)
Para que la app muestre los datos, publicamos las hojas de cálculo como **CSV**. 
*   La app descarga estos archivos de texto livianos.
*   Un script en el navegador (JS) los "parsea" y los convierte en las tarjetas que vemos en el Inicio y en el Panel Admin.

## 🧠 Lógica de Match (El Cerebro)

El sistema de coincidencias no ocurre en un servidor, sino en el navegador del usuario que entra al Panel de Match:
1.  Busca en la lista de "Necesidades" y en la de "Donaciones".
2.  Compara por **Categoría** (ej: "Ropa") y **Zona** (ej: "Barrio 3 de Abril").
3.  Si coinciden, genera un aviso de "Match" y permite que el Conector vea los datos de contacto para coordinar la entrega por WhatsApp.

## 📱 Interfaz de Usuario

*   **Diseño**: Se usó CSS puro con variables para que sea fácil cambiar los colores de la escuela.
*   **Portabilidad**: Está pensado para que funcione bien en celulares viejos (que es lo que suelen tener los vecinos o alumnos en el barrio).
*   **Offline-ish**: Usamos `localStorage` para que si se corta el internet un segundo, los datos que ya se cargaron no se pierdan.

---
Este sistema es un ejemplo de cómo usar "tecnología de guerrilla" para resolver problemas sociales reales sin presupuesto técnico.
