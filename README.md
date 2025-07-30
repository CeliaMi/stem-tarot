# Briefing  Tarot STEM
Con este proyecto podrás conocer a las mujeres del mundo de la ciencia y tecnología, o lo que es lo mismo, las Diosas contemporaneas 👩‍🔬
> Este proyecto lo realizamos en colaboración con el equipo formativo FactoriaF5 Barcelona🌟 que ha creado esta API tan chula que ahora vamos a consumir desde React
>
> agradecimiento especial a [@MAlexGG](https://github.com/MAlexGG)

## Objetivo general  
Desarrollar una aplicación web en React que permita visualizar cartas de tarot, ver el detalle de cada una y para aquellas personas que quieran dar un paso más, realizar una lectura de tres cartas asignadas a pasado, presente y futuro.

---

## Nivel 1: Visualización básica de cartas

### Funcionalidad principal : Consumir la API pública de cartas de tarot:  
  [https://6872278c76a5723aacd3cbb3.mockapi.io/api/v1/tarot](https://6872278c76a5723aacd3cbb3.mockapi.io/api/v1/tarot)
  
- 1️⃣ Mostrar todas las cartas en una página principal, boca abajo (sin revelar el contenido):

   > 👉 Hacer un GET de todas las cartas y mostrarlas en pantalla
  
   > 👉 Hooks que necesitamos: `useEffect` y `useState`

  
- 2️⃣ Al hacer click en una carta, navegar a una página de detalle mostrando más información sobre las cartas:
  
  > 👉 Hacer una petición GET por ID de cada carta y mostrar la información en pantalla
  
  > 👉 Hooks que necesitamos:  `useParams`, `useEffect`, y `useState`



### Recomendaciones técnicas  
- React con `react-router-dom` para navegación con createBrowserRouter.  (archivo router.jsx)
- Lógica para hacer la petición de cartas en un archivo  separado `services.js`.  
- Uso de hooks `useEffect` y `useState` para gestionar estado y efectos.  

---

## Nivel 2: Lectura de cartas (Pasado, Presente, Futuro)

### Funcionalidad principal : Crear una página para “Echar las cartas”.   

- 1️⃣ Permitir al usuario seleccionar **solo tres cartas**, asignándolas a las posiciones: **Pasado, Presente, Futuro.**
     
  > 👉 Prevenir que se puedan elegir más de tres cartas.
     
- 2️⃣ Al seleccionar cada carta, mostrar su significado y la diosa contemporánea asociada, según la posición.
    
    
  > 👉 Permitir reiniciar la lectura para comenzar de nuevo.  

### Requisitos técnicos  
- Reutilizar la lógica y componentes del nivel 1 para mostrar cartas.  
- Gestionar estado para las cartas seleccionadas y sus posiciones.  
- Visualización clara y diferenciada de las cartas asignadas a cada posición.  

---

## Consideraciones generales  
- Mantener código modular, limpio y bien documentado.  
- La UI debe ser intuitiva y clara para facilitar la selección de cartas.  
- Evitar recargas innecesarias y optimizar las peticiones a la API.  
---

# Documentación de la estructura de cartas del API de Tarot
Cada elemento del array representa una carta del tarot y tiene la siguiente estructura:

```json
{
  "id": "1",
  "arcaneNumber": "0",
  "arcaneName": "El Loco",
  "arcaneDescription": "Descripción detallada del significado de la carta.",
  "arcaneImage": {
    "imageSrc": "URL de la imagen de la carta",
    "author": "Autor de la imagen",
    "license": "Licencia de uso"
  },
  "goddessName": "Nombre de la diosa contemporánea asociada",
  "goddessDescription": "Descripción biográfica o información relevante sobre la diosa contemporánea.",
  "goddessImage": {
    "imageSrc": "URL de la imagen de la diosa",
    "author": "Autor de la imagen",
    "licenseUrl": "URL de la licencia de uso"
  }
}
```



