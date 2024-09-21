.PHONY: clean all run
SRC_DIR = ../src
INC_DIR = ../inc
BUILD_DIR = .

CC = gcc
CFLAGS = -Wall -g -O2 -I$(INC_DIR)

targets = hello
sources = $(SRC_DIR)/main.c $(SRC_DIR)/HW.c
objects = main.o HW.o

all: $(targets)
	@echo "all done" 

$(targets): $(objects)
	$(CC) $(CFLAGS) $(objects) -o $@

$(BUILD_DIR)/%.o: $(SRC_DIR)/%.c
	$(CC) $(CFLAGS) -c $< -o $@

run: $(targets)
	./$(targets)

clean:
	rm -f *.o $(targets)
