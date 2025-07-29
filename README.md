# Briefing  Tarot STEM
Con este proyecto podrás conocer a las mujeres del mundo de la ciencia y técnología, o lo que es lo mismo, las Diosas contemporaneas 👩‍🔬
> Este proyecto lo realizamos en colaboración con el equipo formativo FactoriaF5 Barcelona🌟 que ha creado esta API tan chula que ahora vamos a consumir desde React
>
> agradecimiento especial a [@MAlexGG](https://github.com/MAlexGG)

## Objetivo general  
Desarrollar una aplicación web en React que permita visualizar cartas de tarot, ver el detalle de cada una y realizar una lectura de tres cartas asignadas a pasado, presente y futuro.

---

## Nivel 1: Visualización básica de cartas

### Funcionalidad principal  
- Consumir la API pública de cartas de tarot:  
  `https://6872278c76a5723aacd3cbb3.mockapi.io/api/v1/tarot`
- Mostrar todas las cartas en una página principal, boca abajo (sin revelar el contenido).
- Al hacer clic en una carta, navegar a una página de detalle mostrando:  
  - Nombre de la carta  
  - Significado  
  - Diosa contemporánea asociada  

### Requisitos técnicos  
- React con `react-router-dom` para navegación con createBrowserRouter.  
- Lógica para hacer la petición de cartas en un archivo `services.js`.  
- Uso de hooks `useEffect` y `useState` para gestionar estado y efectos.  

---

## Nivel 2: Lectura de cartas (Pasado, Presente, Futuro)

### Funcionalidad principal  
- Crear una página para “Echar las cartas”.   
- Permitir al usuario seleccionar **solo tres cartas**, asignándolas a las posiciones:  
  1. Pasado  
  2. Presente  
  3. Futuro  
- Al seleccionar cada carta, mostrar su significado y la diosa contemporánea asociada, según la posición.  
- Prevenir que se puedan elegir más de tres cartas.  
- Permitir reiniciar la lectura para comenzar de nuevo.  

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

# Campos detallados
| Campo              | Tipo     | Descripción                                                                                         |
|--------------------|----------|-------------------------------------------------------------------------------------------------|
| `id`               | string   | Identificador único de la carta.                                                                 |
| `arcaneNumber`     | string   | Número asociado a la carta dentro del arcano (puede ser "0", "1", etc.).                         |
| `arcaneName`       | string   | Nombre de la carta del tarot (por ejemplo, "El Loco").                                           |
| `arcaneDescription`| string   | Descripción o significado de la carta en términos esotéricos y simbólicos.                       |
| `arcaneImage`      | object   | Objeto con información de la imagen de la carta:                                                |
| &nbsp;&nbsp;&nbsp;&nbsp;`imageSrc` | string   | URL con la imagen que representa la carta.                                                       |
| &nbsp;&nbsp;&nbsp;&nbsp;`author`   | string   | Nombre del autor o fuente de la imagen.                                                         |
| &nbsp;&nbsp;&nbsp;&nbsp;`license`  | string   | Información sobre la licencia de uso de la imagen.                                              |
| `goddessName`      | string   | Nombre de la diosa contemporánea asociada simbólicamente a la carta.                             |
| `goddessDescription`| string  | Descripción o biografía breve de la diosa contemporánea.                                        |
| `goddessImage`     | object   | Objeto con información de la imagen de la diosa:                                                |
| &nbsp;&nbsp;&nbsp;&nbsp;`imageSrc` | string   | URL con la imagen de la diosa.                                                                   |
| &nbsp;&nbsp;&nbsp;&nbsp;`author`   | string   | Nombre del autor o fuente de la imagen de la diosa.                                             |
| &nbsp;&nbsp;&nbsp;&nbsp;`licenseUrl`| string  | URL que apunta a la licencia bajo la cual está publicada la imagen de la diosa.                 |


