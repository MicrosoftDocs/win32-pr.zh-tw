---
title: MultipleInstancesPolicy (settingsType) 元素
description: 指定原則，定義工作排程器處理工作之多個實例的方式。
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- MultipleInstancesPolicy 元素工作排程器
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d7728d2b39fbcbed060fce409f4d721b59ef5ca324cd141d7777a5ffed110a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072448"
---
# <a name="multipleinstancespolicy-settingstype-element"></a>MultipleInstancesPolicy (settingsType) 元素

指定原則，定義工作排程器處理工作之多個實例的方式。

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

**MultipleInstancesPolicy** 元素是由 [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) simple 型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ITaskSettings 的 MultipleInstances 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances)。

如需腳本開發，請參閱 [**TaskSettings. MultipleInstances**](tasksettings-multipleinstances.md)。

### <a name="restricted-values"></a>限制的值

這個元素會限制為下列值。

-   Parallel：當現有的實例正在執行時，啟動新的實例。
-   Queue：在工作的所有其他實例完成之後，啟動新的工作實例。
-   IgnoreNew：預設值。 如果工作的現有實例正在執行，則不會啟動新的實例。
-   StopExisting：停止工作的現有實例，然後啟動新的實例。

## <a name="examples"></a>範例

下列 XML 會定義允許多個工作實例平行執行的設定元素。


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





