## 工作环境安装说明
===========================
### tmux无root安装

* tmux依赖于libevent，首先安装libevent，指定--prefix参数。如：

./configure --prefix=/home/work/.install/libevent

* 指定libevent依赖路径

LIBEVENT_PATH=/home/work/.install/libevent/

export LD_LIBRARY_PATH="$LIBEVENT_PATH/lib/:$LD_LIBRARY_PATH

* 编译安装tmux，指定--prefix等参数

./configure --prefix=/home/work/tmux CFLAGS="-I$LIBEVENT_PATH/include" LDFLAGS="-L$LIBEVENT_PATH/lib"


