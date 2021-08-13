---
description: 深入瞭解： VistaApi. JetOSSnapshotTruncateLogInstance 方法
title: 'VistaApi. JetOSSnapshotTruncateLogInstance 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetOSSnapshotTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55104197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00a30d604aa57aeaff1d97ca8f92397d6919a769f9416eb504b2d22abe186f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471218"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a>VistaApi. JetOSSnapshotTruncateLogInstance 方法

在快照會話期間截斷指定之實例的記錄檔。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLogInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLogInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLogInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - 快照集  
    類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    快照集識別碼。

<!-- end list -->

  - instance  
    類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    要 truncat 記錄檔的實例。

<!-- end list -->

  - grbit  
    類型： [SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)的類型。  
    
    此呼叫的選項。

## <a name="remarks"></a>備註

只有在使用 [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) 選項建立快照集時，才應該呼叫這個函數。 否則，在呼叫 [JetOSSnapshotThaw (JET_OSSNAPID，SnapshotThawGrbit) ](./api.jetossnapshotthaw-method.md)之後，快照集會話就會結束。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[VistaApi 類別](./vistaapi-class.md)

[VistaApi 成員](./vistaapi-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
