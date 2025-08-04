# LaTeX to PDF con Docker

Sistema simple para compilar archivos LaTeX a PDF usando Docker.

## Estructura

```
latex-docker/
├── docker-compose.yml   # Configuración de Docker Compose
├── Dockerfile          # Imagen con TeXLive
├── src/               # Archivos .tex fuente
│   └── hello.tex      # Ejemplo "Hola Mundo"
└── output/            # PDFs generados (volumen)
```

## Uso

1. **Compilar el PDF:**
   ```bash
   cd latex-docker
   docker compose up --build
   ```

2. El PDF generado estará en `output/hello.pdf`

## Personalización

- Coloca tus archivos `.tex` en el directorio `src/`
- Modifica el comando en `docker-compose.yml` para compilar diferentes archivos:
  ```yaml
  command: pdflatex -output-directory=/work/output /work/src/tu-archivo.tex
  ```

## Características

- ✅ Compilación automatizada con Docker
- ✅ Volúmenes para entrada/salida
- ✅ TeXLive completo con fuentes y paquetes extra
- ✅ Sin necesidad de instalar LaTeX localmente