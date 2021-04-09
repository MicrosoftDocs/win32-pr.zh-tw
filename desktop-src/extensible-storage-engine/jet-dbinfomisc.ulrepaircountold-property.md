---
description: 深入瞭解： JET_DBINFOMISC ulRepairCountOld 屬性
title: JET_DBINFOMISC ulRepairCountOld 屬性
TOCTitle: 'ulRepairCountOld property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.ulRepairCountOld
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.ulrepaircountold(v=EXCHG.10)
ms:contentKeyID: 39509775
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.ulRepairCountOld
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.ulRepairCountOld
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_ulRepairCountOld
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_ulRepairCountOld
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66439ba4b137aecb16e94910c69ee0cb8d731ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690355"
---
# <a name="jet_dbinfomisculrepaircountold-property"></a>JET_DBINFOMISC ulRepairCountOld 屬性

取得在上次磁碟重組之前修復此資料庫的次數。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ulRepairCountOld As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Integer

value = instance.ulRepairCountOld
```

``` csharp
public int ulRepairCountOld { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
