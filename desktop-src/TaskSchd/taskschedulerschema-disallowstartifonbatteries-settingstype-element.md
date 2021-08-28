---
title: DisallowStartIfOnBatteries (settingsType) 元素
description: 指定當電腦以電池執行時，工作將不會啟動。
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- DisallowStartIfOnBatteries 元素工作排程器
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efd78b3e868c41431521b4c584a4044b9086362cf55d86466eb38ed75fcee148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100038"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a>DisallowStartIfOnBatteries (settingsType) 元素

指定當電腦以電池執行時，工作將不會啟動。

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

**DisallowStartIfOnBatteries** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

此元素的預設設定為 True。

針對腳本開發，這項資訊是透過 [**TaskSettings DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) 屬性來存取。

針對 c + + 開發，此資訊可透過 [**ITaskSettings：:D isallowstartifonbatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) 屬性來存取。

## <a name="examples"></a>範例

下列 XML 定義的設定元素不允許在電腦以電池執行時執行工作。


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
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

 

 





