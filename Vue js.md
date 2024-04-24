# 1 - Introduccion a Vue.js

<image src="guia_vue_1.jpg" alt="guia practica vue.js">

## 1.1 - Que es Vue.js?

Vue.js es un framework progresivo de JavaScript utilizado principalmente para construir interfaces de usuario interactivas y de una sola página (SPA, por sus siglas en inglés). Fue creado por Evan You en 2014 y desde entonces ha ganado una gran popularidad en el desarrollo web.

Vue.js se destaca por su facilidad de aprendizaje y su enfoque incremental, lo que significa que puedes comenzar a usarlo fácilmente en partes de tu proyecto existente sin necesidad de reescribir todo el código. Además, Vue.js es altamente modular, lo que facilita la integración de bibliotecas y herramientas externas.

Una de las características clave de Vue.js es su sistema de reactividad, que permite que los componentes de la interfaz de usuario se actualicen automáticamente cuando cambian los datos subyacentes. Esto hace que sea muy eficiente y fácil de mantener.

En resumen, Vue.js es una herramienta poderosa y versátil para la construcción de aplicaciones web modernas y dinámicas.

## 1.2 - Ventjas de usar Vue.js

Hay varias ventajas al usar Vue.js para el desarrollo de aplicaciones web:

1. **Facilidad de aprendizaje:** Vue.js tiene una curva de aprendizaje suave, lo que lo hace ideal para desarrolladores de todos los niveles de experiencia. Su sintaxis clara y concisa permite a los desarrolladores comenzar rápidamente y construir aplicaciones de manera eficiente.

2. **Flexibilidad y modularidad:** Vue.js es altamente modular, lo que significa que puedes integrarlo fácilmente en proyectos existentes o combinarlo con otras bibliotecas y herramientas. Esto proporciona una gran flexibilidad para adaptarse a las necesidades específicas de tu proyecto.

3. **Reactividad:** Vue.js utiliza un sistema de reactividad para actualizar automáticamente la interfaz de usuario cuando cambian los datos subyacentes. Esto simplifica el desarrollo al eliminar la necesidad de actualizar manualmente la interfaz de usuario en respuesta a cambios de datos.

4. **Rendimiento:** Vue.js ofrece un rendimiento excepcional gracias a su enfoque en la optimización y su tamaño reducido. Además, Vue.js utiliza una técnica llamada "Virtual DOM" para minimizar los cambios en el DOM real, lo que mejora aún más el rendimiento de las aplicaciones.

5. **Comunidad activa y ecosistema robusto:** Vue.js cuenta con una comunidad activa de desarrolladores y una amplia variedad de bibliotecas, complementos y herramientas disponibles. Esto facilita el desarrollo de aplicaciones completas y potentes utilizando Vue.js.

6. **Documentación completa y recursos educativos:** Vue.js ofrece una documentación completa y bien organizada, así como una amplia variedad de recursos educativos, tutoriales y ejemplos para ayudar a los desarrolladores a aprender y dominar el framework.

## 1.3 - Historia y evolucion de Vue.js

Vue.js fue creado por Evan You, un desarrollador de software que trabajaba en Google en 2013, donde estaba involucrado en proyectos utilizando AngularJS. Si bien disfrutaba trabajar con AngularJS, notó que tenía ciertas limitaciones y complejidades que dificultaban su uso en proyectos específicos.

Con el objetivo de abordar estas limitaciones y crear una herramienta más flexible y fácil de usar, Evan comenzó a trabajar en un nuevo proyecto que finalmente se convertiría en Vue.js. En 2014, lanzó la primera versión pública de Vue.js.

En sus primeras etapas, Vue.js ganó tracción rápidamente entre los desarrolladores web debido a su enfoque claro y conciso, su curva de aprendizaje suave y su capacidad para integrarse fácilmente en proyectos existentes. A medida que crecía su popularidad, Evan continuó trabajando en el framework, agregando nuevas características y mejoras con cada versión.

Una de las características que ayudó a impulsar la adopción de Vue.js fue su sistema de reactividad, que permitía actualizar automáticamente la interfaz de usuario cuando cambian los datos subyacentes. Esto hizo que fuera fácil y eficiente construir aplicaciones interactivas y dinámicas con Vue.js.

Con el tiempo, Vue.js se convirtió en uno de los frameworks de JavaScript más populares del mundo, utilizado por miles de desarrolladores y empresas en una amplia variedad de proyectos web. La comunidad de Vue.js creció rápidamente, lo que llevó a una amplia gama de complementos, bibliotecas y herramientas disponibles para facilitar el desarrollo con Vue.js.

A medida que Vue.js continuaba evolucionando, se agregaron nuevas características importantes, como el enrutamiento oficial (Vue Router) y la gestión del estado (Vuex), que ampliaron aún más su funcionalidad y utilidad para una variedad de casos de uso.

# 2 - Fundamentos de Vue.js

## 2.1 - Instalacion y configuracion

La instalación y configuración de Vue.js es bastante sencilla. Puedes empezar siguiendo estos pasos:

### Crear un proyecto Vue.js SPA (single page aplication)

El proyecto creado utilizará una configuración de compilación basada en Vite y permmite la utilización de componentes de archivo único (SFC) de Vue.js.

Tener en cuenta tener instalada una versión actualizada de Node.js y de que el directorio de trabajo actual sea aquel en el que se desea crear el proyecto.

### con NPM:

```bash
npm create vue@latest
```

### con PNPM:

```bash
pnpm create vue@latest
```

### con YARN:

```bash
yarn create vue@latest
```

Estos comandos instalará y ejecutará create-vue, la herramienta oficial de andamiaje de proyectos de Vue. La herramienta le presentará indicaciones para varias funciones opcionales, como TypeScript y soporte de pruebas.
Es decir puede iniciar un proyecto con una mayor o menor configuración inicial:

```
| Project name: ..<your-project-name>
| Add TypeScript?... No / Yes
| Add JSX Support?... No / Yes
| Add Vue Router for Single Page Aplication development?... No / Yes
| Add Pinia for state management?... No / Yes
| Add Vitest for Unit testing?...No / Yes
| Add an End-to-End Testing Solution?... No / Cypress / Playwright
| Add ESLint for code quality?... No / Yes
| Add Prettier for code formating?... No / Yes
| Add Vue DevTools 7 extension for debugging? (experimental)... No / Yes
Scaffolding project in ./<your-project-name /> ...
Done.
```

Si no comprende del todo alguna de estas opciones, simplemente elija No por ahora. Una vez creado el proyecto, siga las instrucciones para instalar las dependencias e iniciar el servidor de desarrollo:

### con npm y pnpm:

Para pnpm debe reemplazar el comando donde corresponda:

```html
cd
<your-project-name>
  npm install
  <!-- o pnpm install-->
  npm run dev
  <!-- o pnpm run dev-->
</your-project-name>
```

### con yarn:

```html
cd <your-project-name> yarn yarn dev </your-project-name>
```

### Instalación con Vue CLI:

Para proyectos más grandes o avanzados, se recomienda utilizar Vue CLI (Command Line Interface), que es una herramienta oficial para crear, configurar y administrar proyectos Vue.js. Para instalar Vue CLI, necesitas tener Node.js y npm (Node Package Manager) instalados en tu sistema.

1. **Instalar Vue CLI globalmente:**

```bash
npm install -g @vue/cli
```

2. **Crear un nuevo proyecto Vue:**

```bash
vue create nombre-del-proyecto
```

3. **Seguir las instrucciones en la terminal:** Vue CLI te guiará a través de varias opciones para configurar tu proyecto, como seleccionar un preset (configuración predefinida) o configurar manualmente.

4. **Navegar al directorio del proyecto:**

```bash
cd nombre-del-proyecto
```

5. **Iniciar el servidor de desarrollo:**

```bash
npm run serve
```

### Instalación con CDN:

