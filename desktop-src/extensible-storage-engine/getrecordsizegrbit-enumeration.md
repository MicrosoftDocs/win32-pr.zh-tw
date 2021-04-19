---
description: 深入瞭解： GetRecordSizeGrbit 列舉
title: GetRecordSizeGrbit 列舉
TOCTitle: GetRecordSizeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getrecordsizegrbit(v=EXCHG.10)
ms:contentKeyID: 39514742
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee95d29ed1913993aa37062137807bf8d635eecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980739"
---
# <a name="getrecordsizegrbit-enumeration"></a>GetRecordSizeGrbit 列舉

[JetGetRecordSize (JET_SESID、JET_TABLEID、JET_RECSIZE、GetRecordSizeGrbit) ](./vistaapi.jetgetrecordsize-method.md)的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetRecordSizeGrbit
'Usage
Dim instance As GetRecordSizeGrbit
```

``` csharp
[FlagsAttribute]
public enum GetRecordSizeGrbit
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
<td>預設選項。</td>
</tr>
<tr class="even">
<td></td>
<td>InCopyBuffer</td>
<td>取得已備妥或更新之複製緩衝區中的記錄大小。 否則，tableid 必須位於記錄上，而且將會使用該記錄。</td>
</tr>
<tr class="odd">
<td></td>
<td>>runningtotal</td>
<td>在填滿內容之前，JET_RECSIZE 不會歸零，可有效地做為已造訪或更新之多筆記錄的統計資料累積。</td>
</tr>
<tr class="even">
<td></td>
<td>本機</td>
<td>忽略非內建函式的 Long 值。 只會使用頁面上的本機記錄。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
