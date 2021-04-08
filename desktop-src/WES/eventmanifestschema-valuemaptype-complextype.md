---
title: ValueMapType 複雜類型
description: 定義整數值與字串值之間的名稱/值對應清單。
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- ValueMapType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28fde51466ba506802c8dbc5379f1628fd943fa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685461"
---
# <a name="valuemaptype-complex-type"></a>ValueMapType 複雜類型

定義整數值與字串值之間的名稱/值對應清單。

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                     | 類型                                                                           | Description                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**地圖**](eventmanifestschema-map-valuemaptype-element.md) | [**ValueMapValueType**](eventmanifestschema-valuemapvaluetype-complextype.md) | 定義整數值與字串值之間的對應。<br/> |



## <a name="attributes"></a>屬性



| 名稱   | 類型                                                              | 描述                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NAME   | 字串                                                            | 值對應的名稱。 使用資料元素中的名稱來參考對應。<br/>                                                                                                                                                                                                                     |
| 符號 | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來參考應用程式中對應的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立對應的常數。 如果您未指定符號，編譯器會為您產生一個符號。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





