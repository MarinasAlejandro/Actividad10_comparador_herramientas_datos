# Comparación Conceptual: Tableau vs Power BI

## 1. Qué es cada herramienta

### Tableau
Plataforma de visualización de datos y business intelligence desarrollada por Tableau Software (adquirida por **Salesforce en 2019** por $15.7B). Se centra en la exploración visual e interactiva de datos. Su filosofía es "ver y entender datos" — prioriza la calidad visual y la exploración ad-hoc. Actualmente se ofrece como **Tableau Cloud** (SaaS), **Tableau Server** (on-premise) y **Tableau Desktop** (autoría).

### Power BI
Suite de análisis y BI de **Microsoft**, lanzada en 2015, integrada profundamente en el ecosistema Microsoft 365 / Azure. Combina preparación de datos, modelado, visualización y distribución de informes. Se ofrece como **Power BI Desktop** (gratuito), **Power BI Pro**, **Power BI Premium** y **Power BI Embedded**. Desde 2024, Power BI forma parte de **Microsoft Fabric**, la plataforma unificada de datos y analytics de Microsoft.

---

## 2. Tipo de problemas para los que están diseñadas

| Aspecto | Tableau | Power BI |
|---------|---------|----------|
| **Foco principal** | Exploración visual de datos, análisis ad-hoc avanzado | Reporting corporativo, dashboards operacionales, self-service BI |
| **Escenario ideal** | Analista que necesita explorar datasets complejos visualmente, descubrir patrones, crear visualizaciones sofisticadas | Organizaciones que necesitan informes periódicos, KPIs, integración con datos de Microsoft (Excel, Dynamics, Azure) |
| **Complejidad de datos** | Datasets grandes y variados, múltiples fuentes heterogéneas | Datos corporativos estructurados, modelos dimensionales, datos del ecosistema Microsoft |
| **Tipo de análisis** | Exploratorio, descriptivo, geoespacial avanzado | Descriptivo, operacional, predictivo (con integración de Azure ML) |

---

## 3. Principal fortaleza de cada una

**Tableau:** La **calidad y flexibilidad de las visualizaciones**. Su motor VizQL traduce acciones de arrastrar-y-soltar en consultas de datos optimizadas. Permite crear visualizaciones complejas y personalizadas que en Power BI requerirían workarounds o custom visuals. Es considerado el estándar de referencia en data visualization.

**Power BI:** La **integración con el ecosistema Microsoft y la relación calidad-precio**. Para organizaciones que ya usan Microsoft 365, Azure y Excel, Power BI se integra de forma nativa. El modelado de datos con DAX y Power Query (M) es extremadamente potente. Power BI Desktop es gratuito, y Pro cuesta ~$10/usuario/mes — una fracción de Tableau.

---

## 4. Tipo de usuario principal

| Perfil | Tableau | Power BI |
|--------|---------|----------|
| **Data Analyst** | Uso intensivo — su público objetivo | Uso frecuente |
| **Business Analyst** | Uso frecuente | Uso intensivo — su público objetivo |
| **Data Scientist** | Integración con Python/R, TabPy | Integración con Python/R, Azure ML |
| **BI Developer** | Uso moderado | Uso intensivo (modelado DAX) |
| **Ejecutivo / Manager** | Consumidor de dashboards | Consumidor de dashboards + integración Teams |
| **Data Engineer** | Uso bajo (Tableau Prep para ETL ligero) | Uso moderado (Power Query, Dataflows, ahora Fabric) |
| **Citizen developer** | Curva de aprendizaje media | Accesible si conoce Excel |

---

## 5. Ventajas y limitaciones

### Tableau

| Ventajas | Limitaciones |
|----------|-------------|
| Visualizaciones best-in-class, muy personalizables | **Precio elevado**: Tableau Creator ~$75/usuario/mes |
| Motor VizQL optimizado para grandes volúmenes | Modelado de datos menos potente que DAX |
| Multiplataforma (Windows, Mac, web) | ETL limitado (Tableau Prep es funcional pero básico) |
| Comunidad activa (Tableau Public, Tableau Community) | Requiere Tableau Server/Cloud para compartir — coste adicional |
| Excelente para análisis geoespacial y mapas | Menor integración nativa con ecosistemas corporativos |
| Soporte nativo de LOD Expressions (cálculos a distintos niveles de granularidad) | Menor adopción en PYMES por coste |
| Tableau Accelerators (dashboards preconstruidos) | Licenciamiento complejo (Creator, Explorer, Viewer) |

### Power BI

