---
title: principalsType 複雜類型
description: 定義主體元素的子項目。
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- principalsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa2aecd8ea71769b51792fcc5bd26ceca11309f43697037964a900d45c0d8254
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131739"
---
# <a name="principalstype-complex-type"></a>principalsType 複雜類型

定義 [**主體**](taskschedulerschema-principals-tasktype-element.md) 元素的子項目。

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                  | 類型                                                                   | 描述                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**主要**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | 指定主體的安全性認證。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





