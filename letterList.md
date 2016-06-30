[toc]

#checkboxGroup 侧边折叠导航栏
> Version 1.0.0
> Update 2016年6月30日

##API 文档

###属性
| 属性名 | 类型 | 描述 |
| - | - | - |
| data | Array:{text,value,_checked} | 值 |
| >idName | String |  值 |
| >textName | String | 文本 |
| must | Boolean | 必选 |
| tip | String | 提示文字 |
| readonly | Boolean | 只读 |
| isInit | Boolean | 是否初始化完毕 |
| isValid | Boolean | 是否正在验证 |
| validInfo | Boolean | 错误信息 |
| formName | string | 写入,提交名 |

###事件
| 方法名 | 类型 | 传入参数 | 描述 |
| - | - | - | - |
| onInit | sync | ev:Object , vm:Object | 当组件内部初始化完毕后调度 |
| onChecked | async | ev:Object , vm:Object | 单复选选中 |
| onCancel | async | ev:Object , vm:Object | 当复选框取消 |
| onChange | async | ev:Object , vm:Object | 当组件值发生变化时触发 |

###方法
| 方法名 | 返回值类型 | 参数 | 描述 |
| - | - | - | - |
| _trigger | void | ev:Object , type:String | 事件触发器 |
| doSetCheckbox | Void |ev:Object,item:data>item| 点击选中(todo) |
| _setCheckedState | Void | item:data>item | 选中(todo) |
| _setCheckedStateById | Void | val:String | 选中(todo) |
| setValue | Void | val:string | 表单设值 |
| getValue | string-json | 无 | 表单取值 |
| setData | Void | val:json | 设值(todo) |
| getData | json | 无 | 取值(todo getCheckedData) |
### 事件详情
* #### onInit
+ 描述
当组件内部初始化完毕后调度
+ 参数
ev : Object - 触发的事件对象
vm : Object - 当前组件的vm

* #### onChecked
+ 描述
当单复选框选中
+ 参数
ev : Object - 触发的事件对象
vm : Object - 当前组件的vm

* #### onCancel
+ 描述
当复选框取消
+ 参数
ev : Object - 触发的事件对象
vm : Object - 当前组件的vm

* #### onChanged
+ 描述
当组件值发生变化时触发
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

* #### doSetCheckbox
+ 描述
点击选中
+ 参数
ev:Object-触发事件对象
item:data>item
+ 返回值
无
* #### _setCheckbox
+ 描述
设置选中,do的调用
+ 参数
item:data>item
+ 返回值
无
* #### _setCheckboxById
+ 描述
设置选中,通过唯一键
+ 参数
val:string
+ 返回值
无
 
* #### setValue
+ 描述
表单设值
+ 参数
val:string
+ 返回值
无

* #### getValue
+ 描述
表单取值
+ 参数
无
+ 返回值
val:string

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


