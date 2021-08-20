---
description: 從集合中移除指定的 OID 物件。
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: Oid. Remove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 83f82bd5f514529a8f68e4e75248dbf295c86d4a2fb5e621b522d5b5b3254eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979244"
---
# <a name="oidsremove-method"></a>Oid. Remove 方法

\[**Remove** 方法可在 [需求] 區段中指定的作業系統中使用。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]

**Remove** 方法會從集合中移除指定的 [**OID**](oid.md)物件。

## <a name="syntax"></a>語法


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要移除之 [**OID**](oid.md) 物件的索引。 這可以是集合中的索引或 OID 的點值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
