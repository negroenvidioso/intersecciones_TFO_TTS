# Análisis de Interacciones TFO y TTS

Este proyecto utiliza Python para analizar y visualizar interacciones entre TFO (Triplex Forming Oligonucleotides) y TTS (Triplex Target Sites) a partir de un archivo de datos.

## Requisitos

- Python 3.x
- pandas
- matplotlib
- seaborn

Puedes instalar las bibliotecas necesarias utilizando pip:

```bash
pip install pandas matplotlib seaborn
```

## Uso

1. **Cargar el archivo de datos**: El archivo `triplex_RN7_noncoding_pretty.out` debe estar en el mismo directorio que el script. Este archivo debe estar separado por tabulaciones (`\t`).

2. **Filtrar los datos**: El script filtra las interacciones con una puntuación (`Score`) mayor o igual a 30 y una tasa de error (`Error-rate`) menor a 0.05.

3. **Generar el gráfico de dispersión**: El gráfico muestra las interacciones entre TFO y TTS, con:
   - `TFO start` en el eje x.
   - `TTS start` en el eje y.
   - `Score` como color (`hue`).
   - `Guanine-rate` como tamaño (`size`).
   - Paleta de colores `viridis`.

4. **Guardar el gráfico**: El gráfico se guarda como `interacciones_TFO_TSS.png` en el directorio actual.

## Ejecución

Para ejecutar el script, simplemente corre el siguiente comando en tu terminal:

```bash
python nombre_del_script.py
```

## Salida

El script generará un archivo de imagen `interacciones_TFO_TSS.png` en el directorio actual y mostrará un mensaje confirmando que la figura se ha guardado correctamente.

## Contacto

Si tienes alguna pregunta o sugerencia, no dudes en contactarme a través de allan.penaloza@ug.uchile.cl
