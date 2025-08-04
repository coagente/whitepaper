FROM ubuntu:22.04

# Evitar prompts interactivos durante la instalación
ENV DEBIAN_FRONTEND=noninteractive

# Actualizar e instalar TeXLive básico
RUN apt-get update && \
    apt-get install -y \
    texlive-latex-base \
    texlive-fonts-recommended \
    texlive-fonts-extra \
    texlive-latex-extra \
    && rm -rf /var/lib/apt/lists/*

# Crear directorio de trabajo
WORKDIR /work

# Crear directorios necesarios
RUN mkdir -p /work/src /work/output

# Comando por defecto
CMD ["pdflatex", "--version"]