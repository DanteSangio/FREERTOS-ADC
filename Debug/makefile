################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include freeRTOS/src/subdir.mk
-include Example/src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: FRTOS_ADC.axf

# Tool invocations
FRTOS_ADC.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"C:\Users\unknown\Documents\LPCWorkspace\lpc_chip_175x_6x\Debug" -Xlinker -Map="FRTOS_ADC.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m3 -mthumb -T "FRTOS_Debug.ld" -o "FRTOS_ADC.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) FRTOS_ADC.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "FRTOS_ADC.axf"; # arm-none-eabi-objcopy -v -O binary "FRTOS_ADC.axf" "FRTOS_ADC.bin" ; # checksum -p LPC1769 -d "FRTOS_ADC.bin";
	-@echo ' '

.PHONY: all clean dependents post-build

-include ../makefile.targets
