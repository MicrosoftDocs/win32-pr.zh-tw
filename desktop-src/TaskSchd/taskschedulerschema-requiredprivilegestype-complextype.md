---
title: requiredPrivilegesType 複雜類型
description: 定義 RequiredPrivileges (requiredPrivilegesType) 元素的子項目和排序資訊。
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- requiredPrivilegesType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d79b75a4d4bb44aded7367fd4acfd758887815bba6fc6fcfd965f9123ac58c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658788"
---
# <a name="requiredprivilegestype-complex-type"></a>requiredPrivilegesType 複雜類型

定義 [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                           | 類型                                                                  | 描述                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [**特權**](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [**privilegeType**](taskschedulerschema-privilegetype-simpletype.md) | 指定工作的必要許可權。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





