---
description: 深入瞭解： JET_INDEX_RANGE startColumns 屬性
title: StartColumns 屬性 (Windows8) 的 JET_INDEX_RANGE。
TOCTitle: 'startColumns property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.startColumns
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_index_range.startcolumns(v=EXCHG.10)
ms:contentKeyID: 55104437
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.startColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.get_startColumns
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.set_startColumns
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE.startColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bbd80d9cec37131d53d6607b9ff17c59eaf73c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997927"
---
# <a name="jet_index_rangestartcolumns-property"></a>JET_INDEX_RANGE startColumns 屬性

取得或設定索引開頭的資料行值。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property startColumns As JET_INDEX_COLUMN()
    Get
    Set
'Usage
Dim instance As JET_INDEX_RANGE
Dim value As JET_INDEX_COLUMN()

value = instance.startColumns

instance.startColumns = value
```

``` csharp
public JET_INDEX_COLUMN[] startColumns { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEX_RANGE 類別](./jet-index-range-class.md)

[JET_INDEX_RANGE 成員](./jet-index-range-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
