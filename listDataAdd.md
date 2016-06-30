[toc]

#listDataAdd (左右移动选择框)
> Version 1.0.0
> Update 2016年6月29日

##API 文档

###属性
| 属性名 | 类型 | 描述 |
| - | - | - |
| cullOrigin | Boolean | 去除已选中,即只能增加,不能减少 |
| originData | Array:{text,id,_checked,key} | 初始值 |
| data | Array:{text,id,_checked,key} | 待选项 |
| >idName | String | 唯一键名 |
| >textName | String | 文本键名 |
| >keyName | String | 字母键名 |
| >_checked | String | 选中 |
| diffData | Array:[dec:data,add:data] | 变化值 |
| q | Object:{left:string,right:string} | 搜索 |
| leftObj,rightObj | data  | 视图显示,左右框中选项 |
| isInit | Boolean | 是否初始化完毕 |

###事件
| 方法名 | 类型 | 传入参数 | 描述 |
| - | - | - | - |
| onInit | sync | ev:Object , vm:Object | 当组件内部初始化完毕后调度 |
| onDataChange | async | ev:Object , vm:Object ,diffData:data  | 保存 | 

###方法
| 方法名 | 返回值类型 | 参数 | 描述 |
| - | - | - | - |
| _trigger | void | ev:Object , type:String | 事件触发器 |
| _genGroup | Void | 无 | 生成视图 |
| doSelectItem | Void | Id:String | 用户点击选中(todo) |
| selectItem | Void | Id:String | 选中 |
| selectAll | Void | 无 | 全选 |
| _addItem | Void | flag:Boolean,position:String | 添加或取消 | 
| setData | Void | Array:data | 设待选项 | 

### 事件详情
* #### onInit
+ 描述
当组件内部初始化完毕后调度
+ 参数
ev : Object - 触发的事件对象
vm : Object - 当前组件的vm

* #### onClicked
+ 描述
点击输入框
+ 参数
ev : Object - 触发的事件对象
vm : Object - 当前组件的vm

* #### onDataChanged
+ 描述
保存,值变化
+ 参数
ev : Object - 触发的事件对象
vm : Object - 当前组件的vm

### 方法详情
* #### _trigger
+ 描述
事件触发器, 触发外部事件
+ 参数
ev : Object - 触发的事件对象
type : string - 触发的事件类型
+ 返回值
无

* #### _genGroup
+ 描述
生成视图,左右框内各项
+ 参数
无
+ 返回值
无

* #### doSelectItem
+ 描述
用户点击选中
+ 参数
id:string
+ 返回值
无

* #### selectItem
+ 描述
选中,id选择
+ 参数
id:string
+ 返回值
无

* #### selectAll
+ 描述
全选
+ 参数
无
+ 返回值
无

* #### _addItem
+ 描述
添加或取消按钮,参数区分左右框
+ 参数
flag:Boolean,position:String
+ 返回值
无

