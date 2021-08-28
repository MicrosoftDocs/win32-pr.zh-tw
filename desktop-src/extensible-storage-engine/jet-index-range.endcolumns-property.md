---
description: 深入瞭解： JET_INDEX_RANGE endColumns 屬性
title: EndColumns 屬性 (Windows8) 的 JET_INDEX_RANGE。
TOCTitle: 'endColumns property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.endColumns
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_index_range.endcolumns(v=EXCHG.10)
ms:contentKeyID: 55107824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.endColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.set_endColumns
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.endColumns
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.get_endColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 25491afd74b0ccfd20d90a72bdefd7b0cfd844a7f3f4eb1e7136452897e7d2a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119110079"
---
# <a name="jet_index_rangeendcolumns-property"></a>JET_INDEX_RANGE endColumns 屬性

取得或設定索引結尾的資料行值。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property endColumns As JET_INDEX_COLUMN()
    Get
    Set
'Usage
Dim instance As JET_INDEX_RANGE
Dim value As JET_INDEX_COLUMN()

value = instance.endColumns

instance.endColumns = value
```

``` csharp
public JET_INDEX_COLUMN[] endColumns { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEX_RANGE 類別](./jet-index-range-class.md)

[JET_INDEX_RANGE 成員](./jet-index-range-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
