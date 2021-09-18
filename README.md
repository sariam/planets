# Planets
---

Planets es una aplicación que descarga una lista con información acerca de planetas, valiendose de la api pública [API APOD](https://apodapi.herokuapp.com/).

La aplicación contines está compuesta por cuatro módulos.

## Home
---

Vista principal. 

Al entrar en la vista veremos un idicador de carga mientras el viewModel está descargando la lista. Una vez tiene la lista, esconde el indicador y muestra la tabla. 

Con la variable `let NUMBER_OF_ITEMS = 10` indicamos el número de items a listar. Hemos puesto 10 para que vaya más rápido.

- Si deslizamos una celda a la izquierda, veremos que nos sale la opción de eliminar. Hay un alert para confirmar la acción.
- Si deslizamos a la derecha, veremos la opción de editar. Ésta nos llevará a otra vista donde podremos modificar la información.
- Si estiramos la tabla hacia abajo volverá a actualizar la lista llevándola a su estado original.
- En la barra de navegación tenemos un título y un botón para añadir un nuevo item.

## FormPlanet
---

- Si `var index: Int?` contiene un índice, nos indica que estamos en modo editar. De lo contrario estamos creando un nuevo item.
- El botón de continuar sólo está habilitado si el item tiene todos los campos completos.  
- Si pulsamos sobre la imagen, podremos seleccionar una de la galería o tomar una foto. En esta primera versión no se está almacenando esta imagen en ningún sitio por lo que al salir de la vista perderemos la imagen

## DetailPlanet
---

Vista en la que podemos ver toda la información del item, incluida su descripción.

Si pulsamos sobre la imagen, iremos al módulo de ZoomPlanet

## ZoomPlanet
---

Hemos mostrado esta vista en un modal y no dentro de la navegación, sólo cono ejemplo de como abrir otra vista de una forma distinta aunque no es del todo práctica con el zoom.

En este módulo podemos hacer zoom sobre la imagen con el gesto de pinza o con dos toques para hacer zoom y nuevamente dos toques para volver al estado original.
