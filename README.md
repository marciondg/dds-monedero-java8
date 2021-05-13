## Monedero

### Contexto

Este repositorio contiene el código de un _monedero virtual_, al que podemos agregarle y quitarle dinero, a través 
de los métodos `Monedero.sacar` y `Monedero.poner`, respectivamente. 
Pero hay algunos problemas: por un lado el código no está muy bien testeado, y por el otro, hay numeros _code smells_. 

### Consigna

Tenés seis tareas: 

 1. :fork_and_knife: Hacé un _fork_ de este repositorio (presionando desde Github el botón Fork)
 2. :arrow_down: Descargalo y construí el proyecto, utilizando `maven`
 2. :nose: Identificá y anotá todos los _code smells_ que encuentres 
 3. :test_tube: Agregá los tests faltantes y mejorá los existentes. 
     * :eyes: Ojo: ¡un test sin ningún tipo de aserción está incompleto!
 4. :rescue_worker_helmet: Corregí smells, de a un commit por vez. 
 5. :arrow_up: Subí todos los cambios a tu _fork_

### Code Smells encontrados

- Duplicated Code: Código duplicado en métodos de la misma clase.
```    
Cuenta.java:32 :42
  if (cuanto <= 0) {
  throw new MontoNegativoException(cuanto + ": el monto a ingresar debe ser un valor positivo");
  }
```

- Long Parameter List: Se puede pasar directamente el Movimiento directamente como parámetro
```
Cuenta.java:57
  public void agregarMovimiento(LocalDate fecha, double cuanto, boolean esDeposito) {
    Movimiento movimiento = new Movimiento(fecha, cuanto, esDeposito);
    movimientos.add(movimiento);
  }
```


  


