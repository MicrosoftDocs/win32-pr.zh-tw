---
description: 深入瞭解： JET_DBINFOMISC dbstate 屬性
title: JET_DBINFOMISC dbstate 屬性
TOCTitle: 'dbstate property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.dbstate(v=EXCHG.10)
ms:contentKeyID: 39513341
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.dbstate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_dbstate
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.dbstate
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 90d1cbb9ed4418d88a2a76f9a9922305d83d3ac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510944"
---
# <a name="jet_dbinfomiscdbstate-property"></a>JET_DBINFOMISC dbstate 屬性

取得資料庫的一致/不一致狀態。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property dbstate As JET_dbstate
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_dbstate

value = instance.dbstate
```

``` csharp
public JET_dbstate dbstate { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_dbstate](./jet-dbstate-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
