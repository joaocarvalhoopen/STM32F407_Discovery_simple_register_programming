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
test_reg_001.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
test_reg_001.list \

OBJCOPY_BIN += \
test_reg_001.bin \


# All Target
all: test_reg_001.elf secondary-outputs

# Tool invocations
test_reg_001.elf: $(OBJS) $(USER_OBJS) C:\ST\workbench_1.3.0\test_reg_001\STM32F407VGTX_FLASH.ld
	arm-none-eabi-gcc -o "test_reg_001.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\ST\workbench_1.3.0\test_reg_001\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="test_reg_001.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

test_reg_001.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "test_reg_001.list"
	@echo 'Finished building: $@'
	@echo ' '

test_reg_001.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "test_reg_001.bin"
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
