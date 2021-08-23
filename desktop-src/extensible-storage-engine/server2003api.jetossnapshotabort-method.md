---
description: 深入瞭解： Server2003Api. JetOSSnapshotAbort 方法
title: 'Server2003Api. JetOSSnapshotAbort 方法 (Server2003 的) '
TOCTitle: 'JetOSSnapshotAbort method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetossnapshotabort(v=EXCHG.10)
ms:contentKeyID: 55104209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ca7633ce07468c7c516988e7e048b6c9673bc3ed685bbee35a4f5f094a59db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780218"
---
# <a name="server2003apijetossnapshotabort-method"></a>Server2003Api. JetOSSnapshotAbort 方法

通知引擎在凍結期間結束時，它可以繼續正常 IO 作業，並以失敗的快照集結束。

**命名空間：**  [Microsoft Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetOSSnapshotAbort ( _
    snapid As JET_OSSNAPID, _
    grbit As SnapshotAbortGrbit _
)
'Usage
Dim snapid As JET_OSSNAPID
Dim grbit As SnapshotAbortGrbitServer2003Api.JetOSSnapshotAbort(snapid, _
    grbit)
```

``` csharp
public static void JetOSSnapshotAbort(
    JET_OSSNAPID snapid,
    SnapshotAbortGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - snapid  
    類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    快照會話的識別碼。

<!-- end list -->

  - grbit  
    型別： [Server2003. SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)  
    
    此呼叫的選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Server2003Api 類別](./server2003api-class.md)

[Server2003Api 成員](./server2003api-members.md)

[Server2003 命名空間。](./microsoft.isam.esent.interop.server2003-namespace.md)
