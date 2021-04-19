---
description: 深入瞭解： UInt32ColumnValue。 Size 屬性
title: UInt32ColumnValue. Size 屬性
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.UInt32ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint32columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55104179
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt32ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt32ColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.UInt32ColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c80fd3afb34c73d5d054a11f57c42af52be776ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978996"
---
# <a name="uint32columnvaluesize-property"></a>UInt32ColumnValue. Size 屬性

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

[UInt32ColumnValue 類別](./uint32columnvalue-class.md)

[UInt32ColumnValue 成員](./uint32columnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
