---
title: BitMapType 複雜類型
description: 定義位值與字串值之間的名稱/值對應清單。
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- BitMapType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466973"
---
# <a name="bitmaptype-complex-type"></a>BitMapType 複雜類型

定義位值與字串值之間的名稱/值對應清單。

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                   | 類型                                                                       | Description                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**地圖**](eventmanifestschema-map-bitmaptype-element.md) | [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md) | 定義位值與字串值之間的對應。<br/> |



## <a name="attributes"></a>屬性



| 名稱   | 類型                                                              | 描述                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NAME   | 字串                                                            | 點陣圖的名稱。<br/>                                                                                                                                                                                                                                                                                  |
| 符號 | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來參考應用程式中對應的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立對應的常數。 如果您未指定符號，編譯器會為您產生一個符號。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





