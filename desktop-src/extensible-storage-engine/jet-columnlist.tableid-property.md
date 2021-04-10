---
description: 深入瞭解： JET_COLUMNLIST tableid 屬性
title: JET_COLUMNLIST tableid 屬性
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103528
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.get_tableid
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.set_tableid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0eb1c2338fca9a1ce503033b83a9c134a08d6a9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194303"
---
# <a name="jet_columnlisttableid-property"></a>JET_COLUMNLIST tableid 屬性

取得臨時表的 tableid。 當不再需要資料表時，這應該會關閉。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNLIST
Dim value As JET_TABLEID

value = instance.tableid
```

``` csharp
public JET_TABLEID tableid { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COLUMNLIST 類別](./jet-columnlist-class.md)

[JET_COLUMNLIST 成員](./jet-columnlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
