# MeasureAlgoTime
用于计算C++程序或算法的运行时间，基于C++11实现。

使用方便、简洁，并且可以指定以不同时间单位来测量程序的运行时间，如：

`AlgoTimeNs` -- 以纳秒为时间单位

`AlgoTimeUs` -- 以微秒为时间单位

`AlgoTimeMs` -- 以毫秒为时间单位

`AlgoTimeS` -- 以秒为时间单位

`AlgoTimeM` -- 以分钟为时间单位

`AlgoTimeH` -- 以小时为时间单位 

基本使用：
```cpp
#include "MeasureAlgoTime.hpp"

int main() {

	// 创建一个以“微秒”为单位的算法时间对象
	// 当然也可以使用其它时间单位的时间对象，如毫秒、秒等
	Tools::Time::AlgoTimeUs time;
	
	// 启动计时
	time.start();
	for (int i = 0; i < 1024; ++i) {
		std::cout << "hello C++11 !" << std::endl;
	}

	// 直接在标准输出设备中输出程序的运行时间
	time.printElapsed();
	
	// 或者使用以下方式进行运行时间的输出
	auto elapsed = time.elapsed();
	std::cout << elapsed << "us" << std::endl;
	
	return 0;
}

```
