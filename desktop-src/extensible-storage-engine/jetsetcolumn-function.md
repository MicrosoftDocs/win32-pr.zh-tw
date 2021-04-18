---
description: 深入瞭解： JetSetColumn 函數
title: JetSetColumn 函式
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971253"
---
# <a name="jetsetcolumn-function"></a><span data-ttu-id="f1dcf-103">JetSetColumn 函式</span><span class="sxs-lookup"><span data-stu-id="f1dcf-103">JetSetColumn Function</span></span>


<span data-ttu-id="f1dcf-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f1dcf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumn-function"></a><span data-ttu-id="f1dcf-105">JetSetColumn 函式</span><span class="sxs-lookup"><span data-stu-id="f1dcf-105">JetSetColumn Function</span></span>

<span data-ttu-id="f1dcf-106">**JetSetColumn** 函式會修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-106">The **JetSetColumn** function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="f1dcf-107">它可以覆寫現有的值、將新的值加入至多重值資料行中的值序列、從多重值資料行中的值序列移除值，或更新完整或部分的完整值、 [JET_coltypLongText](./jet-coltyp.md) 或 [JET_coltypLongBinary](./jet-coltyp.md)類型的資料行。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-107">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value, a column of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="f1dcf-108">參數</span><span class="sxs-lookup"><span data-stu-id="f1dcf-108">Parameters</span></span>

<span data-ttu-id="f1dcf-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-109">*sesid*</span></span>

<span data-ttu-id="f1dcf-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-110">The session to use for this call.</span></span>

<span data-ttu-id="f1dcf-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-111">*tableid*</span></span>

<span data-ttu-id="f1dcf-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-112">The cursor to use for this call.</span></span>

<span data-ttu-id="f1dcf-113">*columnid*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-113">*columnid*</span></span>

<span data-ttu-id="f1dcf-114">要抓取之資料行的 [JET_COLUMNID](./jet-columnid.md) 。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-114">The [JET_COLUMNID](./jet-columnid.md) of the column to be retrieved.</span></span> <span data-ttu-id="f1dcf-115">或者，您可以指定 *columnid* 值 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-115">Alternatively, a *columnid* value of 0 (zero) can be given.</span></span> <span data-ttu-id="f1dcf-116">當 *columnid* 0 (零) 時，所有標記的資料行、稀疏和多重值資料行都會被視為單一資料行。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-116">When *columnid* 0 (zero) is given, all tagged columns, sparse and multi-valued columns, are treated as a single column.</span></span> <span data-ttu-id="f1dcf-117">這有助於抓取記錄中所有的稀疏資料行。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-117">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="f1dcf-118">*pvData*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-118">*pvData*</span></span>

<span data-ttu-id="f1dcf-119">輸入緩衝區，其中包含要用於資料行值的資料。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-119">Input buffer containing data to use for column value.</span></span>

<span data-ttu-id="f1dcf-120">*cbData*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-120">*cbData*</span></span>

<span data-ttu-id="f1dcf-121">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-121">Size in bytes of the input buffer.</span></span>

<span data-ttu-id="f1dcf-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-122">*grbit*</span></span>

