---
description: 深入瞭解： SnapshotTruncateLogGrbit 列舉
title: 'SnapshotTruncateLogGrbit 列舉 (的列舉) '
TOCTitle: SnapshotTruncateLogGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.snapshottruncateloggrbit(v=EXCHG.10)
ms:contentKeyID: 39516474
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8baf9f9ec15e91183d2b01a07da9aeda0c7fec18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973874"
---
# <a name="snapshottruncateloggrbit-enumeration"></a>SnapshotTruncateLogGrbit 列舉

[JetOSSnapshotTruncateLog (JET_OSSNAPID、SnapshotTruncateLogGrbit) ](./vistaapi.jetossnapshottruncatelog-method.md)和[JetOSSnapshotTruncateLogInstance (JET_OSSNAPID、JET_INSTANCE、SnapshotTruncateLogGrbit) ](./vistaapi.jetossnapshottruncateloginstance-method.md)的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotTruncateLogGrbit
'Usage
Dim instance As SnapshotTruncateLogGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotTruncateLogGrbit
```

## <a name="members"></a>成員

<table>
<thead>
<tr class="header">
<th></th>
<th>成員名稱</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>無</td>
<td>不會發生截斷。</td>
</tr>
<tr class="even">
<td></td>
<td>AllDatabasesSnapshot</td>
<td>附加所有資料庫，讓儲存引擎可以計算並進行記錄截斷。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
