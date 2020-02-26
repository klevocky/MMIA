################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
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
cv04\ ad\ prevodnik.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
cv04\ ad\ prevodnik.list \

OBJCOPY_BIN += \
cv04\ ad\ prevodnik.bin \


# All Target
all: cv04\ ad\ prevodnik.elf secondary-outputs

# Tool invocations
cv04\ ad\ prevodnik.elf: $(OBJS) $(USER_OBJS) D:\Documents\MMIA\cv04\ ad\ prevodnik\STM32F030R8TX_FLASH.ld
	arm-none-eabi-gcc -o "cv04 ad prevodnik.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"D:\Documents\MMIA\cv04 ad prevodnik\STM32F030R8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="cv04 ad prevodnik.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

cv04\ ad\ prevodnik.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "cv04 ad prevodnik.list"
	@echo 'Finished building: $@'
	@echo ' '

cv04\ ad\ prevodnik.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "cv04 ad prevodnik.bin"
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
