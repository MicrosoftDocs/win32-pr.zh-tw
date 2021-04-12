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
ms.openlocfilehash: f28a3f0c7d69f8ce7e8e688b6fb7b2fecafcce44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191654"
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
