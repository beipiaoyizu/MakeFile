include $(PROJECT_ROOT)/Makefile.dir
include $(PROJECT_ROOT)/Makefile.common

DIR = .

INCLUDE = $(PROJECTINCLUDE) -I.

LIB = -Xlinker "-("  -Xlinker "-)"

TARGET = main

SRC := $(foreach dir, $(DIR), $(wildcard $(dir)/*.cpp))

#OBJ := $(patsubst %.cpp,%.o, $(SRC))
OBJ := $(patsubst %.cpp,%.o, $(patsubst %.cc,%.o, $(SRC)))

DEPEND := $(shell ls -a ".depend" 2>/dev/null)

all: $(TARGET)

ifeq ($(DEPEND), .depend)
include .depend
endif

include $(PROJECT_ROOT)/Makefile.tail
