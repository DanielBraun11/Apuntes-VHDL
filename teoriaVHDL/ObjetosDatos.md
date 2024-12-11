# Objetos de Datos
### Constantes
Se utilizan cuando se necesita un valor estático. 
Ej. inicializar registros con un valor predefinido o para comparar señales con un valor constante.

```vhdl
constant a : integer := 1;
constant b : std_logic := '0';
constant c : real := 0.123;
```

### Señales
Se itilizan para definir conexiones esternas(cables) del diseño. 
Ej. entradas/salidas de un módulo que se conectan con otros modulos.

```vhdl
signal sig1 : integer := 0;     
signal sig2 : integer := '0';
sig1 <= 14;
sig <=sig1;  
```

### Variables
Son los valores internos dentro de un proceso.

```vhdl
variable var1 : integer := 0;
variable var2 : integer := 1;
var1 := var2;
```

# Asignación Condicional
Forma general
```vhdl
<target> <= <expresion> when <condicion> else
            <expresion> when <condicion> else
            expresion>
```

### Ejemplo:
Arquitectura VHDL que implemente la función: 
F3 = (LM)'N + LM

```vhdl
f3 <= '1' when l = '0' and m = '0' and n = '1'
      else
      '1' when l = '1' and m = '1'
      else
      '0';
```


