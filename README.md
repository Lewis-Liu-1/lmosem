# LMOSEM

LMOSEM（liberty，madness，operating，system，embedded）是一个完全从第一行引导代码开始编写，基于ARM平台，支持多进程、多CPU、内存管理、文件与设备管理的全32位操作系统内核.

LMOSEM总体上分为三大层：HAL层（针对ARM体系，方便移植）、内核功能层（实现内核服务：其中有内存管理、进程管理、驱动模型等）、接口层（提供应用程序接口).


若要进行开发：

1. 请clone本代码仓库
2. 安装ARM-GCC交叉编译工具
3. 配置好相应的开发板
4. 详细请参阅我亲自编写的《深度探索嵌入式操作系统：从零开始设计、架构和开发》一书

# LMOS社区

http://lmoskernel.cn
  
编译说明  
	进行两个宏切换  
1.Makefile  BOARD_PLATFORM  默认为ARM平台  
	
	X86BARD = -f ./Makefile.x86  
	ARM_BARD = -f ./Makefile.arm  
	BOARD_PLATFORM = $(ARM_BARD)  
	#BOARD_PLATFORM = $(X86BARD)  
   
2.include\config.h  

	1.#define CFG_S3C2440A_PLATFORM  
	2.//#define CFG_X86_PLATFORM  