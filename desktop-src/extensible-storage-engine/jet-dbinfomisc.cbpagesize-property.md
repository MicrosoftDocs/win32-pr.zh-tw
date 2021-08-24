---
description: 深入瞭解： JET_DBINFOMISC cbPageSize 屬性
title: JET_DBINFOMISC cbPageSize 屬性
TOCTitle: 'cbPageSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.cbpagesize(v=EXCHG.10)
ms:contentKeyID: 39512879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_cbPageSize
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_cbPageSize
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a4b72ff96337637c90aaeaa48bfbb344f0d36e9658536cb6efa9c5399741063
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891418"
---
# <a name="jet_dbinfomisccbpagesize-property"></a>JET_DBINFOMISC cbPageSize 屬性

取得資料庫頁面大小。 值為0表示有 4 Kb 的頁面。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbPageSize As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Integer

value = instance.cbPageSize
```

``` csharp
public int cbPageSize { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