| Ventajas | Limitaciones |
|----------|-------------|
| **Precio competitivo**: Desktop gratuito, Pro ~$10/usuario/mes | Visualizaciones menos flexibles out-of-the-box que Tableau |
| Integración nativa con Microsoft 365, Teams, SharePoint, Azure | **Solo Windows** para Desktop (la versión web es limitada para autoría) |
| DAX es un lenguaje de modelado muy potente | DAX tiene curva de aprendizaje empinada |
| Power Query (M) para ETL robusto | Limitación de 1 GB por dataset en Pro (10 GB en Premium) |
| Microsoft Fabric unifica pipelines, lakehouse y BI | Rendimiento puede degradarse con modelos complejos sin Premium |
| Actualizaciones mensuales con nuevas features | Dependencia del ecosistema Microsoft |
| Copilot integrado (IA generativa para crear informes) | Gobernanza más compleja en despliegues grandes |
| Amplio marketplace de custom visuals | Algunas features avanzadas solo en Premium/Fabric |

---

## 6. Comparación de features

### Visualizaciones

| Feature | Tableau | Power BI |
|---------|---------|----------|
| **Tipos nativos** | ~24+ tipos (incluye Sankey, radial, mapas avanzados) | ~30+ tipos nativos + marketplace de custom visuals (1,000+) |
| **Personalización** | Muy alta — control granular de cada elemento visual | Media-alta — más limitado sin custom visuals |
| **Mapas** | Excelente (Mapbox integrado, spatial joins, mapas de densidad) | Bueno (ArcGIS, Azure Maps, Bing Maps) |
| **Dashboards** | Interactivos, multi-hoja, story points | Interactivos, multi-página, bookmarks |
| **Visualización de grandes volúmenes** | Superior — VizQL optimiza renderizado | Bueno con DirectQuery, limitado en Import mode |

### Interactividad

| Feature | Tableau | Power BI |
|---------|---------|----------|
| **Filtros cruzados** | Sí (actions, highlighters) | Sí (cross-filtering nativo, más intuitivo) |
| **Drill-down** | Sí, con jerarquías | Sí, nativo y muy fluido |
| **Tooltips dinámicos** | Sí, con Viz in Tooltip | Sí, con Report Page Tooltips |
| **Parámetros** | Sí (Parameter Actions desde v2019) | Sí (What-if parameters, Field parameters) |
| **Mobile** | Tableau Mobile (iOS/Android) | Power BI Mobile (iOS/Android), mejor integrado |
| **Natural Language Query** | Ask Data (mejorado con Tableau AI/Pulse) | Q&A (más maduro, integrado con Copilot) |

### Conectores de datos

| Feature | Tableau | Power BI |
|---------|---------|----------|
| **Número de conectores** | ~90+ nativos | ~150+ nativos |
| **Bases de datos** | Todos los principales (SQL Server, PostgreSQL, Oracle, Snowflake, BigQuery, Databricks...) | Igual + ventaja en Azure SQL, Synapse, Fabric |
| **Cloud / SaaS** | Salesforce (nativo), Google Analytics, SAP | Dynamics 365, SharePoint, Azure services (nativo) |
| **Archivos** | CSV, Excel, JSON, PDF, estadísticos (.sav, .sas7bdat) | CSV, Excel, JSON, PDF, Parquet |
| **Live connection** | Sí (Live / Extract) | Sí (DirectQuery / Import / Dual) |
| **Dataflows / ETL** | Tableau Prep (herramienta separada) | Power Query integrado + Dataflows en servicio |

### Facilidad de uso y curva de aprendizaje

| Aspecto | Tableau | Power BI |
|---------|---------|----------|
| **Primeros pasos** | Intuitivo para visualizar, drag-and-drop natural | Intuitivo si vienes de Excel |
| **Curva para dominar** | Media — LOD expressions, cálculos de tabla | Media-alta — DAX es potente pero complejo |
| **Documentación** | Excelente + Tableau Public como recurso de aprendizaje | Excelente + Microsoft Learn + comunidad enorme |
| **Comunidad** | Tableau Community, Tableau Public (millones de vizzes) | Power BI Community, Microsoft Fabric Community |
| **Certificaciones** | Tableau Desktop Specialist, Certified Data Analyst | PL-300 (Power BI Data Analyst) |

### Sharing y publicación

| Feature | Tableau | Power BI |
|---------|---------|----------|
| **Publicación web** | Tableau Public (gratis, público), Tableau Cloud/Server | Power BI Service (Pro/Premium), publicar en web (público) |
| **Embedding** | Tableau Embedded Analytics (coste adicional) | Power BI Embedded (modelo por capacidad) |
| **Colaboración** | Comentarios en Tableau Cloud | Integración con Teams, comentarios, suscripciones por email |
| **Exportación** | PDF, imagen, PowerPoint, CSV | PDF, PowerPoint, Excel, CSV, PBIX |
| **Alertas** | Data-driven alerts | Alertas + suscripciones + integración Power Automate |
| **Row-level security** | Sí | Sí (RLS y OLS nativo) |

### Precio y licenciamiento (2025-2026)

