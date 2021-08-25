---
title: ProcessingErrorDataType 複雜類型
description: 定義在轉譯事件的事件資料時所發生的錯誤。
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- ProcessingErrorDataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ee34e566bafa72812303fcb1f41b664a45aa77772e6ee818b9cb79bc94cbb51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904521"
---
# <a name="processingerrordatatype-complex-type"></a>ProcessingErrorDataType 複雜類型

定義在轉譯事件的事件資料時所發生的錯誤。 如果事件資料與資訊清單中的事件資料範本定義不相符，就會發生這種情況。

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
         />
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

## <a name="child-elements"></a>子元素



| 元素                                                                          | 類型        | 描述                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [**DataItemName**](eventschema-dataitemname-processingerrordatatype-element.md) | 字串      | 造成錯誤之事件資料項目的名稱。<br/>                    |
| [**ErrorCode**](eventschema-errorcode-processingerrordatatype-element.md)       | unsignedInt | 轉譯事件資料時所發生的錯誤錯誤碼。<br/> |
| [**EventPayload**](eventschema-eventpayload-processingerrordatatype-element.md) | hexBinary   | 包含整個事件資料的二進位 blob。<br/>                        |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





