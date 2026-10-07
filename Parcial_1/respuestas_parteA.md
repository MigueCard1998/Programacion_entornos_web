1.Un usuario reporta: «la página carga, pero las imágenes salen rotas». En DevTools → pestaña Network, las
peticiones de las imágenes muestran el estado 404 .
(a) ¿Qué significa exactamente ese 404 ? ¿El problema está del lado del cliente o del servidor? Justifica.
R= Significa que no se encuentra el recurso el error esta del lado del cliente

(b) ¿Qué dato de la petición fallida revisarías primero para encontrar la causa, y con qué lo compararías?
R=Revisaria la Url y la ruta de la ubicacion del archivo para

2. HTML semántico
Reescribe este fragmento con las etiquetas semánticas correctas y justifica dos de tus decisiones.
--Ejemplo
<div class="top">
<div class="logo">Mi blog</div>
</div>
<div class="links">...</div>
<div class="post">
<div class="titulo-grande">Mi
viaje</div>
<p>...</p>
</div>
--Correccion
<header>
  <h1>Mi blog</h1>
</header>
<nav>…</nav>
<article>
  <h2>Mi viaje</h2>
  <p>…</p>
</article>
__justificacion
Lo hago de esta manera ya que la etiqueta header con h1 da una mejor descripcion al usuario de la pagina a visitar
en la segunda parte se cambia por un nav ya que en este se añaden los enlaces de navegacionn para el usuario y titulo grande por un h2 ya que es mejor presentacion de la pagina

3. Especificidad: ¿qué regla gana?
p { color: black; }
#zona p { color: green; }
.destacado { color: orange; }
p.destacado { color: purple; }

<div id="zona">
<p class="destacado">Texto</p>
</div>

(a) ¿De qué color se ve «Texto»? Explica por qué, calculando la especificidad de las reglas que aplican.

R= Gana el color verde por el #que la hace ser prioritaria

(b) Si se elimina la regla #zona p , ¿de qué color queda y por qué?
Despues quedaria morado por el orden de especificidad 

Una caja tiene width: 300px; padding: 24px; border: 2px solid; margin: 16px;
(a) Calcula el ancho visible de la caja (borde a borde, sin contar el margin) con box-sizing: content-box y
con box-sizing: border-box . Muestra la operación.

Modo	       |Operación	                            | Ancho visible
content-box	   | 300 + (24 × 2) + (2 × 2) = 300 + 48 + 4	|352px
border-box	   |El width ya incluye padding y borde	    |300px


(b) ¿Por qué el curso pone *, *::before, *::after { box-sizing: border-box; } como primera línea de
toda hoja de estilos?

R=Porque así el width incluye el padding y el borde, y la caja mide exactamente lo que le pones. Con content-box el padding y el borde se suman por fuera y la caja crece, lo que daña los diseños. Se aplica a *, ::before y ::after para que lo cumplan todos los elementos, incluidos los pseudo-elementos.

5. Flexbox, Grid y responsive 10%
Una grilla de productos debe mostrar 1 columna en el celular y hasta 4 en escritorio. Dos estudiantes proponen:

/* Propuesta A */
.grilla { display: flex; flex-wrap: wrap; gap:
16px; }
.tarjeta { flex: 1 1 250px; }

/* Propuesta B */
.grilla {
display: grid; gap: 16px;
grid-template-columns:
repeat(auto-fit, minmax(250px, 1fr));
}

(a) ¿En qué situación visible se comportan distinto las dos propuestas? Descríbela (puedes dibujarla).
R= Se comportarian diferente al ampliarla hasta que se puedan ver las 4 tarjetas en el escritorio 
la quinta quedaria de tod el ancho de la pantalla en flex mientras que en grid conservaria un tamaño igual a las demas en la primera columna
(b) ¿Cuál usarías para una grilla uniforme de tarjetas y por qué?
Usaria grid ya que lo que se pide es un tamaño uniforme de las tarjetas este me permite que todas conserven las mismas caracteristicas al momento de ampliar o reducir la pantalla.

