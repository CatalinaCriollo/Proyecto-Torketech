# Evaluación Económica del proyecto

## Presupuesto de Adquisiciones – Evaluación de Proyectos (APM)

El presente presupuesto compila todas las adquisiciones necesarias para la implementación del sistema automatizado de fabricación de motorreductores, considerando los costos iniciales (CAPEX), los costos operativos anuales (OPEX) y las proyecciones financieras para 10 años. 
Todos los datos y calculos necesarios estan en el excel Lista de gastos.
### 1. Criterios Financieros Utilizados

Para garantizar consistencia y comparabilidad, se definieron los siguientes parámetros macroeconómicos:

- Tasa impositiva: 35%

- Gradiente de crecimiento de ingresos: 4% anual

- Inflación: 3.5%

- Costo de la deuda: 20%

- Participación de deuda: 30% del CAPEX

- Tasa de rechazo (yield perdida): 5%

- Horizonte de evaluación: 10 años


### 2. Presupuesto de Adquisiciones (CAPEX – Año Cero)

A continuación, se resumen los costos asociados a los componentes y equipos necesarios para la implementación de la celda robotizada y la línea de fabricación:

**2.1 Celda Robotizada**

Incluye el robot ABB IRB 1600 con su controlador IRC5, cercado industrial, gripper neumático, compresor, paros de emergencia, tablero eléctrico y sistemas de seguridad.

Total estimado: $137.050.000 COP

**2.2 Sistema de Pintado / Movimiento Lineal**

Incluye rieles lineales, bases giratorias, pistolas de pintura, conexiones y soportes estructurales.

Total estimado: $10.400.000 COP

**2.3 Sistema de Control Industrial**

Se contemplan PLC, módulos de E/S, HMI, comunicación Ethernet/IP, cableado, gabinetes y fuente de poder.

Total estimado: $22.300.000 COP

**2.4 Maquinaria para Mecanizado**

Incluye dos talladoras y una rectificadora industrial para engranajes.

Total estimado: $110.000.000 COP

**2.5 Sensores y Actuadores**

Incluye cilindros neumáticos, sensores ultrasónicos, válvulas y actuadores requeridos.

Total estimado: $2.880.000 COP

**2.6 Mecanismo de Banda Transportadora**

Compuesto por banda transportadora industrial de 70 metros y su variador de velocidad.

Total estimado: $85.000.000 COP

**2.7 Software Industrial**

Incluye licencias de: Siemens Tecnomatix, Studio 5000 Logix Designer, NX Mechatronics, Ignition Maker + Azure, RobotStudio, RSLinx Classic

Total estimado: $54.130.000 COP

#### TOTAL CAPEX (Año 0): $ 490.760.000,00 COP

### 3. Costos Operativos Anuales (OPEX)

Se consideran todos los gastos recurrentes asociados a operación, mantenimiento y administración:

**3.1 Mano de Obra Operativa***

Incluye técnicos, operadores, almacenamiento, programación, mantenimiento y soporte mecánico.

Total anual: $348.000.000 COP

**3.2 Costos Energéticos y Servicios**

- Energía eléctrica → $65.700.000

- Servicios (agua, internet, otros) → $114.000.000

. Seguro industrial → $30.000.000

**3.3 Arrendamiento**

Basado en una bodega industrial entre 800–1000 m² en parque industrial. Arrendamiento anual: $300.000.000 COP

**3.4 Mantenimiento**

Incluye mantenimiento preventivo y correctivo semestral para maquinaria, robot, banda y sistema neumático.
Total anual: $11.000.000 COP

**3.5 Administración**

Costos de nómina administrativa y soporte operativo.
Total anual: $261.000.000 COP

### 4. Producción, Costos Variables e Ingresos

Se proyecta la fabricación mensual de tres tipos de motorreductores:

| Tipo                   | Unidades/mes | Precio unitario |
| :--------------------- | :----------: | --------------: |
| Sin fin–corona        |     160      |     $1.980.000  |
| Engranajes cónicos    |     160      |     $1.650.000  |
| Engranajes helicoidales |   180      |     $2.920.000  |


## Flujo de Caja

El siguiente flujo de caja resume el comportamiento económico del proyecto durante un horizonte de 10 años, incorporando ingresos, costos operativos, depreciación, impuestos, inversiones iniciales (CAPEX) y el efecto de la financiación mediante deuda.

