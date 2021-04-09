---
description: 深入瞭解： JET_ENUMCOLUMN cEnumColumnValue 屬性
title: JET_ENUMCOLUMN cEnumColumnValue 屬性
TOCTitle: 'cEnumColumnValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.cenumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103498
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_cEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_cEnumColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee9649f7c546dee155dfcda35ece32dfe346c689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689615"
---
# <a name="jet_enumcolumncenumcolumnvalue-property"></a>JET_ENUMCOLUMN cEnumColumnValue 屬性

取得針對資料行列舉的資料行值數目。 只有在未[ColumnSingleValue](./jet-wrn-enumeration.md) [err](./jet-enumcolumn.err-property.md)時，才會使用這個成員。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cEnumColumnValue As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As Integer

value = instance.cEnumColumnValue
```

``` csharp
public int cEnumColumnValue { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_ENUMCOLUMN 類別](./jet-enumcolumn-class.md)

[JET_ENUMCOLUMN 成員](./jet-enumcolumn-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
