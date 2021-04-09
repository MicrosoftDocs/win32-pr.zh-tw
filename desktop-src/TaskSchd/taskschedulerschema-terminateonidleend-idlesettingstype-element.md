---
title: StopOnIdleEnd (idleSettingsType) 元素
description: 指定如果閒置條件在工作完成之前結束，工作排程器將停止工作。
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- StopOnIdleEnd 元素工作排程器
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934977"
---
# <a name="stoponidleend-idlesettingstype-element"></a>StopOnIdleEnd (idleSettingsType) 元素

指定如果閒置條件在工作完成之前結束，工作排程器將停止工作。

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

**StopOnIdleEnd** 元素是由 [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                       | 衍生自                                                                 | Description                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | 指定當電腦處於閒置狀態時，工作排程器如何執行工作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IIdleSettings 的 StopOnIdleEnd 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend)。

如需腳本開發，請參閱 [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md)。

## <a name="examples"></a>範例

下列 XML 定義閒置設定，指出當閒置條件結束時，不應執行工作。


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
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
</dt> </dl>

 

 





