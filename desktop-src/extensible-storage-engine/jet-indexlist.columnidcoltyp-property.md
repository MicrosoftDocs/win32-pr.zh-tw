---
description: 深入瞭解： JET_INDEXLIST columnidcoltyp 屬性
title: JET_INDEXLIST columnidcoltyp 屬性
TOCTitle: 'columnidcoltyp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcoltyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcoltyp(v=EXCHG.10)
ms:contentKeyID: 55103600
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcoltyp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcoltyp
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcoltyp
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcoltyp
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee68e506f1a1c885cded32e562a73d683b20f9723ecafa592f0453edaecb30a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117704646"
---
# <a name="jet_indexlistcolumnidcoltyp-property"></a>JET_INDEXLIST columnidcoltyp 屬性

取得臨時表中資料行的 columnid，該資料表會儲存正在編制索引之資料行的資料行類型。 資料行的類型為 [Long](./jet-coltyp-enumeration.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidcoltyp As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcoltyp
```

``` csharp
public JET_COLUMNID columnidcoltyp { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXLIST 類別](./jet-indexlist-class.md)

[JET_INDEXLIST 成員](./jet-indexlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
