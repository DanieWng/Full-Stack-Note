#iOS Error Solution

* <h3>clang: error: no such file or directory: xxx</h3>

	####solution:

	1. check `Build Phases` -> `Target Dependencies` or `Compile Sources`内是否包含相关文件或目录

* <h3>Apple Match-O Linker(Id) Error</h3>

	####solution:
	
	1. 检查 `Build Phase`->`Link Binary With libraries`内是否有漏掉的`framework` or `lib`
	2. SDK 版本是否过于老旧
	3. SDK 是否有需要设置`Bitcode Enable`为`false`
	4. 