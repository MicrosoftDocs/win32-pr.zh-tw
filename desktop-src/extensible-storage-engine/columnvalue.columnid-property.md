---
description: 深入瞭解： ColumnValue. Columnid 屬性
title: ColumnValue. Columnid 屬性
TOCTitle: 'Columnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Columnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.columnid(v=EXCHG.10)
ms:contentKeyID: 55101205
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Columnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Columnid
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Columnid
- Microsoft.Isam.Esent.Interop.ColumnValue.set_Columnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61743d1aa49200cf871b9ec37d3506ed3ccd040c87dfea5ca1f4150b57328278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083779"
---
# <a name="columnvaluecolumnid-property"></a>ColumnValue. Columnid 屬性

取得或設定要設定或取出的 columnid。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property Columnid As JET_COLUMNID
    Get
    Set
'Usage
Dim instance As ColumnValue
Dim value As JET_COLUMNID

value = instance.Columnid

instance.Columnid = value
```

``` csharp
public JET_COLUMNID Columnid { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnValue 類別](./columnvalue-class.md)

[ColumnValue 成員](./columnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
