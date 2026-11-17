# Monitor HACCP — Pulpa de Cacao Pasteurizada y Refrigerada

Aplicación web autónoma (*Single File Application*) diseñada para el control digital en tiempo real de los Puntos Críticos de Control (**PCC**) en la línea de producción de **PULPA DE CACAO PASTEURIZADA Y REFRIGERADA ESPECIAL PARA NÉCTARES Y HELADERÍA**.

---

## 📋 Información Académica y Autores

* **Institución:** Servicio Nacional de Aprendizaje — **SENA** (Centro Agroindustrial, Regional Quindío — Armenia, Quindío)
* **Programa:** Tecnología en Sistemas Integrados de Gestión (Quinto Trimestre)
* **Ficha:** 3309920
* **Área:** Inocuidad Alimentaria
* **Instructor:** Carlos Barco
* **Equipo Desarrollador (Aprendices):**
  * Diego Fernando Moreno
  * Sonia Mendez
  * Manuela Arango
  * Oscar Ospina
  * Harbey Vallejos

---

## 🎯 Límites Críticos HACCP Configurados

El sistema evalúa automáticamente cada toma de muestra frente a los parámetros normativos establecidos para el proceso:

| Punto Crítico (PCC) | Etapa del Proceso | Límite Crítico | Objetivo de Inocuidad | Acción ante Desviación |
| :--- | :--- | :--- | :--- | :--- |
| **PCC-1** | Cocción / Pasteurización | **≥ 85.0 °C** | Eliminación de microorganismos patógenos e inactivación de levaduras fermentativas salvajes. | Alerta roja inmediata y bloqueo del registro hasta documentar **Acción Correctiva** obligatoria. |
| **PCC-2** | Enfriamiento Rápido | **≤ 4.0 °C** | Ruptura de la zona de peligro térmico y conservación sensorial antes del envasado y distribución. | Alerta roja inmediata y exigencia de medida de contención o reproceso térmico. |

---

## 🚀 Funcionalidades Principales (Versión Comercial v13)

1. **Identificación Corporativa Editable (Multi-empresa):** Permite registrar y guardar de forma permanente en el navegador (`localStorage`) la **Razón Social**, **NIT**, **Dirección de Planta** y **Teléfono de Contacto** de la empresa procesadora cliente.
2. **Integridad Temporal Anti-Fraude:** Sello de **Fecha y Hora (`YYYY-MM-DD HH:MM:SS`)** en modo de solo lectura (`readonly`) sincronizado automáticamente con el reloj del sistema operativo Windows (`time.windows.com`), impidiendo alteraciones manuales en las auditorías.
3. **Motor de Validación en Tiempo Real:** Evalúa la temperatura antes y durante el guardado, desplegando alertas visuales y exigiendo una **Acción Correctiva** obligatoria cuando un lote sale de norma.
4. **Gráfico de Tendencia Dinámico por Días:** Renderizado nativo en `<canvas>` HTML5 que permite filtrar las curvas térmicas tanto por etapa (**PCC-1 Cocción** / **PCC-2 Enfriamiento**) como por **día específico de producción** o vista histórica consolidada.
5. **Exportación Gerencial a Excel (`.xls`) por Día o Historial Completo:**
   * Genera hojas de cálculo personalizadas con el encabezado legal de la empresa cliente y el producto final.
   * Permite descargar **todos los registros de un día específico** o el consolidado completo.
   * Aplica formato condicional visual resaltando en **fondo rojo intenso, letra blanca y negrita** (estrictamente desde la **columna A hasta la columna H**) todas las filas que presentaron **Alerta Crítica**.
6. **Operación 100% Offline y Síncrona:** Construida en **HTML5, CSS3 y JavaScript puro (Vanilla JS)** sin dependencias externas, garantizando ejecución instantánea desde cualquier navegador web, tablet de planta o servidor estático.

---

## 🛠️ Guía de Instalación y Despliegue

### Ejecución Local
1. Descargue el archivo principal de la aplicación (`Monitor_HACCP_Cacao_v13.html`) y renómbrelo como **`index.html`**.
2. Ábralo directamente haciendo doble clic en **Google Chrome**, **Microsoft Edge** o mediante la extensión *Live Server* en **Visual Studio Code**.

### Publicación en la Nube (GitHub Pages / Netlify)
1. Suba los archivos **`index.html`** y **`README.md`** a la rama principal (`main`) de este repositorio.
2. Active **GitHub Pages** (*Settings > Pages > Branch: main*) o importe el repositorio en **Netlify** para obtener una URL pública HTTPS lista para usar desde dispositivos móviles en planta.

---

## 📄 Licencia y Uso Comercial
Proyecto desarrollado con fines académicos y comerciales como plantilla digital B2B para plantas procesadoras de pulpas de frutas, néctares y bases de heladería.
