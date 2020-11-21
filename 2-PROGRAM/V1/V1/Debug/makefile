################################################################################
# 自动生成的文件。不要编辑！
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
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
V1.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
V1.list \

OBJCOPY_BIN += \
V1.bin \


# 所有目标
all: V1.elf secondary-outputs

# 工具调用
V1.elf: $(OBJS) $(USER_OBJS) D:\Project\F4board\2-PROGRAM\V1\V1\STM32F407ZETX_FLASH.ld
	arm-none-eabi-gcc -o "V1.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Project\F4board\2-PROGRAM\V1\V1\STM32F407ZETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="V1.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo '已结束构建目标： $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo '已结束构建： $@'
	@echo ' '

V1.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "V1.list"
	@echo '已结束构建： $@'
	@echo ' '

V1.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "V1.bin"
	@echo '已结束构建： $@'
	@echo ' '

# 其他目标
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
