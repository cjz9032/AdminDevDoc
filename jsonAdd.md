[toc]

#sidebar ����۵�������
> Version 1.0.0
> Update 2016��6��24��

##API �ĵ�

###����
| ������ | ���� | ���� |
| - | - | - |
| active | Number | ��ǰչ�����index |
| data | Array:Objcet | ����������Դ |
| > _select | Boolean | ��ǰ���Ƿ�ѡ�� |
| > text | String | ��ǰ�۵������������ |
| > href | ?String | ��ǰ������� |
| > children | Array:Objcet | �������� |
| isInit | Boolean | �Ƿ��ʼ����� |
| $allPanelBody | DOM:jQuery | ����������� |

###�¼�
| ������ | ���� | ������� | ���� |
| - | - | - | - |
| onInit | sync | ev:Object , vm:Object | ������ڲ���ʼ����Ϻ���� |
| onChange | async | ev:Object , vm:Object | �������������仯ʱ���� |

###����
| ������ | ����ֵ���� | ���� | ���� |
| - | - | - | - |
| _trigger | void | ev:Object , type:String | �¼������� |
| _clickPanel | Void | ev:Object , idx:Number | �����չ����£�¼� |
| _setSelect | Void | href:String | ����ѡ���� |
| changeData | Number | newData:Object | �ı䵱ǰ�����data����Դ |
| setActive | this | idx:Number | ����չ���� |
| getActive | Number |  | ��ȡ��ǰչ����index |

### �¼�����
* #### onInit
+ ����
������ڲ���ʼ����Ϻ����
+ ����
ev : Object - �������¼�����
vm : Object - ��ǰ�����vm

* #### onChanged
+ ����
�������������仯ʱ����
+ ����
vm : Object - ��ǰ�����vm

### ��������
* #### _trigger
+ ����
�¼�������, �����ⲿ�¼�
+ ����
ev : Object - �������¼�����
type : string - �������¼�����

* #### _renderContent
+ ����
��Ⱦ�����, ���ز�����html����, ��html��������ʾ
+ ����
idx : Number - Ҫ��Ⱦ�Ĳ�����index
+ ����ֵ
String - �ò�����html�ַ���

* #### _clickPanel
+ ����
�����չ����£�¼�
+ ����
ev : Object - �������¼�����
idx : Number - ���������index

* #### _setSelect
+ ����
����ѡ����
+ ����
href : String - Ҫѡ�����href

* #### setActive
+ ����
���ü�����
+ ����
idx : Number - Ҫչ�������index
+ ����ֵ
��ǰ���ø÷����Ķ���

* #### getActive
+ ����
��ȡ��ǰչ����index
+ ����
idx : Number - Ҫ��������index
+ ����ֵ
Number - ��ǰ�������index