Si deseas comenzar a trabajar con Vue.js rápidamente, puedes simplemente incluirlo en tu proyecto a través de un CDN (Content Delivery Network). Esto te permite agregar Vue.js directamente a tu HTML sin necesidad de instalar ninguna herramienta adicional.

1. **Agregar Vue.js a tu HTML:**

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2"></script>
```

### Usando Vue en un archivo HTML:

Si prefieres trabajar directamente en un archivo HTML sin configurar un entorno de desarrollo completo, puedes hacerlo incluyendo Vue desde un CDN como se mencionó anteriormente y luego escribiendo tu código Vue en una etiqueta `<script>` dentro del archivo HTML.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2"></script>
  </head>
  <body>
    <div id="app">{{ message }}</div>

    <script>
      var app = new Vue({
        el: "#app",
        data: {
          message: "¡Hola, Vue!",
        },
      });
    </script>
  </body>
</html>
```

Estos son solo algunos métodos básicos para instalar y configurar Vue.js. Dependiendo de tus necesidades y preferencias, puedes elegir el método que mejor se adapte a tu proyecto.

## 2.2 - Vue instance

Una instancia de Vue es la piedra angular de cualquier aplicación Vue.js. Representa el ViewModel, que es la capa del modelo de Vista y proporciona la conexión entre los datos y la interfaz de usuario. Aquí tienes una breve descripción de cómo se crea y utiliza una instancia de Vue:

### Crear una instancia de Vue:

Puedes crear una instancia de Vue utilizando el constructor `Vue`. Este constructor toma un objeto de opciones como argumento, que define el comportamiento y la configuración de la instancia.

```javascript
var app = new Vue({
  // Opciones de configuración
});
```

### Opciones de configuración comunes:

- **el:** Especifica el elemento HTML al que la instancia de Vue está asociada. Puede ser un selector CSS o un elemento DOM.

- **data:** Define los datos que la instancia de Vue manejará. Pueden ser objetos, arrays u otros tipos de datos.

- **methods:** Contiene métodos que pueden ser llamados desde la interfaz de usuario o dentro de la instancia de Vue.

- **computed:** Define propiedades calculadas que se actualizan automáticamente cuando cambian los datos subyacentes.

- **watch:** Observa cambios en los datos y ejecuta código en respuesta a estos cambios.

- **lifecycle hooks:** Métodos especiales que se ejecutan en momentos específicos del ciclo de vida de la instancia de Vue, como `created`, `mounted`, `updated`, etc.

### Ejemplo de instancia de Vue:

```javascript
var app = new Vue({
  el: "#app",
  data: {
    message: "¡Hola, Vue!",
  },
  methods: {
    saludar: function () {
      alert(this.message);
    },
  },
});
```

### Uso en HTML:

Puedes usar la instancia de Vue en tu HTML para mostrar datos y responder a eventos.

```html
<div id="app">
  <p>{{ message }}</p>
  <button @click="saludar">Saludar</button>
</div>
```

En este ejemplo, cuando haces clic en el botón, se llamará al método `saludar`, que mostrará una alerta con el mensaje definido en los datos de la instancia de Vue.

Las instancias de Vue son fundamentales para desarrollar aplicaciones Vue.js y proporcionan una forma poderosa de manejar la lógica y la interacción de la interfaz de usuario.

## 2.3 - Directivas

Las directivas en Vue.js son atributos especiales que se pueden agregar a elementos HTML para aplicar comportamientos dinámicos a ellos. Estas directivas se identifican mediante el prefijo `v-` y se utilizan para manipular el DOM, asociar datos y controlar el comportamiento de la interfaz de usuario. Aquí tienes algunas de las directivas más comunes en Vue.js:

### `v-bind` (abreviado como `:`):

Esta directiva se utiliza para asociar dinámicamente el valor de un atributo HTML a una expresión Vue.js.

```html
<a v-bind:href="url">Enlace</a>
```

```html
<a :href="url">Enlace</a>
```

### `v-model`:

Esta directiva se utiliza para crear una vinculación de datos bidireccional entre un elemento de formulario y los datos de Vue.js.

```html
<input v-model="message" type="text" />
```

### `v-if`, `v-else-if`, `v-else`:

Estas directivas se utilizan para condicionalmente renderizar elementos HTML en función de expresiones booleanas.

```html
<div v-if="mostrarMensaje">Mensaje mostrado</div>
<div v-else>No hay mensaje para mostrar</div>
```

### `v-for`:

Esta directiva se utiliza para iterar sobre una matriz o un objeto y renderizar dinámicamente elementos HTML basados en cada elemento del iterable.

```html
<ul>
  <li v-for="item in items">{{ item }}</li>
</ul>
```

### `v-on` (abreviado como `@`):

Esta directiva se utiliza para adjuntar eventos DOM a métodos de Vue.js.

```html
<button v-on:click="handleClick">Haz clic</button>
```

```html
<button @click="handleClick">Haz clic</button>
```

### `v-show`:

Esta directiva se utiliza para condicionalmente mostrar u ocultar elementos HTML en función de una expresión booleana.

```html
<div v-show="mostrarElemento">Elemento mostrado</div>
```

### `v-cloak`:

Esta directiva se utiliza para ocultar temporalmente elementos que contienen la interpolación de Vue.js hasta que la instancia Vue está completamente cargada y lista para ser renderizada.

```html
<div v-cloak>{{ mensaje }}</div>
```

Estas son solo algunas de las directivas más comunes en Vue.js. Hay muchas más disponibles para diversas tareas, y puedes incluso crear tus propias directivas personalizadas si es necesario. Las directivas son una parte fundamental de Vue.js y proporcionan una forma elegante y poderosa de manipular el DOM y crear interfaces de usuario dinámicas.

## 2.4 - Eventos y metodos

En Vue.js, los eventos y los métodos son fundamentales para la interactividad de la aplicación. Los eventos son desencadenados por acciones del usuario, como hacer clic en un botón, mientras que los métodos son funciones definidas en la instancia de Vue que responden a estos eventos o realizan otras tareas. Aquí tienes una visión general de cómo funcionan los eventos y los métodos en Vue.js:

### Eventos en Vue.js:

Los eventos en Vue.js se pueden escuchar utilizando la directiva `v-on` o su atajo `@`. Pueden ser eventos DOM estándar o eventos personalizados emitidos por componentes Vue.

#### Escuchando eventos DOM:

```html
<button v-on:click="handleClick">Haz clic</button>
```

#### Escuchando eventos personalizados:

```html
<custom-component v-on:custom-event="handleCustomEvent"></custom-component>
```

### Métodos en Vue.js:

Los métodos en Vue.js son funciones definidas en el objeto de opciones de la instancia Vue y se pueden invocar para realizar diversas tareas, como manipular datos, realizar cálculos, realizar llamadas a la API, etc.

```javascript
var app = new Vue({
  data: {
    message: "¡Hola, Vue!",
  },
  methods: {
    handleClick: function () {
      console.log("Haz clic en el botón");
    },
    handleCustomEvent: function (payload) {
      console.log("Evento personalizado recibido:", payload);
    },
  },
});
```

En este ejemplo, `handleClick` es un método que se ejecutará cuando se haga clic en el botón, y `handleCustomEvent` es un método que se ejecutará cuando se emita el evento personalizado desde un componente.

### Llamar métodos desde eventos:

Puedes llamar a métodos desde eventos DOM utilizando `v-on` o su atajo `@`.

```html
<button v-on:click="handleClick">Haz clic</button>
```

### Pasar parámetros a métodos:

Puedes pasar parámetros a métodos en Vue.js utilizando la sintaxis de método llamando a la función directamente y pasando los parámetros como argumentos.

```html
<button v-on:click="handleClick('parámetro')">Haz clic</button>
```

```javascript
methods: {
  handleClick: function(param) {
    console.log('Parámetro:', param);
  }
}
```

