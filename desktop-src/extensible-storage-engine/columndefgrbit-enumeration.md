---
description: 深入瞭解： ColumndefGrbit 列舉
title: ColumndefGrbit 列舉
TOCTitle: ColumndefGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumndefGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columndefgrbit(v=EXCHG.10)
ms:contentKeyID: 39513005
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c94dcf7d454c5f0ea11fcee0bd46655099dfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974331"
---
# <a name="columndefgrbit-enumeration"></a>ColumndefGrbit 列舉

JET_COLUMNDEF 結構的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ColumndefGrbit
'Usage
Dim instance As ColumndefGrbit
```

``` csharp
[FlagsAttribute]
public enum ColumndefGrbit
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
<td>ColumnFixed</td>
<td>將會修正此資料行。 無論資料儲存在資料行中的資料量為何，它一律會使用資料列中相同數量的空間。 ColumnFixed 不能搭配 ColumnTagged 使用。 這個位不能搭配 JET_coltyp 的 long 值 (使用。LongText 和 JET_coltyp。LongBinary) 。</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnTagged</td>
<td>將會標記資料行。 如果標記的資料行不包含資料，就不會佔用資料庫中的任何空間。 此位無法與 ColumnFixed 搭配使用。</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnNotNull</td>
<td>資料行絕對不能設定為 Null 值。 在 Windows XP 上，這只能套用至固定的資料行， (位、位元組、整數等) 。</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnVersion</td>
<td>此資料行是版本資料行，可指定資料列的版本。 此資料行的值從零開始，而且會針對資料列上的每個更新自動遞增。 此選項只能套用至 JET_coltyp。長的資料行。 此選項不能與 ColumnAutoincrement、ColumnEscrowUpdate 或 ColumnTagged 搭配使用。</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnAutoincrement</td>
<td>將會自動遞增資料行。 此數位是遞增的數位，而且在資料表中保證是唯一的。 不過，數位可能不是連續的。 例如，如果將五個數據列插入資料表中， &quot; 自動遞增 &quot; 資料行可以包含值 {1，2，6，7，8}。 這個位只能用在 JET_coltyp 類型的資料行上。Long 或 JET_coltyp。貨幣。</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnMultiValued</td>
<td>此資料行可以是多重值。 多重值資料行可以有零個、一個或多個相關聯的值。 多重值資料行中的各種值是由稱為 itagSequence 成員的數位所識別，其屬於各種結構，包括： JET_RETINFO、JET_SETINFO、JET_SETCOLUMN、JET_RETRIEVECOLUMN 和 JET_ENUMCOLUMNVALUE。 多重值資料行必須是標記的資料行;也就是說，它們不能是固定長度或可變長度的資料行。</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnEscrowUpdate</td>
<td>指定資料行是「正在託管」更新資料行。 您可以透過 JetEscrowUpdate 的不同會話同時更新交易的更新資料行，並將維持交易一致性。 「正在進行」的更新資料行也必須符合下列條件：只有當資料表是空的時，才可以建立「僅限」更新資料行。 「使用中」更新資料行的類型必須是 JET_coltypLong。 [保管更新] 資料行必須有預設值。 JET_bitColumnEscrowUpdate 不能與 ColumnTagged、ColumnVersion 或 ColumnAutoincrement 搭配使用。</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUnversioned</td>
<td>將在中建立資料行，而不含版本資訊。 這表示嘗試加入具有相同名稱之資料行的其他交易將會失敗。 這個位只對 JetAddColumn 很有用。 它不能用在交易內。</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnMaybeNull</td>
<td>在進行外部聯結時，抓取資料行作業可能不會與內部資料表相符。</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUserDefinedDefault</td>
<td>資料行的預設值將由回呼函數提供。 具有使用者定義預設值的資料行必須是標記的資料行。 指定 JET_bitColumnUserDefinedDefault 表示 pvDefault 必須指向 JET_USERDEFINEDDEFAULT 結構，而且 cbDefault 必須設定為 sizeof ( JET_USERDEFINEDDEFAULT ) 。</td>
</tr>
<tr class="even">
<td></td>
<td>TTKey</td>
<td>資料行將是臨時表的索引鍵資料行。 在輸入陣列中指定此選項的資料行定義順序，將會決定臨時表的每個索引鍵資料行的優先順序。 陣列中具有這個選項組的第一個資料行定義將是最重要的索引鍵資料行，依此類推。 如果要求的索引鍵資料行數目超過 database engine 所能支援的數量，則會忽略不受支援索引鍵資料行的這個選項。</td>
</tr>
<tr class="odd">
<td></td>
<td>TTDescending</td>
<td>臨時表之索引鍵資料行的排序次序應該是遞減的，而不是遞增的。 如果在沒有 TTKey 的情況下指定此選項，則會忽略此選項。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

[ColumnCompressed](./windows7grbits.columncompressed-field.md)
