---
description: 將指定的 OID 物件加入至集合。
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: Oid. Add 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981371"
---
# <a name="oidsadd-method"></a>Oid. Add 方法

\[**Add** 方法可用於 [需求] 區段中指定的作業系統。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]

**Add** 方法會將指定的 [**OID**](oid.md)物件加入至集合。

## <a name="syntax"></a>語法


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*OID* \[在\]
</dt> <dd>

要加入至集合的 [**OID**](oid.md) 物件。 **OID** 物件會根據其點值以排序的順序加入。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
