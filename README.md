# ArredondoGarridoLaura
Ejercicio Funko, Laura Garrido Arredondo
![image](https://github.com/Vanelota/ArredondoGarridoLaura/assets/132077920/b691bf13-bfaa-49a5-9f63-259d66a8915f)
<br>
<p>Primero esto es la base de mi respositorio.</p>
<h1>Tenemos en la carpeta src/main:</h1>
<b>-CSV:</b>
<p>Dentro de esta carpeta esta el fichero de funkos csv</p>
<b>-->Carpeta java (Donde se encuentra la codificación)</b>
<br>
<b>-Carpeta adaptador:</b>
<p>Dentro de esta carpeta esta el fichero encargado de que no de problemas el LocalDate a la hora de leer o crear el fichero json de Funkos.</p>

![image](https://github.com/Vanelota/ArredondoGarridoLaura/assets/132077920/80d1d8e7-c6e0-440d-9bef-d7e8c6c91abf)
<ul>
  <p>Formato de Fecha y Hora:</p>
  <li>La clase utiliza `DateTimeFormatter` para especificar el formato en el que se deben representar las fechas `LocalDate` cuando se conviertan a JSON. El formato utilizado es "yyyy-MM-dd" para mayor entendimiento.</li>
  <p>Método write</p>
<li>El método `write` se encarga de convertir un objeto `LocalDate` en una cadena JSON y escribirlo en un `JsonWriter`.</li> 
<li>Si el valor del `LocalDate` es nulo, se llama a `out.nullValue()` para representarlo como un valor nulo en JSON y asi evitar problemas.</li>
<li> Si el valor de `LocalDate` no es nulo, se utiliza el formateador para convertirlo en una cadena con el formato especificado y se escribe en el `JsonWriter`.</li>
  <p>Método read</p>
<li>El método `read` se encarga de convertir una cadena JSON en un objeto `LocalDate` al leer desde un `JsonReader`.</li>
   <li>Comienza comprobando si el próximo token en el `JsonReader` es un valor nulo y Si es así, significa que el valor de `LocalDate` en JSON es nulo.</li>
  <li>Si el próximo no es un valor nulo, se lee la cadena JSON que representa la fecha utilizando `in.nextString()`, y luego se utiliza el formateador para convertirla en un objeto `LocalDate` utilizando `LocalDate.parse(dateStr, formatter)`.</li>
</ul>

<b>-Carpeta Crud: </b>
<p>Dentro de esta carpeta se encuentran los ficheros para poder hacer el crud de Funko, con una interfaz y las clases Repositorio y Servicio que se encargaran de manejar los crud y find by nombre y id.</p>
<b>-Carpeta database:</b>
<p>Esta carpeta esta encargada de crear la base de datos, con sus propiedades, configuracion y su manejador de problemas.</p>
<b>-Carpeta model:</b>
<p>En esta carpeta se encontrara el fichero Funko del cual sera la base para funko y sus propiedades establecidas. Junto con el Main de la clase, del cual inicializara las busquedas.</p>
<b>-Fichero Leercsv:</b>
<p>Se encargará de leer el fichero csv de funkos.</p>
<b>-Fichero write Json:</b>
<p>Se encargará de escribir el json de funkos.</p>
<b>-Carpeta Json donde estara el json de Funkos.</b>
<b>-Carpeta resources</b>
