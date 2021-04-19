---
description: 深入瞭解： RetrieveColumnGrbit 列舉
title: RetrieveColumnGrbit 列舉
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a223a288b8ad2d2e976be3bb9f2f524f78b9a8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979184"
---
# <a name="retrievecolumngrbit-enumeration"></a>RetrieveColumnGrbit 列舉

JetRetrieveColumn 的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
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
<td>RetrieveCopy</td>
<td>此旗標會使抓取資料行抓取修改過的值，而不是原始的值。 如果尚未修改此值，則會取出原始值。 如此一來，在插入或更新記錄的作業期間，可能會取出尚未插入或更新的值。</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveFromIndex</td>
<td>此選項可用來從索引取出資料行值（如果可能的話），而不需要存取記錄。 如此一來，當索引項目本身有需要的資料時，就可以避免不必要的記錄載入。</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveFromPrimaryBookmark</td>
<td>此選項是用來從索引書簽中取出資料行值，而且當資料行同時出現在主要索引和目前索引中時，可能會與索引值不同。 如果目前的索引是叢集或主要索引，則不應指定此選項。 如果也設定了 RetrieveFromIndex，則無法設定此位。</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveTag</td>
<td>此選項可用來在 JET_RETINFO itagSequence 中取出多重值資料行值的序號。 抓取序號可能是成本高昂的作業，而且只在必要時才執行。</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveNull</td>
<td>此選項可用來取出多值資料行 Null 值。 如果未指定此選項，則會自動略過多重值資料行的 Null 值。</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveIgnoreDefault</td>
<td>此選項只會影響多重值資料行，而且當要求的序號為1，而且記錄中的資料行沒有設定值時，就會傳回 Null 值。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
