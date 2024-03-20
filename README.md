# Mensajeros de película

Inspirado en [Wollok Team](https://github.com/wollok/polimorfismoColeccionesMensajerosDePelicula)

### Ejercicio incremental: Polimorfismo - Colecciones - Colecciones con bloques 
## Parte 1: Destinos y mensajeros

Steven Spilberg está por cumplir años y quiero realizarle un regalo. Por eso compré un álbum de figuritas de ET y lo envolví en un paquete para ser entregado por una empresa de mensajería, que ofrece un menú de distintos mensajeros de película para llevar un paquete a distintos lugares.

No estoy seguro del lugar en el cual está Steven, es posible que ande paseando por Brooklyn o esté haciendo de las suyas en la Matrix.

La empresa utiliza un sistema desarrollado en objetos para poder determinar qué mensajero
podrá llevar mi paquete.

Por lo tanto, el primer requerimiento es determinar si mi paquete puede ser entregado por un mensajero en determinado lugar. Pero cumplir el objetivo no es tan sencillo, porque hay varias reglas que cumplir.

1. Por empezar, para que el paquete pueda ser entregado, debe estar pago.

2. Luego, cada destino le pone restricciones a los mensajeros que quieren llegar a él. Existen dos destinos posibles:
El puente de Brooklyn (único acceso a Brooklyn para los mensajeros): deja pasar a todo lo que pese hasta una tonelada (1000 kilos).
La Matrix: deja entrar a quien pueda hacer una llamada.

3. Por el momento, nuestra empresa de mensajería tiene 3 mensajeros, con éstas características:
- Chuck Norris: Chuck norris siempre pesó y seguirá pesando 900 kg por toda la eternidad. Puede llamar a cualquier persona del universo con sólo llevarse el pulgar al oído y el meñique a la boca.
- Neo: vuela, así que no pesa nada. Y anda con celular, el muy canchero. El tema es que a veces no tiene crédito.
- Lincoln Hawk: Su peso varía con el tiempo. Viaja en bicicleta ó camión. Si viaja en bicicleta, el peso que cuenta es el suyo propio + 10kg por la bici. Si viaja en camión, su peso propio más media tonelada (peso del camión)  más media tonelada adicional por cada acoplado. Hawk no tiene un mango, gracias que tiene cubiertas, y no puede llamar a nadie.

**Aclaraciones**

Para el cálculo del peso, el peso del paquete es despreciable.
Se recomienda implementar un objeto “paquete” que entienda el mensaje:
paquete.podesSerEntregado(unaPersona, unLugar)
Pensar cómo inicializar todos los objetos implicados antes de usarlo.


**Condiciones para comprobar el funcionamiento en el main**

Mi paquete que no está pago no puede ser llevado por Neo a la Matrix.
Mi paquete que sí está pago puede ser llevado por Chuck a la Matrix.
Mi paquete que sí está pago no puede ser llevado por Lincoln Hawk (80kg) a Brooklyn si es que utiliza un camión con un acoplado.
La entrega anterior puede hacerse si Lincoln Hawk usa una bicicleta.


