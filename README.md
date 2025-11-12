# Lab-5-VFC

## Introducción

### Actividad simpática y parasimpática del sistema nervioso autónomo

**Sistema Nervioso Autónomo (SNA)**  
Es la parte funcional del sistema nervioso que se encarga de la regulación de las funciones viscerales involuntarias del organismo, mantiene la homeostasis y controla la presión arterial, la frecuencia cardiaca, entre otros. Se puede dividir funcionalmente en **simpático** y **parasimpático**:

- **Simpático:**  
  Es controlado por los nervios simpáticos y tiene su origen en la médula espinal. Se encarga de acelerar el ritmo cardiaco y llevar más sangre a las zonas del cuerpo donde se necesita más oxígeno. Afecta al sistema inmunitario y la reparación del cuerpo.  
  En resumen, el sistema nervioso simpático transmite señales de alerta al cuerpo.

- **Parasimpático:**  
  Se encarga de relajar el cuerpo tras periodos de estrés o peligro. Ayuda a ejecutar procesos vitales como la digestión y los momentos de relajación.  
  Permite controlar la frecuencia cardiaca, la sudoración, entre otros.

---

### Efecto de la actividad simpática y parasimpática en la frecuencia cardiaca

La **actividad simpática** normalmente **aumenta la frecuencia cardiaca**, la fuerza de las contracciones del músculo cardiaco y dilata las vías respiratorias para mejorar la respiración.  
Cuando la rama simpática está más activa, la frecuencia cardíaca suele aumentar y late a un ritmo más regular, **reduciendo la variabilidad de la frecuencia**.

Por otra parte, el **sistema parasimpático** **reduce la frecuencia cardiaca** y la fuerza de contracción del corazón (vasoconstricción) para relajar el sistema del cuerpo.  
La rama parasimpática aumenta la variabilidad de la frecuencia en las altas frecuencias.

---

### Variabilidad de la frecuencia cardiaca (HRV)

La **HRV (Heart Rate Variability)** es la variación en el tiempo de los latidos consecutivos, es decir, del intervalo **R–R** en un ECG.  
El corazón se controla por medio del SNA, por lo tanto:

- Cuando la rama **parasimpática** está más activa → la HRV **aumenta**.  
- Cuando se activa la rama **simpática** → la HRV **disminuye**.

La HRV es un **indicador del equilibrio** entre las dos ramas del sistema nervioso autónomo y una **medida indirecta del estrés** (mayor HRV indica menor estrés).

El análisis de HRV se realiza a partir de una serie de intervalos R–R registrados durante un periodo mínimo de 5 minutos, evaluando cómo cambian estos valores de un latido al siguiente.

#### Bandas de frecuencia en el análisis de HRV:

| Banda | Rango (Hz) | Asociación |
|-------|-------------|------------|
| Alta frecuencia (HF) | 0.15 – 0.40 | Parasimpático |
| Baja frecuencia (LF) | 0.04 – 0.15 | Mezcla simpático-parasimpático |
| Muy baja frecuencia (VLF) | 0.003 – 0.04 | Equilibrio autónomo (LF/HF) |

---

### Transformada Wavelet: definición, usos y tipos en señales biológicas

La **Transformada Wavelet** es una herramienta matemática que permite representar señales en función del **tiempo y la frecuencia** simultáneamente.  
Se usa ampliamente en el **procesamiento de señales biológicas** y la **detección de anomalías médicas**, ya que permite analizar señales **no estacionarias** (que cambian en el tiempo).

A diferencia de la Transformada de Fourier (que da solo información global de frecuencia), la Wavelet permite identificar **cuándo ocurren los cambios de frecuencia**.

#### Tipos de Transformada Wavelet:

- **Transformada Wavelet Discreta (DWT):**  
  Se usa para descomponer la señal en diferentes escalas y eliminar el ruido.

- **Transformada Wavelet Continua (CWT):**  
  Permite obtener una visión más detallada de la señal, ideal para estudiar la variación de la frecuencia a lo largo del tiempo en señales fisiológicas.

#### Tipo de Wavelet utilizada:

- **Daubechies:**  
  Se caracteriza por su gran compactación del soporte y su capacidad para detectar **cambios bruscos o discontinuidades** en una señal.  
  Es esencial para eliminar el ruido y analizar datos biológicos con precisión.

---

