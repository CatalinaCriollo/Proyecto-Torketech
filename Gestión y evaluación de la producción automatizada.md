• Diagrama de operaciones de proceso.

El siguiente DOP toma en cuenta todas las operaciones que se deben cumplir en la fabricación de un motoreductor fabricado en la empresa RAMFÉ. Cabe remarcar que como se ve en la figura el total de tiempo acumulado en todas estas operaciones da un resultado de 750 minutos por pieza, sin embargo esta cantidad de minutos no contempla el número de máquinas que se deispone para hacer la misma operación ni tampoco si algunas de estas labores se fabrican en paralelo. Este análisis se realizará posteriormente evaluando primero los procesos que se realizan en paralelo o incluso 

[![operaciones2-3.png](https://i.postimg.cc/cLHYnXkZ/operaciones2-3.png)](https://postimg.cc/xcwcrySF)

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




• Diagrama de análisis de proceso.

• Layout (distribución de planta actual)

• Diagrama de Espagueti (flujo físico de materiales)

• Realizar una estimación preliminar de los tiempos en cada etapa de proceso para poder incorporar estos valores
en los diagramas de análisis de proceso y VSM.

• Diagrama VSM (Value Stream Mapping) antes de automatizar.

• Presentar indicadores y parámetros que se puedan reportar para fabricar un lote de 500 motorreductores por mes.
(Takt, Tc, Tsu, Rp, MLT).

• Análisis con el software de simulación de planta en donde se incorporen aspectos de fallas de equipos,
disponibilidad, calidad, set-up, tiempos de producción, balance de líneas, colas, determinación de OEE, aplicación
de estrategias de pre- automatización.
• Diagrama VSM (Value Stream Mapping) despues de automatizar.
