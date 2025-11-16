# lABORATORIO_Variabilidad-de-la-Frecuencia-Card-aca-HRV-y-balance-auton-mico

## OBJETIVOS:
Identificar cambios en el balance autonómico mediante análisis temporal de la variabilidad de la frecuencia cardíaca (HRV).

#PARTE A.

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

 -SD1/SD2:Índice de balance autonómico.
     Valores elevados → predominancia del vago.
     Valores bajos → Estrés o predominancia simpática.

Formas típicas del diagrama: Nube elíptica estrecha demuestra un HRV bajo, mientras que un elipse más redondeada y dispersa demuestra una alta HRV, y si se ven figuras irregulares muestra que hay arritmias o dinámica compleja.
     
- **Variabilidad de la frecuencia cardíaca (HRV) y balance autonómico**

  
- **Formulación del plan de acción para cumplir con el objetivo de la práctica y diagrama de flujo.**

## b. Adquisición de la señal ECG

Seleccionar a un sujeto de prueba para adquirir la señal electrocardiográfica;
grabar la señal ECG durante 4 minutos, de los cuales, el participante
permanecerá inmóvil y en silencio total durante los 2 primeros minutos, y
luego leerá en voz alta un pasaje de un texto seleccionado por el equipo
durante los dos últimos minutos.
Verificar que la frecuencia de muestreo y los niveles de cuantificación
establecidos sean los apropiados para este tipo de señal. 

# PARTE B

## c. Pre-procesamiento de la señal

-Aplicar los filtros digitales necesarios para eliminar el ruido de la señal,
demostrando su diseño.

 Diseñar un filtro IIR de acuerdo con los parámetros de la señal.

 Obtener la ecuación en diferencias del filtro.

 Implementar el filtro a la señal obtenida asumiendo parámetros
iniciales en 0.

-Dividir la señal filtrada en dos segmentos de señal con duración de 2 minutos
cada uno.

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




