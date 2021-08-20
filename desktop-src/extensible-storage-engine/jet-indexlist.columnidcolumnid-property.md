---
description: 深入瞭解： JET_INDEXLIST columnidcolumnid 屬性
title: JET_INDEXLIST columnidcolumnid 屬性
TOCTitle: 'columnidcolumnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcolumnid(v=EXCHG.10)
ms:contentKeyID: 55103608
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcolumnid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcolumnid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1290cec2c959bb59d3eaa9603b4b48de3e27ab139756be7168c45dbae4a1ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118074896"
---
# <a name="jet_indexlistcolumnidcolumnid-property"></a>JET_INDEXLIST columnidcolumnid 屬性

取得臨時表中的資料行 columnid，此資料表會儲存正在編制索引之資料行的 columnid。 資料行的類型為 [Long](./jet-coltyp-enumeration.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidcolumnid As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcolumnid
```

``` csharp
public JET_COLUMNID columnidcolumnid { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXLIST 類別](./jet-indexlist-class.md)

[JET_INDEXLIST 成員](./jet-indexlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
