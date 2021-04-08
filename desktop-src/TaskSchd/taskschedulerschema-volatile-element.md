---
title: Volatile 元素
description: 指出每次 Windows 啟動時是否自動停用工作。
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- Volatile 元素工作排程器
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca697bd0dff3a1fffd0b92a29d2fc88f1d4ed433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686361"
---
# <a name="volatile-element"></a>Volatile 元素

指出每次 Windows 啟動時是否自動停用工作。

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

**Volatile** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自 | Description                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) |              | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

若是 c + + 程式設計，則會使用 [**ITaskSettings3：： Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) 屬性來指定此閒置設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





