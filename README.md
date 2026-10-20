# Centro de Control & Inteligencia Operativa IT | AUSOL & GCO (Grupo Abertis)

> **Dashboard Ejecutivo Interactivo y Multi-Página de Telemetría de Peajes, Gobierno de Datos & Arquitectura Cloud**  
> Desarrollado por **Rubén Barrios** (Data & Analytics Specialist).

🌐 **Acceso Público en Vivo:** [https://rubenbarrios-bigdata.github.io/ausol-gco-dashboard/](https://rubenbarrios-bigdata.github.io/ausol-gco-dashboard/)

---

## 📌 Descripción del Proyecto

Este dashboard interactivo simula la plataforma de monitoreo y analítica en tiempo real para las dos principales concesiones viales de la República Argentina operadas por el **Grupo Abertis**:
1. **Autopistas del Sol (AUSOL):** Acceso Norte / Troncal Panamericana (Ramales Campana, Pilar y Tigre) y Avenida General Paz.
2. **Grupo Concesionario del Oeste (GCO):** Autopista Acceso Oeste (Troncal Ituzaingó, Luján).

Combina **telemetría operativa de vías de peaje** (Sistemas SAC en carril y servidores locales BOS), **normativa tarifaria oficial de la Dirección Nacional de Vialidad (DNV)** y el **Marco de Gobierno de TI COBIT** (integrado con la plataforma corporativa Enaxis GRC).

---

## 🚀 Módulos y Páginas del Dashboard

El dashboard cuenta con navegación instantánea por pestañas y simulación de filtros dinámicos por estación:

1. **🛡️ Gobierno IT & SLAs (COBIT):**  
   Monitoreo de Acuerdos de Nivel de Servicio (SLA) para componentes tecnológicos críticos: Uptime de antenas RFID (Kapsch), cámaras ANPR/OCR, clearing de TelePASE y disponibilidad de servidores BOS.
2. **⏱️ Operaciones & Franjas DNV:**  
   Análisis de tránsito vehicular y recaudación segmentado por franjas Pico (07:00-10:00 CABA / 17:00-20:00 Provincia) y No Pico, con comparativa de tiempos de atención en carril.
3. **📊 Saturación de Vías (`Window Functions`):**  
   Ranking analítico por estación con funciones de ventana SQL (`DENSE_RANK()` y `SUM(...) OVER(PARTITION BY...)`) para determinar el porcentaje de absorción vehicular de cada carril sobre el total del peaje.
4. **🔍 Auditoría de Fugas e Incidentes:**  
   Detección y valorización económica de tránsitos no cobrados (tags inválidos en lista negra, evasiones por barrera violentada y discrepancias de lectura de patente).
5. **⚡ Linaje de Datos: BigQuery + dbt Core:**  
   Arquitectura técnica integral desde la ingesta cruda (JSON/Avro) en BigQuery hasta las capas de transformación y modelado dimensional en dbt (Staging, Intermediate y Marts) con pruebas automatizadas de calidad (`dbt test`).

---

## 🛠️ Stack Tecnológico

* **Visualización:** HTML5 moderno, CSS3 Vanilla con diseño Dark Mode & Glassmorphism, Chart.js.
* **Procesamiento Analítico:** Google BigQuery (Data Warehouse Cloud), dbt Core (Modelado y Pruebas de Calidad), MySQL 8.0+.
* **Gobernanza:** Marco COBIT 2019 (BAI04, APO10, EDM03), Enaxis GRC.

---
© 2026 Rubén Barrios. Preparado para presentación técnica ejecutiva.
