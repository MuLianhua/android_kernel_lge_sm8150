obj-$(CONFIG_PATHMASK) += pathmask.o

# 将源码和依赖库一起编译
pathmask-y := src/pathmask.o
pathmask-y += $(shell find deps -name '*.c' | sed 's/\.c$/.o/')

# 指定头文件搜索路径（包括自己的源码目录、依赖目录和SDK目录）
ccflags-y += -I$(srctree)/fs/pathmask/src
ccflags-y += -I$(srctree)/fs/pathmask/deps
ccflags-y += -I$(srctree)/fs/pathmask/.sdk
