---
title: strTableRef 簡單類型
description: 定義字串，這個字串會參考資訊清單中的字串資料表中所定義的訊息字串，或是在 ( 的訊息中，) 檔案。
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- strTableRef 簡單類型 EventLog
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97280b342015338be1cea089f8cb14121e2e51466506e89818501302c3fa891a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750914"
---
# <a name="strtableref-simple-type"></a>strTableRef 簡單類型

定義字串，這個字串會參考資訊清單中的字串資料表中所定義的訊息字串，或是在 ( 的訊息中，) 檔案。

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**StrTableRef** 簡單類型是以下列模式限制的 **xs： string** ：

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    字串的格式必須是 $string。*stringid 指定* 或 $mc.*symbolid*。 如果字串的格式為，$string。*stringid 指定*，它必須參考資訊清單 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的字串。 如果字串的格式為 $mc *symbolid*，它必須參考訊息檔中定義的符號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 





