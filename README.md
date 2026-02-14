# dataProject_dashBoard_AnalisisDeDatos

📊 Análisis Descriptivo Inicial del Dataset

Este dataset recoge información sobre publicaciones virales en varias redes sociales. Incluye datos temporales, temáticos, geográficos y métricas de interacción, lo que permite entender cómo se comporta el contenido digital en diferentes plataformas.

🗓️ 1. Dimensión temporal (Post_Date)

La fecha de publicación permite:

- Identificar tendencias a lo largo del tiempo.
- Analizar cómo evoluciona el engagement por periodos.
- Relacionar picos de viralidad con eventos o momentos concretos.
- Aporta contexto y orden cronológico al comportamiento del contenido.

📱 2. Plataforma (TikTok, Instagram, Twitter, YouTube)

Cada plataforma tiene algoritmos, formatos y audiencias distintas. Esto permite:

- Comparar el rendimiento entre redes.
- Ver dónde se concentra el contenido viral.
- Detectar qué formatos funcionan mejor en cada plataforma.

🔥 3. Hashtags (temas o tendencias)

Los hashtags clasifican el contenido por temática. Gracias a ellos se puede:

- Identificar los temas más virales.
- Analizar qué categorías generan más interacción.
- Detectar patrones de viralidad asociados a tendencias (#Gaming, #Education, #Comedy, etc.).

🎬 4. Tipo de contenido (Content_Type)

Incluye formatos como Video, Shorts, Reel, Post, Live Stream o Tweet. Permite:

- Comparar el rendimiento entre formatos.
- Ver qué tipo de contenido genera más interacción.
- Analizar la evolución de formatos cortos vs. largos.

🌍 5. Región

La región añade una dimensión geográfica que permite:

Identificar mercados con mayor viralidad.
Comparar comportamientos entre países.
Detectar si ciertos temas funcionan mejor en regiones específicas.

📈 6. Métricas cuantitativas (Views, Likes, Shares, Comments)

Estas métricas miden el rendimiento de cada publicación:

- Views: alcance
- Likes: aprobación
- Shares: viralidad
- Comments: interacción activa

Permiten analizar:

- Distribuciones y rangos.
- Valores atípicos (posts extremadamente virales).
- Comparaciones entre plataformas, hashtags o regiones.
- Relaciones entre métricas (por ejemplo, muchas views pero pocos likes).

También permiten calcular indicadores derivados como:

- Tasa de interacción
- Ratio de compartidos por visualización
- Comentarios por like

⭐ 7. Engagement_Level (Low, Medium, High)

Clasifica el rendimiento global de cada publicación. Es útil para:

- Identificar rápidamente qué contenido funciona mejor.
- Comparar grupos sin cálculos adicionales.
- Detectar patrones comunes en publicaciones de alto engagement.


🧩 ¿Qué aporta este dataset en conjunto?

Este dataset permite:

- Entender cómo se comporta el contenido viral en distintas plataformas.
- Analizar qué temas, formatos y regiones generan más interacción.
- Detectar patrones temporales de viralidad.
- Comparar métricas de rendimiento entre categorías.
- Identificar factores asociados a niveles altos de engagement.
- Construir modelos predictivos o segmentaciones basadas en comportamiento.

En resumen, es un dataset rico, multidimensional y muy útil para análisis de tendencias digitales, ideal para:

- Exploración inicial
- Visualización de patrones
- Modelos de predicción de engagement
- Estudios de comportamiento por plataforma o región


📊 ESTRUCTURA GENERAL DEL DASHBOARD

El dashboard responderá a 4 preguntas clave:

- ¿Cómo evoluciona el rendimiento en el tiempo?
- ¿Qué plataforma y formato funcionan mejor?
- ¿Qué temas (hashtags) generan más engagement?
- ¿Dónde (región) se genera más viralidad?

🔹 KPIs PRINCIPALES (Parte superior del Dashboard)

- Total Views
- Total Likes
- Total Shares
- Total Comments
- Engagement Rate promedio  
  ( (Likes + Shares + Comments) / Views )
- % Posts High Engagement


# LAS 10 GRÁFICAS / TABLAS

1️⃣ **Evolución de Views en el tiempo**

- **Tipo:** Gráfico de líneas  
- **Eje X:** Año-Mes (derivado de Post_Date)  
- **Valores:** SUM de Views  
- **Objetivo:** Ver tendencia de alcance.

2️⃣ **Evolución del Engagement Rate en el tiempo**

- **Tipo:** Línea  
- **Valores:** Engagement Rate promedio por mes  
- Permite ver calidad vs volumen.

3️⃣ **Views por Plataforma**

- **Tipo:** Columnas agrupadas  
- **Eje:** Platform  
- **Valores:** SUM Views  
- Respuesta: dónde hay mayor alcance.

4️⃣ **Engagement Rate por Plataforma**

- **Tipo:** Columnas  
- **Eje:** Platform  
- **Valores:** Engagement Rate promedio  
- Detecta qué plataforma convierte mejor.

5️⃣ **Engagement Level — Distribución**

- **Tipo:** Torta o barra horizontal  
- **Eje:** Engagement_Level  
- **Valores:** Conteo de Post_ID  
- Muestra proporción Low / Medium / High.

6️⃣ **Top 10 Hashtags por Views**

- **Tipo:** Barra horizontal  
- **Eje:** Hashtag  
- **Valores:** SUM Views  
- **Filtro:** Top 10  
- Detecta temas virales.

7️⃣ **Engagement Rate por Content_Type**

- **Tipo:** Columnas  
- **Eje:** Content_Type  
- **Valores:** Engagement Rate promedio  
- Responde qué formato funciona mejor.

8️⃣ **Interacciones promedio por formato**

- **Tipo:** Columnas apiladas  
- **Valores:**  
  - Likes promedio  
  - Shares promedio  
  - Comments promedio  
- **Agrupado por:** Content_Type  
- Permite ver patrones de comportamiento.

9️⃣ **Views por Región**

- **Tipo:** Mapa (Excel 365) o barras  
- **Eje:** Region  
- **Valores:** SUM Views  
- Detecta mercados más fuertes.

🔟 **Relación Views vs Engagement**

- **Tipo:** Dispersión  
- **Eje X:** Views  
- **Eje Y:** Engagement Rate  
- **Cada punto:** un Post  
- Útil para detectar outliers y analizar si más views implican mejor engagement.


# 🎛 Segmentadores 

Agrega 4 slicers:

- Platform
- Hashtag
- Content_Type
- Region

Todos conectados a todas las tablas dinámicas. 
Esto, permite tener un dashboard interactivo.

# 🧱 ESTRUCTURA DE HOJAS

- **Hoja 1 → tblPosts**  
  Tabla estructurada

- **Hoja 2 → dat_validaciones**  
Validación de datos originales: quitar duplicados, validar que no contenga datos vacios, etc.

- **Hoja 3 → Base_Pivot**
Tablas dinámicas que alimentan al dashboard

- **Hoja 34 → Dashboard**

# 📐 Métrica clave creadas en la tabla original

Columnas nuevas (calculadas):

**Interactions =** Likes + Shares + Comments

**Engagement_Rate =**  Interactions / Views

**Year_Month =**  @Post_Date pero en formato aaaa-mm

