---
description: 深入瞭解： JET_INDEX_COLUMN columnid 屬性
title: Columnid 屬性 (Windows8) 的 JET_INDEX_COLUMN。
TOCTitle: 'columnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN.columnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_index_column.columnid(v=EXCHG.10)
ms:contentKeyID: 55104448
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN.columnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN.get_columnid
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN.set_columnid
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN.columnid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3fbb5cce3ccaa809ab56e5538fd2875c4b1d471639245e71a3c1b84159d4fbd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039126"
---
# <a name="jet_index_columncolumnid-property"></a>JET_INDEX_COLUMN columnid 屬性

取得或設定要取得之資料行的資料行識別碼。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnid As JET_COLUMNID
    Get
    Set
'Usage
Dim instance As JET_INDEX_COLUMN
Dim value As JET_COLUMNID

value = instance.columnid

instance.columnid = value
```

``` csharp
public JET_COLUMNID columnid { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEX_COLUMN 類別](./jet-index-column-class.md)

[JET_INDEX_COLUMN 成員](./jet-index-column-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
