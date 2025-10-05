# Differences between ZC702 and PYNQ-Z2

- [Differences between ZC702 and PYNQ-Z2](#differences-between-zc702-and-pynq-z2)
  - [Objectives](#objectives)
  - [Lab 1](#lab-1)
  - [Lab 2](#lab-2)
  - [Lab 3](#lab-3)

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

## Lab 3

1. When editting `led_ip_slave_lite_v1_0_S_AXI.v`, just copy the content of [{sources}/lab3/led_ip_slave_lite_v1_0_S_AXI.v](sources/lab3/led_ip_slave_lite_v1_0_S_AXI.v)

2. In the **Add or Create Constraints** step, select the [lab3_zc702.xdc](sources/lab3/lab3_zc702.xdc) in `{sources}/lab3` folder
   - Notice that in lab3_zc702.xdc, each ***LED pin in Block Design*** is assigned to a ***Zc702 physical package pin***. These package pins can be found in **page 47** of [ZC702 User Guide](notes/refs/ug850-zc702-eval-bd-1596187.pdf)
  
    <p align="center">
    <img src ="notes/pics/lab3/1_ListOfUserLED.png" width="80%" height="80%"/>
    </p>
    <p align = "center">
    <i>List of User LED on Zc702. You can use whatever LED you want</i>
    </p>

    - In order to assign ***LED pin in Block Design*** to other ***Zc702 physical package pin*** (which means you will create your own `lab3_zc702.xdc` file), follow these steps:
      - Open **I/O Planning** layout as guided in Lab 2 (Lab 2, section `Make GPIO Peripheral Connections External`, step 10)
      - Expand the ***LED pin in Block Design***, then assign the ***Package Pin*** and ***IO Standard*** as stated in `ZC702 User Guide`, page 47
      - Press Ctrl+S to save it as `.xdc` file

    <p align="center">
    <img src ="notes/pics/lab3/2_IOPlanning.png" width="80%" height="80%"/>
    </p>
    <p align = "center">
    <i>Assign package pin and IO standard</i>
    </p>