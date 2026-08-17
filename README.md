# Akropolis · Planilla de puntos

Planilla web para sumar los puntos de una partida de **Akropolis** (Jules Messaud, ilustración de Pauline Détraz, Gigamic). Pensada para usarse en el celular, sobre la mesa, al terminar la partida.

🔗 **[akropolis-scorepad.vercel.app](https://akropolis-scorepad.vercel.app/)**

## Qué hace

- 1 a 4 jugadores, con nombres.
- Para cada color cargás **la suma de niveles** de los distritos que puntúan y **cuántas plazas** tenés. La app aplica las estrellas de cada plaza y hace la multiplicación.
- Suma las **piedras** sobrantes (1 punto cada una) y resuelve el **desempate** por piedras.
- Modo **Variantes ×2**, con las cinco condiciones de la carta de referencia.
- Ranking en vivo y tabla de detalle auditable, con el multiplicador ya resuelto.
- Te avisa si cargaste distritos de un color pero ninguna plaza (ese color suma 0, el error más común).
- Dos temas: **mármol** para jugar de día y **noche** para poca luz.
- Recordatorio de reglas, cantidades de piezas por número de jugadores y la carta de referencia ampliable.

## Cómo se puntúa

Cada color se puntúa por separado:

```
suma de niveles × estrellas de plazas
```

Cada distrito vale tantos puntos como el nivel en el que está (nivel 1 → 1 pt, nivel 3 → 3 pts). Cada plaza vale una cantidad fija de estrellas según su color, y se acumulan. Las plazas **no** valen más por estar en alto. Sin plaza de un color, ese color vale 0.

| Color | Cuenta | ★ por plaza |
|---|---|---|
| Casas | por cada casa en el grupo conectado más grande | 1★ |
| Mercados | por cada mercado aislado | 2★ |
| Cuarteles | por cada cuartel en un borde | 2★ |
| Templos | por cada templo completamente rodeado | 2★ |
| Jardines | por cada jardín | 3★ |
| Canteras | +1 piedra cada vez que cubrís una | — |

Con las variantes activas, cada distrito que cumple su condición vale el doble: cargás en el campo **×2** la suma de niveles que se duplica, y el color pasa a valer `(niveles + duplicados) × estrellas`.

## Estructura

```
index.html     todo el sitio: HTML, CSS, JS e imágenes en base64
favicon.svg    ícono
og.jpg         imagen de la tarjeta al compartir el link
vercel.json    cabeceras de caché y seguridad
```

Un solo archivo, sin dependencias, sin build. Las imágenes van embebidas en base64, así que la página funciona sin conexión una vez cargada.

## Créditos

Reglas, arte e imágenes son de **Akropolis** — Jules Messaud, ilustración de Pauline Détraz, editado por Gigamic. Las fotos provienen de la [ficha del juego en Maldón](https://maldon.com.ar/blog/projects/akropolis/), su distribuidor en Argentina, y se usan aquí de forma no comercial a modo de referencia.

Planilla no oficial, hecha para la mesa por [Agustín](https://x.com/aciampagna).
