---
description: 深入瞭解： JET_INDEXLIST columnidLCMapFlags 屬性
title: JET_INDEXLIST columnidLCMapFlags 屬性
TOCTitle: 'columnidLCMapFlags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55103667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidLCMapFlags
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidLCMapFlags
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2efdab9e48ad578b7a737479d2171b8d3f08599b8161deb238d7e3c5a0d9d877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485650"
---
# <a name="jet_indexlistcolumnidlcmapflags-property"></a>JET_INDEXLIST columnidLCMapFlags 屬性

取得臨時表中的資料行 columnid，此資料表會儲存索引的 unicode 正規化旗標。 資料行的類型為 [Long](./jet-coltyp-enumeration.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidLCMapFlags As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidLCMapFlags
```

``` csharp
public JET_COLUMNID columnidLCMapFlags { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXLIST 類別](./jet-indexlist-class.md)

[JET_INDEXLIST 成員](./jet-indexlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
