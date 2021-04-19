---
title: KeywordListType 複雜類型
description: 定義分類事件的關鍵字清單。 |KeywordListType 複雜類型
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- KeywordListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106989155"
---
# <a name="keywordlisttype-complex-type"></a>KeywordListType 複雜類型

定義分類事件的關鍵字清單。

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                | 類型                                                               | Description                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**關鍵 字**](eventmanifestschema-keyword-keywordlisttype-element.md) | [**KeywordType**](eventmanifestschema-keywordtype-complextype.md) | 定義可識別事件類別目錄的關鍵字。 您可以指定最多48個關鍵字。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





