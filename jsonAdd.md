[toc]

#jsonAdd 侧边折叠导航栏
> Version 1.0.0
> Update 2016年6月29日

##API 文档

###属性
| 属性名 | 类型 | 描述 |
| - | - | - |
| keyName | String | 当前展开项的index |
| data | Array:Objcet | 面板对象数据源 |
| > _select | Boolean | 当前项是否选中 |
| > text | String | 当前折叠项的文字描述 |
| > href | ?String | 当前项的链接 |
| > children | Array:Objcet | 子项数组 |
| isInit | Boolean | 是否初始化完毕 |
| $allPanelBody | DOM:jQuery | 所有面板主体 |

###事件
| 方法名 | 类型 | 传入参数 | 描述 |
| - | - | - | - |
| onInit | sync | ev:Object , vm:Object | 当组件内部初始化完毕后调度 |
| onChange | async | ev:Object , vm:Object | 当组件激活项发生变化时触发 |

###方法
| 方法名 | 返回值类型 | 参数 | 描述 |
| - | - | - | - |
| _trigger | void | ev:Object , type:String | 事件触发器 |
| _clickPanel | Void | ev:Object , idx:Number | 面板点击展开收拢事件 |
| _setSelect | Void | href:String | 设置选中项 |
| changeData | Number | newData:Object | 改变当前组件的data数据源 |
| setActive | this | idx:Number | 设置展开项 |
| getActive | Number |  | 获取当前展开项index |

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
