铅笔道PHP面试题
======


1. 写出下面程序运行结果 *每个小题号都是一个独立的题目*
```php
// 1.1
$str1 = null;
$str2 = false;
echo $str1 == $str2 ? '相等' : '不相等';
$str3 = '';
$str4 = 0;
echo $str3 == $str4 ? '相等' : '不相等';
$str5 = 0;
$str6 = '0';
echo $str5 === $str6 ? '相等' : '不相等';
// 1.2
$test = 'A';
$abc  = &$test;
$test = 'X';
unset($test);
$test = 'Y';
echo $abc;
// 1.3
echo 1 <=> 2
echo 1 << 10;
echo 32 >> 1;
// 1.4
$i = 10;
function count() {
	static $i = 0;
	return $i++;
}
echo $i;
++$i;
echo count();
echo count();
// 1.5
for ($i = 0, $j = 0; $i < 10, $j < 5; $i++, $j++) {
	$k = $i + $j;
}
echo $k;
echo $i;
echo $j;
```
2. 分别使用冒泡算法、三元运算符获取下面三个数的最大数和最小数
```php
$a = 10;
$b = 20;
$c = 30;
```
3. 有10个人（1-10）围成一个圈，从第一人开始数，每隔两人就踢出一人，一直循环到最后只剩下一个人为止。问：最后那个人的编号是什么？写出过程
```php
$men = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
```
4. 现需要抽象一个账号类，其中属性包含`姓名、性别、年龄、积分、身份证号`，其中`年龄、积分、身份证号`是保密的，同时还有一个修改`积分`的方法，请根据描述写出这个类。
5. 有如下三个表

`users`
uid|name|age|height
:----:|:----:|:----:|:----:
1|小明|22|178
2|小王|20|178
3|小红|22|165
4|小明|25|168

`addresses`
uid|address
:----:|:----:
1|北京
2|上海
3|杭州
4|北京

`departments`
uid|department
:----:|:----:
1|技术部
2|市场部
3|技术部
4|编辑部

写出查询如下结果的SQL语句

5.1
name|age|height|address|department
:----:|:----:|:----:|:----:|:----:
小王|20|178|上海|市场部

5.2 列出地址是北京人的所有信息
5.3 求出各个部门的人数
5.4 计算技术部门的平均年龄



