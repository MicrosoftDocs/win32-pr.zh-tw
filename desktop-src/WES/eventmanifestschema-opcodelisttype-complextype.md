---
title: OpcodeListType 複雜類型
description: 定義用來識別應用程式元件之作業的操作碼清單。
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- OpcodeListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c44a2c2fa38957f302dfe3861a89f57dbe51d44ca737268a8988f8c138be8b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767298"
---
# <a name="opcodelisttype-complex-type"></a>OpcodeListType 複雜類型

定義用來識別應用程式元件之作業的操作碼清單。

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                             | 類型                                                             | 描述                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [**opcode**](eventmanifestschema-opcode-opcodelisttype-element.md) | [**OpcodeType**](eventmanifestschema-opcodetype-complextype.md) | 定義應用程式元件內的作業。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





