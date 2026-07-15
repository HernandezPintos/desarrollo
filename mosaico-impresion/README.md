# Mosaico de Impresión

Aplicación de escritorio para Linux Mint que compone una o varias imágenes en una grilla, permite previsualizar el resultado y lo exporta a PDF o lo envía al diálogo de impresión del sistema.

Versión actual: **1.0.0**.

## Funciones

- Repetir una única imagen en una grilla, por ejemplo 3 × 3.
- Combinar imágenes diferentes en la misma hoja.
- Repetir cíclicamente varias imágenes cuando hay más celdas que archivos.
- Distribuir automáticamente una colección en varias páginas.
- Elegir hojas A5, A4, A3, Carta, Legal, Oficio, Tabloide o un tamaño personalizado.
- Elegir orientación vertical u horizontal.
- Configurar entre 1 y 20 filas y columnas.
- Ajustar márgenes, separación, bordes y líneas de corte.
- Mostrar la imagen completa, rellenar recortando o estirar.
- Arrastrar imágenes desde Nemo o Nautilus.
- Exportar a PDF a 300 DPI.
- Imprimir mediante Qt y CUPS.
- Recordar preferencias de la interfaz entre ejecuciones.

## Requisitos

La instalación recomendada para Linux Mint usa los paquetes del sistema:

```bash
sudo apt install python3 python3-pyqt5 qt5-image-formats-plugins
```

## Instalación

```bash
git clone https://github.com/HernandezPintos/desarrollo.git
cd desarrollo/mosaico-impresion
chmod +x instalar.sh
./instalar.sh
```

El instalador copia la aplicación dentro del directorio personal del usuario y crea una entrada llamada **Mosaico de Impresión** en el menú de aplicaciones.

## Ejecución sin instalar

```bash
chmod +x ejecutar.sh
./ejecutar.sh
```

## Uso básico

1. Agregá una o varias imágenes.
2. Elegí el tamaño y la orientación de la hoja.
3. Definí filas y columnas, por ejemplo 3 × 3.
4. Elegí el modo de distribución:
   - **Repetir la primera imagen**.
   - **Usar imágenes en orden y repetir el ciclo**.
   - **Distribuir todas en una o varias páginas**.
5. Revisá la vista previa.
6. Exportá a PDF o imprimí.

## Desinstalación

```bash
./desinstalar.sh
```

## Estructura

```text
mosaico-impresion/
├── mosaico_impresion.py   # Aplicación PyQt5
├── mosaico-impresion.svg  # Icono
├── instalar.sh            # Instalación para el usuario actual
├── ejecutar.sh            # Ejecución portable
├── desinstalar.sh         # Limpieza de la instalación
├── requirements.txt       # Dependencia alternativa mediante pip
└── CHANGELOG.md
```

## Verificación realizada

- Compilación sintáctica con `python3 -m py_compile`.
- Validación sintáctica de los scripts con `bash -n`.
- Pruebas de composición con una imagen repetida y con varias imágenes.
- Revisión visual de la interfaz y de la salida renderizada.

La impresión física depende de la configuración local de CUPS y de la impresora disponible.

## Licencia

La licencia de reutilización todavía no fue definida. La publicación del código en GitHub no concede por sí sola permisos adicionales de copia, modificación o redistribución.
