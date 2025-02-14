# Author: Stefano Mercogliano 	<stefano.mercogliano@unina.it>
# Description:
#   This Makefile defines the project name and paths for the common Makefile.
#	Optionally, a user can define additional targets here.

################
# Program Name #
################

# $(MAKEFILE_LIST)			: Contains a list of all Makefiles parsed (This Makefile and common Makefile)
# $(first $(MAKEFILE_LIST))	: Extracts the first entry, which is the current Makefile.
# $(abspath ...)			: Converts the relative path of the Makefile to an absolute path.
# $(dir ...)				: Extracts the directory portion of the absolute path.
# $(shell basename ...)		: Extracts the last component of the directory path, which is the name of the directory containing the Makefile.
PROGRAM_NAME = $(shell basename $(dir $(abspath $(firstword $(MAKEFILE_LIST)))))

#####################
# Paths and Folders #
#####################

SOC_SW_ROOT_DIR = $(SW_ROOT)/SoC

SRC_DIR		= src
OBJ_DIR		= obj
INC_DIR 	= inc 
STARTUP_DIR = $(SOC_SW_ROOT_DIR)/common

LD_SCRIPT 	= ld/user.ld 

#############
# Libraries #
#############

LIB_OBJ_TINYIO 	= $(LIB_DIR)/tinyio/lib/tinyio.a
LIB_INC_TINYIO	= -I$(LIB_DIR)/tinyio/inc

LIB_OBJ_LIST 	= $(LIB_OBJ_TINYIO)
LIB_INC_LIST 	= $(LIB_INC_TINYIO)

#############
# Toolchain #
#############

RV_PREFIX 	= riscv32-unknown-elf-
CC 			= $(RV_PREFIX)gcc
LD 			= $(RV_PREFIX)ld
OBJDUMP 	= $(RV_PREFIX)objdump
OBJCOPY 	= $(RV_PREFIX)objcopy

CFLAGS 		= -march=rv32imad_zicsr_zifencei -O0 -c 
LDFLAGS 	= $(LIB_OBJ_LIST) -nostdlib -T$(LD_SCRIPT)

include $(SW_ROOT)/SoC/common/Makefile
