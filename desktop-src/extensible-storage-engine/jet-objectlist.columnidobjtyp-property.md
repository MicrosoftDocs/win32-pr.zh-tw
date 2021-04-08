---
description: 深入瞭解： JET_OBJECTLIST columnidobjtyp 屬性
title: JET_OBJECTLIST columnidobjtyp 屬性
TOCTitle: 'columnidobjtyp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidobjtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectlist.columnidobjtyp(v=EXCHG.10)
ms:contentKeyID: 55103770
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidobjtyp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.set_columnidobjtyp
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.get_columnidobjtyp
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.columnidobjtyp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21c20b787a01b23d601f2834cdaa8786b30c67a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945181"
---
# <a name="jet_objectlistcolumnidobjtyp-property"></a>JET_OBJECTLIST columnidobjtyp 屬性

取得臨時表中儲存資料表類型之資料行的 columnid。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidobjtyp As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_OBJECTLIST
Dim value As JET_COLUMNID

value = instance.columnidobjtyp
```

``` csharp
public JET_COLUMNID columnidobjtyp { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_OBJECTLIST 類別](./jet-objectlist-class.md)

[JET_OBJECTLIST 成員](./jet-objectlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
