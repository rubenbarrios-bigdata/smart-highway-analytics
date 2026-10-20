# Smart Highway Control Center & IT Governance Analytics | Case Study

> **Interactive Multi-Page Executive Dashboard — Highway Telemetry, Data Governance & Cloud Architecture**  
> Developed by **Rubén Barrios** (Data & Analytics Specialist).

🌐 **Acceso Público en Vivo:** [https://rubenbarrios-bigdata.github.io/smart-highway-analytics/](https://rubenbarrios-bigdata.github.io/smart-highway-analytics/)

---

> [!NOTE]
> **Aviso de Confidencialidad y Propósito del Portafolio:**  
> Este proyecto es un **caso de estudio técnico y prototipo interactivo de Business Intelligence** aplicado a la industria de concesiones viales e infraestructura inteligente de autopistas metropolitanas.  
> **Todos los datos, transacciones vehiculares, identificadores de tags y patentes mostrados son 100% sintéticos y simulados**, generados exclusivamente con fines demostrativos, académicos y de evaluación de arquitectura de datos.

---

## 📌 Descripción del Proyecto

Este dashboard interactivo simula la plataforma de monitoreo y analítica en tiempo real para la gestión operativa y gobernanza tecnológica de concesiones de autopistas de alto tránsito (Red de Accesos Metropolitanos):
1. **Corredor Norte (Troncal Panamericana):** Ramales Campana, Pilar y Tigre.
2. **Corredor Oeste (Troncal del Oeste):** Estaciones troncales Ituzaingó y Luján.

Combina **telemetría operativa de vías de peaje** (Sistemas SAC en carril y servidores locales BOS), **normativa tarifaria oficial de la Dirección Nacional de Vialidad (DNV)** y el **Marco de Gobierno de TI COBIT** (gestión de disponibilidad BAI04 y acuerdos de servicio con proveedores de tecnología APO10).

---

## 🚀 Módulos y Páginas del Dashboard

El dashboard cuenta con navegación instantánea por pestañas y simulación de filtros dinámicos por estación:

1. **🛡️ Gobierno IT & SLAs (COBIT):**  
   Monitoreo de Acuerdos de Nivel de Servicio (SLA) para componentes tecnológicos críticos: Uptime de antenas RFID, cámaras ANPR/OCR, clearing de TelePASE y disponibilidad de servidores de peaje.
2. **⏱️ Operaciones & Franjas DNV:**  
   Análisis de tránsito vehicular y recaudación segmentado por franjas Pico (07:00-10:00 CABA / 17:00-20:00 Provincia) y No Pico, con comparativa de tiempos de atención en carril.
3. **📊 Saturación de Vías (`Window Functions`):**  
   Ranking analítico por estación con funciones de ventana SQL (`DENSE_RANK()` y `SUM(...) OVER(PARTITION BY...)`) para determinar el porcentaje de absorción vehicular de cada carril sobre el total de la plaza de peaje.
4. **🔍 Auditoría de Fugas e Incidentes:**  
   Detección y valorización económica de tránsitos no cobrados (tags inválidos en lista negra, evasiones por barrera violentada y discrepancias de lectura de patente).
5. **⚡ Linaje de Datos: BigQuery + dbt Core:**  
   Arquitectura técnica integral desde la ingesta cruda (JSON/Avro) en BigQuery hasta las capas de transformación y modelado dimensional en dbt (Staging, Intermediate y Marts) con pruebas automatizadas de calidad (`dbt test`).
6. **🎧 Audiolibros & Audio-Guía Interactiva (`audiolibros.html`):**  
   Tres audiolibros completos narrados en español neutro con reproductor multimedia adaptativo (diseño responsive mobile-first), selector de velocidad (0.75x a 2.0x), barra de avance táctil y transcripción técnica sincronizada.

---

## 🛠️ Stack Tecnológico

* **Visualización:** HTML5 moderno, CSS3 Vanilla con diseño Dark Mode & Glassmorphism, Chart.js.
* **Procesamiento Analítico:** Google BigQuery (Data Warehouse Cloud), dbt Core (Modelado y Pruebas de Calidad), MySQL 8.0+.
* **Gobernanza:** Marco COBIT 2019 (BAI04, APO10, EDM03), Enaxis GRC.

---
© 2026 Rubén Barrios. Preparado para presentación técnica ejecutiva y portafolio profesional.
