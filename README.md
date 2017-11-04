# RegExp-notebook
## 实用正则表达式
- 校验手机号码：
    /^1(3|4|5|7|8)\d{9}$/.test(mobile.trim());
- 去除数字和小数点之外的字符：
    str.replace(/[^\d.]/g, "");
- 匹配非元音字母
    /[^aeiou]/
- 匹配数字
    /\d+(\.)?(\d)*/
- 校验excel文件
    /\.xls[x]?$/i
- 匹配jpg、jpeg、gif、png格式
  	/\.(jp[e]?g|gif|png)$/
- 匹配url
	/(\w+):\/\/([\w\.]+)\/(\S*)/

## 练习题
1. 完成rejetRepeatedChars函数，从给定的字符串中剔除连续字符，只保留一个，比如aaabbbcdc，处理完之后返回abcdc。
```javascript
function rejectRepeatedChars(str){
	return str.replace(/(.)\1+/gi, "$1");
}
```

2. 将浮点数小数点左边的数每三位添加一个逗号
```javascript
function commafy(num){
	return num && num.toString().replace(/(\d)(?=(\d{3})+\.)/g, function($1, $2){
		return $2 + ",";
	});
}
```

3. 为仅有一位的数字加上前导零
```javascript
function format (num) {
    return num.toString().replace(/^(\d)$/, "0$1");
}
```

## 相关网站
[JS正则可视化工具](https://regexper.com/)
[https://regexr.com/](https://regexr.com/)
