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

- **Symlets:**  
  Reducen los artefactos al reconstruir una señal y logran mantener una buena localización en el tiempo y en frecuencia.  
  Permiten reconstruir de forma precisa las señales sin distorsión, siendo útiles para análisis donde se requiere alta fidelidad.

- **Coiflets:**  
  Presentan una alta regularidad y momentos nulos tanto en la función wavelet como en la función de escala.  
  Tienen mejor localización en tiempo y frecuencia que las Daubechies, lo que las hace ideales para analizar señales suaves con cambios graduales y caracterizar la forma de las ondas.

- **Morlet:**  
  Es una onda senoidal modulada por una función gaussiana.  
  Ofrece excelente resolución en frecuencia, aunque menor en tiempo.  
  Se usa principalmente para estudiar oscilaciones y eventos transitorios en señales, pero no para compresión, sino para análisis continuo.

- **Mexican Hat:**  
  Tiene forma acampanada y corresponde a la segunda derivada de una función gaussiana.  
  Es muy adecuada para detectar picos o eventos únicos en una señal, como transitorios o impulsos de corta duración.

- **Haar:**  
  Es la wavelet más simple, de forma cuadrada y discontinua.  
  Posee excelente localización temporal pero baja en frecuencia.  
  Se usa especialmente en señales digitales con saltos abruptos o cambios repentinos.

- **Meyer:**  
  Es una wavelet completamente suave e infinitamente diferenciable.  
  No tiene soporte compacto en el tiempo, pero sí en frecuencia, lo que permite una transición suave entre diferentes bandas de frecuencia.

- **Beylkin:**  
  Se utiliza en algoritmos de compresión y en la resolución matemática de ecuaciones integrales.  
  Su alto número de momentos nulos la hace ideal para representar funciones suaves, como las de campos electromagnéticos.

- **Battle-Lemarie:**  
  Se basa en funciones polinómicas por tramos, lo que le otorga continuidad y suavidad.  
  Presenta un buen balance entre localización temporal y frecuencia, siendo útil en aplicaciones donde se requiere una representación estable y continua.
  
Las wavelets más utilizadas en el análisis de señales fisiológicas (como **EEG, ECG y EMG**) son las Symlets, Coiflets, Morlet, Mexican Hat y Haar,  
ya que cada una posee características esenciales para la eliminación de ruido, análisis de frecuencias específicas y detección de patrones.  
Estas propiedades permiten un estudio más preciso y detallado del comportamiento de las señales biológicas.

  ![image](https://github.com/felipeacosta-m/Lab-5-VFC/blob/c16b326b690082e9ac2924843143b869dede6708/Mexican%20hat.jpg)

---

