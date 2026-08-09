# 🏎️ F1 Sponsorship Analytics: Sistema de Soporte a Decisiones (DSS) & Analytics Predictivo

Este proyecto de analítica de datos evalúa oportunidades de patrocinio comercial en la Fórmula 1. Su objetivo es transformar datos históricos y temporales de rendimiento en un **Sistema de Soporte a Decisiones (DSS)** interactivo que permita a una organización auditar riesgos, predecir retornos de inversión (ROI) y definir contratos basados en modelos matemáticos.

El proyecto está estructurado en un modelo de Power BI de **dos páginas** complementarias que integran el diagnóstico exploratorio inicial y la analítica predictiva avanzada.

---

## 🛠️ Stack Tecnológico y Herramientas Utilizadas

* **Microsoft Excel:** 
  * **Uso:** Limpieza inicial, estructuración de dos datasets independientes (`.xlsx`) y procesamiento de datos crudos (ETL).
  * **Técnicas:** Eliminación de duplicados, normalización de campos de texto, tratamiento de valores nulos/ausentes y validación de tipos de datos antes de la ingesta a Power BI.
* **Power BI:** 
  * **Uso:** Modelado de datos, creación de medidas/métricas implícitas y explícitas, diseño de dashboard interactivo de 2 páginas y analítica avanzada para graficar los resultados.
  * **Herramientas:** Tarjetas KPI, gráficos de rosca, distribución de frecuencias, líneas de referencia (Media y Mediana), interacciones unificadas en cascada, líneas de tendencia por regresión lineal y modelos de proyección predictiva (**Forecast**) con un 95% de intervalo de confianza.
* **Markdown:** 
  * **Uso:** Documentación ejecutiva e informe de hallazgos estratégicos.
---

## 📊 PARTE 1: Exploración, Limpieza y Diagnóstico Cualitativo (Página 1)

En la primera etapa del proyecto, el análisis se enfocó en responder a la pregunta inicial de negocio: **¿Cómo seleccionar la escudería o piloto adecuado sin incurrir en los costos desorbitados de los equipos top?**

<img width="1302" height="732" alt="{C58E03AF-A2B4-4859-821A-3CE2F4B4F53D}" src="https://github.com/user-attachments/assets/583dd76d-d80c-4637-874c-843ded96435a" />

### Hallazgos Principales:
1. **Volumen de Muestra:** Control de métricas generales de la parrilla (11 equipos, 22 pilotos y 15 naciones representadas).
2. **Inversiones de Valor (Equipos):** Se preseleccionaron **Alpine F1 Team** y **RB F1 Team** como opciones del pelotón medio con una alta relación costo-beneficio, combinando estabilidad en la tabla media y un sólido market share regional.
3. **Patrocinio a Nivel Piloto (Personal Branding):** Se evaluó la frecuencia en el Top 10 y la distribución de puntos para perfiles con alta tracción comercial o deportiva:
   * **Franco Colapinto:** *Engagement* masivo y monopolio del mercado hispanohablante.
   * **Oliver Bearman:** Talento técnico a un costo accesible.
   * **Liam Lawson:** Consistencia y visibilidad por fricción en pista.
   * **Isack Hadjar:** Proyección directa hacia el podio.

---

## 📈 PARTE 2: Del Análisis a la Decisión Inteligente (Página 2 - Power BI & DSS)

En la segunda etapa, se profundizó en la estadística descriptiva y la predicción visual para auditar matemáticamente las hipótesis cualitativas de la Parte 1.

<img width="1247" height="701" alt="{CE788CB2-AE54-4598-9BCB-9083160E69AA}" src="https://github.com/user-attachments/assets/5f90fe86-8e11-437d-b4a4-9367600eb821" />

### 1. Diagnóstico Estadístico y Outliers

#### A. La realidad detrás del "Promedio" (Media vs. Mediana)
* **Media de Puntos por Equipo:** `83,27`
* **Mediana de Puntos por Equipo:** `44,00`
* **Interpretación:** Existe una marcada asimetría hacia la derecha provocada por los líderes (Mercedes con 151 y Ferrari con 102). En la F1, usar la Media distorsiona la realidad; la **Mediana (44,00)** es la métrica de negocio real que divide equilibradamente a la parrilla.

#### B. Caza de Valores Atípicos (Outliers) y Anomalías
<img width="1248" height="701" alt="{13C041D7-54F0-49B1-8AF7-2F60AF868E72}" src="https://github.com/user-attachments/assets/35f82cfa-f595-42f6-9191-e60e8b8151b6" />

<img width="1247" height="698" alt="{E707FD5D-1EA1-464A-AD18-5B2354E754FF}" src="https://github.com/user-attachments/assets/05e6da4e-e213-4167-86f9-5b7854e289f7" />

