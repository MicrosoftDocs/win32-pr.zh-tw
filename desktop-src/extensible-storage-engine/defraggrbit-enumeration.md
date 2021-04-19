---
description: 深入瞭解： DefragGrbit 列舉
title: DefragGrbit 列舉
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5da047fbdad20ac40d780dc5b0bba9e986e7672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991371"
---
# <a name="defraggrbit-enumeration"></a>DefragGrbit 列舉

[JetDefragment (JET_SESID、JET_DBID、String、int32、int32、DefragGrbit) ](./api.jetdefragment-method.md)的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
```

## <a name="members"></a>成員

<table>
<thead>
<tr class="header">
<th></th>
<th>成員名稱</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>AvailSpaceTreesOnly</td>
<td>重組 ESE 資料庫空間配置的可用空間部分。 資料庫空間分為兩種類型：擁有的空間和可用空間。 擁有的空間會配置給資料表或索引，而可用空間可供在資料表或索引內使用。 可用空間的行為更動態，而且需要進行線上磁碟重組，而非擁有的空間或資料表或索引資料。</td>
</tr>
<tr class="even">
<td></td>
<td>BatchStart</td>
<td>開始新的磁碟重組工作。</td>
</tr>
<tr class="odd">
<td></td>
<td>BatchStop</td>
<td>停止磁碟重組工作。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
