---
description: 深入瞭解： JET_DBINFOMISC fUpgradeDb 屬性
title: JET_DBINFOMISC fUpgradeDb 屬性
TOCTitle: 'fUpgradeDb property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.fUpgradeDb
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.fupgradedb(v=EXCHG.10)
ms:contentKeyID: 39514685
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.fUpgradeDb
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_fUpgradeDb
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_fUpgradeDb
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.fUpgradeDb
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 702f66afe13a0355744477d23e79eb147a463328
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468724"
---
# <a name="jet_dbinfomiscfupgradedb-property"></a>JET_DBINFOMISC fUpgradeDb 屬性

取得值，指出是否正在升級資料庫。 此值僅供內部使用。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property fUpgradeDb As Boolean
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Boolean

value = instance.fUpgradeDb
```

``` csharp
public bool fUpgradeDb { get; internal set; }
```

#### <a name="property-value"></a>屬性值

型別： [system.object](/dotnet/api/system.boolean)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
