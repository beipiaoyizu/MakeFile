include $(PROJECT_ROOT)/Makefile.common

DIR = .

INCLUDE = $(PROJECTINCLUDE) -I.

LIB = $(PROJECTLIBS)

TARGET_ALL = libasyncclient.a

SRC := $(foreach dir, $(DIR), $(wildcard $(dir)/*.cpp))

OBJ := $(patsubst %.cpp,%.o, $(SRC))

DEPEND := $(shell ls -a ".depend" 2>/dev/null)

all: $(TARGET_ALL)

ifeq ($(DEPEND), .depend)
include .depend
endif

include $(PROJECT_ROOT)/Makefile.so.tail
