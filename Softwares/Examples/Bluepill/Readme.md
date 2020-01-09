# BluePill
![Blue Pill Image](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/BluePilll_Image.jpg)

STM32F103C8T6 

# BluePill pinouts

![Pinouts](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/stm32f103-pinout-diagram.png)

## Related Documents

  * [Datasheet - stm32f103c8](../../../Docs/F1&#32;series/Datasheet&#32;stm32f103c8.pdf)
  *  [User Manual - Description of STM32F1 HAL and Low-layer drivers](../../../Docs/F4&#32;series/../F1&#32;series/User&#32;Manual&#32;en.DM00154093.pdf)

## Settings for St-link-v2

![ST-LINK-V2](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/ST-link-v2.png)

#### Connections 

<table>
    <thead>
        <td colspan="2">
            <b> STM32 Blue Pill </b>
        </td>
        <td colspan="2">
            <b> ST-Link V2 USB Debugger </b>
        </td>
    </thead>
    <tbody>
        <tr>
            <td> V3 </td><td> [Red] </td>
            <td> 3.3V </td><td> (Pin 8) </td>
        </tr>
        <tr>
            <td> IO </td><td> [Orange] </td>
            <td> SWDIO </td><td> (Pin 4) </td>
        </tr>
        <tr>
            <td> CLK </td><td> [Brown] </td>
            <td> SWDCLK </td><td> (Pin 2) </td>
        </tr>
        <tr>
            <td> GND </td><td> [Black] </td>
            <td> GND </td><td> (Pin 6) </td>
        </tr>
    </tbody>
</table>

If you are using above swd debugger - ST-link-v2 with BluePill in  STM32CubeIDE enivornment, then use following settings to debug your code:-

1. Step1 - Select clock source
   
    ![Step1](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/1_Select_clock_source.png)

2. Step2 Select swd-serial debug in cubeMx settings
   
    ![Step2](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/2_Debug_setting.png)

3. Step3 Configure Clock as per requirement
   
    ![Step3](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/3_configure_clock.png)


To generate the code by clicking on build project (hammer icon).



4. Step4 

    Now, to push the generated code using Stlink-V2 do the following configuration in debug settings.   
    
    ![Step4](../../../Docs/F1&#32;series/BluePill_Settings_for_stLink_v2/../../F1&#32;series/BluePill_Settings_for_stLink_v2/4_debug_configuration.png)

