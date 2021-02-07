#### Minority

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.all;

entity minority is
	port (
		a, b, c: in STD_LOGIC;
		Y: out STD_LOGIC);
end minority;

architecture synth of minority is
begin
	y <= (not a ant not b) or (not a and not c) or (not b and not c);
end synth;
```
#### Schematic
![alt text](https://github.com/Notios/vhdl/blob/main/images/Ex_4.PNG "Ex_4")
