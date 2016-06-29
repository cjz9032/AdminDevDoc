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
| doAddItem | Void |无 | 点击增加 |
| _addItem | Void | 无 | 增加一个值 |
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

* #### _renderContent
+ 描述
渲染插入点, 返回插入点的html内容, 以html过滤器显示
+ 参数
idx : Number - 要渲染的插入点的index
+ 返回值
String - 该插入点的html字符串

* #### _clickPanel
+ 描述
面板点击展开收拢事件
+ 参数
ev : Object - 触发的事件对象
idx : Number - 点击的面板的index

* #### _setSelect
+ 描述
设置选中项
+ 参数
href : String - 要选中项的href

* #### setActive
+ 描述
设置激活项
+ 参数
idx : Number - 要展开的项的index
+ 返回值
当前调用该方法的对象

* #### getActive
+ 描述
获取当前展开项index
+ 参数
idx : Number - 要激活的项的index
+ 返回值
Number - 当前激活项的index
