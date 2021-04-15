---
description: 深入瞭解： JetRelop 列舉
title: JetRelop 列舉 (Windows8) 的列舉
TOCTitle: JetRelop enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JetRelop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jetrelop(v=EXCHG.10)
ms:contentKeyID: 55104456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7839e0223eb9dd773ca9a5d10b5210b10b0a944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321143"
---
# <a name="jetrelop-enumeration"></a>JetRelop 列舉

篩選準則定義為 [JET_INDEX_COLUMN](./jet-index-column-class.md)的比較作業。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Enumeration JetRelop
'Usage
Dim instance As JetRelop
```

``` csharp
public enum JetRelop
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
<td>等於</td>
<td>只接受資料行值等於指定值的資料列。</td>
</tr>
<tr class="even">
<td></td>
<td>PrefixEquals</td>
<td>只接受具有符合指定值之資料行的資料列。</td>
</tr>
<tr class="odd">
<td></td>
<td>NotEquals</td>
<td>只接受資料行值不等於指定值的資料列。</td>
</tr>
<tr class="even">
<td></td>
<td>LessThanOrEqual</td>
<td>只接受資料行值小於或等於指定值的資料列。</td>
</tr>
<tr class="odd">
<td></td>
<td>LessThan</td>
<td>只接受資料行值小於指定值的資料列。</td>
</tr>
<tr class="even">
<td></td>
<td>GreaterThanOrEqual</td>
<td>只接受資料行值大於或等於指定值的資料列。</td>
</tr>
<tr class="odd">
<td></td>
<td>GreaterThan</td>
<td>只接受資料行值大於指定值的資料列。</td>
</tr>
<tr class="even">
<td></td>
<td>BitmaskEqualsZero</td>
<td>只接受資料行值以 and 連結且指定的位元遮罩產生零的資料列。</td>
</tr>
<tr class="odd">
<td></td>
<td>BitmaskNotEqualsZero</td>
<td>只接受資料行值為以 and 連結且指定的位元遮罩為非零的資料列。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
