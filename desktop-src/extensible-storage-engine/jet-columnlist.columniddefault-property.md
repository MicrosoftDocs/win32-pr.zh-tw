---
description: 深入瞭解： JET_COLUMNLIST columnidDefault 屬性
title: JET_COLUMNLIST columnidDefault 屬性
TOCTitle: 'columnidDefault property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.columnidDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnlist.columniddefault(v=EXCHG.10)
ms:contentKeyID: 55103427
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.columnidDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.get_columnidDefault
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.columnidDefault
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.set_columnidDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bec13f48ac58def00ddc8d6bc3ae51b5f67ad01ae271898522cddfe2960f20c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968389"
---
# <a name="jet_columnlistcolumniddefault-property"></a>JET_COLUMNLIST columnidDefault 屬性

取得臨時表中儲存資料行預設值之資料行的 columnid。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidDefault As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNLIST
Dim value As JET_COLUMNID

value = instance.columnidDefault
```

``` csharp
public JET_COLUMNID columnidDefault { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COLUMNLIST 類別](./jet-columnlist-class.md)

[JET_COLUMNLIST 成員](./jet-columnlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
