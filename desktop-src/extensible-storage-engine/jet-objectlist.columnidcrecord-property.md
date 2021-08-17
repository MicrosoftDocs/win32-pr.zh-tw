---
description: 深入瞭解： JET_OBJECTLIST columnidcRecord 屬性
title: JET_OBJECTLIST columnidcRecord 屬性
TOCTitle: 'columnidcRecord property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidcRecord
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectlist.columnidcrecord(v=EXCHG.10)
ms:contentKeyID: 55103775
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidcRecord
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.set_columnidcRecord
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidcRecord
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.get_columnidcRecord
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec087e6ed3b7499b9b6c58c778576c31102c6b08e03c835319c2af422ecf9b6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765024"
---
# <a name="jet_objectlistcolumnidcrecord-property"></a>JET_OBJECTLIST columnidcRecord 屬性

取得臨時表中的資料行 columnid，其中儲存資料表中的記錄數目。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidcRecord As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_OBJECTLIST
Dim value As JET_COLUMNID

value = instance.columnidcRecord
```

``` csharp
public JET_COLUMNID columnidcRecord { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_OBJECTLIST 類別](./jet-objectlist-class.md)

[JET_OBJECTLIST 成員](./jet-objectlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
