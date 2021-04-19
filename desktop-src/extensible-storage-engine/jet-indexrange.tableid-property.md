---
description: 深入瞭解： JET_INDEXRANGE tableid 屬性
title: JET_INDEXRANGE tableid 屬性
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexrange.tableid(v=EXCHG.10)
ms:contentKeyID: 55103657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.set_tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.get_tableid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afd5c9401b3b0284f463aa1dbd6676440fd64b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979257"
---
# <a name="jet_indexrangetableid-property"></a>JET_INDEXRANGE tableid 屬性

取得或設定包含索引範圍的資料指標。 資料指標的索引範圍應設定為 JetSetIndexRange。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Set
'Usage
Dim instance As JET_INDEXRANGE
Dim value As JET_TABLEID

value = instance.tableid

instance.tableid = value
```

``` csharp
public JET_TABLEID tableid { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXRANGE 類別](./jet-indexrange-class.md)

[JET_INDEXRANGE 成員](./jet-indexrange-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
