---
description: 抓取集合中的 Oid 數目。
ms.assetid: 074ab4a2-b48e-4f43-8ea2-9d28477b2b33
title: Oid 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 88d6e436305f50ad2288ec2a3cd2546be23371415a744e7107b88216d5ebfef1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979612"
---
# <a name="oidscount-property"></a>Oid 屬性

\[[ **計數** ] 屬性可用於 [需求] 區段中指定的作業系統。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]

**Count** 屬性會抓取集合中的 oid 數目。

## <a name="syntax"></a>Syntax


```VB
OIDs.Count As Long
```



## <a name="property-value"></a>屬性值

集合中的 [**OID**](oid.md) 物件數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Oid**](oids.md)
</dt> </dl>

 

 
