# 🔎​ Conoce el Entorno de Desarrollo de Unity

[![GitHub Profile](entorno-desarrollo-unity.png)](https://github.com/devTever)

## 1) Actualización de Unity y versión con la que vamos a trabajar
- Comienza mostrando el **Unity Hub**.  
- Explica brevemente la importancia de tener Unity actualizado.  
- Indica la **versión que usarás en el curso/proyecto** (ejemplo: *Unity 2022 LTS*), destacando que es estable y recomendada para aprendizaje.  
- 👉 Consejo: comenta que se puede instalar más de una versión para distintos proyectos.

---

## 2) Crear un nuevo proyecto
- Abre Unity Hub → **New Project**.  
- Elige la plantilla **2D** o **3D** (según lo que uses para este ejercicio).  
- Ponle nombre (ejemplo: *ProyectoVentanasUnity*).  
- Selecciona la carpeta donde guardar y haz clic en **Create Project**.  

---

## 3) Espacio de trabajo de Unity con sus lugares
Muestra y explica las **ventanas principales**:  
- **Scene (Escena):** donde colocamos y organizamos objetos.  
- **Game (Juego):** vista previa de cómo se verá al ejecutar.  
- **Hierarchy (Jerarquía):** lista de todos los objetos de la escena.  
- **Inspector:** donde editamos las propiedades del objeto seleccionado.  
- **Project:** donde están los archivos del proyecto (scripts, imágenes, sonidos, etc.).  
- **Console:** mensajes, errores y avisos.  

👉 Consejo: recalca que las ventanas se pueden mover y reorganizar.

---

## 4) Ejemplo sencillo de un texto con un botón
1. **Crear UI básica**:  
   - Menú `GameObject → UI → Text (TMP)` → aparecerá un texto.  
   - Cámbialo en el Inspector a: **"Hola, toca el botón"**.  
   - Ajusta la posición para que quede visible.  

2. **Crear botón**:  
   - `GameObject → UI → Button (TextMeshPro)`  
   - Cambia el texto del botón a “Tocar”.  

3. **Crear script**:  
   - En la carpeta *Scripts* → `BotonTexto.cs`
     
   ```csharp
   using UnityEngine;
   using TMPro;   // Necesario para usar TextMeshPro
   using UnityEngine.UI;

   public class BotonTexto : MonoBehaviour
   {
       public TMP_Text mensaje;

       public void CambiarTexto()
       {
           mensaje.text = "Has tocado el botón";
       }
   }
   ```

4. **Configurar**:  
   - Arrastra el script al botón.  
   - En el componente, asigna el objeto **Texto** en la variable `mensaje`.  
   - En el botón → `OnClick()` → arrastra el botón y selecciona `BotonTexto → CambiarTexto()`.  

---

## 5) [Recomendación] Tener Visual Studio Code como editor de código
- Explica que es ligero y rápido.  
- Instalar **Visual Studio Code** desde su web oficial.  
- Plugins recomendados:  
  - *C#* (de Microsoft)  
  - *Unity Tools*  
  - *Debugger for Unity*  
  - *Unity Snippets* (atajos de código)  

---

## 6) Probar el ejercicio
- Vuelve a Unity.  
- Haz clic en **Play ▶️**.  
- Muestra el texto inicial: *“Hola, toca el botón”*.  
- Haz clic en el botón y que cambie a: *“Has tocado el botón”*.  