* **Outliers de Mercado:** Mercedes y Ferrari se despegan del bloque medio (concentrado por debajo de los 30 puntos), reflejando las brechas presupuestarias de la categoría.
* **Explicación Fina de Anomalías en Carreras:**
  * **Alpine F1 Team (Picos de P14 en Rondas 5 y 9):** La caída en la Ronda 5 fue de origen accidental (choque de Gasly con Lawson, mientras Colapinto lograba un P6). En la Ronda 9, la anomalía obedeció a un estancamiento en el paquete de mejoras aerodinámicas frente a Audi y RB.
  * **RB F1 Team (Picos en Rondas 5 y 6):** En la Ronda 5, el incidente Lawson-Gasly relegó a Lawson al P20. En la Ronda 6, Lindblad sufrió fallas mecánicas (P22 virtual), pero Lawson amortiguó el golpe alcanzando un P7.

---

### 2. Visualización Predictiva y Diagnóstico por Piloto

Utilizando el motor predictivo de Power BI proyectado a **3 carreras** con un **95% de confianza**, se evaluó el desempeño individual filtrando interactivamente en el tablero:

#### Franco Colapinto (Engagement Regional)
<img width="1248" height="701" alt="{13C041D7-54F0-49B1-8AF7-2F60AF868E72}" src="https://github.com/user-attachments/assets/35f82cfa-f595-42f6-9191-e60e8b8151b6" />
* **Diagnóstico:** Línea de tendencia horizontal y estable en la frontera de los puntos, con oscilaciones ligadas a las mejoras del auto.
* **Criterio ROI:** Activo de alto impacto de *personal branding*. Carreras históricas como la de Miami peleándole a Lewis Hamilton generan picos de sobreexposición emocional que garantizan el monopolio de la atención regional.

#### Oliver Bearman (Proyección Técnica)
<img width="1252" height="700" alt="{5E9F2DB1-93E0-4938-BE4A-3CACE3E1A9E1}" src="https://github.com/user-attachments/assets/93084373-bad0-4062-833d-466cf74ade90" />
* **Diagnóstico:** Inicio competitivo (P7/P5) con una tendencia posterior al descenso debido a que el chasis no acompaña su talento.
* **Criterio ROI:** Clasificado como *"Sponsor en Proyección"*. Permite adquirir derechos comerciales a bajo costo a la espera de un auto más competitivo a futuro.

#### Liam Lawson (Alta Consistencia)
<img width="1247" height="698" alt="{E707FD5D-1EA1-464A-AD18-5B2354E754FF}" src="https://github.com/user-attachments/assets/05e6da4e-e213-4167-86f9-5b7854e289f7" />
* **Diagnóstico:** Salvo el accidente de la Ronda 5, demuestra una presencia constante en los puntos (Top 6 y Top 7 recurrentes).
* **Criterio ROI:** La opción de menor riesgo deportivo. Su estilo de conducción agresivo genera *"visibilidad por fricción"*, garantizando minutos extra de transmisión oficial en pantalla.

#### Isack Hadjar (Rendimiento Premium)
<img width="1249" height="699" alt="{FC882BB9-AA75-4B93-9DCE-9D185088724E}" src="https://github.com/user-attachments/assets/3a91a269-645a-488c-8844-af98fbc9c419" />
* **Diagnóstico:** Tras superar dos choques iniciales, registra la tendencia ascendente más agresiva de la parrilla (P5, P4, P6).
* **Criterio ROI:** Rendimiento deportivo directo con proyección a podio, aunque bajo la cotización de derechos más elevada al estar en la estructura principal de Red Bull.

---

## 💡 Propuesta Estratégica e Impacto Tecnológico

### A. Operatividad del Sistema DSS
El dashboard opera como un **Sistema de Soporte a Decisiones (DSS)** mediante interacciones en cascada:
1. Filtrar por "Escudería" analiza el rendimiento macro del equipo.
2. El selector de "Piloto" se condiciona automáticamente mostrando solo sus corredores sin romper la línea temporal del equipo.
3. Si el Forecast de un piloto cae por debajo de los umbrales de competitividad del negocio (mediana general), la gerencia comercial puede identificar el riesgo al instante y activar cláusulas de penalización o congelar bonificaciones.

### B. Escalabilidad en la Nube (Big Data & Cloud)
Ante el crecimiento del volumen de datos (telemetría de sensores en tiempo real, streaming y redes sociales), la migración a la **Nube (Azure / AWS / GCP)** aporta:
* **Procesamiento de Big Data:** Superar el límite de filas y procesamiento de Excel local.
* **Actualización Automatizada:** Ingesta continua de métricas sin intervención manual.
* **Disponibilidad Global:** Acceso elástico al DSS para ejecutivos desde cualquier dispositivo.

---

## 🏆 Conclusión General y Veredicto de Inversión

* **Veredicto a Nivel Equipo:** Mientras Alpine muestra picos atractivos pero sujetos a volatilidad técnica, **RB F1 Team se consolida como la inversión corporativa de menor riesgo general** debido a su resiliencia operativa y consistencia en la zona de puntos.
* **Veredicto a Nivel Piloto:** La estrategia de inversión debe diversificarse según el objetivo: **Colapinto** para el monopolio de engagement regional, **Lawson** para consistencia y minutos de pantalla, y **Hadjar / Bearman** para rendimiento *Premium* o apuestas de proyección futura respectivamente.
