This file has written by Nguyen Kien K66-EDABK. Thank you ^_^
# Differences between ZCU104 and PYNQ-Z2

## Objectives
This file points out some notes when using ZCU104 board.

## Lab 1

1.	Select UART0 when customizing Zynq MPSoC Processing System. It is stated in **page 52** of [ZCU104 User Guide](notes\refs\ug1267-zcu104-eval-bd.pdf)
    <p align="center">
    <img src ="notes\pics\1_select_UART_zcu104.png" width="80%" height="80%"/>
    </p>
    <p align = "center">
    <i>UART1</i>
    </p>
2.	Select I2C0 when customizing Zynq MPSoC Processing System. I2C0 is not only a regular peripheral but also used to communicate with power management ICs, such as INA226 power monitors or other components on the board.
    <p align="center">
    <img src ="notes\pics\2_selec_I2C0_zcu104.png" width="80%" height="80%"/>
    </p>
    <p align = "center">
    <i>UART1</i>
    </p>
3.	Block Design final result:
    <p align="center">
    <img src ="notes\pics\3_BlockDesignResult_zcu104.png" width="60%" height="60%"/>
    </p>
    <p align = "center">
    <i>Block Design</i>
    </p>