Los eventos y los métodos en Vue.js permiten que la aplicación responda a las acciones del usuario de manera dinámica y controlada, lo que hace que el desarrollo de interfaces de usuario interactivas sea muy flexible y poderoso.

## 2.5 - Binding de datos

El binding de datos en Vue.js es un concepto central que permite enlazar dinámicamente los datos de la aplicación con la interfaz de usuario. Esto significa que cualquier cambio en los datos se reflejará automáticamente en la vista y cualquier interacción del usuario que modifique la vista actualizará los datos subyacentes. Aquí tienes una descripción de los diferentes tipos de binding de datos en Vue.js:

### `Interpolación:`

La interpolación es la forma más básica de binding de datos en Vue.js y se utiliza para mostrar datos en la vista. Se utiliza la sintaxis de dobles llaves `{{ }}` para vincular datos a elementos HTML.

```html
<p>{{ mensaje }}</p>
```

### `Binding de atributos:`

El binding de atributos se utiliza para establecer dinámicamente los valores de los atributos de elementos HTML utilizando la directiva `v-bind` o su abreviatura `:`.

```html
<img v-bind:src="imagenURL" />
```

### `Binding de clase y estilo:`

El binding de clase y estilo se utiliza para aplicar dinámicamente clases y estilos a elementos HTML en función de expresiones de datos.

#### Binding de clase:

```html
<div
  v-bind:class="{ 'clase-activa': isActive, 'clase-inactiva': !isActive }"
></div>
```

#### Binding de estilo:

```html
<div v-bind:style="{ color: textColor, fontSize: fontSize + 'px' }"></div>
```

### `Binding de eventos:`

El binding de eventos se utiliza para adjuntar eventos DOM a métodos de Vue.js utilizando la directiva `v-on` o su abreviatura `@`.

```html
<button v-on:click="handleClick">Haz clic</button>
```

### `Binding de formulario:`

El binding de formulario se utiliza para crear vinculaciones bidireccionales entre los datos de Vue.js y los elementos de formulario, como `input`, `textarea`, y `select`.

```html
<input v-model="nombre" type="text" />
```

### `Binding de contenido HTML:`

El binding de contenido HTML se utiliza para insertar HTML generado dinámicamente en la vista utilizando la directiva `v-html`.

```html
<p v-html="htmlContent"></p>
```

Estos son algunos de los principales tipos de binding de datos en Vue.js. Utilizando estos mecanismos, puedes crear fácilmente aplicaciones interactivas y dinámicas donde los datos y la interfaz de usuario están estrechamente vinculados y se actualizan automáticamente según sea necesario.

# 3 - Componentes de Vue.js

Los componentes en Vue.js son bloques de construcción reutilizables que encapsulan la funcionalidad y la interfaz de usuario de una parte de la aplicación. Los componentes permiten dividir la interfaz de usuario en piezas más pequeñas y manejables, lo que facilita el desarrollo, el mantenimiento y la reutilización del código. Aquí tienes una descripción de cómo funcionan los componentes en Vue.js:

### Definición de componentes:

Los componentes en Vue.js se pueden definir utilizando el método `Vue.component()` o mediante opciones de componente dentro de una instancia Vue.

#### Definición mediante `Vue.component()`:

```javascript
Vue.component("nombre-del-componente", {
  // opciones del componente
});
```

#### Definición mediante opciones de componente en una instancia Vue:

```javascript
var ComponentePadre = new Vue({
  el: "#app",
  components: {
    "nombre-del-componente": {
      // opciones del componente
    },
  },
});
```

### Estructura de un componente:

Un componente en Vue.js generalmente consta de tres partes principales:

1. **Template:** Define la estructura y la apariencia del componente utilizando HTML y directivas de Vue.js.

2. **Script:** Contiene la lógica del componente, incluyendo datos, métodos, propiedades calculadas y ganchos de ciclo de vida.

3. **Estilos:** Opcionalmente, se pueden incluir estilos CSS para dar estilo al componente.

### Comunicación entre componentes:

Los componentes en Vue.js pueden comunicarse entre sí de varias maneras, como el uso de props para pasar datos de un componente padre a un componente hijo, la emisión de eventos para comunicar cambios de un componente hijo a un componente padre, y el uso de un sistema centralizado de gestión de estado como Vuex para compartir datos entre múltiples componentes.

### Reutilización y composición:

Los componentes en Vue.js están diseñados para ser reutilizables y componibles, lo que significa que puedes crear componentes pequeños y especializados y luego combinarlos para construir interfaces de usuario complejas. Esto facilita la construcción de aplicaciones modulares y escalables.

**Ejemplo:**

```html
<template>
  <div>
    <h1>{{ titulo }}</h1>
    <p>{{ descripcion }}</p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        titulo: "Mi componente",
        descripcion: "Este es un ejemplo de componente en Vue.js",
      };
    },
  };
</script>

<style scoped>
  h1 {
    color: blue;
  }
  p {
    font-style: italic;
  }
</style>
```

En este ejemplo, se define un componente simple con un template que contiene un título y una descripción, un script que define los datos del componente, y estilos CSS para dar estilo al componente. Este componente puede ser reutilizado y combinado con otros componentes para construir interfaces de usuario más complejas.

## 3.1 - Creacion de componentes

La creación de componentes en Vue.js es una parte fundamental del desarrollo de aplicaciones Vue.js, ya que permite modularizar y reutilizar el código de manera efectiva. Aquí te muestro cómo crear componentes en Vue.js:

### `Definir un componente:`

Puedes definir un componente Vue.js utilizando el método `Vue.component()` o mediante la opción `components` en una instancia Vue.

#### Mediante `Vue.component()`:

```javascript
Vue.component("nombre-del-componente", {
  // opciones del componente
});
```

#### Mediante la opción `components` en una instancia Vue:

```javascript
var ComponentePadre = new Vue({
  el: "#app",
  components: {
    "nombre-del-componente": {
      // opciones del componente
    },
  },
});
```

### `Opciones del componente:`

Las opciones del componente son similares a las opciones de una instancia Vue, y puedes definir propiedades de datos, métodos, propiedades calculadas, y más.

```javascript
Vue.component("nombre-del-componente", {
  data: function () {
    return {
      mensaje: "¡Hola, soy un componente!",
    };
  },
  template: "<div>{{ mensaje }}</div>",
  methods: {
    metodoPersonalizado: function () {
      // código del método
    },
  },
});
```

### ` Uso del componente:`

Una vez definido, puedes utilizar el componente en cualquier parte de tu aplicación Vue.js, simplemente haciendo referencia a su nombre como un elemento HTML.

```html
<div id="app">
  <nombre-del-componente></nombre-del-componente>
</div>
```

### ` Propiedades del componente:`

Los componentes pueden aceptar propiedades para pasar datos desde el componente padre al componente hijo. Se definen utilizando la opción `props` y se utilizan como atributos en el componente.

```javascript
Vue.component("nombre-del-componente", {
  props: ["propiedad1", "propiedad2"],
  template: "<div>{{ propiedad1 }}, {{ propiedad2 }}</div>",
});
```

```html
<nombre-del-componente
  :propiedad1="valor1"
  :propiedad2="valor2"
></nombre-del-componente>
```

### `Ciclo de vida del componente:`

Los componentes Vue.js tienen un ciclo de vida que consta de varios hooks que se ejecutan en diferentes etapas, como `created`, `mounted`, `updated`, y `destroyed`. Puedes utilizar estos hooks para realizar acciones específicas en cada etapa del ciclo de vida del componente.

```javascript
Vue.component("nombre-del-componente", {
  created: function () {
    console.log("El componente se ha creado");
  },
  mounted: function () {
    console.log("El componente se ha montado en el DOM");
  },
  destroyed: function () {
    console.log("El componente se ha destruido");
  },
});
```

La creación de componentes en Vue.js te permite construir aplicaciones modulares y escalables, donde el código puede organizarse de manera efectiva y los componentes pueden ser reutilizados en diferentes partes de la aplicación.

