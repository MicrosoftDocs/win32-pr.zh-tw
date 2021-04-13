---
description: 深入瞭解： SetColumnGrbit 列舉
title: SetColumnGrbit 列舉
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469200"
---
# <a name="setcolumngrbit-enumeration"></a>SetColumnGrbit 列舉

JetSetColumn 的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
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
<td>AppendLV</td>
<td>這個選項是用來將資料附加至類型 JET_coltypLongText 或 JET_coltypLongBinary 的資料行。 您可以藉由判斷現有 long 值的大小，並在 psetinfo 中指定 ibLongValue，來達成相同的行為。 不過，由於知道現有資料行值的大小不是必要的，因此使用此 grbit 比較簡單。</td>
</tr>
<tr class="odd">
<td></td>
<td>OverwriteLV</td>
<td>這個選項是用來將現有的 long 值取代為新提供的資料。 使用這個選項時，就好像現有的 long 值已設定為 0 (零) 長度，然後再設定新的資料。</td>
</tr>
<tr class="even">
<td></td>
<td>RevertToDefaultValue</td>
<td>此選項僅適用于已標記、稀疏或多重值的資料行。 它會在後續的取出資料行作業中，讓資料行傳回預設資料行值。 移除所有現有的資料行值。</td>
</tr>
<tr class="odd">
<td></td>
<td>SeparateLV</td>
<td>這個選項是用來強制執行 long 值，也就是 JET_coltyp 類型的資料行。LongText 或 JET_coltyp。LongBinary，可與記錄資料的其餘部分分開儲存。 這種情況通常會在長值的大小防止與剩餘的記錄資料一起儲存時發生。 不過，這個選項可以用來強制儲存較長的值。 請注意，在大小較小的四個位元組之間，不能被強制分開。 在這種情況下，會忽略選項。</td>
</tr>
<tr class="even">
<td></td>
<td>SizeLV</td>
<td>此選項可用來將輸入緩衝區轉譯為整數位節數，以設定為指定 columnid 所描述的完整值長度（如果有提供的話），psetinfo-itagSequence 中的序號 &gt; 。 如果指定的大小大於現有的資料行值，資料行會以0到0進行擴充。 如果大小小於現有的資料行值，則會截斷此值。</td>
</tr>
<tr class="odd">
<td></td>
<td>UniqueMultiValues</td>
<td>此選項用來強制多重值資料行中的所有值都是相異的。 此選項會將來源資料行資料（沒有任何轉換）與其他現有的資料行值進行比較，如果找到重複的資料，就會傳回錯誤。 如果指定此選項，則也不能提供 AppendLV、OverwriteLV 和 SizeLV。</td>
</tr>
<tr class="even">
<td></td>
<td>UniqueNormalizedMultiValues</td>
<td>此選項用來強制多重值資料行中的所有值都是相異的。 這個選項會比較資料行資料的索引鍵正規化轉換，以及其他類似轉換的現有資料行值，如果找到重複的資料行，就會傳回錯誤。 如果指定此選項，則也不能提供 AppendLV、OverwriteLV 和 SizeLV。</td>
</tr>
<tr class="odd">
<td></td>
<td>ZeroLength</td>
<td>此選項可用來將值設定為零長度。 一般來說，資料行值會藉由將 0 (零) 的 cbMax 傳遞至 Null。 不過，針對某些類型，例如 JET_coltyp。文字，資料行值可以是 0 (零) 長度，而不是 Null，而且此選項可用來區分 Null 和 0 (零) 長度。</td>
</tr>
<tr class="even">
<td></td>
<td>IntrinsicLV</td>
<td>嘗試將長值資料行儲存在記錄中，即使它們超過預設的分隔大小也一樣。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

[Compressed](./windows7grbits.compressed-field.md)

[未壓縮](./windows7grbits.uncompressed-field.md)
