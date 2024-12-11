# Decisiones
## if - then - else
```vhdl
if(a = b) then
  out1 <= 1;
elsif(a > b) then
  out1 <= 2;
else
  out1 <= 0;
end if;
```

## case - when
```vhdl
case a is
  when '0' =>
    out1 <= 1;
  when '1' =>
    out1 <= 2;
  when others =>
    out1 <= 0;
end case;
```

# Bucles
## for
```vhdl
signal a : std_logic_vector (7 downto 0)
for i in 0 to 7 loop
    a(i) <= '1';
end loop;
```
