## Plan de ataque 
1- Al abrir el archivo html en el navegador, al momento de ingresar un número no realizaba ninguna acción. 
2- Revisando el codigo del script, en las funciones estaban mal escritas los eventos, al momento de dar clic que son los que hacen la accion de ingresar el número: 
como estaba escrito: addeventListener
corrección: addEventListener
estos eventos mal escritos se encuentran en las funciones: checkGuess y setGameOver
3- cuando se ingresaba los numeros se percato que el código que generaba los numeros aleaorios estaba en el rango de decimales del 1 al 10, segun el caso de uso son numeros enteros del 1 al 100 el rango.
Corrección:  let randomNumber = Math.floor(Math.random () * 100) + 1;
4- Seleccion incorrecta del elemento lowOrHi, 
correción:.lowOrHi
5- Al momento de realizar esta correción, al ingresar el número si lo mostraba pero no guardaba los anteriores solo mostraba los que se iban digitando. 
corrección: let userGuess = parseInt(guessField.value), ya que la comparacion de randomNumber es un número con userGuess que estaba definido como un String
6- al realizar estos cambios, los mensajes en la parte de las condiciones no coincidian, ya que mostraba el mensaje de '!!!Pérdistes!!!' aun cuando el primer número no coincidia.
Correccion: mensajes definidos correctamentes en las condiciones
7- en la funcion de resenGame, tenia el mismo rango de numeros generados de manera random entre 0-10
correción: randomNumber = Math.floor(Math.random() * 100) + 1;
8- Los intentos definidos en el codigo inical son de 5.
Corrección: const ATTEMPS = 10;
 