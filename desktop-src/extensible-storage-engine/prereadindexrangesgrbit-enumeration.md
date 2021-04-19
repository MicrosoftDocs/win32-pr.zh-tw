---
description: 深入瞭解： PrereadIndexRangesGrbit 列舉
title: PrereadIndexRangesGrbit 列舉 (Windows8) 的列舉
TOCTitle: PrereadIndexRangesGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.prereadindexrangesgrbit(v=EXCHG.10)
ms:contentKeyID: 55104328
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4bc1b9877d4548a68aa71ea4def536af09d9693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979187"
---
# <a name="prereadindexrangesgrbit-enumeration"></a>PrereadIndexRangesGrbit 列舉

[JetPrereadIndexRanges (JET_SESID、JET_TABLEID、 \[ \] 、int32、int32、int32、 \[ \] 、PrereadIndexRangesGrbit) ](./windows8api.jetprereadindexranges-method.md)的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration PrereadIndexRangesGrbit
'Usage
Dim instance As PrereadIndexRangesGrbit
```

``` csharp
[FlagsAttribute]
public enum PrereadIndexRangesGrbit
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
<td>轉寄</td>
<td>向前 Preread。</td>
</tr>
<tr class="even">
<td></td>
<td>向後</td>
<td>向後 Preread。</td>
</tr>
<tr class="odd">
<td></td>
<td>FirstPageOnly</td>
<td>Preread 任何長時間資料行的第一頁。</td>
</tr>
<tr class="even">
<td></td>
<td>NormalizedKey</td>
<td>提供正規化的索引鍵/書簽，而不是資料行值。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
