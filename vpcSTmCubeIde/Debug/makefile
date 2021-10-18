################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
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
vpcSTmCubeIde.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
vpcSTmCubeIde.list \

OBJCOPY_BIN += \
vpcSTmCubeIde.bin \


# All Target
all: vpcSTmCubeIde.elf secondary-outputs

# Tool invocations
vpcSTmCubeIde.elf: $(OBJS) $(USER_OBJS) C:\My\ Datas\Project\Test\ Projects\STm32F429IGTx\vpcSTmCubeIde\STM32F429ZITX_FLASH.ld
	arm-none-eabi-gcc -o "vpcSTmCubeIde.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\My Datas\Project\Test Projects\STm32F429IGTx\vpcSTmCubeIde\STM32F429ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="vpcSTmCubeIde.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

vpcSTmCubeIde.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "vpcSTmCubeIde.list"
	@echo 'Finished building: $@'
	@echo ' '

vpcSTmCubeIde.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "vpcSTmCubeIde.bin"
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
