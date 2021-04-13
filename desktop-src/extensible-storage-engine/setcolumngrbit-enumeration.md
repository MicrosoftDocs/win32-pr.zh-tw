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
# <a name="setcolumngrbit-enumeration"></a><span data-ttu-id="473dd-103">SetColumnGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="473dd-103">SetColumnGrbit enumeration</span></span>

<span data-ttu-id="473dd-104">JetSetColumn 的選項。</span><span class="sxs-lookup"><span data-stu-id="473dd-104">Options for JetSetColumn.</span></span>

<span data-ttu-id="473dd-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="473dd-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="473dd-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="473dd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="473dd-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="473dd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="473dd-108">語法</span><span class="sxs-lookup"><span data-stu-id="473dd-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="473dd-109">成員</span><span class="sxs-lookup"><span data-stu-id="473dd-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="473dd-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="473dd-110">Member name</span></span></th>
<th><span data-ttu-id="473dd-111">描述</span><span class="sxs-lookup"><span data-stu-id="473dd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="473dd-112">無</span><span class="sxs-lookup"><span data-stu-id="473dd-112">None</span></span></td>
<td><span data-ttu-id="473dd-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="473dd-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="473dd-114">AppendLV</span><span class="sxs-lookup"><span data-stu-id="473dd-114">AppendLV</span></span></td>
<td><span data-ttu-id="473dd-115">這個選項是用來將資料附加至類型 JET_coltypLongText 或 JET_coltypLongBinary 的資料行。</span><span class="sxs-lookup"><span data-stu-id="473dd-115">This option is used to append data to a column of type JET_coltypLongText or JET_coltypLongBinary.</span></span> <span data-ttu-id="473dd-116">您可以藉由判斷現有 long 值的大小，並在 psetinfo 中指定 ibLongValue，來達成相同的行為。</span><span class="sxs-lookup"><span data-stu-id="473dd-116">The same behavior can be achieved by determining the size of the existing long value and specifying ibLongValue in psetinfo.</span></span> <span data-ttu-id="473dd-117">不過，由於知道現有資料行值的大小不是必要的，因此使用此 grbit 比較簡單。</span><span class="sxs-lookup"><span data-stu-id="473dd-117">However, its simpler to use this grbit since knowing the size of the existing column value is not necessary.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="473dd-118">OverwriteLV</span><span class="sxs-lookup"><span data-stu-id="473dd-118">OverwriteLV</span></span></td>
<td><span data-ttu-id="473dd-119">這個選項是用來將現有的 long 值取代為新提供的資料。</span><span class="sxs-lookup"><span data-stu-id="473dd-119">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="473dd-120">使用這個選項時，就好像現有的 long 值已設定為 0 (零) 長度，然後再設定新的資料。</span><span class="sxs-lookup"><span data-stu-id="473dd-120">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="473dd-121">RevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="473dd-121">RevertToDefaultValue</span></span></td>
<td><span data-ttu-id="473dd-122">此選項僅適用于已標記、稀疏或多重值的資料行。</span><span class="sxs-lookup"><span data-stu-id="473dd-122">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="473dd-123">它會在後續的取出資料行作業中，讓資料行傳回預設資料行值。</span><span class="sxs-lookup"><span data-stu-id="473dd-123">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="473dd-124">移除所有現有的資料行值。</span><span class="sxs-lookup"><span data-stu-id="473dd-124">All existing column values are removed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="473dd-125">SeparateLV</span><span class="sxs-lookup"><span data-stu-id="473dd-125">SeparateLV</span></span></td>
<td><span data-ttu-id="473dd-126">這個選項是用來強制執行 long 值，也就是 JET_coltyp 類型的資料行。LongText 或 JET_coltyp。LongBinary，可與記錄資料的其餘部分分開儲存。</span><span class="sxs-lookup"><span data-stu-id="473dd-126">This option is used to force a long value, columns of type JET_coltyp.LongText or JET_coltyp.LongBinary, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="473dd-127">這種情況通常會在長值的大小防止與剩餘的記錄資料一起儲存時發生。</span><span class="sxs-lookup"><span data-stu-id="473dd-127">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="473dd-128">不過，這個選項可以用來強制儲存較長的值。</span><span class="sxs-lookup"><span data-stu-id="473dd-128">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="473dd-129">請注意，在大小較小的四個位元組之間，不能被強制分開。</span><span class="sxs-lookup"><span data-stu-id="473dd-129">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="473dd-130">在這種情況下，會忽略選項。</span><span class="sxs-lookup"><span data-stu-id="473dd-130">In such cases, the option is ignored.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="473dd-131">SizeLV</span><span class="sxs-lookup"><span data-stu-id="473dd-131">SizeLV</span></span></td>
<td><span data-ttu-id="473dd-132">此選項可用來將輸入緩衝區轉譯為整數位節數，以設定為指定 columnid 所描述的完整值長度（如果有提供的話），psetinfo-itagSequence 中的序號 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="473dd-132">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="473dd-133">如果指定的大小大於現有的資料行值，資料行會以0到0進行擴充。</span><span class="sxs-lookup"><span data-stu-id="473dd-133">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="473dd-134">如果大小小於現有的資料行值，則會截斷此值。</span><span class="sxs-lookup"><span data-stu-id="473dd-134">If the size is smaller than the existing column value then the value will be truncated.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="473dd-135">UniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="473dd-135">UniqueMultiValues</span></span></td>
<td><span data-ttu-id="473dd-136">此選項用來強制多重值資料行中的所有值都是相異的。</span><span class="sxs-lookup"><span data-stu-id="473dd-136">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="473dd-137">此選項會將來源資料行資料（沒有任何轉換）與其他現有的資料行值進行比較，如果找到重複的資料，就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="473dd-137">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="473dd-138">如果指定此選項，則也不能提供 AppendLV、OverwriteLV 和 SizeLV。</span><span class="sxs-lookup"><span data-stu-id="473dd-138">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="473dd-139">UniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="473dd-139">UniqueNormalizedMultiValues</span></span></td>
<td><span data-ttu-id="473dd-140">此選項用來強制多重值資料行中的所有值都是相異的。</span><span class="sxs-lookup"><span data-stu-id="473dd-140">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="473dd-141">這個選項會比較資料行資料的索引鍵正規化轉換，以及其他類似轉換的現有資料行值，如果找到重複的資料行，就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="473dd-141">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="473dd-142">如果指定此選項，則也不能提供 AppendLV、OverwriteLV 和 SizeLV。</span><span class="sxs-lookup"><span data-stu-id="473dd-142">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="473dd-143">ZeroLength</span><span class="sxs-lookup"><span data-stu-id="473dd-143">ZeroLength</span></span></td>
<td><span data-ttu-id="473dd-144">此選項可用來將值設定為零長度。</span><span class="sxs-lookup"><span data-stu-id="473dd-144">This option is used to set a value to zero length.</span></span> <span data-ttu-id="473dd-145">一般來說，資料行值會藉由將 0 (零) 的 cbMax 傳遞至 Null。</span><span class="sxs-lookup"><span data-stu-id="473dd-145">Normally, a column value is set to NULL by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="473dd-146">不過，針對某些類型，例如 JET_coltyp。文字，資料行值可以是 0 (零) 長度，而不是 Null，而且此選項可用來區分 Null 和 0 (零) 長度。</span><span class="sxs-lookup"><span data-stu-id="473dd-146">However, for some types, like JET_coltyp.Text, a column value can be 0 (zero) length instead of NULL, and this option is used to differentiate between NULL and 0 (zero) length.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="473dd-147">IntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="473dd-147">IntrinsicLV</span></span></td>
<td><span data-ttu-id="473dd-148">嘗試將長值資料行儲存在記錄中，即使它們超過預設的分隔大小也一樣。</span><span class="sxs-lookup"><span data-stu-id="473dd-148">Try to store long-value columns in the record, even if they exceed the default separation size.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="473dd-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="473dd-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="473dd-150">參考</span><span class="sxs-lookup"><span data-stu-id="473dd-150">Reference</span></span>

[<span data-ttu-id="473dd-151">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="473dd-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="473dd-152">Compressed</span><span class="sxs-lookup"><span data-stu-id="473dd-152">Compressed</span></span>](./windows7grbits.compressed-field.md)

[<span data-ttu-id="473dd-153">未壓縮</span><span class="sxs-lookup"><span data-stu-id="473dd-153">Uncompressed</span></span>](./windows7grbits.uncompressed-field.md)
