###############################################################################
# Makefile for project 
###############################################################################

## General options
PROJECT = 
MCU = 80C51
COMPILER = "ASEM-51 (Proteus)"
TARGET = Debug
SHELL = C:\Windows\system32\cmd.exe

## Tools general options

## Processing Tools
ASM=asem.exe
DDX=ASEMDDX.EXE
#  E:/博士后/教学/计组实验 教学改革/PROTEUS系列实验/SCUT版实验系列final/第三章 系统结构实验系列 修订版/实验3.1 微程序版CPU 修订版/80C51/Debug/Debug.HEX: TOOL=ASM
#  Post: $(DDX) $(DDXFLAGS) Debug.lst
#     E:/博士后/教学/计组实验 教学改革/PROTEUS系列实验/SCUT版实验系列final/第三章 系统结构实验系列 修订版/实验3.1 微程序版CPU 修订版/PROGRAMS/PUSH_POP.ASM

# Build tree:
all:	Debug

Debug:	Debug.HEX

Debug.HEX:	../../PROGRAMS/PUSH_POP.ASM 
	$(ASM) "..\..\PROGRAMS\PUSH_POP.ASM" "Debug.HEX" Debug.lst $(ASMFLAGS)  /INCLUDES:"C:\Program Files\Labcenter Electronics\Proteus 8 Professional\Tools\ASEM51"
	$(DDX) $(DDXFLAGS) Debug.lst

# tidy - delete all temporary files which are not involved in the target generation
tidy:
	rm -rf Debug.lst

# cleanup - delete all generated files
clean:	tidy
	rm -rf Debug.HEX
	rm -rf Debug.SDI

