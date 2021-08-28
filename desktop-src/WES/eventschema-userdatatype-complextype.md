---
title: UserDataType 複雜類型
description: 定義指定事件資料版面配置的 XML 片段。
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- UserDataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747f2e30f6b2588cdfd6a9f0dd50187b73817996bd3725a571283a7929c91b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904188"
---
# <a name="userdatatype-complex-type"></a>UserDataType 複雜類型

定義指定事件資料版面配置的 XML 片段。

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





