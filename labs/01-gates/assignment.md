# Lab 1: Josef Macek

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

   ![image](https://user-images.githubusercontent.com/99491847/155221528-cb4a2d40-4d63-4563-b203-b8e4e7aaab79.png)

2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of demorgan is
begin
    f_org_o  <= (not(b_i) and a_i) or (not(c_i) and not(b_i));
    f_nand_o <= not(not(not(b_i) and a_i) and not(not(c_i)and not(b_i)));
    f_nor_o  <= not(b_i or not(a_i or not(c_i)) or b_i);
end architecture dataflow;
```


Hi, i am here
3. Complete table with logic functions' values:

| **c** | **b** |**a** | **f(c,b,a)_ORG** | **f(c,b,a)_NAND** | **f(c,b,a)_NOR** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![image](https://user-images.githubusercontent.com/99491847/155214174-de8173c2-7712-408d-b262-743f4ba8ada1.png)

2. Link to your public EDA Playground example:

   https://www.edaplayground.com/x/D942
