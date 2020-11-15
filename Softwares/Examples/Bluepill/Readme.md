# STEPS FOR FLASHING CODE IN BLUEPILL FROM STM32CUBEIDE
![Blue Pill Image](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/BluePilll_Image.jpg)

Micro-Controller on Bluepill - **STM32F103C8T6** 

# BluePill pinouts

![Pinouts](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/stm32f103-pinout-diagram.png)

# Related Documents

  * [Datasheet - STM32F103C8T6](../../../Docs/F1&#32;series/Datasheet&#32;stm32f103c8.pdf)
  *  [User Manual - Description of STM32F1 HAL and Low-layer drivers](../../../Docs/F4&#32;series/../F1&#32;series/User&#32;Manual&#32;en.DM00154093.pdf)

# Software Requirements :
1. Java Runtime Environment - [Click here to go to download page](https://www.oracle.com/java/technologies/javase-jre8-downloads.html) 

2. STM32CubeIDE - [Click here to go to download page](https://www.st.com/en/development-tools/stm32cubeide.html#get-software) 

3. STM32CubeMX - [Click here to go to download page](https://www.st.com/en/development-tools/stm32cubemx.html)

4. STM32 ST-LINK Utility (Can be used to flash binary files build using STM32CubeIDE) - [Click here to go to download page](https://www.st.com/en/development-tools/stsw-link004.html)

# Creating a Blink LED project :

1. Open STM32CubeIDE --> Create a new workspace --> Start new STM32 project.

2. In MCU/MPU selector tab search for part no. STM32F103C8.
    ![](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/blink_steps2.png)

3. Enter project name and click Finish. Device configuration tool will open.

4. Select clock source.
   
    ![](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/1_Select_clock_source.png)

5. Select swd-serial debug in cubeMx settings
   
    ![](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/2_Debug_setting.png)

6. Configure Clock as per requirement
   
    ![Step3](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/3_configure_clock.png)

7. Click on pin PC13(on Board LED on bluepill) and choose GPIO_Output.
    ![](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/blink_steps7.JPG)

**CubeMX configurations are completed. Press CTRL + S to auto generate code as per desired configurations.** 

## Setting up St-Link-V2

![ST-LINK-V2](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/ST-link-v2.png)

### A. Connections :  

<table>
    <thead>
        <td colspan="2">
            <b> STM32BluePill </b>
        </td>
        <td colspan="2">
            <b> ST-Link V2 USB Debugger </b>
        </td>
    </thead>
    <tbody>
        <tr>
            <td> 3V3 </td><td>  </td>
            <td> 3.3V </td><td> (Pin 8) </td>
        </tr>
        <tr>
            <td> IO </td><td> </td>
            <td> SWDIO </td><td> (Pin 4) </td>
        </tr>
        <tr>
            <td> CLK </td><td>  </td>
            <td> SWDCLK </td><td> (Pin 2) </td>
        </tr>
        <tr>
            <td> GND </td><td>  </td>
            <td> GND </td><td> (Pin 6) </td>
        </tr>
    </tbody>
</table>

### B. Following Settings are needed to flash and debug the code.

1. In while(1) add following:

```HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_13);```

```HAL_Delay(1000);```

Blink LED project is present in this directory [BLINK_LED](AllPheripheralsUsingCubeMx/DigitalWrite/)

2. Build the project by clicking on hammer icon.

3. Now, to push the generated code using Stlink-V2 do the following configuration in debug settings, and click debug.
    
    ![Step4](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/4_debug_configuration.png)

# Examples

* [Example based on only HAL Based libraries](Using_HAL_Libraries/)
* [Example based on FreeRtos and HAL based libraries](Using_FreeRtos_and_HAL/)
