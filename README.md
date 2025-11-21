# lABORATORIO_Variabilidad-de-la-Frecuencia-Card-aca-HRV-y-balance-auton-mico

## OBJETIVOS:
Identificar cambios en el balance autonómico mediante análisis temporal de la variabilidad de la frecuencia cardíaca (HRV).

# PARTE A.

## a. Fundamento teórico

Antes de iniciar la práctica, los estudiantes deberán realizar una investigación teórica que incluya los siguientes temas:

- **Actividad simpática y parasimpática del sistema nervioso autónomo.**
  El sistema nervioso autónomo se divide en 3, sin embargo hablaremos de los mas importante el simpatico y el parasimaptico, el sistema nervios simpatico prepara el cuerpo para la lucha o huida ya que aumenta la frecuencia cardiac y la presión arterial, por el contrario el parasimpático es del descanso y digestión ezste busca la recuperación y calma, el simpático Usa principalmente el neurotansmisor norepinefrina (fibras adrenérgicas), mientras el parasimpático usa principalmente acetilcolina (fibras colinérgicas) para las neuronas preganglionares y posganglionares que activan los receptores muscarínicos.
  
- **Efecto de la actividad simpática y parasimpática en la frecuencia
cardíaca.**
El plexo cardíaco es la red nerviosa que inerva el corazón.  Esta red es alimentada por contribuciones que vienen de los nervios vagos, tanto el derecho como el izquierdo, además del tronco simpático.  Estos nervios regulan e impactan la frecuencia de los latidos del corazón, el gasto cardíaco y la fuerza con que se contrae el corazón.
  Simpático:
Segrega neurotransmisores como la norepinefrina, que se acoplan a los receptores cardíacos, lo que incrementa la entrada de calcio.
Elevar la frecuencia del corazón.
Incrementar la potencia de contracción del miocardio.
La reacción de "huida o lucha", que incrementa la frecuencia cardíaca.

  Parasimpático: La estimulación parasimpática de los receptores M2 en el corazón causa que la frecuencia del corazón y la velocidad de conducción a través del nodo AV se reduzcan.
Libera acetilcolina, que se une a los receptores muscarínicos, lo que disminuye la entrada de calcio en los cardiomiocitos y reduce el funcionamiento eléctrico.
Disminuye  la frecuencia cardíaca.
Disminuir la potencia de contracción del corazón.
Vasoconstricción (estrechamiento) de las arterias del corazón.


- **Variabilidad de la frecuencia cardíaca (HRV) obtenida a partir de la señal electrocardiográfica (ECG).**
  La variabilidad de la frecuencia cardiaca (HRV, por su sigla en inglés), son las oscilaciones en el intervalo de tiempo entre latidos cardíacos consecutivos (intervalos R-R) son representadas por la HRV.  Es un biomarcador del control autónomo del corazón y se relaciona con la salud física y mental.  Las métricas comunes abarcan:
 -Promedio de los intervalos R-R
 -Desviación estándar (SDNN)
 -RMSSD (raíz cuadrada de la media de las diferencias sucesivas)
 -pNN50 (porcentaje de pares de R-R cuya diferencia es mayor a 50 ms)
 Los componentes de frecuencia que son importantes para el estudio de la HRV son:
 -Frecuencia baja (LF, entre 0.04 y 0.15 Hz):  Conectada con la regulación parasimpática y simpática.
 -Alta frecuencia (HF, entre 0.15 y 0.4 Hz):  Principalmente vinculada con la actividad parasimpática.

  Para calcular el HVR a partir de un ECG, se debe seguir los siguientes pasos:
  1. Filtrar la señal de ECG esto para eliminar el ruido y la interferencia
  2. Detectar los picos R-R usando algoritmos en este caso wavelets pero se podrian usar Pab-Tompkins o umbrales adaptativos
  3. Calcular la serie de intervalos R-R excluyendo los latidos ectópicos
  4. Aplicar algunas metricas no lineales como el diagrama de Poincar


