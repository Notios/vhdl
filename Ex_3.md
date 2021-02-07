#### If - elsif - else

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.all;

entity Exercise is port (
	A, B, C : in STD_LOGIC;
	Y : out STD_LOGIC);
end Exercise;

architecture EX_BEH of Exercise is
begin
	process (A, B, C) begin
		if (A = '0') and (B = '0')then Y <= '1';
		elsif (C = '1') then Y <= '1' ;
		else Y <= '0';
		end if;
	end process;
end EX_BEH;
```
#### Schematic
![alt text](https://github.com/Notios/vhdl/blob/main/images/Ex_3.PNG "Ex_3")
