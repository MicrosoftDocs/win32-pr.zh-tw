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
ms.openlocfilehash: 78c4fb3a8ca85cea5b765fc1fc4521f968efd76e9169613dc4a1565a43ee1b36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131827"
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



| 元素                                                            | 類型                                                                    | 描述                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**名稱**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | 在電子郵件訊息中指定標頭欄位的名稱。<br/> |
| [**值**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | 指定電子郵件訊息中標頭欄位的值。<br/>  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





