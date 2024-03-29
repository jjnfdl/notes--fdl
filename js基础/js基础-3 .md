# js基础-3
## 数组
### 创建数组
- `var arr = new Array();`创建空数组
有参数时
`var arr1 = new Array(3);`一个参数表示创建数组包含三个空元素
`var arr2 = new array(3,4,5);`多个参数表示数组中的元素
- `var arr3 = [1,2,3,4,5];`

### 数组的增删改查
var arr = [1,2,3,4,6,7,6];
`arr.length`表示数组的长度
`arr[i]` `i`表示元素的索引(下标)
> 下标从 0 开始
- 查找元素 `arr[i]`;
`var arr1 = new Array();`
- 添加(追加)元素 `arr1[i]` = 元素;
- 取 修改元素
`arr[i]`获取`arr`数组中第`i-1`个元素;
`var arr = new Array();`

### 遍历数组元素
> js-3 练习 遍历数组元素


### 求数组的平均值
> js-3 练习 求数组平均值

### 数组的基本方法
var arr = [1,2,4,5];
- 从前删除第一个  `arr.shift()`
- 从后删除第一个  `arr.pop()`
> 返回值都是删除的元素,都修改了原数组
- 从后添加一个元素  `arr.push()`
- 从前添加一个元素  `arr.unshift()`
> 都会修改原数组,返回值是修改后数组的长度
var arr1 = [5,6,7,8];
- 拼接数组  `arr.concat(arr1)`
会组成一个新数组,不会修改原数组
- 将数组改为字符串  `arr.join()`
返回值为转换后的字符串,不会改变原数组,()内可以指定字符串的连接符,不写默认是`,`;
- 通过指定分隔符,将字符串分割为字符串数组  `arr.split()`


### 数组高级
> var arr = ["a", "b", "c", "d", "e", "f"];
- 反转数组,返回值为反转后的数组 `arr.reverse();
会改变原数组
- sort()方法 对数组的元素进行从小到大来排序（ 会改变原来的数组）
    - 没有参数时  默认按照`Unicode`编码 从小到大排序
        - 元素为字符串
        ```
        var arr1 = ["e", "b", "d", "a", "f", "c"];
	    console.log(arr1.sort()); // a ,b ,c ,d ,e ,f
        ```
        - 元素为数字时
        var arr2 = [5, 2, 11, 3, 4, 1];
		console.log(arr2.sort()); //1,11,2,3,4,5
    - 有参数时
    ```
    var arr3 = [5, 2, 11, 3, 4, 1];
			arr3.sort(function(a, b) {
				// 指定排序规则
				// 从小到大排
				return a - b;
				// 根据回调函数的返回值来决定元素的排序：（ 重要）
				// 如果返回一个大于 0 的值， 则元素会交换位置
				// 如果返回一个小于 0 的值， 则元素位置不变
				// 如果返回一个 0， 则认为两个元素相等， 则不交换位置

				// 想  从大到小排
				// return b - a;
			});
    ```
    - js-3 练习    `sort()`用法 
- `arr.slice()`    从数组中提取指定元素(一个或多个),返回值为新的数组(不会改变原数组)
    - 有参数时
    1.两个参数时,从开始索引截取到结束索引(包含开始索引，不包含结束索引)
    2.一个参数时,从开始索引截取到数组最后
    3.`arr.slice(0)`复制数组
- 删除替换  `arr.splice()`
    - 两个参数时,从开始索引删除(第二个参数表示删除几个元素)
    - 多余两个参数时,第三个参数之后表示在原位置添加元素 
- 获取元素的索引  `arr.indexOf()`  `arr.lastIndexOf()`    
`indexOf` 是从前 匹配,找到之后不再匹配,然后返回匹配值的下标
`lastIndexOf` 是从后往前 匹配,找到之后不再匹配,然后返回匹配值的下标


### 冒泡排序
js-3 练习 冒泡排序

比较相邻的元素。 如果第一个比第二个大， 就交换他们两个。
对每一对相邻元素作同样的工作， 从开始第一对到结尾的最后一对。 在这一点， 最后的元素应该会是最大的数。
针对所有的元素重复以上的步骤， 除了最后一个。
持续每次对越来越少的元素重复上面的步骤， 直到没有任何一对数字需要比较。
之所以叫冒泡排序， 每一轮两两比较之后， 都会冒出一个本轮最大的数， 将其移动到本轮尾部。

### 选择排序
js-3 练习 选择排序

选择排序是一种简单直观的排序算法。
它的工作原理是每一次从待排序的数据元素中选出最小（或最大）的一个元素，存放在序列的起始位置，
然后，再从剩余未排序元素中继续寻找最小（大）元素，然后放到已排序序列的末尾。
以此类推，直到全部待排序的数据元素排完。
选择排序是不稳定的排序方法。


### 插入排序
js-3 练习 插入排序



