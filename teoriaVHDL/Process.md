# Process
- Construcción que nos permite ejecutar instrucciones de forma secuencial.
- En el process las instrucciones se ejecutan de forma secuencial.
- Fuera del process las instrucciones se siguen ejecutando en paralelo.
- Si hay varios process, se ejecutan en paralelo entre ellos.
- El tiempo solo avanza al fianalizar el process.
- Las señales modelan hilos, sólo pueden cambiar si avanza el tiempo.
- Los procesos se disparan cuando cambia alguna señal de su lista sensibilidad.

### Ejemplo
```vhdl
p_process_name : process (lista_de_sensibilidad) is
  --declaracion de señales y variables
begin
  --instrucciones secuenciales
end p_process_name;
```

### XOR usando asignación concurrente
```vhdl
--libreria
library ieee;
use ieee.std_logic_1164.all;

--entidad
entity my_xor is
  port(
      a, b : in std_logic;
      f : out std_logic;
      );
end my_xor;

--arquitectura
arquitecture dataflow of my_xor is
begin
    f <= a xor b;
end dataflow;
```

### XOR usando process
```vhdl
--libreria
library ieee;
use ieee.std_logic_1164.all;

--entidad
entity my_xor is
  port(
    a,b : in std_logic;
    f : out std_logic
      );
end my_xor;

--arquitectura
arquitecture Behavior of my_xor is
begin
    xor_proc : process(a,b) is
    begin
      f <= a xor b;
    end process xor_proc;
end Behavior;
```

### Ejemplo - For loop
```vhdl
arquitecture my_sol of my_example is
    signal a, b : std_logic_vector (7 downto 0);

begin
  my_proc : process(a, b)
begin
  for ii in 0 to 7 loop
    if ii < 3 then
      c(ii) <= a(ii) and b(ii);
    else
      c(ii) <= a(ii) or b(ii);
    end if;
  end loop;
end process my_proc;
end my_sol;
```




