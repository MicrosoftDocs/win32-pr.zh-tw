---
description: 深入瞭解： JET_DBINFOMISC ulBadChecksum 屬性
title: JET_DBINFOMISC ulBadChecksum 屬性
TOCTitle: 'ulBadChecksum property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.ulBadChecksum
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.ulbadchecksum(v=EXCHG.10)
ms:contentKeyID: 39515424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.ulBadChecksum
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.ulBadChecksum
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_ulBadChecksum
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_ulBadChecksum
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e67b29b889bc8196c7da33b513717ac3fb1161b6c3a497726a9fb837477a624
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891218"
---
# <a name="jet_dbinfomisculbadchecksum-property"></a>JET_DBINFOMISC ulBadChecksum 屬性

取得找到不可更正的總和檢查碼錯誤的次數。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ulBadChecksum As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Integer

value = instance.ulBadChecksum
```

``` csharp
public int ulBadChecksum { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
