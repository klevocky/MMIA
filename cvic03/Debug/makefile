################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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
cvic03.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
cvic03.list \

OBJCOPY_BIN += \
cvic03.bin \


# All Target
all: cvic03.elf secondary-outputs

# Tool invocations
cvic03.elf: $(OBJS) $(USER_OBJS) D:\Documents\MMIA\cvic03\STM32F030R8TX_FLASH.ld
	arm-none-eabi-gcc -o "cvic03.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"D:\Documents\MMIA\cvic03\STM32F030R8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="cvic03.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

cvic03.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "cvic03.list"
	@echo 'Finished building: $@'
	@echo ' '

cvic03.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "cvic03.bin"
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
