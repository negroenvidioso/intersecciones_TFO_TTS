# Filtrar GTF para Coordenadas de Genes

Este script en Python filtra un archivo GTF para obtener las coordenadas de genes específicos y formatear esta información para su visualización en el genome browser de la UCSC.

## Requisitos

- Python 3.x
- Módulos: `argparse`, `multiprocessing`

## Uso

### Argumentos

- `-q`, `--gtf`: Archivo GTF de entrada (requerido).
- `-i`, `--input`: Archivo de texto con la lista de genes a buscar (requerido).
- `-c`, `--cores`: Número de núcleos a utilizar (opcional, por defecto es 1).

### Ejemplo de Uso

```bash
python filtrar_gtf.py -q archivo.gtf -i genes.txt -c 4
```

## Descripción del Código

### Funciones

- `parse_gtf(gtf_file, genes_to_search)`: Lee un archivo GTF y busca genes específicos. Si encuentra un gen de interés, extrae y formatea la información relevante (ID del transcripto, cromosoma, inicio y fin) y la guarda en una lista.
- `read_genes_list(genes_file)`: Lee un archivo de texto que contiene una lista de genes y devuelve una lista de genes.

### Función Principal `main()`

1. Configura el analizador de argumentos para recibir el archivo GTF, el archivo de genes y el número de núcleos a utilizar.
2. Lee la lista de genes a buscar.
3. Utiliza un pool de procesos para ejecutar `parse_gtf` en paralelo.
4. Imprime los resultados obtenidos.

## Ejemplo de Archivos

### genes.txt

```
BRCA1
TP53
EGFR
```

### Salida Esperada

```
ENST00000357654    chr17:43044295-43125482
ENST00000269305    chr17:43124095-43125482
ENST00000380152    chr7:55086714-55279321
```

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o envía un pull request para discutir cualquier cambio.
