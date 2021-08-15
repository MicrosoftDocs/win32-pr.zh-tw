---
description: 深入瞭解： SeekGrbit 列舉
title: SeekGrbit 列舉
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12a65021d8c224d2a0ed50082b3120c94fc8c83f25c9aaf3eaf6e71d3f3f45f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978588"
---
# <a name="seekgrbit-enumeration"></a>SeekGrbit 列舉

JetSeek 的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
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
<td>SeekEQ</td>
<td>資料指標將定位於最接近索引開頭的索引項目目，此索引項目目完全符合搜尋索引鍵。</td>
</tr>
<tr class="even">
<td></td>
<td>SeekLT</td>
<td>資料指標將放置在最接近索引結尾的索引項目目，此索引項目目小於符合搜尋條件的索引項目。</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekLE</td>
<td>資料指標將定位於最接近索引結尾的索引項目目，這個專案小於或等於符合搜尋準則的索引項目目。</td>
</tr>
<tr class="even">
<td></td>
<td>SeekGE</td>
<td>資料指標將定位於最接近索引開頭的索引項目目，此索引項目目大於或等於符合搜尋條件的索引項目目。</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekGT</td>
<td>資料指標將放置在索引項目目的開頭最接近索引的開頭，而該索引項目大於符合搜尋準則的索引項目目。</td>
</tr>
<tr class="even">
<td></td>
<td>SetIndexRange</td>
<td>將會針對完全符合搜尋索引鍵的所有索引鍵，自動設定索引範圍。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
