# Proyecto1-Portfolio

Este será el repositorio designado para realizar el primer proyecto de FoxCoding. Este primer proyecto va a ser un portfolio web personal donde cada uno podrá ir mostrando su perfil profesional.

Cada quien va a realizar su portfolio entero dentro de una branch personal, es decir, este repositorio va a contener todos los portfolios.

El stack tecnológico que utilizaremos es: HTML, CSS, JS y React. 
<div style=" display: flex; width: fit-content; justify-content: left; align-items: center; gap: 30px; padding:20px 20px 20px 0px; background-color:white; border:4px solid yellow">
    <img src="assets/HTML.webp" alt="Logo de HTML"
         style="width: 150px; height: 150px; object-fit: contain;">
    <img src="assets/CSS.png" alt="Logo de CSS"
         style="width: 150px; height: 150px; object-fit: contain;">
    <img src="assets/JS.png" alt="Logo de JavaScript"
         style="width: 150px; height: 150px; object-fit: contain;">
    <img src="assets/REACT.webp" alt="Logo de JavaScript"
         style="width: 150px; height: 150px; object-fit: contain;">
</div>

*Cada quien puede investigar y personalizar su portfolio con otras tecnologías.*

# Guía de contribución

Cada integrante tendrá:

- Una carpeta personal dentro de `portfolios/`.
- Una branch permanente para trabajar.
- Un proyecto independiente de React.
- La responsabilidad de modificar únicamente su carpeta.

## Estructura del repositorio

```text
Proyecto1-portfolio/
├── portfolios/
│   ├── nombre-integrante1/
│   │   ├── Proyecto de React alumno 1/
│   ├── nombre-integrante2/
│   │   ├── Proyecto de React alumno 2/
│   └── ...
├── .gitignore
└── README.md
```

## Reglas generales

1. Trabajar siempre en la branch personal asignada.
2. Modificar solamente la carpeta personal correspondiente.
3. No modificar el portfolio de otro integrante.
4. Todos los cambios deben integrarse a `main` mediante un Pull Request.
5. Solo se debe tener un Pull Request abierto por integrante.
6. Antes de solicitar una revisión, el proyecto debe ejecutarse correctamente.

## Branch personal

Cada integrante tendrá una branch permanente con su nombre:

Ejemplos:

```text
/Derek Beltran
/Emilio Fernandez
/Ruben Yañez
```

Para cambiar a tu branch:

```bash
git switch /nombre
```

Verifica que estás en la branch correcta:

```bash
git branch
```

La branch actual aparecerá marcada con un asterisco:

```text
* /nombre
  main
```

## Preparar el proyecto

### Crear el proyecto de React

Este paso se realiza solamente la primera vez.

Primero, entra a tu carpeta personal:

```bash
cd portfolios/nombre
```

Cambia `nombre` por el nombre de tu carpeta asignada. Por ejemplo:

```bash
cd portfolios/Derek-Beltran
```

Crea el proyecto de React con Vite dentro de la carpeta actual:

```bash
npm create vite@latest . -- --template react
```

El punto `.` indica que el proyecto debe crearse dentro de la carpeta actual.

Instala las dependencias:

```bash
npm install
```

Ejecuta el proyecto:

```bash
npm run dev
```

Vite mostrará una dirección local similar a:

```text
http://localhost:5173/
```

Abre esa dirección en tu navegador para visualizar el proyecto.

Antes de subir tus cambios, verifica que el proyecto compile correctamente:

```bash
npm run build
```

> Si el proyecto de React ya existe dentro de tu carpeta, no vuelvas a ejecutar el comando de creación. Solamente ejecuta `npm install` y después `npm run dev`.

## Subir cambios

Primero, revisa los archivos modificados:

```bash
git status
```

Agrega únicamente tu carpeta:

```bash
git add portfolios/nombre/
```

Crea un commit con una descripción clara:

```bash
git commit -m "feat(nombre): agrega sección de proyectos"
```

Sube los cambios a tu branch:

```bash
git push origin /nombre
```

## Crear un Pull Request

Después de subir los cambios:

1. Abre el repositorio en GitHub.
2. Selecciona **Pull requests**.
3. Presiona **New pull request**.
4. Selecciona `main` como branch de destino.
5. Selecciona tu branch personal como branch de origen.
6. Escribe un título que explique el cambio.
7. Describe brevemente lo que realizaste.
8. Solicita la revisión del coordinador.
9. No elimines tu branch después del merge.

La comparación debe verse de esta manera:

```text
base: main ← compare: /nombre
```

## Formato de los commits

Utiliza mensajes breves y descriptivos:

```text
tipo: descripción
```

Tipos recomendados:

| Tipo | Uso |
|---|---|
| `feat` | Agregar una funcionalidad |
| `fix` | Corregir un error |
| `style` | Cambiar estilos o diseño |
| `refactor` | Mejorar código sin cambiar su función |

Ejemplos:

```text
feat: agrega sección de experiencia
style: mejora diseño responsive
fix: corrige enlaces de navegación
docs: actualiza información personal
```

## Actualizar la branch después de un merge

Después de que un Pull Request sea aceptado, actualiza tu branch personal con los cambios más recientes de `main`:

```bash
git switch /nombre
git fetch origin
git merge origin/main
git push origin /nombre
```

Si aparece un conflicto, no borres archivos ni uses comandos desconocidos. Solicita ayuda a un coordinador.

## Un Pull Request será rechazado si

- Modifica la carpeta de otro integrante.
- Modifica archivos generales sin autorización.
- El proyecto no ejecuta o no compila.
- Contiene archivos que no corresponden al cambio.
- Se creó desde una branch que no pertenece al integrante.
