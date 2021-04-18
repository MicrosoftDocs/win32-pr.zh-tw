---
title: RestartOnIdle (idleSettingsType) 元素
description: 指定當電腦迴圈進入閒置條件超過一次時，是否重新開機工作。
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- RestartOnIdle 元素工作排程器
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965533"
---
# <a name="restartonidle-idlesettingstype-element"></a>RestartOnIdle (idleSettingsType) 元素

指定當電腦迴圈進入閒置條件超過一次時，是否重新開機工作。

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

**RestartOnIdle** 元素是由 [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                       | 衍生自                                                                 | Description                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | 指定當電腦處於閒置狀態時，工作排程器如何執行工作。<br/> |



## <a name="remarks"></a>備註

只有當 [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) 元素設定為 True 時，才會使用這個元素。

針對腳本開發，此工作設定會使用 [**IdleSettings. RestartOnIdle**](idlesettings-restartonidle.md) 屬性來指定。

針對 c + + 開發，此工作設定會使用 [**IIdleSettings：： RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) 屬性來指定。

## <a name="examples"></a>範例

下列 XML 定義閒置設定，指出當閒置條件迴圈時，不應重新開機工作。


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





