# coro_epoll_kqueue
c++20 coroutine with epoll and queue
C++20 coroutine对于epoll和kqueue的封装示例，只有500行代码，适合学习参考。echo_server.cpp就是使用示例。
为了提升速度，注释掉了控制台输出

编译：
```
git clone https://github.com/franktea/coro_epoll_kqueue.git;
cd coro_epoll_kqueue;
cmake -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -S . -B build/
cd build;
make
```

测试
/home/ubuntu2004/tools/fortio/bin/fortio load -qps 0 -n 100000 tcp://localhost:12345


最初参考了https://github.com/Ender-events/epoll-coroutine