| Concepto                         | Año 0            | Año 1              | Año 2              | Año 3              | Año 4              | Año 5              | Año 6              | Año 7              | Año 8              | Año 9              | Año 10             |
|----------------------------------|------------------|--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|
| **INGRESOS**                    | $0               | $13,276,800,000    | $13,807,872,000    | $14,360,186,880    | $14,934,594,355    | $15,531,978,129    | $16,153,257,255    | $16,799,387,545    | $17,471,363,047    | $18,170,217,568    | $18,897,026,271    |
| **Costos**                      | $0               | $12,357,878,400    | $12,790,404,144    | $13,238,068,289    | $13,701,400,679    | $14,180,949,703    | $14,677,282,943    | $15,190,987,846    | $15,722,672,420    | $16,272,965,955    | $16,842,519,763    |
| **Utilidad Bruta**              | $0               | $918,921,600       | $1,017,467,856     | $1,122,118,591     | $1,233,193,676     | $1,351,028,426     | $1,475,974,312     | $1,608,399,699     | $1,748,690,626     | $1,897,251,614     | $2,054,506,508     |
| **Gastos administrativos**      | $0               | $899,832,000       | $931,326,120       | $963,922,534       | $997,659,823       | $1,032,577,917     | $1,068,718,144     | $1,106,123,279     | $1,144,837,594     | $1,184,906,909     | $1,226,378,651     |
| **EBITDA**                      | $0               | $19,089,600        | $86,141,736        | $158,196,057       | $235,533,853       | $318,450,510       | $407,256,168       | $502,276,420       | $603,853,033       | $712,344,704       | $828,127,857       |
| **Depreciación**                | $0               | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        |
| **Utilidad Operacional (EBIT)** | $0               | -$29,986,400       | $37,065,736        | $109,120,057       | $186,457,853       | $269,374,510       | $358,180,168       | $453,200,420       | $554,777,033       | $663,268,704       | $779,051,857       |
| **Intereses**                   | —                | —                  | —                  | —                  | —                  | —                  | —                  | —                  | —                  | —                  | —                  |
| **EBT**                         | $0               | -$29,986,400       | $37,065,736        | $109,120,057       | $186,457,853       | $269,374,510       | $358,180,168       | $453,200,420       | $554,777,033       | $663,268,704       | $779,051,857       |
| **Impuestos**                   | $0               | -$10,495,240       | $12,973,008        | $38,192,020        | $65,260,249        | $94,281,078        | $125,363,059       | $158,620,147       | $194,171,962       | $232,144,046       | $272,668,150       |
| **Utilidad Neta**               | $0               | -$19,491,160       | $24,092,728        | $70,928,037        | $121,197,605       | $175,093,431       | $232,817,109       | $294,580,273       | $360,605,071       | $431,124,658       | $506,383,707       |
| **Depreciación**                | $0               | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        | $49,076,000        |
| **Flujo Operativo**             | $0               | $29,584,840        | $73,168,728        | $120,004,037       | $170,273,605       | $224,169,431       | $281,893,109       | $343,656,273       | $409,681,071       | $480,200,658       | $555,459,707       |
| **CAPEX**                       | $490,760,000     | —                  | —                  | —                  | —                  | —                  | —                  | —                  | —                  | —                  | —                  |
| **Flujo de Caja Libre**         | -$490,760,000    | $29,584,840        | $73,168,728        | $120,004,037       | $170,273,605       | $224,169,431       | $281,893,109       | $343,656,273       | $409,681,071       | $480,200,658       | $555,459,707       |
| **Flujo Acumulado**             | -$490,760,000    | -$461,175,160      | -$388,006,432      | -$268,002,395      | -$97,728,790       | $126,440,641       | $408,333,751       | $751,990,024       | $1,161,671,095     | $1,641,871,753     | $2,197,331,460     |


### Indicadores Financieros del Proyecto (sin deuda)

- TIR: 30%
- Costo de capital (Ke): 15.81%
- VPN: $491.738.580 COP
- ROI: 18.26%
- Payback: 4.77 años

## Flujo de Caja del Inversionista (con deuda)

Se considera un financiamiento del 30% de la inversión inicial, con un costo de deuda del 20% anual.

Se incorporan: Intereses después de impuestos, Pago de capital anual, Servicio de la deuda

| Concepto                         | Año 0             | Año 1             | Año 2             | Año 3             | Año 4             | Año 5             | Año 6             | Año 7             | Año 8             | Año 9             | Año 10            |
|----------------------------------|-------------------|-------------------|-------------------|-------------------|-------------------|-------------------|-------------------|-------------------|-------------------|-------------------|-------------------|
| **Intereses · (1 – tx)**        | $0,00             | $29.445.600,00    | $28.311.274,31    | $26.950.083,48    | $25.316.654,49    | $23.356.539,70    | $21.004.401,94    | $18.181.836,64    | $14.794.758,28    | $10.730.264,25    | $5.852.871,41     |
| **Intereses descontados**       | $0,00             | $19.139.640,00    | $18.402.328,30    | $17.517.554,26    | $16.455.825,42    | $15.181.750,80    | $13.652.861,26    | $11.818.193,82    | $9.616.592,88     | $6.974.671,76     | $3.804.366,42     |
| **Pago de capital**             | $0,00             | $5.671.628,45     | $6.805.954,14     | $8.167.144,97     | $9.800.573,96     | $11.760.688,75    | $14.112.826,51    | $16.935.391,81    | $20.322.470,17    | $24.386.964,20    | $29.264.357,04    |
| **Capital inicial**             | $147.228.000,00   | —                 | —                 | —                 | —                 | —                 | —                 | —                 | —                 | —                 | —                 |
| **Flujo de caja del inversionista** | -$343.532.000,00 | $4.773.571,55     | $47.960.445,96    | $94.319.337,66    | $144.017.205,17   | $197.226.991,80   | $254.127.421,61   | $314.902.687,66   | $379.742.008,32   | $448.839.021,80   | $522.390.983,43   |
| **Flujo acumulado**             | —                 | -$338.758.428,45  | -$290.797.982,49  | -$196.478.644,83  | -$52.461.439,66   | $144.765.552,14   | $398.892.973,75   | $713.795.661,40   | $1.093.537.669,72 | $1.542.376.691,52 | $2.064.767.674,95 |


### Indicadores Financieros del Inversionista (con deuda)

- TIR apalancada: 34%
- Costo de capital: 15.81%
- VPN: $507.613.132 COP
- ROI: 14.26%
- Payback: 4.36 años

## Resultados

Los resultados financieros muestran que el proyecto es económicamente viable:

- La **TIR del proyecto (30%)** y la **TIR apalancada (34%)** son significativamente superiores al costo de capital (15,81%).  
- El **VPN positivo** en ambos casos indica creación de valor para los inversionistas.  
- El **periodo de recuperación** de la inversión se sitúa entre **4,3 y 4,8 años**, dentro del horizonte de evaluación de 10 años.


## Modelo de negocio. (Modelo Canva de propuesta de valor)

![](Imagenes/Canvadenegociomejor.png)

