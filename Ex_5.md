#### JK-Flip-Flop (w/ mux 4-to-1)

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity JKFF is
port (
        CLK, A, B, D  : in STD_LOGIC;
        Q             : out STD_LOGIC
      );
end JKFF;

architecture JKFF_BEH of JKFF is

signal Q_in : std_logic;
	begin
	process(CLK)
		variable AB: std_logic_vector(1 downto 0);
		begin
			if (CLK = '1' and CLK'event) then
				AB := A & B;
				case AB is
					when "00" => Q_in <= Q_in;
					when "01" => Q_in <= not Q_in;
					when "10" => Q_in <= '0';
					when "11" => Q_in <= D;
					when others => null;
				end case;
			end if;
	end process;
	Q <= Q_in;
end JKFF_BEH;
```
#### Schematic
![alt text](https://github.com/Notios/vhdl/blob/main/images/Ex_5.PNG "Ex_5")
