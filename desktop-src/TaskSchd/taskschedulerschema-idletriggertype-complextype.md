---
title: idleTriggerType 複雜類型
description: 定義 IdleTrigger 元素的基底類型。
ms.assetid: 05beabb7-2e6f-4df1-809a-9f64a578d80a
keywords:
- idleTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- idleTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5c1ae0c6a88576eb7996a8151e96bb92c4a47c0d732a3558deede3b835356f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100018"
---
# <a name="idletriggertype-complex-type"></a>idleTriggerType 複雜類型

定義 [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) 元素的基底類型。

``` syntax
<xs:complexType name="idleTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
         />
    </xs:complexContent>
</xs:complexType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





