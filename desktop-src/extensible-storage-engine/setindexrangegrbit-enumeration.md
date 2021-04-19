---
description: 深入瞭解： SetIndexRangeGrbit 列舉
title: SetIndexRangeGrbit 列舉
TOCTitle: SetIndexRangeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setindexrangegrbit(v=EXCHG.10)
ms:contentKeyID: 39515181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cda73597f88d2c8fca911ebb96d7a3c6399ed9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974074"
---
# <a name="setindexrangegrbit-enumeration"></a>SetIndexRangeGrbit 列舉

JetSetIndexRange 的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetIndexRangeGrbit
'Usage
Dim instance As SetIndexRangeGrbit
```

``` csharp
[FlagsAttribute]
public enum SetIndexRangeGrbit
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
<td>RangeInclusive</td>
<td>此選項表示索引範圍的限制為內含。</td>
</tr>
<tr class="odd">
<td></td>
<td>RangeUpperLimit</td>
<td>資料指標中的搜尋索引鍵代表索引項目的搜尋準則，最接近索引的結尾會符合索引範圍。</td>
</tr>
<tr class="even">
<td></td>
<td>RangeInstantDuration</td>
<td>索引範圍應在建立後立即移除。 這適合用來測試符合搜尋準則的索引項目是否存在。</td>
</tr>
<tr class="odd">
<td></td>
<td>RangeRemove</td>
<td>取消和現有的索引範圍。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
