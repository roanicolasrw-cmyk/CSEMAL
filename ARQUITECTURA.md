# Arquitectura del Sistema: Comunidad Solidaria

Este documento detalla la estructura técnica y lógica de la plataforma. El diseño prioriza la **autonomía institucional**, el **costo cero** y la **facilidad de uso** para personas con conocimientos básicos de ofimática.

## 📐 Componentes Principales

### 1. Capa de Presentación (Web App)
*   **Tecnologías**: HTML puro, CSS (con variables dinámicas) y JavaScript nativo.
*   **Navegación**: Funciona como una SPA (Single Page Application) para cargar instantáneamente en conexiones de baja velocidad.
*   **Adaptabilidad**: Diseño 100% responsivo, optimizado para celulares usados por los Conectores en el terreno.

### 2. Motor de Datos (Google Workspace)
En lugar de una base de datos SQL o servidores complejos, el sistema se apoya en el ecosistema de Google para la gestión de información:
*   **Entrada (POST)**: JavaScript envía los datos de los formularios directamente a los endpoints de **Google Forms**.
*   **Persistencia**: Los datos se organizan automáticamente en **Google Sheets**.
*   **Salida (FETCH)**: La aplicación lee los datos publicados en formato **CSV** desde las hojas de cálculo para refrescar el tablero de control.

### 3. Lógica de "Match"
El proceso de emparejamiento ocurre en el lado del cliente (Navegador):
*   **Filtros**: El script compara las categorías de los pedidos pendientes contra las donaciones disponibles.
*   **Zonificación**: Prioriza las coincidencias en el mismo barrio o zona de Rawson para facilitar el transporte.
*   **Acción**: Genera botones directos de WhatsApp para que el Conector contacte a ambas partes sin intermediarios técnicos.

## 🔄 Flujo de Información

1.  **Registro**: Un vecino o conector carga un dato (ej: "Necesito Calzado").
2.  **Sincronización**: El dato viaja a la nube de Google.
3.  **Actualización**: El Panel Admin detecta el nuevo registro al sincronizar el CSV.
4.  **Vinculación**: Si existe una donación compatible, el sistema muestra el aviso de "Match".
5.  **Entrega**: El conector coordina, entrega y marca el pedido como "Finalizado".

---
Esta arquitectura permite que la **EMAL 2702** sea dueña de sus datos y de la herramienta, sin depender de servicios externos pagados ni de mantenimiento especializado.
