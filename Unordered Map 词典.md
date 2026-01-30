# Unordered Map 词典

## 1. 常用操作

```cpp
#include <iostream>
#include <unordered_map>
#include <string>

int main() {
    
    unordered_map<std::string, int> m; // 声明语法：unordered_map <Key类型, Value类型> 名;

    // 插入数据
    m["Alice"] = 95;                  // 方式 A：下标法（最常用）
    m.insert({"Bob", 88});            // 方式 B：insert 插入 pair
    m.emplace("Charlie", 92);         // 方式 C：emplace 原地构造（效率更高）

    // 访问数据
    std::cout << "Alice's score: " << m["Alice"] << std::endl;

	m.find(key)						// 查找，返回迭代器，若找不到则等于m.end()
	m.count(key)					// 计数，返回 1（存在）或 0（不存在）
	m.erase(key)					// 删除
	m.size()						// 大小
	m.clear()						// 清空
	m.empty()						// 检查为空

}
```
