---
title: InputTypeListType 複雜類型
description: 定義輸入類型的清單。
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- InputTypeListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106037"
---
# <a name="inputtypelisttype-complex-type"></a>InputTypeListType 複雜類型

定義輸入類型的清單。

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                | 類型                                                           | Description                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [**inType**](eventmanifestschema-intype-inputtypelisttype-element.md) | [**InputType**](eventmanifestschema-inputtype-complextype.md) | 定義輸入類型。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





