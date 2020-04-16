################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include USB_DEVICE/Target/subdir.mk
-include USB_DEVICE/App/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src/subdir.mk
-include Drivers/oled/Fonts/subdir.mk
-include Drivers/oled/subdir.mk
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
2.USB_RS232.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
2.USB_RS232.list \

OBJCOPY_BIN += \
2.USB_RS232.bin \


# All Target
all: 2.USB_RS232.elf secondary-outputs

# Tool invocations
2.USB_RS232.elf: $(OBJS) $(USER_OBJS) C:\Users\MECHANIC\STM32CubeIDE\USB\2.USB_RS232\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "2.USB_RS232.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\MECHANIC\STM32CubeIDE\USB\2.USB_RS232\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="2.USB_RS232.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

2.USB_RS232.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "2.USB_RS232.list"
	@echo 'Finished building: $@'
	@echo ' '

2.USB_RS232.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "2.USB_RS232.bin"
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
