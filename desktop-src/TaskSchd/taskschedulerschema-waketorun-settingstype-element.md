---
title: WakeToRun (settingsType) 元素
description: 指定工作排程器會在執行工作時喚醒電腦。
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- WakeToRun 元素工作排程器
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12d16f9f06685a427a8f3e7c4f2356dff0bc6415e50379ba752a4bc3a3fec8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872058"
---
# <a name="waketorun-settingstype-element"></a>WakeToRun (settingsType) 元素

指定工作排程器會在執行工作時喚醒電腦。

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

**WakeToRun** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

當工作排程器服務喚醒電腦以執行工作時，即使電腦不再處於睡眠或睡眠模式，畫面仍會保持關閉狀態。 當 Windows Vista 偵測到使用者已回到使用電腦時，畫面會開啟。

針對 c + + 開發，請參閱 [**ITaskSettings 的 WakeToRun 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun)。

如需腳本開發，請參閱 [**TaskSettings. WakeToRun**](tasksettings-waketorun.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





