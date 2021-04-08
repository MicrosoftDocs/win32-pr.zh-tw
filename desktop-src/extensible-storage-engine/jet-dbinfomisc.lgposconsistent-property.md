---
description: 深入瞭解： JET_DBINFOMISC lgposConsistent 屬性
title: JET_DBINFOMISC lgposConsistent 屬性
TOCTitle: 'lgposConsistent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.lgposConsistent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.lgposconsistent(v=EXCHG.10)
ms:contentKeyID: 39516221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.lgposConsistent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_lgposConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.lgposConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_lgposConsistent
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3549e02b99b70f0704cd716410123dd732b1e518
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112120"
---
# <a name="jet_dbinfomisclgposconsistent-property"></a>JET_DBINFOMISC lgposConsistent 屬性

取得資料庫保持一致時的 lgpo。 如果資料庫不一致，則此值為 null。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property lgposConsistent As JET_LGPOS
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LGPOS

value = instance.lgposConsistent
```

``` csharp
public JET_LGPOS lgposConsistent { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
