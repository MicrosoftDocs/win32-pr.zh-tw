---
description: 深入瞭解： JET_coltyp 列舉
title: JET_coltyp 列舉
TOCTitle: JET_coltyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_coltyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_coltyp(v=EXCHG.10)
ms:contentKeyID: 39511169
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 616dc80d835e22502b6781355a2eff35a6375e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975463"
---
# <a name="jet_coltyp-enumeration"></a>JET_coltyp 列舉

ESENT 資料行類型。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Enumeration JET_coltyp
'Usage
Dim instance As JET_coltyp
```

``` csharp
public enum JET_coltyp
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
<td>零</td>
<td>Null 資料行類型。 建立資料行時無效。</td>
</tr>
<tr class="even">
<td></td>
<td>bit</td>
<td>True、False 或 Null。</td>
</tr>
<tr class="odd">
<td></td>
<td>UnsignedByte</td>
<td>1位元組整數，不帶正負號。</td>
</tr>
<tr class="even">
<td></td>
<td>Short</td>
<td>2位元組整數，已簽署。</td>
</tr>
<tr class="odd">
<td></td>
<td>long</td>
<td>4位元組整數，已簽署。</td>
</tr>
<tr class="even">
<td></td>
<td>貨幣</td>
<td>8個位元組的整數（帶正負號）。</td>
</tr>
<tr class="odd">
<td></td>
<td>IEEESingle</td>
<td>4位元組 IEEE 單一精確度。</td>
</tr>
<tr class="even">
<td></td>
<td>IEEEDouble</td>
<td>8位元組 IEEE 雙精確度。</td>
</tr>
<tr class="odd">
<td></td>
<td>Datetime</td>
<td>整數日期、小數時間。</td>
</tr>
<tr class="even">
<td></td>
<td>Binary</td>
<td>二進位資料，最多255個位元組。</td>
</tr>
<tr class="odd">
<td></td>
<td>Text</td>
<td>文字資料，最多255個位元組。</td>
</tr>
<tr class="even">
<td></td>
<td>LongBinary</td>
<td>二進位資料，最多 2 GB。</td>
</tr>
<tr class="odd">
<td></td>
<td>LongText</td>
<td>文字資料，最多 2 GB。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
