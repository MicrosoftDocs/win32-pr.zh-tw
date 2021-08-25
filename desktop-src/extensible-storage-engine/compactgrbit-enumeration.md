---
description: 深入瞭解： CompactGrbit 列舉
title: CompactGrbit 列舉
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a85f3298e4127a35acd5a39839f788fc404269f80a07463bde1417dc04f7fe16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976538"
---
# <a name="compactgrbit-enumeration"></a>CompactGrbit 列舉

[JetCompact (的選項 JET_SESID、字串、字串、JET_PFNSTATUS、JET_CONVERT、CompactGrbit) ](./api.jetcompact-method.md)。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
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
<td>狀態</td>
<td>讓 JetCompact 將源資料庫的統計資料傾印到名為 DFRGINFO.TXT 的檔案。 統計資料包括源資料庫中每個資料表的名稱、每個資料表中的資料列數目、每個資料表中所有資料列的總大小（以位元組為單位）、 <a href="hh577895(v=exchg.10).md">LongText</a> 或 <a href="hh577895(v=exchg.10).md">LongBinary</a> 類型的所有資料行大小總計（以位元組為單位），且足以與記錄分開儲存、叢集索引分葉頁面數目，以及 long 值分葉頁面數目。 此外，摘要統計資料，包括源資料庫的大小、目的地資料庫、資料庫壓縮所需的時間，也會全部傾印暫存資料庫空間。</td>
</tr>
<tr class="odd">
<td></td>
<td>修復</td>
<td><strong>已淘汰。</strong> 當源資料庫已知已損毀時使用。 它會啟用一組完整的新行為，以盡可能從源資料庫中回收最多的資料。 使用這個選項組的 JetCompact 可能會傳回 <a href="hh564840(v=exchg.10).md">成功</a> ，但不會複製在源資料庫中建立的所有資料。 將略過源資料庫中損毀部分的資料。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
