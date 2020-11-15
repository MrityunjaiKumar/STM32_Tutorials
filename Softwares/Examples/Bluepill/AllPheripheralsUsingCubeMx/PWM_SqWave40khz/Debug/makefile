################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
PWM_SqWave40khz.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
PWM_SqWave40khz.list \

OBJCOPY_BIN += \
PWM_SqWave40khz.bin \


# All Target
all: PWM_SqWave40khz.elf secondary-outputs

# Tool invocations
PWM_SqWave40khz.elf: $(OBJS) $(USER_OBJS) E:\CEDT\ projects\MJ\ sir\ bluepill\ repo\STM32_Tutorials\Softwares\Examples\Bluepill\AllPheripheralsUsingCubeMx\PWM_SqWave40khz\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "PWM_SqWave40khz.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"E:\CEDT projects\MJ sir bluepill repo\STM32_Tutorials\Softwares\Examples\Bluepill\AllPheripheralsUsingCubeMx\PWM_SqWave40khz\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="PWM_SqWave40khz.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

PWM_SqWave40khz.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "PWM_SqWave40khz.list"
	@echo 'Finished building: $@'
	@echo ' '

PWM_SqWave40khz.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "PWM_SqWave40khz.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
