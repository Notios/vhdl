### Register-transfer level (RTL)
#### Παράδειγμα δημιουργίας ενός απλού λογικού κυκλώματος

```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity Ex_1 is
	port( 
	   swt   : in std_logic_vector (3 downto 0);
	   led_0 : out std_logic);
end Ex_1;

architecture Behavioral of Ex_1 is
signal t1, t2 : std_logic;
begin
    t1 <= swt(3) xor swt(2);
	t2 <= swt(1) xor swt(0);
	led_0 <= t1 xor t2;

end Behavioral;
```
#### Schematic
![alt text](https://github.com/Notios/vhdl/blob/main/Ex_1.PNG "Ex_1")
