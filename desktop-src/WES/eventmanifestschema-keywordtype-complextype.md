---
title: KeywordType 複雜類型
description: 定義可識別事件類別目錄的關鍵字。 |KeywordType 複雜類型
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- KeywordType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d444c39796f741cd800fb393527e5adca6e50cef05de0c55c1def2bb40142a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124378"
---
# <a name="keywordtype-complex-type"></a>KeywordType 複雜類型

定義可識別事件類別目錄的關鍵字。 關鍵字是您附加至事件的標籤，用來根據事件的使用方式將事件分組。

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱    | 類型                                                              | 描述                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 遮罩    | [**HexInt64Type**](eventmanifestschema-hex64type-simpletype.md)  | 位元遮罩，必須只有一個位集。 位代表事件的類別 (例如，讀取事件或寫入事件) 。 您可以從0x0000000000000001 到0x0000800000000000 的範圍中指定位值， (位0到 47) 。<br/>                                                         |
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | 關鍵字的當地語系化顯示名稱。 訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。<br/>                                                                                                       |
| NAME    | **QName**                                                         | 關鍵字的名稱。 在提供者定義的關鍵字清單中，此名稱必須是唯一的。<br/>                                                                                                                                                                                                     |
| 符號  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來在應用程式中參考關鍵字的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立關鍵字的常數。 如果您未指定符號，編譯器會為您產生一個符號。<br/> |



## <a name="remarks"></a>備註

包含在 Windows SDK 中的 Winmeta.xml 檔案包含關鍵字清單。 這些關鍵字是保留的，不應該使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





