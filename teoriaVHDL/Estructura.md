# Estructura en VHDL
### Introducción
- Librerías: se añaden en el encabezado para incluir otros circuitos, constantes, etc.
- Entidad: describe nuestro circuito como una `caja negra`con sus puertos y E/S(entradas y salidas)
- Arquitectura: describe el `contenido`de la caja negra y su Comportamiento/ Estructura

Ejemplo:
```vhdl
library ieee;
use ieee.std_logic_1164.all;

entity mux2_1 is
  port (a : in std_logic;
        s : in std_logic;
        y : out std_logic;
        b : in std_logic;
      );
  end mux2_1;

arquitecture behavior of mux2_1 is
  begin
      y <= a when(s = '0') else b;
  end behavior;
```

## Librerias
- Una librería es un conjunto de paquetes.
- Hay que especificar los paquetes que usamos de la librería, no vale solo con incluirla.

```vhdl
library ieee; --libreria
use ieee.std_logic_1164.all;  --paquete de la libreria
```

## Enity "caja negra"
- La entidad describe cómo se conecta el componente a otros diseños (otros niveles de jerarquia)
- Puede contener los siguientes campos:
  - **Ports**: son los puertos de E/S que permiten que el componente se conecte con otros.
  - **Generics**: permite definir parámetros del componente de modo que no sea nev¡cesario repetir su definición.
  - **Constants**: permite definir constantes que se utilizarán en la arquietctura del componente.

```vhdl
entity ejemplo is
  port (in1 : in std_logic;
        in2 : in std_logic;
        out1 : out std_logic
        );

  generic ( gen1 : integer := 4;
            gen2 : time := 10ns
          );

  constant : cnst1 : real := 1000.0;

end ejemplo;
```








