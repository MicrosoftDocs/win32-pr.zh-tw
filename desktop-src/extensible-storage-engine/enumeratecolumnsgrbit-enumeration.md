---
description: 深入瞭解： EnumerateColumnsGrbit 列舉
title: EnumerateColumnsGrbit 列舉
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979408"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>EnumerateColumnsGrbit 列舉

JetEnumerateColumns 的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a>成員

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
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
<td>EnumerateCompressOutput</td>
<td>列舉資料行值時，我們將會以壓縮格式傳回所有資料行，而這些資料行只會傳回一個非 Null 資料行值。 這類資料行的狀態將會設定為 <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> ，而資料行值的大小和包含資料行值的記憶體則會直接傳回 <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> 結構中。 不保證會以這種方式壓縮所有合格的資料行。 如需詳細資訊，請參閱 <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> 。</td>
</tr>
<tr class="odd">
<td></td>
<td>EnumerateCopy</td>
<td>此選項表示應該列舉記錄的已修改資料行值，而不是原始資料行值。 如果資料行值尚未修改，則會列舉原始資料行值。 如此一來，插入或更新記錄時，可能會列舉尚未插入或更新的資料行值。
<p>此選項與 <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>相同。</p></td>
</tr>
<tr class="even">
<td></td>
<td>EnumerateIgnoreDefault</td>
<td>如果指定的資料行不存在於記錄中，則不會傳回任何資料行值。 一般來說，在此案例中會傳回資料行的預設值（如果有的話）。 如果資料行設定為與預設值不同的值，則會傳回不同的值 (也就是說，如果具有預設值的資料行明確設定為 Null，則會傳回 Null 做為該資料行的值) 。 即使已要求此選項，仍然可以看到剛好等於預設值的資料行值。 移除符合其預設值的資料行值不會進行任何工作。 請務必記住，在搭配 EnumeratePresenceOnly 或 EnumerateTaggedOnly 使用時，此選項會影響 <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID、JET_TABLEID、Int32、[]、int32、[]、JET_PFNREALLOC、IntPtr、int32、EnumerateColumnsGrbit) </a> 的輸出。</td>
</tr>
<tr class="odd">
<td></td>
<td>EnumeratePresenceOnly</td>
<td>如果要求的資料行或資料行值有非 Null 的值，則不會傳回相關聯的資料。 相反地，該資料行或資料行值的關聯狀態將會設定為 <a href="hh557250(v=exchg.10).md">ColumnPresent</a>。 如果資料行或資料行的值為 Null，則 <a href="hh557250(v=exchg.10).md">ColumnNull</a> 會如往常般傳回。</td>
</tr>
<tr class="even">
<td></td>
<td>EnumerateTaggedOnly</td>
<td>列舉記錄中的所有資料行值時 (例如，當 numColumnids 為零) 時，只會傳回已標記的資料行值。 列舉資料行識別碼的特定陣列時，不允許使用這個選項。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

[EnumerateIgnoreUserDefinedDefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[EnumerateInRecordOnly](./windows7grbits.enumerateinrecordonly-field.md)
