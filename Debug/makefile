################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/MCAL/UART/subdir.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
LSS += \
Atmega32_Peripherals_Interfacing.lss \

FLASH_IMAGE += \
Atmega32_Peripherals_Interfacing.hex \

SIZEDUMMY += \
sizedummy \


# All Target
all: Atmega32_Peripherals_Interfacing.elf secondary-outputs

# Tool invocations
Atmega32_Peripherals_Interfacing.elf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: AVR C Linker'
	avr-gcc -Wl,-Map,Atmega32_Peripherals_Interfacing.map -mmcu=atmega32 -o "Atmega32_Peripherals_Interfacing.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

Atmega32_Peripherals_Interfacing.lss: Atmega32_Peripherals_Interfacing.elf
	@echo 'Invoking: AVR Create Extended Listing'
	-avr-objdump -h -S Atmega32_Peripherals_Interfacing.elf  >"Atmega32_Peripherals_Interfacing.lss"
	@echo 'Finished building: $@'
	@echo ' '

Atmega32_Peripherals_Interfacing.hex: Atmega32_Peripherals_Interfacing.elf
	@echo 'Create Flash image (ihex format)'
	-avr-objcopy -R .eeprom -R .fuse -R .lock -R .signature -O ihex Atmega32_Peripherals_Interfacing.elf  "Atmega32_Peripherals_Interfacing.hex"
	@echo 'Finished building: $@'
	@echo ' '

sizedummy: Atmega32_Peripherals_Interfacing.elf
	@echo 'Invoking: Print Size'
	-avr-size --format=avr --mcu=atmega32 Atmega32_Peripherals_Interfacing.elf
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(FLASH_IMAGE)$(ELFS)$(OBJS)$(ASM_DEPS)$(S_DEPS)$(SIZEDUMMY)$(S_UPPER_DEPS)$(LSS)$(C_DEPS) Atmega32_Peripherals_Interfacing.elf
	-@echo ' '

secondary-outputs: $(LSS) $(FLASH_IMAGE) $(SIZEDUMMY)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
