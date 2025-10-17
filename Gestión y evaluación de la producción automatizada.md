• Diagrama de operaciones de proceso.

El siguiente DOP toma en cuenta todas las operaciones que se deben cumplir en la fabricación de un motoreductor fabricado en la empresa RAMFÉ. Cabe remarcar que como se ve en la figura el total de tiempo acumulado en todas estas operaciones da un resultado de 750 minutos por pieza, sin embargo esta cantidad de minutos no contempla el número de máquinas que se deispone para hacer la misma operación ni tampoco si algunas de estas labores se fabrican en paralelo. Este análisis se realizará posteriormente evaluando primero los procesos que se realizan en paralelo.

[![operaciones2-6.png](https://i.postimg.cc/15z7mL9F/operaciones2-6.png)](https://postimg.cc/14LrM7VR)

A continuación se muestran las operaciones más críticas

[![diagrama-operaciones-3.png](https://i.postimg.cc/MTTKZQSd/diagrama-operaciones-3.png)](https://postimg.cc/McC8dXXQ)

##  Análisis del Estado Actual de la Planta RAMFE

###  1. Maquinaria Disponible

| Tipo de máquina | Cantidad | Descripción | Piezas / Operaciones | Observaciones |
|-----------------|-----------|--------------|----------------------|----------------|
| **Torno manual** | 4 | Tornos funcionales operados manualmente. | Torneado para generar *blanks* o ejes base. | Depende totalmente del operario. |
| **Torno para tornillo sin fin** | 1 | Torno sincronizado en avances y rotación. | Fabricación de tornillos sin fin. | Proceso lento y especializado. |
| **Fresadoras manuales** | 6 | Máquinas convencionales para operaciones varias. | Taladrado, chaveteros y mecanizado de engranajes. | Requieren alta destreza manual. |
| **Fresadora CNC (3 ejes)** | 1 | Control numérico computarizado. | Acabados de piezas con geometrías complejas. | Mayor precisión, bajo aprovechamiento. |
| **Talladora (Shaper)** | 1 | Mecanizado de engranajes internos. | Engranes para reductores. | Limitada capacidad productiva. |

---

###  2. Capacidad de Producción Actual

- **Tiempo disponible por jornada:** 480 minutos (8 horas).  
- **Tiempo disponible por semana:** 2400 minutos (5 días).  
- **Tiempo de tallado por pieza (crítico):** 120 minutos.  
- **Total de engranajes por día por talladora:** 4 unidades.  
- **Producción semanal estimada:** 12 engranajes por máquina.  
- **Demanda semanal estimada:** 205 engranajes (sin fin, cónicos y helicoidales).  

> 💡 *Conclusión:* La capacidad actual es insuficiente para cubrir la demanda proyectada de **500 motorreductores mensuales**, lo que justifica la necesidad de implementar **automatización** en las etapas de mecanizado.

---

### 3. Identificación de Cuellos de Botella

Los principales cuellos de botella se presentan en las **operaciones de tallado y fresado**, debido a:

- Alta dependencia de operarios.  
- Tiempos de cambio de herramienta y sujeción elevados.  
- Falta de integración entre máquinas.  
- Baja disponibilidad de equipos CNC automatizados.

---

### 4. Potenciales de Mejora

| Área | Problema actual | Oportunidad de mejora |
|------|-----------------|-----------------------|
| **Mecanizado de engranajes** | Operación lenta y manual. | Automatizar mediante celda robotizada de carga y descarga. |
| **Torneado y fresado** | Variabilidad por habilidad del operario. | Implementar control numérico e integración con PLC. |
| **Transporte de piezas** | Movimientos manuales entre estaciones. | Incorporar banda transportadora sincronizada con robot. |
| **Trazabilidad y control** | Sin registro digital de datos. | Integrar SCADA e IoT para monitoreo y registro en tiempo real. |




• Layout (distribución de planta actual)

[![layout-Actual.jpg](https://i.postimg.cc/kGSQGFpP/layout-Actual.jpg)](https://postimg.cc/CnFB6D0c)


• Diagrama de Espagueti (flujo físico de materiales)

[![diagram-Espagueti.jpg](https://i.postimg.cc/wvyJ4QHN/diagram-Espagueti.jpg)](https://postimg.cc/wyz77J1x)


• Diagrama VSM (Value Stream Mapping) antes de automatizar.

[![Copia-de-VSM-actual-2.png](https://i.postimg.cc/XvJ7HqTF/Copia-de-VSM-actual-2.png)](https://postimg.cc/cvpS6x14)

• Presentar indicadores y parámetros que se puedan reportar para fabricar un lote de 500 motorreductores por mes.
(Takt, Tc, Tsu, Rp, MLT).


# Análisis de tiempos y capacidad productiva

## Supuestos (explícitos — importantes)

- **Jornada laboral:**  
  1 turno × 8 h/día × 5 días = **40 h/semana = 2 400 min/semana** (por recurso/máquina).

- **Tiempos por operación:**  
  Basados en los valores (en minutos por pieza).  
  Los tiempos en rojo/alto fueron tomados directamente:  
  - Pintado = 180  
  - Templado (espera sinfín) = 150  
  - Hobbing = 120  
  - Rectificados (tornillo / corona) = 100  
  - Mecanizado de caras = 60  

- **Operaciones comunes agrupadas:**  
  Incluyen preparación de blanks, torneado, fresado de chavetero, taladrado, inspecciones, transportes internos y ensamblajes.  
  Total = **365 min** (incluye pintado de carcasas).

### Operaciones específicas por tipo

| Tipo               | Operaciones específicas (min) | Total específico | Observaciones                        |
|--------------------|------------------------------:|-----------------:|--------------------------------------|
| Sinfín - Corona    | Fresado helicoidal 20 + Rectificado tornillo 100 + Transporte 40 | +160 | Incluye espera de templado (150 min/carga) |
| Helicoidal / Cónico| Hobbing 120 + Rectificado corona 100 + Inspección 20 | +240 | — |

- **Setup (Tsu):** 30 min por cambio de lote  
- **Downtime:** 10% (escenario alternativo para capacidad)

---

## 1. Takt time

**Demanda semanal:** 125 unidades  
**Tiempo disponible por puesto:** 2 400 min


![equation](https://latex.codecogs.com/svg.image?\bg{black}\color{white}Takt=\frac{2400}{125}=19.20\text{min/u})


**Interpretación:**  
Para cumplir la demanda con un solo puesto, cada **19,2 min** debe salir una unidad.

---

## 2. Cycle time (Tc) — tiempo activo por unidad

- **Bloque común:** 365 min  

![eq1](https://latex.codecogs.com/svg.image?\bg{white}\color{white}Tc_{\text{sinfin}}=365+160=525\text{min/u})

![eq2](https://latex.codecogs.com/svg.image?\bg{white}\color{white}Tc_{\text{helicoidal}}=365+240=605\text{min/u})

![eq3](https://latex.codecogs.com/svg.image?\bg{white}\color{white}Tc_{\text{conico}}=605\text{min/u})

**Promedio ponderado (mix 45/40/40):**

![equation](https://latex.codecogs.com/svg.image?\bg{black}\color{white}Tc_{avg}=\frac{45(525)&plus;40(605)&plus;40(605)}{125}=576.2\text{min/u}\;(\approx&space;9.6&space;h/u))

**Interpretación:**  
El alto Tc refleja operaciones largas por lote (pintado, hobbing, rectificado), sin paralelización.

---

## 3. Setup time (Tsu)

Asumiendo **30 min por cambio de lote**:

![equation](https://latex.codecogs.com/svg.image?\bg{black}\color{white}Tsu_{\text{por&space;unidad}}=\frac{30}{\text{tamano&space;del&space;lote}})

| Tipo        | Lote | Tsu (min/u) |
|--------------|------|-------------|
| Sinfín       | 45   | 0.67        |
| Helicoidal   | 40   | 0.75        |
| Cónico       | 40   | 0.75        |

Más lotes por semana ⇒ mayor costo de setup por unidad.  
Implementar **SMED** reduciría este tiempo y mejoraría el rendimiento.

---

## 4. Manufacturing Lead Time (MLT)

Incluye tiempos de espera (templado), transporte y procesamiento.

![equation](https://latex.codecogs.com/svg.image?\bg{black}\color{white}MLT_{\text{sinf&space;n}}=Tc_{\text{sinf&space;n}}&plus;150=525&plus;150=675\text{min}\;(\approx&space;11h&space;15min))

![equation](https://latex.codecogs.com/svg.image?\bg{black}\color{white}MLT_{\text{helicoidal}}=Tc_{\text{helicoidal}}=605\text{min}\;(\approx&space;10h&space;5min))

![MLT conico](https://latex.codecogs.com/svg.image?\bg{black}\color{white}MLT_{conico}=605\text{min})



**Interpretación:**  
Los MLT son elevados (10–11 h/unidad) debido a operaciones largas y en lote.

---

## 5. Rendimiento / Capacidad (Rp) y máquinas necesarias

**Disponibilidad:** 2 400 min/semana por máquina.  
**Capacidad por máquina = 2 400 / Tc_tipo**

### Sin downtime:

| Tipo | Tc (min/u) | Capacidad (u/sem/máquina) |
|------|-------------|----------------------------|
| Sinfín | 525 | 4.57 |
| Helicoidal | 605 | 3.97 |
| Cónico | 605 | 3.97 |

### Con 10% downtime (2 160 min útiles):

| Tipo | Tc (min/u) | Capacidad (u/sem/máquina) |
|------|-------------|----------------------------|
| Sinfín | 525 | 4.26 |
| Helicoidal | 605 | 3.57 |
| Cónico | 605 | 3.57 |

### Máquinas necesarias para cubrir la demanda semanal

| Tipo | Demanda | Capacidad sin DT | Máquinas sin DT | Capacidad con DT | Máquinas con DT |
|------|----------|------------------|------------------|------------------|------------------|
| Sinfín | 45 | 4.57 | 10 | 4.26 | 11 |
| Helicoidal | 40 | 3.97 | 11 | 3.57 | 12 |
| Cónico | 40 | 3.97 | 11 | 3.57 | 12 |

**Interpretación:**  
Con una máquina que realice todo el proceso secuencial, se cubriría solo entre **3–5 unidades/semana**, es decir, **~10% de la demanda**.

![equation](https://latex.codecogs.com/svg.image?\bg{black}\color{white}Rp=\frac{\text{Capacidad&space;por&space;m&space;quina}}{\text{Demanda}}\times&space;100&space;)

Ejemplo (sinfín):

![equation](https://latex.codecogs.com/svg.image?\bg{black}\color{white}Rp=\frac{\text{Capacidad&space;por&space;m&space;quina}}{\text{Demanda}}\times&space;100&space;Rp=\frac{4.57}{45}\times&space;100\approx&space;10.2\%)

---

## 6. Conclusión

- **Takt requerido:** 19.2 min/u  
- **Tc medio actual:** 576.2 min/u  
  ⇒ **El proceso actual es mucho más lento que el takt.**

Para cumplir la demanda semanal (125 u/semana) en un turno, se requerirían:
- **10–12 máquinas por tipo**, o  
- **Reducción drástica de tiempos críticos** (pintado, hobbing, rectificado, templado), o  
- **Paralelización / subcontratación de procesos largos**.

**Conclusión general:**  
Con los tiempos actuales y un solo recurso por tipo, **no es factible** cumplir la demanda semanal sin aumentar significativamente la capacidad o mejorar la eficiencia de los procesos.


• Diagrama VSM (Value Stream Mapping) despues de automatizar.

[![VSM-actual-1.png](https://i.postimg.cc/PrTLbXrx/VSM-actual-1.png)](https://postimg.cc/jC3dtrf0)

• Análisis con el software de simulación de planta en donde se incorporen aspectos de fallas de equipos,
disponibilidad, calidad, set-up, tiempos de producción, balance de líneas, colas, determinación de OEE, aplicación
de estrategias de pre- automatización.

