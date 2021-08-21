---
description: 深入瞭解： ColumnInfo DefaultValue 屬性
title: ColumnInfo DefaultValue 屬性
TOCTitle: 'DefaultValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnInfo.DefaultValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columninfo.defaultvalue(v=EXCHG.10)
ms:contentKeyID: 55100932
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnInfo.DefaultValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnInfo.DefaultValue
- Microsoft.Isam.Esent.Interop.ColumnInfo.get_DefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74ba20fbeae81dcaaa7c52a14021450348734e3da09dfd337e50ff8ea4a47682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042406"
---
# <a name="columninfodefaultvalue-property"></a>ColumnInfo DefaultValue 屬性

取得資料行的預設值。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property DefaultValue As IList(Of Byte)
    Get
'Usage
Dim instance As ColumnInfo
Dim value As IList(Of Byte)

value = instance.DefaultValue
```

``` csharp
public IList<byte> DefaultValue { get; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.collections.generic.ilist-1) 。\<[Byte](/dotnet/api/system.byte)\>  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnInfo 類別](./columninfo-class.md)

[ColumnInfo 成員](./columninfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
