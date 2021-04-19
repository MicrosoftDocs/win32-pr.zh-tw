---
description: 深入瞭解： JET_OBJECTLIST columnidgrbit 屬性
title: JET_OBJECTLIST columnidgrbit 屬性
TOCTitle: 'columnidgrbit property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidgrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectlist.columnidgrbit(v=EXCHG.10)
ms:contentKeyID: 55103774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidgrbit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.get_columnidgrbit
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidgrbit
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.set_columnidgrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5019e2066c87960db1cf5375e1cfb69575a44528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978344"
---
# <a name="jet_objectlistcolumnidgrbit-property"></a>JET_OBJECTLIST columnidgrbit 屬性

取得臨時表中的資料行 columnid，此資料表會儲存建立資料表時所使用的 grbits。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidgrbit As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_OBJECTLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbit
```

``` csharp
public JET_COLUMNID columnidgrbit { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_OBJECTLIST 類別](./jet-objectlist-class.md)

[JET_OBJECTLIST 成員](./jet-objectlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
