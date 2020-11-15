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
DigitalRead.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
DigitalRead.list \

OBJCOPY_BIN += \
DigitalRead.bin \


# All Target
all: DigitalRead.elf secondary-outputs

# Tool invocations
DigitalRead.elf: $(OBJS) $(USER_OBJS) E:\CEDT\ projects\MJ\ sir\ bluepill\ repo\STM32_Tutorials\Softwares\Examples\Bluepill\AllPheripheralsUsingCubeMx\DigitalRead\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "DigitalRead.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"E:\CEDT projects\MJ sir bluepill repo\STM32_Tutorials\Softwares\Examples\Bluepill\AllPheripheralsUsingCubeMx\DigitalRead\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="DigitalRead.map" -Wl,--gc-sections -static -specs=rdimon.specs -lc -lrdimon --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

DigitalRead.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "DigitalRead.list"
	@echo 'Finished building: $@'
	@echo ' '

DigitalRead.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "DigitalRead.bin"
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
