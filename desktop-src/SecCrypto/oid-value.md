---
description: 設定或抓取識別碼的 OID 點值。
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: 老。Value 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: edaca987dbba57127c922161fbc6c6cd9473732ba1b7d1339618009335c904cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979730"
---
# <a name="oidvalue-property"></a>老。Value 屬性

\[[ **值** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請在 [**system.object**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)命名空間中使用 [**Oid 類別**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1)。\]

**Value** 屬性會設定或抓取識別碼的 OID 點值。

## <a name="syntax"></a>Syntax


```VB
OID.Value As String
```



## <a name="property-value"></a>屬性值

識別碼的 OID 點值。 如需可能的值，請參閱 Wincrypt。

## <a name="remarks"></a>備註

如果已設定 **Value** 屬性， [**FriendlyName**](oid-friendlyname.md) 屬性會設定為對應的顯示名稱。 如果已設定 [ **FriendlyName** ] 屬性，則 [ **值** ] 屬性會設定為對應的點值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**老**](oid.md)
</dt> </dl>

 

 
