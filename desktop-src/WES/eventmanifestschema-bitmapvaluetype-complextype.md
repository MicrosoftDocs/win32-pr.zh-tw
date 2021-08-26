---
title: BitMapValueType 複雜類型
description: 定義位值與字串值之間的對應。 |BitMapValueType 複雜類型
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- BitMapValueType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d5f1b254ad4a833c1523f5a139224fc1fed508d4530a056ffdb0f111db5769e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032348"
---
# <a name="bitmapvaluetype-complex-type"></a>BitMapValueType 複雜類型

定義位值與字串值之間的對應。

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱    | 類型                                                              | 描述                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | 位值所對應的當地語系化字串值。 訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。 <br/>                                                                                  |
| 符號  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來在應用程式中參考地圖的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立對應的常數。 如果您未指定符號，編譯器會為您產生一個符號。<br/> |
| 值   | [**HexInt32Type**](eventmanifestschema-hex32type-simpletype.md)  | 要對應至字串值的位值。 您必須指定已設定單一位的十六進位數位。<br/>                                                                                                                                                                                          |



## <a name="remarks"></a>備註

地圖十六進位值 (數位前面必須加上 0x) ，並將單一位設定為名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





