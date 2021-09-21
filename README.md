ThreadPool
==========

A simple C++11 Thread Pool implementation.

Tested:
 - Windows 10 on Visual Studio 2019 `/std:c++17` and `/std:c++11`
 - Windows 10 on MinGW64 Failed

 
Basic usage:
```c++
// create thread pool with 4 worker threads
ThreadPool pool(4);

// enqueue and store future
auto result = pool.enqueue([](int answer) { return answer; }, 42);

// get result from future
std::cout << result.get() << std::endl;

```
