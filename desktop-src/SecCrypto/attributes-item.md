---
description: 抓取代表索引屬性的屬性物件。
ms.assetid: 35c54c5f-f83f-40eb-b341-129c1aac6181
title: Attributes 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 94f1ab0f9e2ef48892b27ddc51d3ac3fd1a61216d63bf4a81013e7565710a1a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879828"
---
# <a name="attributesitem-property"></a>Attributes 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]

**Item** 屬性會抓取代表索引屬性的 [**屬性**](attribute.md)物件。 這是預設屬性。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Attributes.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>屬性值

表示已編制索引之屬性的 [**屬性**](attribute.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
