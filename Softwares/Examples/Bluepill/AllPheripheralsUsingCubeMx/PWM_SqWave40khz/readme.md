# SQUARE WAVE GENERATION USING PWM

This examples shows how to generate a Square Wave using PWM, frequency is set to 40Khz, clock speed to counter is 36Mhz(prescaler of 2 is set as system clock is 72Mhz), top is set to 899(it's actually 900, from 0-899) to get 40Khz frequency, period is set to half of top(i.e. 449) to get 50% duty cycle.

            ADD LOGIC ANALYSER IMAGE

## Common functions are

1. To start timer : It should be done in ```main```.

    ```HAL_TIM_PWM_Start(htim, Channel);```

2. ```HAL_TIM_PWM_Stop(htim, Channel);```

3. ```HAL_TIM_PWM_ConfigChannel(htim, sConfig, Channel);```