- **Diagrama de Poincaré como herramienta de análisis de la serie R-R.**
  El método no lineal para evaluar la HRV es el diagrama de Poincaré.  Se trata de graficar cada intervalo R-R(n) en relación con el siguiente, que es R-R(n+1).  Esta nube de puntos ilustra de manera visual la dinámica del nodo sinusal.
  
  <img width="469" height="477" alt="Figura-94-Diagrama-de-Poincare-de-una-serie-RR" src="https://github.com/user-attachments/assets/5bcd6d47-b5b6-4bf3-a60b-2db67ebc5e58" />
  
  Las principales ventajas que la Gráfica de Poincaré ofrece en comparación con los métodos tradicionales que se apoyan en parámetros estadísticos son:
  + Permite vizualizar aspectos no lineales de la secuencia de intervalos
  + Fácil visualizació de la variación entre latido
  + Fácil de calcular y un amplio uso
  + No requiere pre-procesos
  + Revela comportamientos dificiles de ver cuando se usan metodos estadísticos
  Interpretación de los parámetros clásicos

 Una elipse se adapta a la distribución de los puntos:

- SD1 (variabilidad en el corto plazo): Mitad de la desviación estándar en dirección perpendicular a la línea de identidad. Se relaciona sobre todo con la actividad parasimpática.

 - SD2 (variabilidad a largo plazo):Dispersión a lo largo de la línea de identidad. Muestra interacción entre el sistema simpático y el parasimpático.

 - SD1/SD2:Índice de balance autonómico.
     Valores elevados → predominancia del vago.
     Valores bajos → Estrés o predominancia simpática.

Formas típicas del diagrama: Nube elíptica estrecha demuestra un HRV bajo, mientras que un elipse más redondeada y dispersa demuestra una alta HRV, y si se ven figuras irregulares muestra que hay arritmias o dinámica compleja.
Una reducción significativa de HRV se asocia con estrés, sobreentrenamiento, diabetes, enfermedades cardíacas y riesgo arrítmico.
     
- **Variabilidad de la frecuencia cardíaca (HRV) y balance autonómico**
  Como vimos anteriormente el sistema nervioso autonomo controla el corazón mediante si es simpatico o parasimpático y la HVR es un indicador directo de este balance
  La metricas mas usadas
  Dominio del tiempo
     SDNN: variabilidad total → salud general del SNA.
     RMSSD: variabilidad de corto plazo → tono vagal.
     pNN50: % de diferencias sucesivas >50 ms → actividad parasimpática.

  Dominio de frecuencia
     LF (0.04–0.15 Hz): mezcla simpática + parasimpática.
     HF (0.15–0.40 Hz): actividad parasimpática.
     LF/HF: indicador del balance autonómico.

  
- **Formulación del plan de acción para cumplir con el objetivo de la práctica y diagrama de flujo.**
- <img width="1022" height="617" alt="image" src="https://github.com/user-attachments/assets/0133083a-1ade-4278-8734-15de608c3253" />


## b. Adquisición de la señal ECG

