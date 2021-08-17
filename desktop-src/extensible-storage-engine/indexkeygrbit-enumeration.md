---
description: 深入瞭解： IndexKeyGrbit 列舉
title: IndexKeyGrbit 列舉
TOCTitle: IndexKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.IndexKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexkeygrbit(v=EXCHG.10)
ms:contentKeyID: 39514044
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit.Ascending
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit.Descending
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit.Descending
- Microsoft.Isam.Esent.Interop.IndexKeyGrbit.Ascending
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ff5ea8eecefdbc68a07fef0dd51776428f2b8ef159b89b7d6d4ecd5deb49a2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093628"
---
# <a name="indexkeygrbit-enumeration"></a>IndexKeyGrbit 列舉

索引鍵定義 grbits。 在抓取索引的相關資訊時使用。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration IndexKeyGrbit
'Usage
Dim instance As IndexKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum IndexKeyGrbit
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
<td>遞增</td>
<td>索引鍵區段是遞增的。</td>
</tr>
<tr class="even">
<td></td>
<td>遞減</td>
<td>索引鍵區段會遞減。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
