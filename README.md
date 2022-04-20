# React Folders Structure

ReactJS application with intermediate folder structure. Here is a full article where i explain all folders and their roles.

```
src/
├─ assets/
│  ├─ fonts/
│  ├─ images/
│  ├─ scss/
├─ components/
├─ config/
├─ containers/
├─ context/
├─ hooks/
├─ helpers/
├─ i18n/
│  ├─ en/
│  ├─ fr/
│  ├─ es/
├─ layouts/
├─ pages/
├─ services/
├─ validations/
```

### **📁 Assets**

- Aquí agrupamos todos nuestros archivos multimedia.
- Contiene subcarpetas como **`Images, Icons, Videos, Audios`,** etc.

### **📁 Components**

- Esta carpeta contiene todos los componentes de presentación de nuestra aplicación (Stateless Components).

  ```jsx
  import React from 'react';

  const Stateless = () => {
  	return <h1>¡Hola!</h1>;
  };

  export default Stateless;
  ```

### **📁 Containers**

- En esta carpeta tenemos los componentes Stateful (Smart component) donde seguimos rastreando el estado.

  ```jsx
  import React, { Component, useState } from 'react';

  const Stateful = () => {

    const [state, setState] = useState({ hello: 'hello world' })

  	return <h1>{this.state.hello}</h1>;
  };

  export default Stateful;

  // or

  class Stateful extends Component {
    constructor(props) {
      super(props);

      this.state = { hello: 'hello world' };
    }

    render() {
      return <h1>{this.state.hello}</h1>;
    }
  }

  export default Stateful;
  ```

### **📁 Constants**

- En este archivo agrupamos todas las constantes como regex.

### **📁 Helpers**

- Aquí creamos y exportamos funciones que serán reutilizadas en diferentes lugares de nuestra aplicación.

### **📁 Hooks**

- Una carpeta hecha para ganchos personalizados.

### **📁 Layouts**

- Contiene archivos de diseño como .**`Navbar, Footer, Sidebar`**
- Los diseños se utilizan para envolver un componente específico.

### **📁 Pages**

- Esta carpeta contiene componentes de páginas como etc...**`Home, Contact`**
- Cada página envuelta con un **`Layout`**

### **📁 Validations**

> Aquí escribimos nuestra validación de formularios y reglas utilizando una biblioteca como Formik o react-hook-form.

### **📁 Services**

- En esta carpeta gestionamos todas las solicitudes de API creando archivos para cada servicio.

### **📁 Contexts**

- Esta carpeta contiene todos los archivos de contexto donde gestionamos y globalizamos el estado en nuestra aplicación como estilos de tematización.

### **📁 Config**

- Toda la configuración de nuestra aplicación estará aquí en esta carpeta.

### **📁 i18n**

- Esta carpeta está hecha para soporte multi-idioma.
- Puede crear subcarpetas con un archivo para cada idioma que desee traducir.**`JSON`**
- Echa un vistazo a su guía Paso a Paso **_[AQUÍ](https://react.i18next.com/latest/using-with-hooks)_**.

## GitFlow

El flujo general de Gitflow es el siguiente:

- Se crea una rama develop a partir de main.
- Se crea una rama release a partir de la develop.
- Se crean ramas feature a partir de la develop.
- Cuando se termina una rama feature, se fusiona en la rama develop.
- Cuando la rama release está lista, se fusiona en las ramas develop y main.
- Si se detecta un problema en main, se crea una rama hotfix a partir de main.
- Una vez terminada la rama hotfix, esta se fusiona tanto en develop como en main.

## Guia de estilos

### Principios

- Mantenerlo simple y reusar lo más posible.
- Un código que luzca como si una sola persona lo haya escrito
- Escribir para escalabilidad.

### Estructura

![style_guide](/screenshots/style_guide.png)

### Generales

- Usamos **BEM** como metodología de creación de código.
- Nombre de archivos en plural (**Ejemplo**: buttons.scss)
- Clases en singular y minúsculas (Ejemplo: .gallery\_\_button)
- Nombrar imágenes relativas a su bloque. (Ejemplo: hero_background.png)

### Sintaxis

1.  Espacio después del selector y antes de {}
2.  Espacios para indentación.
3.  Espacio después del :
    1. Bloques de CSS separados por 2 líneas
    2. Evitar abuso de anidaciones. Limite 1 nivel
    3. Mixins para tamaño, estilos y valores numéricos de fuentes.

### Manejo de propiedades

Propiedades y selectores deben ordenarse de la siguiente forma:

- Propiedades del modelo de caja (display, width, height, margin, etc)
- Posicionamiento (position, left, top, right, etc)
- Tipografía (text-transform, text-decoration)
- Decoración (background-image, color, etc)
- Variables
- Mixins

### Ejemplo de código:

```scss
.button {
	padding: 20px 30px;
	display: block;
	position: relative;
	width: 220px;
	height: 40px;
	text-transform: uppercase;
	font-weight: $semibold;
	color: #ffff;
	background-color: #333333;
	@include font-size(13px);
}
```
