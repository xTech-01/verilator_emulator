# verilator_emulator

## error 
    ```
    implicit conversion to enum 'enum{}$unit::operation_t' from 'logic'
    ```
## fix: op_in_r is an operation, not bit?
        ```
        op_in_r <= '0 -> op_in_r <= nop
        ``` 

## makefile commands
    ```
    make clean
    make waves

    make clean
    make sim
    make waves
    ```

## verilator commands
    ```
    verilator cc alu.sv
    ls -l obj_dir/
    verilator -Wall --trace -cc alu.sv --exe tb_alu.cpp
    make -C obj_dir -f Valu.mk Valu
    ./obj_dir/Valu
    ls
    sudo apt-get install gtkwave
    gtkwave waveform.vcd
    ```
## vim commands
    one more after end of the line:
        `:set ve+=onemore`
    move:
        `alt + h j k l`
    select:
        `V v`
    copy cut paste:
        `y yy 3yy y$ yiw`
        `d dd 3dd d$`
        `P p`

![rst](https://github.com/xTech-01/verilator_emulator/blob/main/rand_expected_dut.png)
![rst](https://github.com/xTech-01/verilator_emulator/blob/main/rand_rst.png)
![alu](https://github.com/xTech-01/verilator_emulator/blob/main/alu_2_states.png)

[Ref](https://itsembedded.com/dhd/verilator_1/)
