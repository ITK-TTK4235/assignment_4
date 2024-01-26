SOURCES := character_count.c

BUILD_DIR := build
LINKER_SCRIPT := $(BUILD_DIR)/linker_script_nrf52.ld

CC	:= gcc

QUIET := @

# Throw errors for warnings and set GNU dialect to ISO C99
CFLAGS += -Wall -Werror -std=gnu99

.PHONY: default debug clean

default:
	@echo Compiling project
	$(CC) $(CFLAGS) $(SOURCES) -o $(BUILD_DIR)/main.o

	
debug:
	@echo Compiling project with debug
	$(CC) $(CFLAGS) -ggdb -Og $(SOURCES) -o $(BUILD_DIR)/main.o

clean:
	$(QUIET)rm $(BUILD_DIR)/main.o