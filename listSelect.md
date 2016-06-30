[toc]

#listSelect (包含letterlist)
> Version 1.0.0
> Update 2016年6月29日

##API 文档

###属性
| 属性名 | 类型 | 描述 |
| - | - | - |
| text | String | 显示文字 |
| value | String | 提交值 |
| must | Boolean | 必选(todo) |
| tip | String | 提示文字 |
| readonly | Boolean | 只读 |
| isInit | Boolean | 是否初始化完毕 |
| isValid | Boolean | 是否正在验证 |
| $list_opt | Object | letterlist配置 |
| data | Array-{textName,idName,_selected} | 待选项 |
| dataSelect | data.item | 选中项 |
| >textName | string | 文本键名 |
| >idName | string | 值键名 |
| >_selected | Boolean | 选中 |
| $data_opt | Object{textName,idName} | data配置 |
| formName | string | 写入,提交名 |
| submitName | string | 提交名(优先) |

###事件
| 方法名 | 类型 | 传入参数 | 描述 |
| - | - | - | - |
| onInit | sync | ev:Object , vm:Object | 当组件内部初始化完毕后调度 |
| onClicked | async | ev:Object , vm:Object | 当点击输入框 |
| onChange | async | ev:Object , vm:Object | 当值发生变化时触发 |

###方法
| 方法名 | 返回值类型 | 参数 | 描述 |
| - | - | - | - |
| _trigger | void | ev:Object , type:String | 事件触发器 |
| clickIpt | Void |ev:Object | 点击输入框(todo) |
| dataSelect | Void | data.item | 增加一个值(todo) |
| setValue | Void | text:string | 表单设值 |
| getValue | val:string | 无 | 表单取值 |
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
vm : Object - 当前组件的vm

* #### onChanged
+ 描述
当值发生变化
+ 参数
vm : Object - 当前组件的vm

### 方法详情
* #### _trigger
+ 描述
事件触发器, 触发外部事件
+ 参数
ev : Object - 触发的事件对象
type : string - 触发的事件类型

* #### clickIpt
+ 描述
点击输入框
+ 参数
ev:Object-触发事件对象
+ 返回值
无

* #### dataSelect
+ 描述
内部添加方法
+ 参数
data.item--{text,val,_selected}
+ 返回值
无

* #### setValue
+ 描述
表单设值,只设定text,val还是空
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


