# dy-js-tools

##### 安装
```
npm install --save dy-js-tools
```

##### 方式一：全局引用
###### 在main.js里面引入
```
// 引入
import dy from 'dy-js-tools';
// 注册
Vue.prototype.$dy = dy;
// 页面调用
this.$dy.log('hello world');
```

##### 方式二：局部引用
###### 在当前的vue文件里面引入
```
// 引入
import dy from 'dy-js-tools';
// 页面调用
dy.log('hello world');
```

#### 常用方法列表
| 函数名 | 参数 | 参数默认值 | 参数说明 | 返回值说明 | 介绍 |
| ---- | ---- | ---- | ---- | ---- | ---- |
| friendTime | dateTime | now Date() | 有效时间 | 返回友好时间提示（刚刚，1分钟前，1小时前，3个月前等） | 友好时间转换 |
| toDecimal | num,len | len=2 | 数字或能有效转换为数字的字符串,保留小数位数 | 保留为小数的字符串 | 精准保留小数点后len位，处理计算带来的误差，如0.1+0.2=0.30000000000000004 |
| judgeType | type |  | any | 返回:无效,null,undefined,function,array,object,number,string,boolean | 精准判断数据类型 |
| moneyToChinese | val |  | 数字或能有效转换为数字的字符串 | 返回中文大写（取绝对值） | 金额转中文大写 |
| dateToFormat | date, format | date=now Date(),format=YYYY-MM-DD hh:mm:ss | 有效时间，有效时间格式： YYYY-MM-DD hh:mm:ss | 返回对应时间格式 | 格式化时间 |
| getIdcardMsg | idcard |  | 有效有效身份证 | 返回 {age:'',birthday:'',sex:''}，object | 获取身份证信息（年龄，生日，性别） |
| createUuid |  |  |  | 返回 uuid | 生成uuid |
| getUrlParams | url | url=location.href | url地址 | 返回url参数，object | 获取url参数 |
| pwStrength | pwd |  | 6-20位密码字符串 | 返回密码强度，（强，中，弱，非常弱） | 获取密码强度 |
| codeHideMiddle | str,startStr,endStr,star | startStr=3, endStr=4, star='*' | any | 返回隐藏中间后的当前字符串：135*****008 | 字符隐藏，转* |

#### 验证方法列表
参数统一为：val=要验证的内容，正则flag: g|i|gi，默认为: g
如果不传参数，则为获取当前函数的正则

| 函数名 | 介绍 |
| ---- | ---- |
| idCardStrictValidate | 1 |
| idCardStrictValidate | 1 |