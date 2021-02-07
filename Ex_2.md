#### D Latch

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.all;

entity D_LATCH is
	port (
		CLK, D : in STD_LOGIC;
		Q : out STD_LOGIC);
end D_LATCH;

architecture D_LATCH_BEH of D_LATCH is
begin
	process (CLK, D)
	begin
		if (CLK = '1') then
			Q <= D;
		end if;
	end process;
end D_LATCH_BEH;
```
#### Schematic
![alt text](https://github.com/Notios/vhdl/blob/main/images/Ex_2.PNG "Ex_1")
