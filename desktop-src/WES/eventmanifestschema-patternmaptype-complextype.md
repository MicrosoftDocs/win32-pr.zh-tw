---
title: PatternMapType 複雜類型
description: 未使用。 定義兩個正則運算式之間的對應。 其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則是用來在服務將字串放回訊息字串之前變更字串。
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- PatternMapType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465757"
---
# <a name="patternmaptype-complex-type"></a>PatternMapType 複雜類型

未使用。 定義兩個正則運算式之間的對應。 其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則是用來在服務將字串放回訊息字串之前變更字串。

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                       | 類型                                                                               | Description                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**地圖**](eventmanifestschema-map-patternmaptype-element.md) | [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md) | 定義用來在訊息字串中尋找相符字串的正則運算式，並加以修改。<br/> |



## <a name="attributes"></a>屬性



| 名稱   | 類型                                                              | Description                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format | anyURI                                                            | 要使用的正則運算式引擎。<br/>                                                                                                                                                                                                                                                                    |
| NAME   | **QName**                                                         | 模式對應的名稱。 使用資料元素中的名稱來參考對應。<br/>                                                                                                                                                                                                                   |
| 符號 | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來參考應用程式中對應的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立對應的常數。 如果您未指定符號，編譯器會為您產生一個符號。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