| Tier | Tableau | Power BI |
|------|---------|----------|
| **Gratuito** | Tableau Public (datos públicos) | Power BI Desktop (autoría local, sin compartir) |
| **Individual/Pro** | Tableau Creator: ~$75/usuario/mes | Power BI Pro: ~$10/usuario/mes |
| **Consumidor** | Tableau Viewer: ~$15/usuario/mes | Incluido en Microsoft 365 E5; sino ~$10/usuario/mes |
| **Enterprise** | Tableau Server/Cloud + licencias por rol | Power BI Premium: desde ~$5,000/mes por capacidad (P1) |
| **Modelo** | Por usuario (Creator, Explorer, Viewer) | Por usuario (Pro) o por capacidad (Premium/Fabric) |

---

## 7. Diferencias técnicas clave

### Motor de datos

| Aspecto | Tableau | Power BI |
|---------|---------|----------|
| **Motor propio** | **Hyper** — motor columnar in-memory, optimizado para extracción y consulta rápida | **Vertipaq (xVelocity)** — motor columnar in-memory con alta compresión, basado en Analysis Services |
| **Modo de conexión** | **Live** (consulta directa a la fuente) o **Extract** (snapshot en formato .hyper) | **Import** (carga en Vertipaq), **DirectQuery** (consulta en vivo), **Dual** (combo) |
| **Compresión** | Buena compresión columnar | Excelente compresión (~10x), muy eficiente en memoria |
| **Límite de datos** | Sin límite práctico en Server/Cloud con Extract | 1 GB/dataset en Pro, 10 GB en Premium, ilimitado en Fabric |
| **Procesamiento** | Query fusion y paralelización en Hyper | Folding en Power Query (push-down a la fuente) |

### Lenguaje propio

| Aspecto | Tableau | Power BI |
|---------|---------|----------|
| **Cálculos** | **VizQL** (interno) + fórmulas de Tableau (similares a Excel) | **DAX** (Data Analysis Expressions) — lenguaje funcional completo |
| **ETL** | **Tableau Prep Flow** (visual, low-code) | **M (Power Query Formula Language)** — funcional, case-sensitive |
| **Cálculos avanzados** | **LOD Expressions** (FIXED, INCLUDE, EXCLUDE) — control de granularidad | **DAX measures + calculated columns** — contexto de evaluación (row context, filter context) |
| **Scripting** | TabPy (Python), R integration | Python visuals, R visuals, Python/R en Power Query (Premium) |
| **Complejidad** | Más accesible para analistas | DAX más potente pero con curva de aprendizaje mayor |

### Integración con ecosistema

| Aspecto | Tableau | Power BI |
|---------|---------|----------|
| **Ecosistema nativo** | Salesforce (CRM, MuleSoft, Slack) | Microsoft 365 (Excel, Teams, SharePoint, Outlook, OneDrive) |
| **Cloud** | Tableau Cloud (AWS-based), conectores multi-cloud | Azure (nativo), AWS y GCP (mediante conectores) |
| **IA / ML** | Tableau AI, Tableau Pulse (insights automáticos), Einstein Discovery | Copilot en Power BI, Azure ML integration, AI visuals, Smart Narratives |
| **Gobierno de datos** | Tableau Catalog, Tableau Data Management | Microsoft Purview, Fabric data governance, lineage nativo |
| **APIs** | REST API, JavaScript API, Hyper API, Metadata API | REST API, JavaScript API, XMLA endpoint (Premium), Semantic Link |
| **Git / CI-CD** | Soporte limitado (contenido XML), mejorando | TMDL + Git integration nativa en Fabric (2024-2025) |
| **Plataforma de datos** | No tiene — se conecta a plataformas externas | **Microsoft Fabric** incluye Lakehouse, Data Warehouse, Pipelines, Real-Time Analytics + Power BI |

---

## Resumen rápido para slides

| Dimensión | Tableau | Power BI |
|-----------|---------|----------|
| **En una frase** | "El mejor en visualización de datos" | "BI corporativo accesible integrado con Microsoft" |
| **Mejor para** | Exploración visual avanzada, data storytelling | Reporting corporativo, organizaciones Microsoft |
| **Peor para** | Presupuestos ajustados, modelado de datos complejo | Visualizaciones muy personalizadas, entornos no-Microsoft |
| **Precio** | Alto ($75/usuario/mes Creator) | Bajo ($10/usuario/mes Pro) |
| **Curva** | Media | Media-alta (por DAX) |
| **Tendencia 2025-2026** | IA con Tableau Pulse + Einstein, integración Salesforce | Microsoft Fabric, Copilot, Direct Lake, TMDL |
| **Cuota de mercado** | #2 en BI (líder histórico en Gartner hasta 2019) | #1 en BI (líder en Gartner Magic Quadrant desde 2020) |
