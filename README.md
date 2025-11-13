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
## Procedimiento 

Este laboratorio fue diseñado para analizar como varia la frecuencia cardiaca (HRV) por medio de la transformada de Wavelet, con el fin de identificar cambios en las frecuencias de la señal capturada y estudiar la variabilidad que tiene en el dominio del tiempo. Permitiendo evaluar como se encuentra el funcionamiento del sistema nervioso autónomo que se compone del sistema nervioso simpático y parasimpático, esto gracias a las fluctuaciones que se evidencien en los intervalos RR que se capten en el ECG.

---
## 1) Cálculos del filtro
Se optó por aplicar un filtro digital Butterworth de tipo pasa bajos debido a su característica principal: una respuesta en frecuencia suave, sin ondulaciones en la banda pasante. Esta propiedad resulta especialmente adecuada para mantener la forma original de la señal cardíaca, evitando distorsiones que podrían afectar su análisis.

La frecuencia de corte seleccionada fue de 250 Hz, lo que permite suprimir eficazmente componentes de alta frecuencia, como el ruido generado por la actividad muscular o las interferencias electromagnéticas, sin comprometer la información relevante del ECG.

Por otro lado, se eligió un filtro de orden 4, ya que proporciona una atenuación eficiente fuera de la banda útil sin comprometer la estabilidad numérica del sistema. Evitar órdenes más altos permite reducir el riesgo de inestabilidades o artefactos indeseados, alineándose con los objetivos del presente laboratorio.
```pyton
# ----------------------------
# 1) Cargar datos
# ----------------------------
from tkinter.filedialog import askopenfilename
file_path = askopenfilename(filetypes=[("Excel files", "*.xlsx")])

df = pd.read_excel(file_path)
t = df['Tiempo (s)'].to_numpy()
x = df['Señal'].to_numpy()

# ----------------------------
# 2) Filtro Butterworth pasa banda
# ----------------------------
fs = 250  # Hz
lowcut, highcut, order = 0.5, 40, 4
nyq = 0.5 * fs
b, a = butter(order, [lowcut/nyq, highcut/nyq], btype='band')

y = np.zeros_like(x)
for n in range(len(x)):
    for i in range(len(b)):
        if n - i >= 0:
            y[n] += b[i] * x[n - i]
    for j in range(1, len(a)):
        if n - j >= 0:
            y[n] -= a[j] * y[n - j]
```

## 2) Cálculo de la Frecuencia
Se seleccionó una frecuencia de corte de 250 Hz considerando tanto criterios fisiológicos como prácticos. Este valor permite conservar la información más relevante del ECG, especialmente los componentes de alta frecuencia del complejo QRS, que son fundamentales para la detección precisa de los picos R. Al mismo tiempo, es lo suficientemente bajo como para atenuar el ruido de alta frecuencia que suele estar presente en las señales biomédicas.

Para implementar el filtro digitalmente, esta frecuencia de corte fue normalizada respecto a la frecuencia de Nyquist, que en este caso es de 500 Hz (la mitad de la frecuencia de muestreo, 250 Hz). La normalización es necesaria ya que las funciones de diseño de filtros digitales trabajan en una escala de 0 a 1, donde 1 representa la frecuencia de Nyquist.

Este valor de 0.5 es el que se utiliza internamente en el diseño del filtro para establecer el punto de corte deseado.
## 3) Detección de Picos R
La detección de los picos R se realiza utilizando la función find_peaks() sobre la señal de ECG previamente filtrada. Para asegurar que solo se identifiquen los verdaderos picos R, se establecen criterios específicos como un umbral mínimo de amplitud y una separación mínima entre picos consecutivos. Esta etapa resulta clave, ya que los intervalos entre picos R constituyen la base para el análisis de la variabilidad de la frecuencia cardíaca (HRV), tanto en el dominio temporal como en el análisis mediante transformada wavelet.
```pyton
# ----------------------------
# 3) Detección de Picos R
# ----------------------------
picos, _ = find_peaks(y, height=0.5, distance=int(0.6 * fs))
tiempos_picos = t[picos]
```
## 4) Cálculo de Intervalos R-R
Los intervalos R-R se obtienen calculando la diferencia entre las posiciones de los picos R consecutivos, utilizando np.diff(picos). Posteriormente, estas diferencias se dividen por la frecuencia de muestreo (fs) para expresar el resultado en segundos. Estos intervalos reflejan el tiempo transcurrido entre latidos sucesivos y constituyen la base para el análisis de la variabilidad de la frecuencia cardíaca (HRV).

```pyton
# ----------------------------
# 4) Cálculo de Intervalos R-R
# ----------------------------
intervalos_rr = np.diff(tiempos_picos)
tiempos_rr = (tiempos_picos[:-1] + tiempos_picos[1:]) / 2
```
## 5) Variabilidad de la frecuencia cardiaca 
A partir de los intervalos RR extraídos, se calcularon varias métricas estándar para evaluar la variabilidad de la frecuencia cardíaca (HRV) en el dominio del tiempo. Se obtuvo el valor medio de los intervalos (rr_mean), el cual representa el ritmo cardíaco promedio durante el periodo de análisis.

La desviación estándar (sdnn) se utilizó como medida global de la variabilidad de los intervalos RR, mientras que el valor de rmssd se calculó para evaluar las diferencias cuadráticas medias entre intervalos sucesivos, lo cual refleja la actividad parasimpática a corto plazo.

Asimismo, se computaron las métricas nn50 y pnn50, que cuantifican cuántos pares de intervalos consecutivos difieren en más de 50 ms y qué porcentaje representan del total, respectivamente. Estas últimas también están relacionadas con el control parasimpático del corazón y son útiles para caracterizar cambios rápidos en el ritmo cardíaco.

Este conjunto de indicadores permite una caracterización inicial del comportamiento dinámico de la señal ECG, y sirve como base para la comparación entre sujetos sanos y aquellos con posibles disfunciones autonómicas.


```pyton
# ----------------------------
# 5) HRV en dominio del tiempo
# ----------------------------
print("\n--- HRV Dominio del tiempo ---")
print(f"Media RR: {intervalos_rr.mean():.4f} s   SDNN: {intervalos_rr.std():.4f} s")

plt.figure(figsize=(8, 4))
plt.hist(intervalos_rr, bins=30, color='skyblue', edgecolor='black')
plt.title('Histograma de Intervalos R-R')
plt.xlabel('RR (s)')
plt.ylabel('Frecuencia')
plt.grid(True)
plt.tight_layout()
plt.show()
```
## 6) Transformada Wavelet
Se utilizo la Transformada Wavelet Continua (CWT) utilizando la wavelet de Morlet para analizar la señal filtered_data. Se utiliza un rango de escalas (widths) de 1 a 49, y un parámetro w=5 que ajusta la forma de la wavelet Morlet. Posteriormente, se calcula la magnitud absoluta de la transformada (cwt_abs) y se suma a lo largo del eje de escalas para obtener un perfil de energía temporal (cwt_sum).
```pyton
# ----------------------------
# 7) Padding para SWT
# ----------------------------
desired_levels = 4
base = 2**desired_levels
L0 = len(rr_interpolados)
Lpad = ((L0 - 1)//base + 1)*base

pad_width = Lpad - L0
rr_pad = np.pad(rr_interpolados, (0, pad_width), 'edge')
t_pad  = np.pad(
    tiempo_interp,
    (0, pad_width),
    mode='linear_ramp',
    end_values=(tiempo_interp[-1],
                tiempo_interp[-1] + pad_width*(1/fs_interp))
)
```
