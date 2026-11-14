obj-$(CONFIG_PATHMASK) += pathmask.o

# 把主程序和 procguard 加入编译
pathmask-y := src/pathmask.o src/procguard.o

# 精准指定 KallRecon 库中属于内核空间的源文件
pathmask-y += deps/KallRecon/lib/access.o
pathmask-y += deps/KallRecon/lib/anchor.o
pathmask-y += deps/KallRecon/lib/core.o
pathmask-y += deps/KallRecon/lib/discover.o
pathmask-y += deps/KallRecon/lib/fastboot.o
pathmask-y += deps/KallRecon/lib/hint.o
pathmask-y += deps/KallRecon/lib/slide.o
pathmask-y += deps/KallRecon/lib/symbol.o

# 指定头文件搜索路径
ccflags-y += -I$(srctree)/fs/pathmask/src
ccflags-y += -I$(srctree)/fs/pathmask/deps/KallRecon/lib
ccflags-y += -I$(srctree)/fs/pathmask/.sdk