## 3.2 - Props y eventos

En Vue.js, los props y los eventos son mecanismos fundamentales para la comunicación entre componentes, permitiendo pasar datos desde el componente padre al hijo mediante props y desde el hijo al padre mediante eventos. Aquí te explico cómo funcionan ambos:

### Props:

Los props son atributos personalizados que se pueden pasar de un componente padre a un componente hijo. Estos props se definen en el componente hijo y se utilizan para pasar datos al componente hijo desde el padre.

#### Definir props en el componente hijo:

```javascript
Vue.component("hijo", {
  props: ["mensaje"],
  template: "<p>{{ mensaje }}</p>",
});
```

#### Utilizar el componente hijo y pasar props desde el componente padre:

```html
<template>
  <div>
    <hijo :mensaje="mensajeDesdePadre"></hijo>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        mensajeDesdePadre: "Hola desde el padre",
      };
    },
  };
</script>
```

### Eventos:

Los eventos son utilizados para comunicarse desde un componente hijo hacia su componente padre. Un componente hijo puede emitir un evento personalizado y el componente padre puede escuchar ese evento y reaccionar en consecuencia.

#### Emitir un evento desde el componente hijo:

```javascript
Vue.component("hijo", {
  template: '<button @click="emitirEvento">Enviar evento al padre</button>',
  methods: {
    emitirEvento: function () {
      this.$emit("evento-personalizado", "datos-del-evento");
    },
  },
});
```

#### Escuchar y manejar el evento en el componente padre:

```html
<template>
  <div>
    <hijo @evento-personalizado="manejarEvento"></hijo>
  </div>
</template>

<script>
  export default {
    methods: {
      manejarEvento: function (datos) {
        console.log("Evento recibido en el padre:", datos);
      },
    },
  };
</script>
```

### Combinando Props y Eventos:

Usualmente, los props se utilizan para pasar datos del padre al hijo y los eventos para comunicar cambios del hijo al padre. De esta manera, se crea una comunicación unidireccional entre los componentes.

```html
<template>
  <div>
    <hijo
      :mensaje="mensajeDesdePadre"
      @evento-personalizado="manejarEvento"
    ></hijo>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        mensajeDesdePadre: "Hola desde el padre",
      };
    },
    methods: {
      manejarEvento: function (datos) {
        console.log("Evento recibido en el padre:", datos);
      },
    },
  };
</script>
```

Usando props y eventos, puedes construir aplicaciones Vue.js altamente modulares y flexibles, donde los componentes pueden comunicarse entre sí de manera eficiente y escalable.

## 3.3 - Slots

Los slots en Vue.js son una característica poderosa que permite crear componentes reutilizables y flexibles al permitir que el contenido se pase desde el componente padre al hijo de una manera dinámica. Los slots permiten insertar contenido HTML o componentes dentro de un componente hijo, lo que lo hace muy versátil. Aquí te explico cómo funcionan los slots en Vue.js:

### Uso básico de slots:

#### Definir un componente hijo con un slot:

```html
<template>
  <div>
    <h2>Componente Hijo</h2>
    <slot></slot>
  </div>
</template>
```

#### Utilizar el componente hijo y pasar contenido desde el componente padre:

```html
<template>
  <div>
    <h1>Componente Padre</h1>
    <Hijo>
      <p>Este es el contenido pasado desde el componente padre.</p>
    </Hijo>
  </div>
</template>

<script>
  import Hijo from "./Hijo.vue";

  export default {
    components: {
      Hijo,
    },
  };
</script>
```

En este ejemplo, cualquier contenido dentro de las etiquetas `<Hijo>` en el componente padre se insertará en el slot del componente hijo.

### Slots con nombre:

Los slots con nombre permiten definir múltiples slots dentro de un componente hijo y asignarles un nombre específico. Esto es útil cuando se quiere pasar contenido específico a diferentes ubicaciones dentro del componente hijo.

#### Definir un componente hijo con slots con nombre:

```html
<template>
  <div>
    <h2>Componente Hijo</h2>
    <slot name="header"></slot>
    <div>
      <slot></slot>
    </div>
    <slot name="footer"></slot>
  </div>
</template>
```

#### Utilizar el componente hijo y pasar contenido a slots con nombre desde el componente padre:

```html
<template>
  <div>
    <h1>Componente Padre</h1>
    <Hijo>
      <template v-slot:header>
        <h3>Encabezado del componente hijo</h3>
      </template>
      <p>Contenido principal del componente hijo.</p>
      <template v-slot:footer>
        <footer>Footer del componente hijo</footer>
      </template>
    </Hijo>
  </div>
</template>

<script>
  import Hijo from "./Hijo.vue";

  export default {
    components: {
      Hijo,
    },
  };
</script>
```

### Uso de slots con valores predeterminados:

Se puede proporcionar contenido predeterminado dentro de un slot en caso de que no se proporcione ningún contenido desde el componente padre.

```html
<template>
  <div>
    <h2>Componente Hijo</h2>
    <slot>
      <p>
        Este es el contenido predeterminado si no se proporciona nada desde el
        componente padre.
      </p>
    </slot>
  </div>
</template>
```

Los slots son una característica potente que permite una mayor flexibilidad y reutilización en la construcción de componentes Vue.js, lo que facilita la creación de interfaces de usuario dinámicas y personalizadas.

## 3.4 - Ciclo de vida de un componente

El ciclo de vida de un componente Vue.js consta de una serie de etapas que ocurren desde su creación hasta su destrucción. Estas etapas permiten ejecutar código en momentos específicos durante la vida útil del componente, lo que brinda la oportunidad de realizar tareas como inicialización de datos, manipulación del DOM y limpieza de recursos. Aquí tienes una descripción de las principales etapas del ciclo de vida de un componente Vue.js:

### **Creación:**

- **`beforeCreate`:** Este hook se ejecuta inmediatamente después de que se haya creado la instancia del componente y se hayan configurado sus opciones, pero antes de que se inicie la observación de los datos y se configure el renderizado del template.

- **`created`:** Se ejecuta después de que la instancia del componente haya sido creada y las observaciones de datos hayan sido establecidas, pero antes de que el DOM del componente haya sido montado y renderizado. En este punto, el componente aún no tiene acceso al DOM.

### **Montaje:**

- **`beforeMount`:** Se ejecuta justo antes de que el componente sea montado en el DOM. En este punto, el template del componente ha sido compilado pero aún no ha sido insertado en el DOM.

- **`mounted`:** Se ejecuta después de que el componente ha sido montado en el DOM. En este punto, el componente tiene acceso completo al DOM y puede interactuar con él. Es común realizar operaciones de inicialización de datos, solicitudes de red y suscripciones a eventos aquí.

### **Actualización:**

- **`beforeUpdate`:** Se ejecuta antes de que los cambios realizados en los datos de la instancia del componente se apliquen al DOM. Es útil para realizar operaciones previas a la actualización del DOM o para acceder a los valores antiguos de los datos antes de que se actualicen.

- **`updated`:** Se ejecuta después de que los cambios en los datos de la instancia del componente se hayan aplicado al DOM. En este punto, el DOM ha sido actualizado para reflejar los cambios en los datos. Es un buen lugar para realizar operaciones de post-actualización del DOM o para acceder al DOM actualizado.

### **Destrucción:**

- **`beforeDestroy`:** Se ejecuta justo antes de que el componente sea destruido. En este punto, el componente aún está completamente funcional y puede realizar limpieza de recursos, como cancelar suscripciones a eventos o temporizadores.

- **`destroyed`:** Se ejecuta después de que el componente haya sido completamente destruido y eliminado del DOM. En este punto, el componente ya no es accesible y cualquier limpieza final de recursos debe realizarse aquí.

  **Ejemplo:**