<span data-ttu-id="f1dcf-123">位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：</span><span class="sxs-lookup"><span data-stu-id="f1dcf-123">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1dcf-124">值</span><span class="sxs-lookup"><span data-stu-id="f1dcf-124">Value</span></span></p></th>
<th><p><span data-ttu-id="f1dcf-125">意義</span><span class="sxs-lookup"><span data-stu-id="f1dcf-125">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-126">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="f1dcf-126">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-127">這個選項是用來將資料附加至類型 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>的資料行。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-127">This option is used to append data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="f1dcf-128">您可以藉由判斷現有 long 值的大小，並在<em>psetinfo</em>中指定<em>ibLongValue</em> ，來達成相同的行為。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-128">The same behavior can be achieved by determining the size of the existing long value and specifying <em>ibLongValue</em> in <em>psetinfo</em>.</span></span> <span data-ttu-id="f1dcf-129">不過，使用此 <em>grbit</em> 比較簡單，因為不需要知道現有資料行值的大小。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-129">However, it's simpler to use this <em>grbit</em> since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-130">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="f1dcf-130">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-131">這個選項是用來將現有的 long 值取代為新提供的資料。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-131">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="f1dcf-132">使用這個選項時，就好像現有的 long 值已設定為 0 (零) 長度，然後再設定新的資料。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-132">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-133">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="f1dcf-133">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-134">此選項僅適用于已標記、稀疏或多重值的資料行。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-134">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="f1dcf-135">它會在後續的取出資料行作業中，讓資料行傳回預設資料行值。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-135">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="f1dcf-136">移除所有現有的資料行值。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-136">All existing column values are removed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-137">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="f1dcf-137">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-138">此選項用來強制將長值（類型 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>的資料行）與記錄資料的其餘部分分開儲存。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-138">This option is used to force a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="f1dcf-139">這種情況通常會在長值的大小防止與剩餘的記錄資料一起儲存時發生。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-139">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="f1dcf-140">不過，這個選項可以用來強制儲存較長的值。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-140">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="f1dcf-141">請注意，在大小較小的四個位元組之間，不能被強制分開。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-141">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="f1dcf-142">在這種情況下，會忽略選項。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-142">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-143">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="f1dcf-143">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-144">此選項可用來將輸入緩衝區轉譯為整數位節數，以設定為指定 <em>columnid</em> 所描述的完整值長度（如果有提供的話），psetinfo-itagSequence 中的序號 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-144">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given <em>columnid</em> and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="f1dcf-145">如果指定的大小大於現有的資料行值，資料行會以0到0進行擴充。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-145">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="f1dcf-146">如果大小小於現有的資料行值，則會截斷此值。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-146">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-147">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="f1dcf-147">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-148">此選項用來強制多重值資料行中的所有值都是相異的。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-148">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="f1dcf-149">此選項會將來源資料行資料（沒有任何轉換）與其他現有的資料行值進行比較，如果找到重複的資料，就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-149">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="f1dcf-150">如果指定此選項，則也不能指定 JET_bitSetAppendLV、JET_bitSetOverwriteLV 和 JET_bitSetSizeLV。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-150">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-151">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="f1dcf-151">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-152">此選項用來強制多重值資料行中的所有值都是相異的。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-152">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="f1dcf-153">這個選項會比較資料行資料的索引鍵正規化轉換，以及其他類似轉換的現有資料行值，如果找到重複的資料行，就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-153">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="f1dcf-154">如果指定此選項，則也不能指定 JET_bitSetAppendLV、JET_bitSetOverwriteLV 和 JET_bitSetSizeLV。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-154">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-155">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="f1dcf-155">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-156">此選項可用來將值設定為零長度。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-156">This option is used to set a value to zero length.</span></span> <span data-ttu-id="f1dcf-157">一般來說，資料行值會藉由將 0 (零) 的 cbMax 傳遞至 <strong>Null</strong> 。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-157">Normally, a column value is set to <strong>NULL</strong> by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="f1dcf-158">不過，對於某些類型，例如 <a href="gg269213(v=exchg.10).md">JET_coltypText</a>，資料行值可以是 0 (零) 長度，而不是 <strong>null</strong>，而且此選項可用來區分 <strong>null</strong> 和 0 (零) 長度。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-158">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 (zero) length instead of <strong>NULL</strong>, and this option is used to differentiate between <strong>NULL</strong> and 0 (zero) length.</span></span></p>
<p><span data-ttu-id="f1dcf-159"><strong>注意</strong>  一般情況下，如果資料行是固定長度的資料行，則會忽略這個位並將資料行設定為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-159"><strong>Note</strong>  In general, if the column is a fixed-length column, this bit is ignored and the column is set to <strong>NULL</strong>.</span></span> <span data-ttu-id="f1dcf-160">但是，如果資料行是固定長度的標記資料行，資料行長度就會設定為0。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-160">However, if the column is a fixed-length tagged column, the column length is set to 0.</span></span> <span data-ttu-id="f1dcf-161">當固定長度的標記資料行設定為0時，嘗試使用 <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> 或 <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> 來取出資料行將會成功，但在 <em>cbActual</em> 參數中傳回的實際長度為0。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-161">When the fixed-length tagged column is set to 0 length, attempts to retrieve the column with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> will succeed, but the actual length that is returned in the <em>cbActual</em> parameter is 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-162">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="f1dcf-162">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-163">此選項是用來將完整的長數值儲存在記錄中。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-163">This option is used to store the entire long value in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-164">JET_bitSetCompressed</span><span class="sxs-lookup"><span data-stu-id="f1dcf-164">JET_bitSetCompressed</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-165">此選項可用來在儲存資料時嘗試資料壓縮。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-165">This option is used to attempt data compression when storing the data.</span></span></p>
<p><span data-ttu-id="f1dcf-166"><strong>Windows 7：</strong>  JET_bitSetCompressed 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-166"><strong>Windows 7:</strong>  JET_bitSetCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-167">JET_bitSetUncompressed</span><span class="sxs-lookup"><span data-stu-id="f1dcf-167">JET_bitSetUncompressed</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-168">儲存資料時，使用這個選項不會嘗試壓縮。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-168">This option is used not attempt compression when storing the data.</span></span></p>
<p><span data-ttu-id="f1dcf-169"><strong>Windows 7：</strong>  JET_bitSetUnCompressed 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1dcf-170">*psetinfo*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-170">*psetinfo*</span></span>

