---
title: IdleSettings (settingsType) 元素
description: 指定當電腦處於閒置狀態時，工作排程器如何執行工作。
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- IdleSettings 元素工作排程器
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105221"
---
# <a name="idlesettings-settingstype-element"></a>IdleSettings (settingsType) 元素

指定當電腦處於閒置狀態時，工作排程器如何執行工作。 如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

**IdleSettings** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素

| 元素                                                           | 衍生自                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |

## <a name="child-elements"></a>子元素

> [!NOTE]
> *持續時間* 和 *WaitTimeout* 設定已淘汰。 它們仍然存在於工作排程器的使用者介面中，而且其介面方法可能仍會傳回有效值，但不再使用這些值。

| 元素                                                                                  | 類型     | Description                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean  | 指定當電腦迴圈進入閒置條件超過一次時，是否重新開機工作。<br/>       |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean  | 指定如果閒置條件在工作完成之前結束，工作排程器將停止工作。<br/> |
| 已 **淘汰**： [**持續時間**](taskschedulerschema-duration-idlesettingstype-element.md)                | duration | 指定在執行工作之前，電腦必須處於閒置狀態的時間長度。<br/>                              |
| 已 **淘汰**： [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          | duration | 指定工作排程器將等候閒置條件發生的時間量。<br/>                |

## <a name="remarks"></a>備註

針對腳本開發，閒置設定會使用 [**TaskSettings. IdleSettings**](tasksettings-idlesettings.md) 屬性來指定。

針對 c + + 開發，閒置設定是使用 [**ITaskSettings：： IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) 屬性來指定。

## <a name="examples"></a>範例

下列 XML 定義了設定元素，可讓工作排程器等候24小時的閒置條件，然後只允許10分鐘的 {IdleDuration) 起始工作。

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |

## <a name="see-also"></a>另請參閱

[工作排程器架構元素](task-scheduler-schema-elements.md)

[工作排程器](task-scheduler-start-page.md)