![Imagen de WhatsApp 2025-11-20 a las 20 01 50_be188a60](https://github.com/user-attachments/assets/7566e757-9e82-459b-81a3-3191abb2c864)

![Imagen de WhatsApp 2025-11-20 a las 20 08 08_56cd2656](https://github.com/user-attachments/assets/a2db78cb-d6ba-40ee-b8cb-e9af7e76c58b)



Seleccionar a un sujeto de prueba para adquirir la señal electrocardiográfica;
grabar la señal ECG durante 4 minutos, de los cuales, el participante
permanecerá inmóvil y en silencio total durante los 2 primeros minutos, y
luego leerá en voz alta un pasaje de un texto seleccionado por el equipo
durante los dos últimos minutos.
Verificar que la frecuencia de muestreo y los niveles de cuantificación
establecidos sean los apropiados para este tipo de señal. 

A continuación se anexa el codigo utilizado para la captura de la señal ECG del sujeto seleccionado:


```
import nidaqmx
from nidaqmx.constants import AcquisitionType
import numpy as np
import time
from nidaqmx.stream_readers import AnalogSingleChannelReader
from scipy.signal import filtfilt


rate = 1600  # Hz
duration = 240  # 4 minutos
save_data = []

task = nidaqmx.Task()
task.ai_channels.add_ai_voltage_chan("Dev5/ai0")
task.timing.cfg_samp_clk_timing(rate, sample_mode=AcquisitionType.CONTINUOUS)

reader = AnalogSingleChannelReader(task.in_stream)

samples_per_read = 1000  # tomador de varias muesstras en la pantalla para optimizar

start_time = time.time()

while time.time() - start_time < duration:
    data = np.zeros(samples_per_read)
    reader.read_many_sample(data, number_of_samples_per_channel=samples_per_read, timeout=5)
    save_data.extend(data)

task.close()

save_data = np.array(save_data)
np.savetxt(r"C:\Users\USUARIO\Desktop\lab 5\Datos4minutosBrayan.csv", save_data, delimiter=",")

print("Total muestras:", len(save_data))

```
Después de la captura de la señal ECG, en drive se adjunta el archivo csv de la señal Ecg del sujeto y se utliza el siguiente codigo para  graficar la señal capturada en google colab.

```
import pandas as pd
import matplotlib.pyplot as plt

file_path = "/content/drive/Shareddrives/Labs procesamiento de señales/Lab 5 este si /Datos4minutosBrayan.csv"
df = pd.read_csv(file_path)
print("Primeras filas del archivo:")
display(df.head())
columna_ecg = df.columns[-1]
print(f"Graficando columna: {columna_ecg}")

# === GRAFICAR LA SEÑAL ECG ===
plt.figure(figsize=(14,4))
plt.plot(df[columna_ecg]) # Changed columna_emg to columna_ecg
plt.title("Señal EcG")
plt.xlabel("Muestras")
plt.ylabel("Amplitud")
plt.grid(True)
plt.show()

```

obtiendo 

<img width="1424" height="482" alt="image" src="https://github.com/user-attachments/assets/220402cd-1ed6-4347-91c6-9c0a2ff224d3" />



A continuacion amplia la anterior grafica para poder observar de mejor forma la señal ECG capturada del sujeto seleccionado.

```
import pandas as pd
import matplotlib.pyplot as plt

file_path = "/content/drive/Shareddrives/Labs procesamiento de señales/Lab 5 este si /Datos4minutosBrayan.csv"  
df = pd.read_csv(file_path)
print("Primeras filas del archivo:")
display(df.head())
columna_ecg = df.columns[-1]   
print(f"Graficando columna: {columna_ecg}")
# === GRAFICAR LA SEÑAL EMG ===
plt.figure(figsize=(14,4))
plt.plot(df[columna_ecg])
plt.axis([10000,30000,0,5.0])
plt.title("Señal EMG")
plt.xlabel("Muestras")
plt.ylabel("Amplitud")
plt.grid(True)
plt.show()

```

<img width="1452" height="485" alt="image" src="https://github.com/user-attachments/assets/38ef6f05-38ac-4ae8-bab7-b542efcd6861" />



# Parte B

c. Pre-procesamiento de la señal 

 Aplicar los filtros digitales necesarios para eliminar el ruido de la señal,
demostrando su diseño.





 Diseñar un filtro IIR de acuerdo con los parámetros de la señal.

```
#FILTRO IIR LIBRO
import numpy as np 
from scipy import signal
import matplotlib.pyplot as plt
import sympy as sp
fs= 1600# hz
ts= 1/fs
hzp1= 0.05 # hz
hzp2= 200 # hz
hzs1= 0.01 # hz
hzs2= 400 #hz
k1= -3 #db
l2 =-15 #db
wp1= hzp1*2*np.pi/fs
wp2= hzp2*2*np.pi/fs
ws1= hzs1*2*np.pi/fs
ws2= hzs2*2*np.pi/fs
print(f"frecuencia pasante 1 :{wp1}")
print(f"frecuencia pasante 2 :{wp2}")
print(f"frecuencia de rechazo 1 :{ws1}")
print(f"frecuencia de rechazo 2 :{ws2}")
omegap1= (2/ts)*np.tan(wp1/2)
omegap2= (2/ts)*np.tan(wp2/2)
omegas1= (2/ts)*np.tan(ws1/2)
omegas2= (2/ts)*np.tan(ws2/2)
print(f"omega pasante 1 :{omegap1}")
print(f"omega pasante 2 :{omegap2}")
print(f"omega de rechazo 1 :{omegas1}")
print(f"omega de rechazo 2 :{omegas2}")
Bw= omegap2 - omegap1
#omega02= omegap1*omegap2
#omegalow= omegas1*omegas2
omega0= np.sqrt(omegap1*omegap2)
E2= 10**((-k1/10))-1
E=1 #aproximacion de la raiz deE2
print(f"E2 :{E2}")
Delta2cuadraro= 10**(l2/10)
print(f"delta2 :{Delta2cuadraro}")
Bw= omegap2 - omegap1
print(f"ancho de banda :{Bw}")
Delta1= np.sqrt((1/Delta2cuadraro)-1)
print(f"delta1 :{Delta1}")
omega_pasaaltos=1
omega02= omegap1*omegap2
print(f"omega02 :{omega02}")
omegas1LP= np.abs(((omegas1**2)-omega02)/(omegas1*Bw))
omegas2LP= np.abs(((omegas2**2)-omega02)/(omegas2*Bw))
print(f"omega de rechazo 1 LP :{omegas1LP}")
print(f"omega de rechazo 2 LP :{omegas2LP}")
BordePrototipo= min(omegas1LP, omegas2LP)
print(f"Borde prototipo :{BordePrototipo}")
reltrancision= BordePrototipo/omega_pasaaltos
print(f"relacion de transicion :{reltrancision}")
N= (np.log10(Delta1/E))/(np.log10(reltrancision))
N= int(np.ceil(N))

print(f"orden del filtro :{N} aproximado a 2")

```
Obteniendo 

<img width="541" height="406" alt="image" src="https://github.com/user-attachments/assets/be6c459f-a535-48f7-b17f-c93929d82314" />


 Obtener la ecuación en diferencias del filtro.

 Implementar el filtro a la señal obtenida asumiendo parámetros
iniciales en 0.

A continuación se anexa el codigo que se utilizo para filtarr la señal ECG capturada

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from scipy import signal

file_path = "/content/drive/Shareddrives/Labs procesamiento de señales/Lab 5 este si /Datos4minutosBrayan.csv"
df = pd.read_csv(file_path)
columna_ecg = df.columns[-1]
ecg = df[columna_ecg].values
b_bp = np.array([ 0.0086791 ,  0.01735821, -0.0086791 , -0.03471642,
                 -0.0086791 ,  0.01735821,  0.0086791 ])
a_bp = np.array([ 1.        , -4.05871114,  6.97438582, -6.56265079,
                  3.57080163, -1.05708974,  0.13326476])
ecg_filtrada = signal.lfilter(b_bp, a_bp, ecg)

plt.figure(figsize=(14,4))
plt.plot(ecg_filtrada)
plt.title("Señal ECG Filtrada (Pasa-Banda)")
plt.axis([0,380000,-3,3.0])
plt.xlabel("Muestras")
plt.ylabel("Amplitud")
plt.grid(True)
plt.show()

plt.figure(figsize=(14,4))
plt.plot(ecg_filtrada)
plt.title("Señal ECG Filtrada (Pasa-Banda)")
plt.axis([10000,30000,-3,3.0])
plt.xlabel("Muestras")
plt.ylabel("Amplitud")
plt.grid(True)
plt.show()
```

Obteniéndose

<img width="975" height="648" alt="image" src="https://github.com/user-attachments/assets/26a5821c-524b-4b8b-bde8-28af0d6e26e1" />


A continuación se adjuntan los filtros que se elaboraron 

Filtro Pasa Bajos 


```
import numpy as np
from scipy import signal
import matplotlib.pyplot as plt
import math

fs = 1600 # Hz. Frecuencia de muestreo [Fs]
N = 4
f_c = 200 # Hz
wn = f_c * 2 * np.pi

b_analog, a_analog = signal.iirfilter(
    N, 
    wn, 
    btype='lowpass', 
    analog=True, 
    ftype='butter'
)

print(" Coeficientes Analógicos H(s) ")
print(f"Numerador bs: {b_analog}")
print(f"Denominador as: {a_analog}\n")

# Transformada Bilineal 

b_digital, a_digital = signal.bilinear(b_analog, a_analog, fs)

filtz = signal.dlti(b_digital, a_digital)

print("--- Coeficientes Digitales H(z) ---")
print(f"Numerador b_z: {filtz.num}")
print(f"Denominador a_z: {filtz.den}\n")

```

Obteniendo 

<img width="839" height="201" alt="image" src="https://github.com/user-attachments/assets/71ad11ff-1bea-4e8a-a0c4-0e88bed85bd8" />

Filtro Pasa Altos

```
import numpy as np
from scipy import signal
import matplotlib.pyplot as plt
import math

fs = 1600
N = 4
f_c = 0.04
zeta = 1 
G = 1     
frad = f_c * 2 * np.pi 
nums = np.array([G, 0, 0]) 
dens = np.array([1, 2 * zeta * frad, frad * frad])
b_digital, a_digital = signal.bilinear(nums, dens, fs)
filtz = signal.dlti(b_digital, a_digital)
print(f"Numerador b_z: {filtz.num}") 
print(f"Denominador a_z: {filtz.den}")
```

Obteniendo 

<img width="593" height="59" alt="image" src="https://github.com/user-attachments/assets/cbf99bf9-a0b8-4cfb-a882-d2f05b0046ce" />

Filtro PASA banda obtenido del Pasa Altos * Pasa Banda

```
import numpy as np
import matplotlib.pyplot as plt
from scipy import signal

#Coeficientes del PASA-BAJOS
b_lp = np.array([0.00869615, 0.03478461, 0.05217692, 0.03478461, 0.00869615])
a_lp = np.array([1.0, -2.06263428, 1.86112855, -0.79314494, 0.13378912])

#Coeficientes del PASA-ALTOS
b_hp = np.array([ 0.99803939 ,-1.99607878 , 0.99803939])
a_hp = np.array([ 1.      ,   -1.99607686 , 0.99608071])

#Multiplicación de funciones
# H_total(z) = H_lp(z) * H_hp(z)
b_bp = np.convolve(b_lp, b_hp)
a_bp = np.convolve(a_lp, a_hp)

print("FILTRO PASA-BANDA RESULTANTE")
print("Numerador b_bp:", b_bp)
print("Denominador a_bp:", a_bp)
```

Obteniendo 

<img width="947" height="124" alt="image" src="https://github.com/user-attachments/assets/0f3a374b-a0c6-49ba-bedd-1260c71aa602" />


-Dividir la señal filtrada en dos segmentos de señal con duración de 2 minutos
cada uno.


<img width="1441" height="496" alt="image" src="https://github.com/user-attachments/assets/557c307a-5c1c-4d09-90c2-c9f77d15a1a6" />


<img width="1435" height="492" alt="image" src="https://github.com/user-attachments/assets/c7840304-558f-46a7-b942-efb7a79a9d34" />



-Identificar los picos R en cada uno de los segmentos, calcular los intervalos
R-R y obtener una nueva señal con dicha información. 

## d. Análisis de la HRV en el dominio del tiempo

- Comparar los valores de los parámetros básicos de la HRV en el dominio del
tiempo, como la media de los intervalos R-R y su desviación estándar, entre
ambos segmentos de señal ECG.

# PARTE C

## e. Construcción del diagrama de Poincaré

- Obtener el diagrama de Poincaré para cada segmento de señal ECG y comparar la dispersión de la nube de puntos que se obtuvo para cada caso.
- Calcular los valores de los índices tanto de actividad vagal (CVI) como de actividad simpática (CSI) que se obtienen a partir del diagrama de Poincaré. 

A continuación se anexa el codigo utilizado para obtener el diagráma de Poincaré

```
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import find_peaks

# Cargar archivo CSV
ruta = r"/content/drive/Shareddrives/Labs procesamiento de señales/Lab 5 este si /Datos4minutosBrayan.csv"
filtrado_final = np.loadtxt(ruta, delimiter=",")

# Frecuencia de muestreo del DAQ
fs = 1600
tiempo = np.arange(len(filtrado_final)) / fs

segment_duration_sec = 60
samples_per_segment = int(segment_duration_sec * fs)
n_segments = len(filtrado_final) // samples_per_segment

min_rr_sec = 0.25               # 250 ms mínimo fisiológico
min_distance = int(min_rr_sec * fs)

resultados = []                 # para guardar SD1, SD2, CVI, CSI
for seg in range(n_segments):

    start = seg * samples_per_segment
    end = start + samples_per_segment

    segmento = filtrado_final[start:end]
    tiempo_seg = tiempo[start:end]

    # Detección de picos R
    umbral = np.mean(segmento) + 0.4*np.std(segmento)
    prominencia = 0.3*np.std(segmento)

    picos, _ = find_peaks(
        segmento,
        distance=min_distance,
        height=umbral,
        prominence=prominencia
    )

    t_picos = tiempo_seg[picos]

    if len(t_picos) < 2:
        print(f"Segmento {seg+1}: insuficientes picos R.")
        continue

    #RR en milisegundos
    rr = np.diff(t_picos) * 1000    # ms

    # rr[n] y rr[n+1]
    rr_n = rr[:-1]
    rr_n1 = rr[1:]

    # Cálculo SD1 y SD2
    diff_rr = rr_n1 - rr_n
    var_diff = np.var(diff_rr, ddof=1)
    var_rr = np.var(rr, ddof=1)

    SD1 = np.sqrt(var_diff / 2)
    SD2 = np.sqrt(2 * var_rr - (var_diff / 2))

    # Cálculo CVI y CSI
    CVI = np.log10(SD1 * SD2)
    CSI = SD2 / SD1

    resultados.append((seg+1, SD1, SD2, CVI, CSI))

    # Diagrama de Poincaré
    plt.figure(figsize=(6,6))
    plt.scatter(rr_n, rr_n1, s=12)
    plt.plot([min(rr_n), max(rr_n)], [min(rr_n), max(rr_n)], '--', linewidth=1)
    plt.title(f"Poincaré Segmento {seg+1}\nSD1={SD1:.2f} ms  SD2={SD2:.2f} ms")
    plt.xlabel("RR(n) [ms]")
    plt.ylabel("RR(n+1) [ms]")
    plt.grid(True)
    plt.gca().set_aspect('equal')
    plt.show()


# Imprimir tabla de resultados
print("\n=== RESULTADOS PARTE C ===")
print("SEG |   SD1(ms)   |   SD2(ms)   |    CVI    |    CSI")
for r in resultados:
    print(f"{r[0]:>3} | {r[1]:>10.2f} | {r[2]:>10.2f} | {r[3]:>8.3f} | {r[4]:>8.3f}")
```

Obteniéndose

<img width="448" height="471" alt="image" src="https://github.com/user-attachments/assets/72bb0cdd-efdc-46ea-95d3-7ea96ab7bb9a" />

<img width="450" height="474" alt="image" src="https://github.com/user-attachments/assets/288d32fb-eb3c-464a-8230-4d3bdade9ef5" />

<img width="451" height="475" alt="image" src="https://github.com/user-attachments/assets/c076f372-1cf4-49ac-b7a2-18153f1b7214" />

<img width="441" height="467" alt="image" src="https://github.com/user-attachments/assets/c1113e08-56aa-4fb9-92d1-e2356b07a5e4" />

<img width="445" height="466" alt="image" src="https://github.com/user-attachments/assets/401d1ca8-ac56-45a6-815d-f83b6bbb9794" />

<img width="456" height="114" alt="image" src="https://github.com/user-attachments/assets/001ebd17-0488-4fe2-bcd6-dbfd6cc77cb7" />



El diagrama de Poincaré es una herramienta de análisis no lineal que contribuye a estudiar la variabilidad de la frecuencia cardíaca (HRV) mediante el análisis de la dispersión de los intervalos RR en un electrocardiograma. Para crearla, se grafica cada intervalo RR_n en comparación con RR_n+1, dando lugar a una nube de puntos que muestra el equilibrio entre las ramas simpática y parasimpática del sistema nervioso autónomo. Esta representación recoge las oscilaciones rápidas y lentas en la actividad del nodo sinusal, proporcionando datos que no se pueden obtener mediante análisis lineales.
En esta actividad, se dividió el ECG en cuatro segmentos de 60 segundos cada uno, los cuales representan intervalos tanto de reposo como de lectura en voz alta. Para cada segmento se generó el diagrama de Poincaré y se calcularon los índices que provienen de la elipse ajustada. CVI, CSI, SD1 y SD2. El índice SD1 evalúa la dispersión que es perpendicular a la diagonal de identidad; se vincula con la variabilidad a corto plazo, que está regulada en gran medida por el funcionamiento parasimpático. Por otro lado, el índice SD2 mide la dispersión en la diagonal y refleja la variabilidad a largo plazo, que está vinculada con la regulación general del sistema cardiovascular, donde intervienen los mecanismos parasimpáticos y simpáticos.
En suma, los diagramas de Poincaré y sus índices muestran con claridad cómo la modulación autonómica es afectada por las variaciones en la actividad. Mientras que la lectura genera una dispersión y variabilidad más amplias, los patrones durante el reposo son más estables. Esto muestra cómo interactúan dinámicamente los mecanismos simpáticos y parasimpáticos.



