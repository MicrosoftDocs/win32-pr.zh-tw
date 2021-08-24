---
title: StopIfGoingOnBatteries (settingsType) 元素
description: 指定當電腦進入電池時，工作將會停止。
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- StopIfGoingOnBatteries 元素工作排程器
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b92be11400d1dbb223115f11334e2a596e94e9df1fd018ce16e4a646c84825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516096"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a>StopIfGoingOnBatteries (settingsType) 元素

指定當電腦進入電池時，工作將會停止。

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

**StopIfGoingOnBatteries** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

此元素的預設設定為 False。 請注意，預設值已與舊版工作排程器變更。

針對腳本開發，此設定會使用 [**TaskSettings. StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) 屬性來指定。

針對 c + + 開發，此設定會使用 [**ITaskSettings：： StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) 屬性來指定。

## <a name="examples"></a>範例

下列 XML 會定義允許工作的永久終止的設定元素。


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
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

 

 





