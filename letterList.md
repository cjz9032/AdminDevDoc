[toc]

#letterList 字母列表--单选(用于listSelect)
> Version 1.0.0
> Update 2016年6月30日

##API 文档

###属性
| 属性名 | 类型 | 描述 |
| - | - | - |
| q | string | 过滤关键字 |
| data | Array:{text,value,_select} | 显示过滤后的值 |
| $originData | Array:{text,value,_select,pic} | 原始值 |
| >idName | string | 唯一键名 |
| >textName | string | 显示键名 |
| >keyName | string | 字母键名 |
| >picName | string | 图标键名 |
| hasPic | Boolean | 是否有图标 |
| tmpActiveItem | Boolean | 选中的项(todo) |
| isInit | Boolean | 是否初始化完毕 |
###事件
| 方法名 | 类型 | 传入参数 | 描述 |
| - | - | - | - |
| onInit | sync | ev:Object , vm:Object | 当组件内部初始化完毕后调度 |
| onChanged | async | ev:Object , vm:Object | 选中变化(todo) |
| onClickBefore | sync | ev:Object , vm:Object | 当点击前 |

###方法
| 方法名 | 返回值类型 | 参数 | 描述 |
| - | - | - | - |
| _trigger | void | ev:Object , type:String | 事件触发器 |
| doSelect | Void |ev:Object,item:data>item| 点击选中(todo) |
| _select | Void | item:data>item | 选中(todo) |
| _clrTmp | Void | 无 | 清楚选中(todo) |
| getSelect | data.item | 无 | 取选中 |
| setSelect | Void | id:string | 设选中(todo) |
| setData | Void | val:json | 设值 |
| getData | json | 无 | 取值(todo) |
### 事件详情
* #### onInit
+ 描述
当组件内部初始化完毕后调度
+ 参数
ev : Object - 触发的事件对象
vm : Object - 当前组件的vm

* #### onClickBefore
+ 描述
选中之前,可以retuan false取消
+ 参数
ev : Object - 触发的事件对象
vm : Object - 当前组件的vm

* #### onChanged
+ 描述
当选中发生变化时触发
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

* #### doSelect
+ 描述
点击选中
+ 参数
ev:Object-触发事件对象
item:data>item
+ 返回值
无

* #### _select
+ 描述
设置选中,do的调用
+ 参数
item:data>item
+ 返回值
无

* #### _clrTmp
+ 描述
清除选中
+ 参数
无
+ 返回值
无
 
* #### getSelect
+ 描述
获取选择项
+ 参数
无
+ 返回值
无

* #### setSelect
+ 描述
设置选中项
+ 参数
id:string
+ 返回值
无

* #### setData
+ 描述
设data,需符合格式
+ 参数
 [{idName,textName}...] 
+ 返回值
无

* #### getData
+ 描述
取data
+ 参数
无
[{keyName,valName}...] 