<span data-ttu-id="f1dcf-171">可使用 [JET_SETINFO](./jet-setinfo-structure.md) 結構為此函式設定之選擇性輸入參數的指標。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-171">Pointer to optional input parameters that can be set for this function using the [JET_SETINFO](./jet-setinfo-structure.md) structure.</span></span>

<span data-ttu-id="f1dcf-172">如果將 *psetinfo* 指定為 **Null** ，則函式的行為會如同 *ItagSequence* 為1，而 *ibLongValue* 為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-172">If *psetinfo* is given as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="f1dcf-173">這會導致資料行集設定多重值資料行的第一個值，並設定從位移0開始的長資料 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-173">This causes column set to set the first value of a multi-valued column, and to set long data beginning at offset 0 (zero).</span></span>

<span data-ttu-id="f1dcf-174">您可以為此參數設定下列選項：</span><span class="sxs-lookup"><span data-stu-id="f1dcf-174">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1dcf-175">值</span><span class="sxs-lookup"><span data-stu-id="f1dcf-175">Value</span></span></p></th>
<th><p><span data-ttu-id="f1dcf-176">意義</span><span class="sxs-lookup"><span data-stu-id="f1dcf-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-177">ibLongValue</span><span class="sxs-lookup"><span data-stu-id="f1dcf-177">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-178">要在其中開始設定資料的長資料行值的二進位位移。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-178">Binary offset into a long column value where set data should begin.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-179">itagSequence</span><span class="sxs-lookup"><span data-stu-id="f1dcf-179">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-180">要設定之所需多重值資料行值的序號。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-180">Sequence number of the desired multi-valued column value to set.</span></span> <span data-ttu-id="f1dcf-181">如果 <em>itagSequence</em> 設定為 0 (零) ，則提供的值應該附加到多值值序列的結尾。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-181">If <em>itagSequence</em> is set to 0 (zero), then the value provided should be appended to then end of the sequence of multi-valued values.</span></span> <span data-ttu-id="f1dcf-182">如果提供的序號大於最後一個現有的多重值，則會再次將指定的值附加至值序列的結尾。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-182">If the sequence number provided is greater than the last existing multi-valued value, then again the given value is appended to the end of the sequence of values.</span></span> <span data-ttu-id="f1dcf-183">如果序號對應至現有的值，則該值會取代為指定的值。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-183">If the sequence number corresponds to an existing value then that value is replaced with the given value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f1dcf-184">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1dcf-184">Return Value</span></span>

