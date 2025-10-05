# Differences between ZC702 and PYNQ-Z2

## Objectives

This file points out some notes when using ZC702 board.

## Lab 1

1.	Select UART1 when customizing Zynq7 Processing System. It is stated in **page 34** of [ZC702 User Guide](notes/refs/ug850-zc702-eval-bd-1596187.pdf).
    <p align="center">
    <img src ="notes/pics/lab1/1_SelectUART.jpg" width="80%" height="80%"/>
    </p>
    <p align = "center">
    <i>UART1</i>
    </p>

2.	Block Design final result:
    <p align="center">
    <img src ="notes/pics/lab1/2_BlockDesignResult.png" width="80%" height="80%"/>
    </p>
    <p align = "center">
    <i>Block Design</i>
    </p>

## Lab 2

1.	Select GP0 and Reset:
    <p align="center">
    <img src ="notes/pics/lab2/1_SetupResetAndGP0.png" width="80%" height="80%"/>
    </p>
    <p align = "center">
    <i>GP0 & Reset</i>
    </p>

2.	Select Clock:
    <p align="center">
    <img src ="notes/pics/lab2/2_SetupCLK.png" width="80%" height="80%"/>
    </p>
    <p align = "center">
    <i>Clock</i>
    </p>

3.	Select interface for buttons and switches:
    <p align="center">
    <img src ="notes/pics/lab2/3_InterfaceButton.png" width="80%" height="80%"/>
    </p>
    <p align = "center">
    <i>Button interface</i>
    </p>

    <p align="center">
    <img src ="notes/pics/lab2/4_InterfaceSwitch.png" width="80%" height="80%"/>
    </p>
    <p align = "center">
    <i>Switch interface</i>
    </p>

4. When running code in hardware via Vitis, if Vitis Serial Terminal does not show anything:
    - For Linux users, restart Vitis Classic under `sudo` right: `sudo vitis --classic`
    - Check if USB-to-UART cable driver has been installed
