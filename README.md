# apuntes-maquinas

Código fuente en LaTeX del libro **Máquinas sonoras: electrónicas y computacionales**, de Aarón Montoya Moraga y Matías Ignacio Serrano Acevedo.

El libro acompaña los cursos DIS8644 Taller de diseño de máquinas electrónicas y DIS8645 Taller de diseño de máquinas computacionales, de la Escuela de Diseño de la Facultad de Arquitectura, Arte y Diseño de la Universidad Diego Portales.

## Leer el libro

La versión más reciente se compila automáticamente con cada cambio en la rama `main` y se publica en:

<https://disenoudp.github.io/apuntes-maquinas/>

## Compilar

Se necesita una distribución de LaTeX con XeLaTeX y biber, por ejemplo TeX Live o MacTeX.

```sh
latexmk principal.tex
```

`latexmk` lee la configuración de `.latexmkrc`: compila con XeLaTeX, corre biber y makeindex, y repite hasta que las referencias se estabilizan. El resultado es `principal.pdf`. Para borrar los archivos intermedios se usa `latexmk -c`.

Cada capítulo es un subarchivo (paquete `subfiles`), así que también se puede compilar por separado desde su carpeta, por ejemplo `xelatex chip555.tex` dentro de `circuitos-integrados/`.

## Estructura

- `principal.tex`: documento principal, preámbulo y orden de los capítulos
- `info/`: prefacio, autores, cursos, herramientas y agradecimientos
- `maquinas/`: relojes, secuenciadores, osciladores, amplificadores, moduladores y filtros
- `electricidad/`: voltaje, corriente, potencia y fuentes de poder
- `componentes-basicos/`: placa de pruebas, cables, resistores, capacitores y diodos
- `interfaces/`: botones
- `circuitos-integrados/`: chips 555, 4017 y 4093
- `computacion/`: variables y funciones
- `ejemplos/`: proyectos completos, como el sintetizador Cuatro cuadradas
- `anexos/`: listas de álbumes, máquinas, organizaciones y personas
- `biblio.bib`: bibliografía
- `glosario.tex`: glosario y siglas
- `nostarch.cls`, `nostarch.ist`, `nshyper.sty`: clase de documento de No Starch Press
- `.github/workflows/compilar-pdf.yml`: compilación y publicación automática en GitHub Pages

## Licencia

Licencia MIT, ver [LICENSE](LICENSE).