```javascript
Vue.component("mi-componente", {
  beforeCreate() {
    console.log("beforeCreate hook");
  },
  created() {
    console.log("created hook");
  },
  beforeMount() {
    console.log("beforeMount hook");
  },
  mounted() {
    console.log("mounted hook");
  },
  beforeUpdate() {
    console.log("beforeUpdate hook");
  },
  updated() {
    console.log("updated hook");
  },
  beforeDestroy() {
    console.log("beforeDestroy hook");
  },
  destroyed() {
    console.log("destroyed hook");
  },
});
```

El ciclo de vida de un componente Vue.js proporciona puntos de enganche importantes para ejecutar código en diferentes momentos de su vida útil, lo que permite realizar tareas específicas en cada etapa según sea necesario. Esto es útil para gestionar el comportamiento del componente y garantizar una experiencia de usuario suave y eficiente.

# 4 - Routing en Vue.js

El enrutamiento en Vue.js permite crear aplicaciones de una sola página (SPA) mediante la navegación entre diferentes vistas o componentes sin necesidad de recargar la página completa. Vue Router es la biblioteca oficial de enrutamiento para Vue.js y proporciona un enrutador de tipo cliente que se integra con la biblioteca principal de Vue.js. Aquí te explico cómo implementar el enrutamiento en Vue.js con Vue Router:

## 4.1 - Configuracion de rutas

La configuración de rutas en Vue Router es fundamental para establecer la correspondencia entre las URL y los componentes que se deben mostrar en la aplicación Vue.js. Aquí te muestro cómo puedes configurar las rutas en Vue Router:

### Instalación de Vue Router:

Primero, asegúrate de haber instalado Vue Router en tu proyecto. Puedes hacerlo utilizando npm o yarn:

```bash
npm install vue-router
```

o

```bash
yarn add vue-router
```

### Configuración de Vue Router:

Luego, debes configurar Vue Router en tu aplicación Vue.js. Esto generalmente se hace en el archivo `main.js` o en un archivo específico para la configuración de Vue Router.

```javascript
import Vue from "vue";
import VueRouter from "vue-router";
import Home from "./components/Home.vue";
import About from "./components/About.vue";

Vue.use(VueRouter);

const routes = [
  { path: "/", component: Home },
  { path: "/about", component: About },
];

const router = new VueRouter({
  routes,
});

new Vue({
  router,
  render: (h) => h(App),
}).$mount("#app");
```

En este ejemplo:

- Se importa Vue Router y se instala en Vue.
- Se importan los componentes que se utilizarán en las rutas.
- Se define un array de rutas, donde cada ruta tiene una URL (`path`) y el componente correspondiente que se mostrará (`component`).
- Se crea una instancia de Vue Router con la configuración de rutas definida.

### Uso de las rutas:

Una vez configurado Vue Router, puedes usar las rutas en tu aplicación Vue.js.

#### Creación de enlaces de navegación:

Puedes crear enlaces de navegación utilizando la directiva `router-link`.

```html
<router-link to="/">Inicio</router-link>
<router-link to="/about">Acerca de</router-link>
```

#### Renderización de la vista correspondiente:

Puedes renderizar la vista correspondiente utilizando el componente `router-view`.

```html
<router-view></router-view>
```

### Rutas con parámetros:

Vue Router permite definir rutas con parámetros que pueden ser utilizados dinámicamente.

```javascript
const routes = [{ path: "/user/:id", component: User }];
```

En este ejemplo, `:id` es un parámetro dinámico que puede ser accesado desde el componente `User` utilizando `this.$route.params.id`.

### Redirecciones y alias:

Vue Router también permite configurar redirecciones y alias para las rutas.

```javascript
const routes = [
  { path: "/redirect", redirect: "/about" },
  { path: "/old-url", redirect: "/new-url" },
  { path: "/about", component: About, alias: "/acerca-de" },
];
```

En este ejemplo, `/redirect` redirige a `/about`, `/old-url` redirige a `/new-url`, y `/about` tiene un alias `/acerca-de`.

### Middleware de navegación:

Vue Router proporciona middleware de navegación que se ejecuta antes de cambiar de ruta. Esto es útil para realizar validaciones o autenticaciones antes de permitir que un usuario acceda a una ruta.

```javascript
router.beforeEach((to, from, next) => {
  // Lógica de autenticación u otras validaciones
  next();
});
```

Con Vue Router, puedes configurar fácilmente las rutas de tu aplicación Vue.js y proporcionar una experiencia de navegación dinámica y fluida para tus usuarios.

## 4.2 - Navegacion entre vistas

Para lograr la navegación entre vistas en una aplicación Vue.js utilizando Vue Router, necesitas configurar las rutas y luego crear enlaces de navegación para cada ruta. Aquí tienes una guía paso a paso sobre cómo hacerlo:

### `Configurar Vue Router:`

Primero, necesitas configurar Vue Router en tu aplicación. Esto se puede hacer en el archivo `main.js` o en un archivo dedicado para la configuración de Vue Router.

```javascript
import Vue from "vue";
import VueRouter from "vue-router";
import Home from "./components/Home.vue";
import About from "./components/About.vue";

Vue.use(VueRouter);

const routes = [
  { path: "/", component: Home },
  { path: "/about", component: About },
];

const router = new VueRouter({
  routes,
});

new Vue({
  router,
  render: (h) => h(App),
}).$mount("#app");
```

En este ejemplo, se definen dos rutas: una para la página de inicio (`'/'`) y otra para la página Acerca de (`'/about'`). Cada ruta tiene un componente asociado que se renderizará cuando la ruta coincida.

### `Crear enlaces de navegación:`

Utiliza la directiva `router-link` para crear enlaces de navegación en tu aplicación.

```html
<router-link to="/">Inicio</router-link>
<router-link to="/about">Acerca de</router-link>
```

Esto creará enlaces de navegación que, cuando se haga clic, llevarán al usuario a la ruta correspondiente.

### `Renderizar la vista correspondiente:`

Utiliza el componente `router-view` para renderizar dinámicamente la vista correspondiente según la ruta actual.

```html
<router-view></router-view>
```

Este componente se encargará de renderizar el componente asociado a la ruta actualmente activa.

### `Navegación programática:`

Además de utilizar los enlaces de navegación, también puedes realizar la navegación de forma programática en tus componentes Vue.js utilizando el objeto `$router`.

Por ejemplo, para navegar a la página de inicio desde un método en un componente:

```javascript
this.$router.push("/");
```

Este código navegará a la ruta especificada (`'/'` en este caso) utilizando la API de navegación proporcionada por Vue Router.

Con estos pasos, puedes lograr fácilmente la navegación entre vistas en tu aplicación Vue.js utilizando Vue Router. Esto proporcionará una experiencia de usuario fluida y dinámica al permitir que los usuarios se muevan entre diferentes páginas de tu aplicación sin necesidad de recargar la página completa.

## 4.3 - Paso de parametros

Para pasar parámetros entre rutas en Vue.js utilizando Vue Router, puedes utilizar la sintaxis de ruta dinámica para definir rutas que contengan segmentos variables en la URL. Luego, puedes acceder a estos parámetros desde el componente asociado a la ruta utilizando `this.$route.params`.

Aquí tienes una guía paso a paso sobre cómo pasar parámetros entre rutas en Vue.js:

### `Definir una ruta con parámetros:`

En tu configuración de Vue Router, define una ruta que contenga segmentos variables en la URL utilizando `:` seguido del nombre del parámetro.

```javascript
const routes = [{ path: "/user/:id", component: User }];
```

En este ejemplo, `:id` es un parámetro dinámico en la URL.

### `Acceder a los parámetros desde el componente:`

En el componente asociado a la ruta, puedes acceder a los parámetros utilizando `this.$route.params`.

```javascript
export default {
  mounted() {
    console.log(this.$route.params.id);
  },
};
```

En este ejemplo, `this.$route.params.id` contiene el valor del parámetro `id` de la URL.

### `Enlaces de navegación con parámetros:`

