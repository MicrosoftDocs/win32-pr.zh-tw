---
description: 定義包含一或多個計數器值的結構。
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: 結構複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983494"
---
# <a name="struct-complex-type"></a>結構複雜類型

定義包含一或多個計數器值的結構。

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱 | 類型                                                                    | 描述                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| NAME | [**男人： CSymbolType**](performance-counters-csymboltype-simple-type.md) | 結構的名稱。<br/>                                                                                                            |
| 類型 | [**男人： CSymbolType**](performance-counters-csymboltype-simple-type.md) | 識別結構的符號名稱。 [CTRPP](ctrpp.md)工具會使用您可以使用的名稱來建立結構變數。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 