<span data-ttu-id="f1dcf-185">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f1dcf-186">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1dcf-187">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f1dcf-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="f1dcf-188">Description</span><span class="sxs-lookup"><span data-stu-id="f1dcf-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f1dcf-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-190">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-191">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="f1dcf-191">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-192">提供的資料行識別碼超出資料行識別碼的合法限制。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-192">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-193">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f1dcf-193">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-194">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-194">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-195">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="f1dcf-195">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-196">給定 <em>columnid</em> 所描述的資料行不存在於資料表中。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-196">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-197">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="f1dcf-197">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-198">在插入複製刪除原始更新作業期間，嘗試更新長值的作業不合法。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-198">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-199">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="f1dcf-199">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-200">輸入緩衝區中提供的指定資料行值資料，超過固定長度資料行的自然大小限制，或是針對固定長度的文字或二進位資料行所設定的大小限制。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-200">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="f1dcf-201">針對長資料行傳遞超過1024個位元組的資料，並設定 JET_bitSetIntrinsicLV 旗標時，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-201">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-202">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f1dcf-202">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-203">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-203">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="f1dcf-204"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-204"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-205">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="f1dcf-205">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-206">指定的資料行值資料大小不符合固定長度資料類型的自然內容。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-206">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-207">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="f1dcf-207">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-208">在插入或更新作業期間，嘗試更新自動遞增資料行，或在取代作業期間更新版本資料行時，發生不合法的嘗試。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-208">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-209">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="f1dcf-209">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-210">提供的選項未知，或已知位設定的不合法組合。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-210">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-211">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f1dcf-211">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-212">給定的 psetinfo- &gt; cbStruct 不是 <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> 結構的有效大小。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-212">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-213">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="f1dcf-213">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-214">Set column 作業嘗試建立重複的值，並指定 JET_bitSetUniqueMultiValues 或 JET_bitSetUniqueNormalizedMultiValues。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-214">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-215">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f1dcf-215">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-216">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-216">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-217">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="f1dcf-217">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-218">當呼叫會話不在交易中時，嘗試更新長的資料行值是不合法的。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-218">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-219">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="f1dcf-219">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-220">嘗試將非<strong>null</strong> 資料行設定為 <strong>null</strong>是不合法的。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-220">An illegal attempt was made to set a non-<strong>NULL</strong> column to <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-221">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="f1dcf-221">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-222">與 JET_errNullInvalid 相同。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-222">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-223">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="f1dcf-223">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-224">無法將資料行值設定為輸入緩衝區中的值，因為它會導致記錄超過其頁面大小的相關大小限制。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-224">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="f1dcf-225"><a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>或<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>類型的資料行可以與剩餘的記錄資料分開儲存。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-225">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="f1dcf-226">不過，其他資料行必須與記錄一起儲存，而且可能會導致超過記錄大小限制。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-226">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="f1dcf-227">即使長的資料行在記錄內需要5個位元組的空間作為連結，但這也可能導致傳回 JET_errRecordTooBig。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-227">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f1dcf-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-229">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f1dcf-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-231">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="f1dcf-232"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-232"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f1dcf-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-234">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-235">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="f1dcf-235">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-236">資料指標目前不在插入新記錄或更新現有記錄的過程中。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-236">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-237">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="f1dcf-237">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-238">當版本存放區的設定大小不足以保存所有未處理的更新時，就會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-238">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-239">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="f1dcf-239">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="f1dcf-240">輸入緩衝區中的資料行值超過可變長度資料行所設定的最大長度，已被截斷。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-240">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1dcf-241">成功時，指定資料行之資料行值的所需部分會設定為從輸入緩衝區複製的資料。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-241">On success, the desired portion of a column value for the given column is set with data copied from the input buffer.</span></span> <span data-ttu-id="f1dcf-242">如果資料集超過為可變長度資料行指定的最大長度，可能已被截斷。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-242">The data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="f1dcf-243">失敗時，資料指標位置會保持不變，而且複製緩衝區中不會更新任何資料行值資料。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-243">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f1dcf-244">備註</span><span class="sxs-lookup"><span data-stu-id="f1dcf-244">Remarks</span></span>

