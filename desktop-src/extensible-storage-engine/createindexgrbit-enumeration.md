---
description: 深入瞭解： CreateIndexGrbit 列舉
title: CreateIndexGrbit 列舉
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997583"
---
# <a name="createindexgrbit-enumeration"></a>CreateIndexGrbit 列舉

JetCreateIndex 的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
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
<td>IndexUnique</td>
<td>不允許有重複的索引項目 (索引鍵) 。 呼叫 JetUpdate 時，不會強制執行這項功能，而不是在呼叫 JetSetColumn 時強制執行。</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexPrimary</td>
<td>索引是主要 (叢集) 索引。 每個資料表都必須只有一個主要索引。 如果未在資料表上明確定義主要索引，則資料庫引擎會建立自己的主要索引。</td>
</tr>
<tr class="even">
<td></td>
<td>IndexDisallowNull</td>
<td>建立索引的資料行都不能包含 Null 值。</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexIgnoreNull</td>
<td>如果要編制索引的所有資料行都是 Null，請勿加入資料列的索引項目。</td>
</tr>
<tr class="even">
<td></td>
<td>IndexIgnoreAnyNull</td>
<td>如果要編制索引的任何資料行都是 Null，請勿加入資料列的索引項目。</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexIgnoreFirstNull</td>
<td>如果要編制索引的第一個資料行是 Null，請勿加入資料列的索引項目。</td>
</tr>
<tr class="even">
<td></td>
<td>IndexLazyFlush</td>
<td>指定將延遲記錄索引作業。 JET_bitIndexLazyFlush 不會影響資料更新的酷。 如果處理常式終止時，索引作業中斷，軟復原仍能讓資料庫處於一致的狀態，但索引可能不存在。</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexEmpty</td>
<td>請勿嘗試建立索引，因為所有專案都會評估為 Null。 傳遞 JET_bitIndexEmpty 時，grbit 也必須指定 JET_bitIgnoreAnyNull。 這是一項效能增強功能。 例如，如果將新的資料行加入至資料表，則會在這個新加入的資料行上建立索引，但會掃描資料表中的所有記錄，即使它們永遠不會加入索引中。 指定 JET_bitIndexEmpty 會略過資料表掃描，這可能會花費很長的時間。</td>
</tr>
<tr class="even">
<td></td>
<td>IndexUnversioned</td>
<td>導致其他交易可以看到索引建立。 一般來說，交易中的會話將無法在另一個會話中看到索引建立作業。 如果另一個交易可能建立相同的索引，而第二個索引建立只會失敗，而不是可能導致許多不必要的資料庫作業，則此旗標很有用。 第二筆交易可能無法立即使用索引。 索引建立作業必須先完成，才可供使用。 會話目前不能在交易中建立索引，而不需要版本資訊。</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexSortNullsHigh</td>
<td>指定此旗標會在索引中的所有資料行資料之後，將 Null 值排序。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
