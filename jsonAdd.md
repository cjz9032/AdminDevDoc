[toc]

#jsonAdd 侧边折叠导航栏
> Version 1.0.0
> Update 2016年6月29日

##API 文档

###属性
| 属性名 | 类型 | 描述 |
| - | - | - |
| value | Array:{keyName,valName} | 值 |
| >keyName | String | ID键名 |
| >valName | String | 值键名 |
| must | Boolean | 必选(todo) |
| tip | String | 提示文字 |
| isHide | Boolean | 显示 |
| placeholder | String | 输入框内提示 |
| readonly | Boolean | 只读 |
| isInit | Boolean | 是否初始化完毕 |
| isValid | Boolean | 是否正在验证 |
| $keyIptVm | VM | 键输入框 |
| $valIptVm | VM | 值输入框 |

###事件
| 方法名 | 类型 | 传入参数 | 描述 |
| - | - | - | - |
| onInit | sync | ev:Object , vm:Object | 当组件内部初始化完毕后调度 |
| onChange | async | ev:Object , vm:Object | 当组件值发生变化时触发 |

###方法
| 方法名 | 返回值类型 | 参数 | 描述 |
| - | - | - | - |
| _trigger | void | ev:Object , type:String | 事件触发器 |
| doAddItem | Void |ev:Object | 点击增加(todo) |
| _addItem | Void | key:String,val:String | 增加一个值(todo) |
| _getValIptVM | Void | 无 | 获取键输入框VM |
| _getKeyIptVM | Void | 无 | 获取值输入框VM |
| _clrIpt | Void | 无 | 清空输入框 |
| _clrEnv | Void | 无 | 清空输入框以及value |
| setValue | Void | val:string-json,isReadonly:Boolean | 表单设值 |
| getValue | string-json | 无 | 表单取值 |
| setData | Void | val:json | 设值 |
| getData | json | 无 | 取值 |
### 事件详情
* #### onInit
+ 描述
当组件内部初始化完毕后调度
+ 参数
ev : Object - 触发的事件对象
vm : Object - 当前组件的vm

* #### onChanged
+ 描述
当组件激活项发生变化时触发
+ 参数
vm : Object - 当前组件的vm

### 方法详情
* #### _trigger
+ 描述
事件触发器, 触发外部事件
+ 参数
ev : Object - 触发的事件对象
type : string - 触发的事件类型

* #### doAddItem
+ 描述
用户点击添加键值对
+ 参数
ev:Object-触发事件对象
+ 返回值
无
* #### _addItem
+ 描述
内部添加方法
+ 参数
key:String,键,val:String:值
+ 返回值
无
* #### _getValIptVM
+ 描述
获取值输入框VM,存储以使用
+ 参数
无
+ 返回值
无
* #### _getKeyIptVM
+ 描述
获取键输入框VM,存储以使用
+ 参数
无
+ 返回值
无

* #### _clrIpt
+ 描述
清空输入框
+ 参数
无
+ 返回值
无

* #### _clrEnv
+ 描述
清空输入框 , value
+ 参数
无
+ 返回值
无

* #### setValue
+ 描述
表单设值,后端交互用String的json
+ 参数
val:string-json,isReadonly:Boolean	
+ 返回值
无

* #### getValue
+ 描述
表单取值,后端交互用String的json
+ 参数
无
+ 返回值
string-json

* #### setData
+ 描述
设值,直接以json返回
+ 参数
 [{keyName,valName}...] 
+ 返回值
无

* #### getData
+ 描述
取值,直接读取json 
+ 参数
无
[{keyName,valName}...] 


