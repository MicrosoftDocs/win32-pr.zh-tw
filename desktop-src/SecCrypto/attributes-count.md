---
description: 抓取集合中的屬性物件數目。
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Attributes 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d7b1f2213fc6de3ec08a9c9b568222f5dd54a6de6f9bdb3adb27e052e8c088e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773503"
---
# <a name="attributescount-property"></a>Attributes 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]

**Count** 屬性會抓取集合中的 [**屬性**](attribute.md)物件數目。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>屬性值

集合中的 [**屬性**](attribute.md) 物件數目。 每個 **屬性** 物件都代表集合中的單一屬性。

## <a name="remarks"></a>備註

當使用 [**Attributes**](attributes-item.md)屬性來抓取特定 **屬性** 物件時，可以使用 **Count** 屬性來指定集合中的最後一個 [**屬性**](attribute.md)物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性**](attributes.md)
</dt> </dl>

 

 