Cuando creas enlaces de navegación que contienen parámetros, utiliza la propiedad `to` de `router-link` para especificar la ruta con los parámetros.

```html
<router-link :to="'/user/' + userId">Ver perfil de usuario</router-link>
```

En este ejemplo, `userId` es una variable que contiene el valor del parámetro `id`.

### `Navegación programática con parámetros:`

Para navegar programáticamente a una ruta que contiene parámetros, utiliza `this.$router.push()` y proporciona la ruta con los parámetros como un objeto.

```javascript
this.$router.push({ path: "/user/" + userId });
```

### `Acceder a los parámetros en la URL:`

En la URL, los parámetros se incluirán después del segmento de ruta correspondiente, separados por `/`.

Por ejemplo, si la ruta es `/user/123`, entonces `123` será el valor del parámetro `id`.

Con estos pasos, puedes pasar fácilmente parámetros entre rutas en Vue.js utilizando Vue Router. Esto es útil para crear aplicaciones dinámicas que respondan a la interacción del usuario y muestren datos específicos según la URL actual.

# 5 - Gestion de estado en Vue.js

En Vue.js, la "gestión de estado" se refiere a la capacidad de manejar y controlar el estado de la aplicación de manera centralizada y eficiente. El estado de una aplicación se refiere a los datos que describen la condición actual de la interfaz de usuario y los datos que se muestran en ella. Esto puede incluir cosas como datos de usuario, datos de sesión, preferencias, estados de componentes y más.

En una aplicación Vue.js típica, el estado puede estar disperso en varios componentes y puede volverse difícil de mantener y sincronizar a medida que la aplicación crece en tamaño y complejidad. Para abordar este problema, muchas aplicaciones utilizan patrones de gestión de estado como Vuex.

### Vuex:

Vuex es una biblioteca de gestión de estado oficial para Vue.js que proporciona una forma de manejar el estado de la aplicación de manera centralizada y predecible. Con Vuex, puedes definir un "almacén" centralizado que contiene el estado de toda la aplicación, y luego acceder y modificar ese estado desde cualquier componente en la aplicación.

El flujo de datos en Vuex sigue un patrón unidireccional, lo que significa que los datos fluyen en una dirección predecible desde el almacén central a los componentes, y cualquier cambio en el estado se maneja mediante mutaciones predefinidas que garantizan la consistencia y predictibilidad del estado de la aplicación.

### Beneficios de la gestión de estado con Vuex:

1. **Centralización del estado:** Todos los datos de la aplicación se almacenan en un solo lugar, lo que facilita la comprensión y el mantenimiento del estado de la aplicación.

2. **Predictibilidad:** Los cambios en el estado se realizan mediante mutaciones predefinidas, lo que garantiza que el estado de la aplicación sea predecible y consistente.

3. **Desarrollo más escalable:** A medida que la aplicación crece en tamaño y complejidad, Vuex facilita la escalabilidad del desarrollo al proporcionar una estructura organizada y coherente para manejar el estado de la aplicación.

4. **Facilidad de depuración:** Al centralizar el estado de la aplicación, Vuex facilita la depuración de problemas relacionados con el estado, ya que solo necesitas buscar en un solo lugar para encontrar la causa de un problema.

En resumen, la gestión de estado en Vue.js, especialmente con Vuex, es una práctica recomendada para aplicaciones de tamaño mediano a grande, ya que proporciona una forma estructurada y eficiente de manejar el estado de la aplicación y garantizar una experiencia de usuario consistente y predecible.

## 5.1 - Vuex: Introduccion y conceptos basicos

Vuex es una biblioteca de gestión de estado para Vue.js que facilita el manejo del estado de la aplicación de manera centralizada. Aquí tienes una introducción a Vuex junto con algunos conceptos básicos:

### Introducción a Vuex:

Vuex se inspira en la arquitectura de Flux, que es un patrón de diseño para gestionar el estado de las aplicaciones de interfaz de usuario. En esencia, Vuex proporciona una manera predecible de manejar el estado de la aplicación a través de un almacén centralizado y de una estructura de flujo de datos unidireccional.

### Conceptos básicos de Vuex:

1. **Estado (State):** El estado de la aplicación se almacena en un único objeto llamado el "estado" (state). Este objeto contiene todos los datos de la aplicación que pueden cambiar con el tiempo.

2. **Mutaciones (Mutations):** Las mutaciones son funciones que modifican el estado de la aplicación de manera predecible. Cada mutación tiene un nombre y una función que actualiza el estado.

3. **Acciones (Actions):** Las acciones son funciones que desencadenan mutaciones. Las acciones pueden contener lógica asíncrona y realizar llamadas a la API antes de comprometerse con una mutación.

4. **Módulos (Modules):** Los módulos permiten dividir el almacén de Vuex en piezas más pequeñas y manejables. Cada módulo puede tener su propio estado, mutaciones, acciones y getters.

5. **Getters:** Los getters son funciones que calculan propiedades derivadas del estado de la aplicación. Se pueden utilizar para obtener datos del estado en formatos específicos o realizar cálculos complejos.

### Configuración básica de Vuex:

Para usar Vuex en tu aplicación Vue.js, primero debes instalarlo y configurarlo.

1. Instalar Vuex:

```bash
npm install vuex
```

2. Configurar Vuex en tu aplicación:

```javascript
import Vue from "vue";
import Vuex from "vuex";

Vue.use(Vuex);

const store = new Vuex.Store({
  state: {
    // Estado de la aplicación
  },
  mutations: {
    // Mutaciones para modificar el estado
  },
  actions: {
    // Acciones que pueden desencadenar mutaciones
  },
  getters: {
    // Getters para obtener datos del estado
  },
});

export default store;
```

Luego, puedes importar este almacén en tu archivo `main.js` y asociarlo con tu instancia Vue:

```javascript
import Vue from "vue";
import App from "./App.vue";
import store from "./store";

new Vue({
  render: (h) => h(App),
  store,
}).$mount("#app");
```

¡Con Vuex configurado, puedes comenzar a utilizarlo para manejar el estado de tu aplicación de manera centralizada y predecible!

## 5.2 - Store, Mutations y Actions

Claro, aquí tienes una explicación detallada sobre Store, Mutations y Actions en Vuex:

### `Store`:

El Store es el objeto central en Vuex que contiene el estado de la aplicación y sirve como un almacén centralizado para todos los datos que pueden cambiar en la aplicación. En el Store, se almacenan los datos de la aplicación, se definen las mutaciones y acciones, y se accede a través de los componentes Vue.

```javascript
import Vue from "vue";
import Vuex from "vuex";

Vue.use(Vuex);

const store = new Vuex.Store({
  state: {
    // Estado de la aplicación
    count: 0,
  },
  mutations: {
    // Mutaciones para modificar el estado
  },
  actions: {
    // Acciones que pueden desencadenar mutaciones
  },
  getters: {
    // Getters para obtener datos del estado
  },
});

export default store;
```

### `Mutations`:

Las mutaciones son funciones que modifican el estado de la aplicación de manera síncrona y predecible. Se utilizan para actualizar el estado del Store de Vuex de forma segura. Las mutaciones reciben el estado actual como primer parámetro y pueden recibir un segundo parámetro opcional, que es el payload (carga útil) que contiene los datos necesarios para la mutación.

```javascript
mutations: {
  increment(state) {
    state.count++;
  },
  decrement(state) {
    state.count--;
  },
  setCount(state, payload) {
    state.count = payload;
  }
}
```

### `Actions`:

Las acciones son funciones que desencadenan mutaciones. A diferencia de las mutaciones, las acciones pueden contener lógica asíncrona y realizar llamadas a la API antes de comprometerse con una mutación. Las acciones reciben un objeto `context` como primer parámetro, que contiene métodos y propiedades que permiten interactuar con el Store, y pueden recibir un segundo parámetro opcional, que es el payload.

