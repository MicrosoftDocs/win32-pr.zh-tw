---
title: RunOnlyIfIdle (settingsType) 元素
description: 指定只有當電腦處於閒置狀態時，才會執行工作。
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- RunOnlyIfIdle 元素工作排程器
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025357"
---
# <a name="runonlyifidle-settingstype-element"></a>RunOnlyIfIdle (settingsType) 元素

指定只有當電腦處於閒置狀態時，才會執行工作。

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

**RunOnlyIfIdle** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ITaskSettings 的 RunOnlyIfIdle 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle)。

如需腳本開發，請參閱 [**TaskSettings. RunOnlyIfIdle**](tasksettings-runonlyifidle.md)。

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

 

 





