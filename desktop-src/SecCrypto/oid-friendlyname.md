---
description: 設定或抓取識別碼的顯示名稱。
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: 老。FriendlyName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001851"
---
# <a name="oidfriendlyname-property"></a>老。FriendlyName 屬性

\[[ **FriendlyName** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請在 [**system.object**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)命名空間中使用 [**Oid 類別**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1)。\]

**FriendlyName** 屬性會設定或抓取識別碼的顯示名稱。

## <a name="syntax"></a>Syntax


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a>屬性值

[**OID**](oid.md)的顯示名稱。

## <a name="remarks"></a>備註

如果已設定 [ **FriendlyName** ] 屬性，則 [ [**值**](oid-value.md) ] 屬性會設定為對應的點值。 如果已設定 **Value** 屬性， **FriendlyName** 屬性會設定為對應的顯示名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**老**](oid.md)
</dt> </dl>

 

 
