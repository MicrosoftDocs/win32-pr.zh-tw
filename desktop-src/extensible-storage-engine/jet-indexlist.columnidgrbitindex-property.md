---
description: 深入瞭解： JET_INDEXLIST columnidgrbitIndex 屬性
title: JET_INDEXLIST columnidgrbitIndex 屬性
TOCTitle: 'columnidgrbitIndex property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidgrbitindex(v=EXCHG.10)
ms:contentKeyID: 55103615
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidgrbitIndex
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidgrbitIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae8d31661451a2bd1c7c5f942141c27ae552c578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851028"
---
# <a name="jet_indexlistcolumnidgrbitindex-property"></a>JET_INDEXLIST columnidgrbitIndex 屬性

取得臨時表中的資料行 columnid，此資料表會儲存用於索引的 grbits。 請參閱 [CreateIndexGrbit](./createindexgrbit-enumeration.md)。 資料行的類型為 [Long](./jet-coltyp-enumeration.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidgrbitIndex As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbitIndex
```

``` csharp
public JET_COLUMNID columnidgrbitIndex { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXLIST 類別](./jet-indexlist-class.md)

[JET_INDEXLIST 成員](./jet-indexlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
