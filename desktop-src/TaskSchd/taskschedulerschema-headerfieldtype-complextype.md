---
title: headerFieldType 複雜類型
description: 定義用來在電子郵件訊息中建立標頭欄位的元素。
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- headerFieldType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969572"
---
# <a name="headerfieldtype-complex-type"></a>headerFieldType 複雜類型

定義用來在電子郵件訊息中建立標頭欄位的元素。

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                            | 類型                                                                    | Description                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Name**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | 在電子郵件訊息中指定標頭欄位的名稱。<br/> |
| [**值**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | 指定電子郵件訊息中標頭欄位的值。<br/>  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