```javascript
actions: {
  incrementAsync(context) {
    setTimeout(() => {
      context.commit('increment');
    }, 1000);
  },
  fetchUserData(context, userId) {
    // Llamada a la API
    axios.get(`/user/${userId}`)
      .then(response => {
        context.commit('setUserData', response.data);
      })
      .catch(error => {
        console.error('Error:', error);
      });
  }
}
```

### Accediendo al Store desde componentes Vue:

Puedes acceder al Store desde componentes Vue utilizando la propiedad `$store`. Por ejemplo, para acceder al estado `count`, puedes usar `$store.state.count`. Para llamar a una mutación o acción, puedes usar `$store.commit('mutationName')` o `$store.dispatch('actionName')`, respectivamente.

```html
<template>
  <div>
    <p>{{ $store.state.count }}</p>
    <button @click="$store.commit('increment')">Incrementar</button>
    <button @click="$store.dispatch('incrementAsync')">
      Incrementar Asíncrono
    </button>
  </div>
</template>
```

### Resumen:

- **Store:** Almacén centralizado que contiene el estado de la aplicación.
- **Mutations:** Funciones síncronas que modifican el estado de la aplicación de manera predecible.
- **Actions:** Funciones que desencadenan mutaciones y pueden contener lógica asíncrona.

Utilizando Store, Mutations y Actions en Vuex, puedes manejar el estado de tu aplicación de manera eficiente, segura y escalable. Esto permite una gestión centralizada del estado y una comunicación predecible entre los componentes Vue de tu aplicación.

## 5.3 - Uso de Getters

Los getters en Vuex son funciones que permiten obtener datos del estado de la aplicación de manera computada. Es decir, los getters calculan propiedades derivadas del estado de forma dinámica y pueden ser utilizados para acceder a datos del estado en formatos específicos o para realizar cálculos complejos. Aquí tienes una explicación sobre cómo utilizar los getters en Vuex:

### Definición de Getters:

En la configuración del Store de Vuex, puedes definir una sección de getters donde especificas las funciones que quieres utilizar para acceder a datos del estado de la aplicación de forma calculada.

```javascript
import Vue from "vue";
import Vuex from "vuex";

Vue.use(Vuex);

const store = new Vuex.Store({
  state: {
    todos: [
      { id: 1, text: "Comprar leche", done: false },
      { id: 2, text: "Ir al gimnasio", done: true },
      { id: 3, text: "Hacer la tarea", done: false },
    ],
  },
  mutations: {
    // Mutaciones para modificar el estado
  },
  actions: {
    // Acciones que pueden desencadenar mutaciones
  },
  getters: {
    // Getters para obtener datos del estado
    doneTodos: (state) => {
      return state.todos.filter((todo) => todo.done);
    },
    remainingTodos: (state) => {
      return state.todos.filter((todo) => !todo.done);
    },
  },
});

export default store;
```

**Uso de Getters en Componentes Vue:**

Para utilizar getters en tus componentes Vue, puedes acceder a ellos mediante la propiedad `$store.getters`. Los getters pueden ser llamados como si fueran propiedades computadas.

```html
<template>
  <div>
    <h2>Tareas Pendientes</h2>
    <ul>
      <li v-for="todo in remainingTodos" :key="todo.id">{{ todo.text }}</li>
    </ul>
    <h2>Tareas Completadas</h2>
    <ul>
      <li v-for="todo in doneTodos" :key="todo.id">{{ todo.text }}</li>
    </ul>
  </div>
</template>

<script>
  export default {
    computed: {
      doneTodos() {
        return this.$store.getters.doneTodos;
      },
      remainingTodos() {
        return this.$store.getters.remainingTodos;
      },
    },
  };
</script>
```

**Beneficios de los Getters:**

- **Reutilización:** Los getters permiten reutilizar la lógica de acceso a los datos del estado en varios componentes Vue.
- **Abstracción:** Los getters abstraen la lógica de acceso a los datos, lo que hace que los componentes sean más simples y fáciles de entender.
- **Computaciones Eficientes:** Los getters calculan propiedades derivadas de forma eficiente, ya que solo se recalculan cuando el estado subyacente cambia.

Con los getters en Vuex, puedes obtener datos del estado de tu aplicación de manera computada y dinámica, lo que facilita la manipulación y presentación de datos en tus componentes Vue.

## 5.4 - Organizacion de la estructura de Vuex

Organizar la estructura de tu Store en Vuex es crucial para mantener una aplicación clara, escalable y fácil de mantener a medida que crece en tamaño y complejidad. Aquí hay algunas prácticas comunes para organizar la estructura de un Store en Vuex:

### `Dividir el Store en Módulos`:

Cuando la aplicación crece, puede volverse difícil manejar un solo Store grande. En su lugar, divide tu Store en módulos más pequeños, cada uno enfocado en una parte específica de la lógica de la aplicación. Cada módulo puede tener su propio estado, mutaciones, acciones y getters.

Por ejemplo, podrías tener módulos para usuarios, productos, pedidos, etc.

```javascript
import userModule from "./modules/user";
import productModule from "./modules/product";
import orderModule from "./modules/order";

export default new Vuex.Store({
  modules: {
    user: userModule,
    product: productModule,
    order: orderModule,
  },
});
```

### `Archivos de Módulos Separados`:

Mantén los módulos en archivos separados para una mejor organización y mantenimiento. Cada archivo contendría el estado, mutaciones, acciones y getters relacionados con un módulo específico.

```javascript
// user.js
const userModule = {
  state: { ... },
  mutations: { ... },
  actions: { ... },
  getters: { ... }
};

export default userModule;
```

### `Nomenclatura Consistente`:

Mantén una nomenclatura consistente para los nombres de los módulos, mutaciones, acciones y getters. Esto facilita la comprensión de la estructura del Store y la navegación dentro de él.

### `Módulos Reutilizables`:

Identifica partes de tu Store que puedan ser reutilizadas en diferentes partes de la aplicación y extráelas en módulos separados para promover la reutilización del código y reducir la duplicación.

### `Documentación`:

Documenta tu estructura de Store de manera clara y concisa. Describe cada módulo, mutación, acción y getter para que otros desarrolladores (y tú mismo en el futuro) puedan entender fácilmente cómo funciona la lógica de la aplicación.

### `Pruebas Unitarias`:

Asegúrate de que tu estructura de Store sea fácil de probar mediante pruebas unitarias. Divide la lógica de tu Store en funciones puras siempre que sea posible para facilitar las pruebas y mejorar la calidad del código.

### `Evitar Anidar Demasiado Profundo`:

Evita anidar módulos o Store demasiado profundamente, ya que esto puede dificultar el mantenimiento y la comprensión de la estructura de tu aplicación.

Con una buena organización de la estructura de tu Store en Vuex, puedes mantener tu código limpio, modular y fácil de entender, lo que facilita el desarrollo y el mantenimiento de aplicaciones Vue.js más grandes y complejas.

# 6 - Desarrollo de aplicaciones avanzadas con Vue.js

## `Integracion con APIs`

Integrar Vuex con APIs es una práctica común en aplicaciones Vue.js para manejar el flujo de datos entre el cliente y el servidor de manera eficiente. Aquí te muestro cómo puedes integrar Vuex con APIs para realizar operaciones como obtener datos, enviar datos y actualizar datos en tu aplicación Vue.js:

### Definir Acciones para Interactuar con la API:

En tu Store de Vuex, define acciones que se encarguen de realizar solicitudes a la API. Estas acciones pueden usar bibliotecas como `axios` o `fetch` para realizar llamadas HTTP.

```javascript
// En el archivo store.js

import axios from "axios";

const store = new Vuex.Store({
  state: {
    todos: [],
  },
  mutations: {
    SET_TODOS(state, todos) {
      state.todos = todos;
    },
  },
  actions: {
    fetchTodos({ commit }) {
      axios
        .get("/api/todos")
        .then((response) => {
          commit("SET_TODOS", response.data);
        })
        .catch((error) => {
          console.error("Error fetching todos:", error);
        });
    },
  },
});
```

