---
title: patternMap (PatternMapListType) 元素
description: 定義兩個正則運算式之間的對應。 其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則用來在服務將字串放回訊息字串之前變更字串。
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- patternMap 元素 EventLog
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024524"
---
# <a name="patternmap-patternmaplisttype-element"></a>patternMap (PatternMapListType) 元素

定義兩個正則運算式之間的對應。 其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則用來在服務將字串放回訊息字串之前變更字串。

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

**PatternMap** 元素是由 [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**patternMaps (NamedQueryType)**](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





