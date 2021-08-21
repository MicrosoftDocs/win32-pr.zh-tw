---
description: 深入瞭解： Int32ColumnValue。 Size 屬性
title: Int32ColumnValue. Size 屬性
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int32columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55103332
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.get_Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 648f6b7250f31983d1a03db4e0fffceb2a5e9aaa7806c030b17fae75b755e44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118767778"
---
# <a name="int32columnvaluesize-property"></a>Int32ColumnValue. Size 屬性

取得資料行中值的大小。 這會針對可變大小的資料行傳回0， (即二進位和字串) 。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Int32ColumnValue 類別](./int32columnvalue-class.md)

[Int32ColumnValue 成員](./int32columnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
