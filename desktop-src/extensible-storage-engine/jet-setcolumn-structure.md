---
description: 深入瞭解： JET_SETCOLUMN 結構
title: JET_SETCOLUMN 結構
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689936"
---
# <a name="jet_setcolumn-structure"></a><span data-ttu-id="c4d4c-103">JET_SETCOLUMN 結構</span><span class="sxs-lookup"><span data-stu-id="c4d4c-103">JET_SETCOLUMN Structure</span></span>


<span data-ttu-id="c4d4c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c4d4c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setcolumn-structure"></a><span data-ttu-id="c4d4c-105">JET_SETCOLUMN 結構</span><span class="sxs-lookup"><span data-stu-id="c4d4c-105">JET_SETCOLUMN Structure</span></span>

<span data-ttu-id="c4d4c-106">**JET_SETCOLUMN** 結構包含 [JetSetColumns](./jetsetcolumns-function.md)的輸入和輸出參數。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-106">The **JET_SETCOLUMN** structure contains input and output parameters for [JetSetColumns](./jetsetcolumns-function.md).</span></span> <span data-ttu-id="c4d4c-107">結構中的欄位描述要設定的資料行值、如何設定它，以及要在哪裡取得資料行集資料。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-107">Fields in the structure describe what column value to set, how to set it, and where to get the column set data.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a><span data-ttu-id="c4d4c-108">成員</span><span class="sxs-lookup"><span data-stu-id="c4d4c-108">Members</span></span>

<span data-ttu-id="c4d4c-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="c4d4c-109">**columnid**</span></span>

<span data-ttu-id="c4d4c-110">要設定之資料行的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-110">The column identifier for a column to set.</span></span>

<span data-ttu-id="c4d4c-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="c4d4c-111">**pvData**</span></span>

<span data-ttu-id="c4d4c-112">要設定為數據行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-112">A pointer to data to set into a column.</span></span>

<span data-ttu-id="c4d4c-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="c4d4c-113">**cbData**</span></span>

<span data-ttu-id="c4d4c-114">配置的大小（以位元組為單位），以位元組為單位從 **pvData** 開始。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-114">The size of allocation, in bytes, starting at **pvData** in bytes.</span></span>

<span data-ttu-id="c4d4c-115">**grbit**</span><span class="sxs-lookup"><span data-stu-id="c4d4c-115">**grbit**</span></span>

