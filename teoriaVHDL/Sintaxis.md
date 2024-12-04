# Sintaxis
- Fin de linea `;` al acabar instrucciones.
- Sensibilidad: VHDL no es sensible a mayúsculas y espacios
```vhdl
S1 <= A and B;
s1 <= a AnD        B;
```
- Comentarios: poniendo 2 guiones
```vhdl
--Comentario
```
- Paréntesis: se ponen por claridad, las operaciones tienen prioridad establecida.
- Identificadores: nombres válidos e inválidos para señales y puertos en VHDL.
- Palabras reservadas: NO pueden ser identidicadores en VHDL.
- Caracteres: se definen entre comillas simples 'A', 'a', '1', 'O'
- Cadenas de caracterese: se definen entre comillas dobles "Una cadena", "1010"
- Cadena de bits: se escribe la base seguida de la cadena de caracteres:
```vhdl
--Binario
B"1010"
--Hexdecimal
X"FA0"
--Octal
O"372"
--Decimal
D"23"
```

### Tipos en VHDL
- `std_logic;` valor presente en un cable de 1 bit
- `std_logic_vector;` para definir buses de datos (vector de bits)






















