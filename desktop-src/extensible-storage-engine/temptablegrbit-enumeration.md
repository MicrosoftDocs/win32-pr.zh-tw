---
description: 深入瞭解： TempTableGrbit 列舉
title: TempTableGrbit 列舉
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989909"
---
# <a name="temptablegrbit-enumeration"></a>TempTableGrbit 列舉

建立臨時表的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
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
<td>索引</td>
<td>此選項會要求臨時表具有足夠的彈性，可允許使用 JetSeek 依索引鍵查閱記錄。 如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</td>
</tr>
<tr class="odd">
<td></td>
<td>唯一</td>
<td>此選項會要求從臨時表的最後一組記錄中，移除具有重複索引鍵的記錄。 在 Windows Server 2003 之前，資料庫引擎一律會假設這個選項有作用，因為所有叢集索引也必須是主鍵，因此必須是唯一的。 從 Windows Server 2003 開始，現在也可以在指定 <a href="dn351284(v=exchg.10).md">ForwardOnly</a> 選項時，建立不會移除重複專案的臨時表。 您無法知道哪些重複專案會獲勝，哪些重複專案會在一般情況下捨棄。 不過，當要求 ErrorOnDuplicateInsertion 選項時，會永遠贏得具有指定索引鍵的第一個記錄插入臨時表中。</td>
</tr>
<tr class="even">
<td></td>
<td>可更新</td>
<td>此選項會要求臨時表具有足夠的彈性，可讓之前插入的記錄之後變更。 如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</td>
</tr>
<tr class="odd">
<td></td>
<td>可捲動</td>
<td>此選項會要求臨時表具有足夠的彈性，可讓您使用 <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) </a>，以任意順序和方向來掃描記錄。 如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</td>
</tr>
<tr class="even">
<td></td>
<td>SortNullsHigh</td>
<td>此選項會要求 Null 索引鍵資料行值的排序比非 Null 索引鍵資料行值更接近索引的結尾。</td>
</tr>
<tr class="odd">
<td></td>
<td>ForceMaterialization</td>
<td>此選項會強制臨時表管理員放棄任何嘗試選擇聰明的策略來管理臨時表，以產生增強的效能。</td>
</tr>
<tr class="even">
<td></td>
<td>ErrorOnDuplicateInsertion</td>
<td>此選項會要求任何嘗試使用與先前所插入記錄相同的索引鍵來插入記錄，將會立即失敗，並出現 <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>。 如果未要求這個選項，則可能會立即偵測到重複的情況，也可能會在稍後根據資料庫引擎根據所要求的功能來執行臨時表所選擇的策略，而失敗或以無訊息方式移除。 如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

[ForwardOnly](./server2003grbits.forwardonly-field.md)

[IntrinsicLVsOnly](./windows7grbits.intrinsiclvsonly-field.md)
