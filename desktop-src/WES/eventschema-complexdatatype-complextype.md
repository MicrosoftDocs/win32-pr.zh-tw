---
title: ComplexDataType 複雜類型
description: 定義包含一或多個資料項目的結構。
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- ComplexDataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f86b15defc32469dd1a4abd0f6366e1a93d4b83441b1e1518ff7ac999f30bd59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055806"
---
# <a name="complexdatatype-complex-type"></a>ComplexDataType 複雜類型

定義包含一或多個資料項目的結構。

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                  | 類型                                                      | 描述                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**資料**](eventschema-data-complexdatatype-element.md) | [**資料類型**](eventschema-datafieldtype-complextype.md) | 結構中資料項目的清單。 專案清單的順序與範本中所定義的順序相同。<br/> |



## <a name="attributes"></a>屬性



| 名稱 | 類型   | 描述                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 名稱 | 字串 | 結構的名稱。 這是您在範本中定義結構時所指定的名稱， (查看 [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) 複雜類型) 。<br/> |



## <a name="remarks"></a>備註

[**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender)函式會以二進位 blob 的形式呈現結構的內容;函數不會轉譯結構的個別資料項目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





