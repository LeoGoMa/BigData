# Big Data — 5to Semestre

Repositorio único de la materia. Cada práctica es un proyecto independiente
dentro de su propia carpeta.

**Repositorio:** https://github.com/LeoGoMa/BigData

## Estructura

```
BigData/                          <- raíz del repositorio Git (único)
├── .gitignore                    <- ignora .venv, cache, etc. para toda la materia
├── README.md
└── 01_1_probabilidad_estadistica/
    ├── .venv/                    <- NO se sube a GitHub
    ├── data/raw/                 <- datasets originales
    ├── notebooks/
    ├── src/
    └── requirements.txt          <- dependencias de esta práctica
```

## Reglas

- Un solo repositorio Git y un solo repositorio GitHub para toda la materia.
- Cada práctica es un proyecto independiente con su propio `.venv`.
- El `.venv` **nunca** se sube a GitHub.
- Cada práctica tiene su propio `requirements.txt`.
- Para trabajar en una práctica se activa el `.venv` de esa práctica.
- Se puede abrir directamente la carpeta de una práctica en VS Code.
- **No** se vuelve a ejecutar `git init` para prácticas nuevas.

## Flujo para una práctica nueva

```bash
# 1. Crear la carpeta de la práctica dentro de BigData/
mkdir 02_nombre_practica && cd 02_nombre_practica

# 2. Crear y activar su entorno virtual
python -m venv .venv
.venv\Scripts\activate          # Windows

# 3. Instalar dependencias y congelarlas
pip install pandas numpy matplotlib
pip freeze > requirements.txt

# 4. Trabajar y versionar (desde cualquier subcarpeta)
git add .
git commit -m "Práctica 02: descripción"
git push
```

## Comandos útiles

```bash
git status                      # estado del repositorio
git rev-parse --show-toplevel   # ruta de la raíz del repositorio
git log --oneline --graph       # historial resumido en forma de grafo
```
