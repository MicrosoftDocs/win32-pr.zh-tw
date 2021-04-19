---
description: 從集合中捕獲 OID 物件。 這是預設屬性。
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: Oid。 Item 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dfdf65f013c5e5e1a031c03c19af9d08b8fc72c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991551"
---
# <a name="oidsitem-property"></a>Oid。 Item 屬性

\[**專案** 屬性可用於 [需求] 區段中指定的作業系統。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]

**Item** 屬性會從集合中抓取 [**OID**](oid.md)物件。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>屬性值

位於指定之索引處的 [**oid**](oid.md) 物件，或具有指定點值的 **oid** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Oid**](oids.md)
</dt> </dl>

 

 
