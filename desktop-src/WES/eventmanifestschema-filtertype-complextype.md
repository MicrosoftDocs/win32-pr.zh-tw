---
title: FilterType 複雜類型
description: 定義會話用來根據事件資料篩選事件的資料篩選。
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- FilterType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467013"
---
# <a name="filtertype-complex-type"></a>FilterType 複雜類型

定義會話用來根據事件資料篩選事件的資料篩選。

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱    | 類型                                                              | Description                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | 篩選的當地語系化描述。 訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。<br/>                                   |
| NAME    | **QName**                                                         | 識別篩選準則的名稱。<br/>                                                                                                                                                                                                    |
| 符號  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來參考應用程式中之篩選準則的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立篩選的常數。<br/> |
| tid     | token                                                             | 範本識別碼，描述當會話啟用提供者時，會話傳遞給提供者的篩選資料。<br/>                                                                                                            |
| value   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | 整數值，可唯一識別您定義之篩選器清單內的篩選準則。<br/>                                                                                                                                      |
| version | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | 識別此篩選版本的整數值。 如果未指定，則值為零。<br/>                                                                                                                                     |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 





