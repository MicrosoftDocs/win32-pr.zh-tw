---
description: 深入瞭解： MakeKeyGrbit 列舉
title: MakeKeyGrbit 列舉
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112509"
---
# <a name="makekeygrbit-enumeration"></a>MakeKeyGrbit 列舉

JetMakeKey 的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
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
<td>NewKey</td>
<td>應建立新的搜尋索引鍵。 任何先前現有的搜尋金鑰都會被捨棄。</td>
</tr>
<tr class="odd">
<td></td>
<td>NormalizedKey</td>
<td>指定此選項時，會忽略所有其他選項，任何先前現有的搜尋金鑰都會被捨棄，而輸入緩衝區的內容會載入為新的搜尋索引鍵。</td>
</tr>
<tr class="even">
<td></td>
<td>KeyDataZeroLength</td>
<td>如果輸入緩衝區的大小為零，且目前的索引鍵資料行是可變長度資料行，則此選項表示輸入緩衝區包含零長度的值。 否則，輸入緩衝區大小為零會指出 Null 值。</td>
</tr>
<tr class="odd">
<td></td>
<td>StrLimit</td>
<td>此選項表示應建立搜尋索引鍵，以便將目前索引鍵資料行後面的任何索引鍵資料行視為萬用字元。</td>
</tr>
<tr class="even">
<td></td>
<td>SubStrLimit</td>
<td>此選項表示應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</td>
</tr>
<tr class="odd">
<td></td>
<td>FullColumnStartLimit</td>
<td>應將搜尋索引鍵的結構化，以便在目前的索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</td>
</tr>
<tr class="even">
<td></td>
<td>FullColumnEndLimit</td>
<td>搜尋索引鍵的建立方式，是在目前的索引鍵資料行之後的任何索引鍵資料行都會被視為萬用字元。</td>
</tr>
<tr class="odd">
<td></td>
<td>PartialColumnStartLimit</td>
<td>應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</td>
</tr>
<tr class="even">
<td></td>
<td>PartialColumnEndLimit</td>
<td>應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