### Llamar a Acciones desde Componentes:

Desde tus componentes Vue, puedes llamar a las acciones definidas en tu Store utilizando `dispatch`.

```javascript
// En un componente Vue

export default {
  created() {
    this.$store.dispatch("fetchTodos");
  },
};
```

### Actualizar el Estado con Mutaciones:

Una vez que la API devuelve los datos, puedes actualizar el estado de la aplicación llamando a mutaciones desde las acciones.

### Enviar Datos a la API:

Para enviar datos a la API, define acciones que realicen solicitudes POST, PUT o DELETE según sea necesario. Puedes pasar datos como parámetros a estas acciones.

### Manejar Respuestas y Errores:

Asegúrate de manejar las respuestas y los errores de las solicitudes API correctamente en tus acciones. Puedes actualizar el estado de la aplicación en función de la respuesta de la API y mostrar mensajes de error al usuario si algo sale mal.

### Autenticación:

Si tu API requiere autenticación, puedes manejarla en tus acciones utilizando tokens de acceso o cookies. Puedes configurar interceptores de solicitudes HTTP para agregar automáticamente encabezados de autenticación a las solicitudes.

### Modularización:

Para mantener tu código limpio y organizado, considera modularizar tu Store de Vuex y definir acciones relacionadas con la API en módulos separados.

Con estos pasos, puedes integrar fácilmente Vuex con APIs en tu aplicación Vue.js para manejar el flujo de datos entre el cliente y el servidor de manera eficiente y robusta. Esto te permitirá crear aplicaciones web interactivas y dinámicas que puedan interactuar de manera fluida con servicios externos.

## `Optimizacion de rendimiento`

La optimización del rendimiento en una aplicación Vue.js es fundamental para garantizar una experiencia de usuario fluida y receptiva. Aquí tienes algunas estrategias y prácticas recomendadas para optimizar el rendimiento de tu aplicación Vue.js:

**1. Minimizar el tamaño del bundle:**

- Utiliza herramientas como Webpack o Parcel para dividir tu aplicación en módulos y reducir el tamaño del bundle final.
- Minimiza y comprime tus archivos CSS y JavaScript para reducir el tiempo de carga de la página.

**2. Carga diferida (Lazy Loading):**

- Utiliza la carga diferida para cargar componentes Vue.js solo cuando sean necesarios, especialmente en rutas de tu aplicación.
- Usa la función `import` de JavaScript o las opciones de carga diferida de herramientas de enrutamiento como Vue Router para implementar esta técnica.

**3. Uso eficiente de componentes:**

- Divide tu aplicación en componentes más pequeños y reutilizables para mejorar la legibilidad y el mantenimiento del código.
- Evita el exceso de componentes anidados que puedan afectar negativamente el rendimiento de la aplicación.

**4. Virtual DOM y Renderizado Reactivo:**

- Aprovecha el sistema de Virtual DOM y el renderizado reactivo de Vue.js para actualizar eficientemente el DOM solo cuando sea necesario.
- Utiliza directivas como `v-if` y `v-show` de manera apropiada para condicionalmente renderizar elementos en la interfaz de usuario.

**5. Uso de Vue DevTools:**

- Utiliza Vue DevTools para perfilar y depurar tu aplicación Vue.js. Esta herramienta te permite inspeccionar el rendimiento y el estado de los componentes en tiempo real.

**6. Optimización del renderizado:**

- Utiliza la directiva `v-for` con `key` para mejorar el rendimiento de las listas renderizadas.
- Evita los métodos computados complejos que puedan ralentizar el rendimiento de la aplicación.

**7. Caché de datos y API:**

- Implementa una estrategia de caché de datos para evitar solicitudes innecesarias a la API y mejorar el tiempo de respuesta de la aplicación.
- Utiliza herramientas como Vuex para gestionar el estado de la aplicación de manera eficiente y centralizada.

**8. Renderizado del lado del servidor (SSR):**

- Considera el renderizado del lado del servidor (SSR) para mejorar el tiempo de carga inicial y el SEO de tu aplicación Vue.js.

### Pruebas de rendimiento:

- Realiza pruebas de rendimiento utilizando herramientas como Lighthouse, WebPageTest o Chrome DevTools para identificar cuellos de botella y áreas de mejora en tu aplicación.

Al implementar estas estrategias de optimización del rendimiento, podrás crear aplicaciones Vue.js rápidas y eficientes que ofrezcan una experiencia de usuario excepcional y una respuesta receptiva.

## `Pruebas unitarias y E2E`

Las pruebas unitarias y las pruebas end-to-end (E2E) son dos aspectos fundamentales para garantizar la calidad y fiabilidad de una aplicación Vue.js. Aquí tienes una explicación sobre cada tipo de prueba y cómo se pueden implementar en tu proyecto Vue.js:

### Pruebas Unitarias:

Las pruebas unitarias son pruebas automatizadas que se centran en probar unidades individuales de código, como funciones, métodos o componentes, de manera aislada. El objetivo principal de las pruebas unitarias es verificar si cada unidad de código funciona como se espera, independientemente del resto de la aplicación.

#### Herramientas de Pruebas Unitarias:

- **Jest:** Jest es un popular marco de pruebas desarrollado por Facebook que se utiliza comúnmente para realizar pruebas unitarias en aplicaciones Vue.js.
- **Mocha:** Mocha es otro marco de pruebas popular que proporciona flexibilidad y potencia para escribir pruebas unitarias.
- **Vue Test Utils:** Vue Test Utils es una biblioteca oficial de Vue.js que proporciona herramientas para probar componentes Vue.js de manera efectiva.

#### Ejemplo de Prueba Unitaria:

```javascript
// Ejemplo de prueba unitaria utilizando Jest y Vue Test Utils
import { mount } from "@vue/test-utils";
import Counter from "@/components/Counter.vue";

describe("Counter.vue", () => {
  it("increments counter when button is clicked", async () => {
    const wrapper = mount(Counter);
    const button = wrapper.find("button");
    await button.trigger("click");
    expect(wrapper.text()).toContain("Counter: 1");
  });
});
```

### Pruebas End-to-End (E2E):

Las pruebas E2E son pruebas automatizadas que simulan la interacción del usuario con la aplicación desde el inicio hasta el final. Estas pruebas verifican si el flujo de la aplicación funciona correctamente desde la perspectiva del usuario, incluyendo la navegación, la interacción con elementos de la interfaz de usuario y la manipulación de datos.

#### Herramientas de Pruebas E2E:

- **Cypress:** Cypress es una herramienta moderna y potente para realizar pruebas E2E en aplicaciones web, incluyendo aplicaciones Vue.js.
- **Puppeteer:** Puppeteer es una biblioteca de Node.js que proporciona una API de alto nivel para controlar Chrome o Chromium a través del protocolo DevTools.
- **TestCafe:** TestCafe es un marco de pruebas E2E que permite escribir y ejecutar pruebas automatizadas en aplicaciones web sin necesidad de configuración adicional.

#### Ejemplo de Prueba E2E:

```javascript
// Ejemplo de prueba E2E utilizando Cypress
describe("Counter", () => {
  it("increments the counter", () => {
    cy.visit("/");
    cy.get("button").click();
    cy.contains("Counter: 1");
  });
});
```

### Integración con Vue.js:

Ambos tipos de pruebas se pueden integrar fácilmente en un proyecto Vue.js. Puedes configurar y ejecutar pruebas unitarias y pruebas E2E utilizando las herramientas y bibliotecas mencionadas anteriormente.

Al implementar pruebas unitarias y pruebas E2E en tu proyecto Vue.js, puedes mejorar la calidad y estabilidad de tu aplicación, detectar problemas de manera temprana y garantizar una experiencia de usuario consistente y sin errores.