<span data-ttu-id="f1dcf-245">設定 long 值、 [JET_coltypLongText](./jet-coltyp.md)或[JET_coltypLongBinary](./jet-coltyp.md)類型之資料行[JET_coltypLongBinary](./jet-coltyp.md)的值，只有在呼叫會話在交易中時才會完成。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-245">Setting long values, values for columns [JET_coltypLongBinary](./jet-coltyp.md) of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md), should be done only when the calling session is in a transaction.</span></span> <span data-ttu-id="f1dcf-246">如果呼叫會話不在交易中，則修改儲存的較長值可能會完全認可，即使稍後取消更新作業也是一樣。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-246">If the calling session is not in a transaction, modifications to long values which are stored separately may be committed fully even when the update operation is later cancelled.</span></span> <span data-ttu-id="f1dcf-247">如果呼叫端會話是在交易中，則可以藉由取消更新並回復會話交易，來完全回復更新的影響。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-247">If the calling session is in a transaction, then the effects of the update can be fully rolled back by canceling the update and rolling back the session transaction.</span></span>

<span data-ttu-id="f1dcf-248">由於 **JetSetColumn** 作業的結果，不會執行索引更新。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-248">Index updates are not performed as a result of **JetSetColumn** operations.</span></span> <span data-ttu-id="f1dcf-249">相反地，只有在所有資料行修改都已完成並呼叫 [JetUpdate](./jetupdate-function.md) 之後，才會更新索引。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-249">Instead, indexes are updated only after all column modifications are complete and [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="f1dcf-250">當索引牽涉到多個要修改的資料行時，這會允許最有效率的索引更新。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-250">This permits the most efficient updating of indexes when indexes involve more than one column being modified.</span></span>

<span data-ttu-id="f1dcf-251">記錄的大小限制為根據資料庫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-251">A record is limited in size based on the database page size.</span></span> <span data-ttu-id="f1dcf-252">記錄中大於五個位元組的任何 long 值將會與記錄分開儲存，因為記錄中的資料會因為 **JetSetColumn** 作業而超過其限制。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-252">Any long values in the record larger than five bytes will be stored separate from the record should the data in the record exceed its limit as a result of a **JetSetColumn** operation.</span></span> <span data-ttu-id="f1dcf-253">只有在所有可分離的記錄資料行資料都與記錄分開儲存，而且記錄仍超過記錄大小限制之後，才會傳回錯誤 JET_errRecordTooBig。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-253">The error JET_errRecordTooBig will only be returned after all separable record column data has been stored separately from the record and the record still exceeds the record size limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f1dcf-254">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1dcf-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-255"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f1dcf-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dcf-256">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-257"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f1dcf-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dcf-258">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-259"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f1dcf-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dcf-260">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dcf-261"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="f1dcf-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dcf-262">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dcf-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f1dcf-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dcf-264">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="f1dcf-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f1dcf-265">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1dcf-265">See Also</span></span>

[<span data-ttu-id="f1dcf-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="f1dcf-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="f1dcf-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f1dcf-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f1dcf-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f1dcf-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f1dcf-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f1dcf-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f1dcf-270">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="f1dcf-270">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="f1dcf-271">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="f1dcf-271">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="f1dcf-272">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="f1dcf-272">JetSetColumns</span></span>](./jetsetcolumns-function.md)
