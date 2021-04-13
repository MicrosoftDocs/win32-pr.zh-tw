---
title: EventRecordID (SystemPropertiesType) 元素
description: 記錄時指派給事件的記錄號碼。
ms.assetid: d042de4d-e532-432e-bba2-1876a26860a4
keywords:
- EventRecordID 元素 EventLog
topic_type:
- apiref
api_name:
- EventRecordID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb937d075bc0ff5fc1cf8bf1335d1274aee4fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384009"
---
# <a name="eventrecordid-systempropertiestype-element"></a>EventRecordID (SystemPropertiesType) 元素

記錄時指派給事件的記錄號碼。

``` syntax
<xs:element name="EventRecordID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedLong"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

**EventRecordID** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