<span data-ttu-id="c4d4c-116">位群組，其中包含要用於此呼叫的選項，包括下列零或多個。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-116">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4d4c-117">值</span><span class="sxs-lookup"><span data-stu-id="c4d4c-117">Value</span></span></p></th>
<th><p><span data-ttu-id="c4d4c-118">意義</span><span class="sxs-lookup"><span data-stu-id="c4d4c-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4d4c-119">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="c4d4c-119">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="c4d4c-120">將資料附加至類型 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>的資料行。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-120">Appends data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="c4d4c-121">您可以藉由判斷現有 long 值的大小，並在<strong>psetinfo</strong>中指定<strong>ibLongValue</strong> ，來達成相同的行為。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-121">The same behavior can be achieved by determining the size of the existing long value and specifying <strong>ibLongValue</strong> in <strong>psetinfo</strong>.</span></span> <span data-ttu-id="c4d4c-122">不過，使用此 <em>grbit</em>比較簡單，因為不需要知道現有資料行值的大小。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-122">However, it's simpler to use this <em>grbit</em>, since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4d4c-123">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="c4d4c-123">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="c4d4c-124">以新資料取代現有的 long 值。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-124">Replaces the existing long value with the new data.</span></span> <span data-ttu-id="c4d4c-125">使用這個選項時，就好像現有的 long 值已設定為 0 (零) 長度，然後再設定新的資料。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-125">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4d4c-126">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="c4d4c-126">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="c4d4c-127">將輸入緩衝區轉譯為整數位節數，以將其設定為指定 columnid 所描述之 long 值的長度（如果有提供的話），psetinfo-itagSequence 中的序號 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-127">Interprets the input buffer as an integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="c4d4c-128">如果指定的大小大於現有的資料行值，資料行會以0到0進行擴充。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-128">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="c4d4c-129">如果大小小於現有的資料行值，則會截斷此值。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-129">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4d4c-130">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="c4d4c-130">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="c4d4c-131">將值設定為零長度。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-131">Sets a value to zero length.</span></span> <span data-ttu-id="c4d4c-132">一般來說，藉由傳遞 cbMax 0 來將資料行值設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-132">Normally, a column value is set to NULL by passing a cbMax of 0.</span></span> <span data-ttu-id="c4d4c-133">不過，對於某些類型而言（例如 <a href="gg269213(v=exchg.10).md">JET_coltypText</a>），資料行值的長度可以是0，而不是 null，而且此選項可用來區分 Null 和0長度。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-133">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 length instead of NULL, and this option is used to differentiate between NULL and 0 length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4d4c-134">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="c4d4c-134">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="c4d4c-135">強制將 long 值、類型 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>的資料行與記錄資料的其餘部分分開儲存。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-135">Forces a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="c4d4c-136">這種情況通常會在長值的大小防止與剩餘的記錄資料一起儲存時發生。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-136">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="c4d4c-137">不過，這個選項可以用來強制儲存較長的值。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-137">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="c4d4c-138">請注意，在大小或較小的四個位元組之間，不能強制為個別的值。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-138">Note that long values four bytes in size or smaller cannot be forced to be separate.</span></span> <span data-ttu-id="c4d4c-139">在這種情況下，會忽略選項。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-139">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4d4c-140">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="c4d4c-140">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="c4d4c-141">強制多重值資料行中的相異值。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-141">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="c4d4c-142">此選項會將來源資料行資料（沒有任何轉換）與其他現有的資料行值進行比較，如果找到重複的資料，就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-142">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="c4d4c-143">如果指定此選項，則也不能指定 JET_bitSetAppendLv、JET_bitSetOverwriteLV 和 JET_bitSetSizeLV。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-143">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4d4c-144">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="c4d4c-144">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="c4d4c-145">強制多重值資料行中的相異值。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-145">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="c4d4c-146">此選項會比較資料行資料的索引鍵正規化轉換與其他類似轉換的現有資料行值，如果找到重複的資料行，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-146">This option compares the key normalized transformation of column data to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="c4d4c-147">如果指定此選項，則也不能指定 JET_bitSetAppendLv、JET_bitSetOverwriteLV 和 JET_bitSetSizeLV。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-147">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4d4c-148">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="c4d4c-148">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="c4d4c-149">導致資料行在後續的取出資料行作業上傳回預設資料行值。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-149">Causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="c4d4c-150">移除所有現有的資料行值。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-150">All existing column values are removed.</span></span> <span data-ttu-id="c4d4c-151">此選項僅適用于已標記、稀疏或多重值的資料行。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-151">This option is only applicable for tagged, sparse, or multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4d4c-152">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="c4d4c-152">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="c4d4c-153">盡可能保留最長的值、 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> 或 JET_coltypeLongBinary 類型的資料行，並盡可能地儲存其他記錄資料。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-153">Keeps the long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or JET_coltypeLongBinary, stored with the remaining record data if possible.</span></span> <span data-ttu-id="c4d4c-154">一般情況下，長的資料行會在其長度超過1024個位元組時分開儲存，否則會導致記錄長度超過其頁面大小的相關大小限制。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-154">Normally, long columns are stored separately when their length exceeds 1024 bytes or would otherwise cause the record length to exceed its page size related size limitation.</span></span> <span data-ttu-id="c4d4c-155">但是，如果設定此選項，set 資料行作業會失敗並出現錯誤 JET_errColumnTooBig，而不是將此資料行值與其余記錄資料分開。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-155">However, if this option is set, the set column operation will fail with error JET_errColumnTooBig rather than store this column value separate from the remaining record data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c4d4c-156">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="c4d4c-156">**ibLongValue**</span></span>

<span data-ttu-id="c4d4c-157">從 [JET_coltypLongBinary](./jet-coltyp.md)或 [JET_coltypLongText](./jet-coltyp.md)類型的資料行抓取的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-157">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="c4d4c-158">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="c4d4c-158">**itagSequence**</span></span>

<span data-ttu-id="c4d4c-159">描述多重值資料行中值的序號。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-159">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="c4d4c-160">**ItagSequence** 為0表示應該將資料行值集加入為多重值資料行的新實例。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-160">An **itagSequence** of 0 indicates that the column value set should be added as a new instance of a multi-valued column.</span></span>

<span data-ttu-id="c4d4c-161">**犯 錯**</span><span class="sxs-lookup"><span data-stu-id="c4d4c-161">**err**</span></span>

<span data-ttu-id="c4d4c-162">從集合資料行作業傳回的錯誤碼和警告。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-162">Error codes and warnings returned from the set column operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="c4d4c-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4d4c-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4d4c-164"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="c4d4c-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c4d4c-165">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4d4c-166"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="c4d4c-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c4d4c-167">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4d4c-168"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="c4d4c-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c4d4c-169">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="c4d4c-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c4d4c-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4d4c-170">See Also</span></span>

[<span data-ttu-id="c4d4c-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="c4d4c-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="c4d4c-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="c4d4c-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="c4d4c-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c4d4c-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c4d4c-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c4d4c-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c4d4c-175">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="c4d4c-175">JetSetColumns</span></span>](./jetsetcolumns-function.md)
