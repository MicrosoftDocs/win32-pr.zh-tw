---
description: 深入瞭解： JetRetrieveColumn 函數
title: JetRetrieveColumn 函式
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985352"
---
# <a name="jetretrievecolumn-function"></a><span data-ttu-id="59014-103">JetRetrieveColumn 函式</span><span class="sxs-lookup"><span data-stu-id="59014-103">JetRetrieveColumn Function</span></span>


<span data-ttu-id="59014-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="59014-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumn-function"></a><span data-ttu-id="59014-105">JetRetrieveColumn 函式</span><span class="sxs-lookup"><span data-stu-id="59014-105">JetRetrieveColumn Function</span></span>

<span data-ttu-id="59014-106">**JetRetrieveColumn** 函式會從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="59014-106">The **JetRetrieveColumn** function retrieves a single column value from the current record.</span></span> <span data-ttu-id="59014-107">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="59014-107">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="59014-108">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="59014-108">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="59014-109">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="59014-109">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="59014-110">除了取得實際的資料行值之外， **JetRetrieveColumn** 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</span><span class="sxs-lookup"><span data-stu-id="59014-110">In addition to retrieving the actual column value, **JetRetrieveColumn** can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="59014-111">參數</span><span class="sxs-lookup"><span data-stu-id="59014-111">Parameters</span></span>

<span data-ttu-id="59014-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="59014-112">*sesid*</span></span>

<span data-ttu-id="59014-113">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="59014-113">The session to use for this call.</span></span>

<span data-ttu-id="59014-114">*tableid*</span><span class="sxs-lookup"><span data-stu-id="59014-114">*tableid*</span></span>

<span data-ttu-id="59014-115">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="59014-115">The cursor to use for this call.</span></span>

<span data-ttu-id="59014-116">*columnid*</span><span class="sxs-lookup"><span data-stu-id="59014-116">*columnid*</span></span>

<span data-ttu-id="59014-117">要取出之資料行的 [JET_COLUMNID](./jet-columnid.md) 。</span><span class="sxs-lookup"><span data-stu-id="59014-117">The [JET_COLUMNID](./jet-columnid.md) of the column to retrieve.</span></span>

<span data-ttu-id="59014-118">*Columnid* 值為 0 (零) 可以提供，而不會參考任何個別的資料行。</span><span class="sxs-lookup"><span data-stu-id="59014-118">A *columnid* value of 0 (zero) can be given which does not itself refer to any individual column.</span></span> <span data-ttu-id="59014-119">當 *columnid* 0 (零) 時，所有標記的資料行、稀疏和多重值資料行都會被視為單一資料行。</span><span class="sxs-lookup"><span data-stu-id="59014-119">When *columnid* 0 (zero) is given, all tagged columns, sparse, and multi-valued columns are treated as a single column.</span></span> <span data-ttu-id="59014-120">這有助於抓取記錄中所有的稀疏資料行。</span><span class="sxs-lookup"><span data-stu-id="59014-120">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="59014-121">*pvData*</span><span class="sxs-lookup"><span data-stu-id="59014-121">*pvData*</span></span>

<span data-ttu-id="59014-122">接收資料行值的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="59014-122">The output buffer that receives the column value.</span></span>

<span data-ttu-id="59014-123">*cbData*</span><span class="sxs-lookup"><span data-stu-id="59014-123">*cbData*</span></span>

<span data-ttu-id="59014-124">輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="59014-124">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="59014-125">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="59014-125">*pcbActual*</span></span>

<span data-ttu-id="59014-126">接收資料行值的實際大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="59014-126">Receives the actual size, in bytes, of the column value.</span></span>

<span data-ttu-id="59014-127">如果此參數為 **Null**，則不會傳回資料行值的實際大小。</span><span class="sxs-lookup"><span data-stu-id="59014-127">If this parameter is **NULL**, then the actual size of the column value will not be returned.</span></span>

<span data-ttu-id="59014-128">*grbit*</span><span class="sxs-lookup"><span data-stu-id="59014-128">*grbit*</span></span>

<span data-ttu-id="59014-129">位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：</span><span class="sxs-lookup"><span data-stu-id="59014-129">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59014-130">值</span><span class="sxs-lookup"><span data-stu-id="59014-130">Value</span></span></p></th>
<th><p><span data-ttu-id="59014-131">意義</span><span class="sxs-lookup"><span data-stu-id="59014-131">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59014-132">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="59014-132">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="59014-133">此旗標會使抓取資料行抓取修改過的值，而不是原始的值。</span><span class="sxs-lookup"><span data-stu-id="59014-133">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="59014-134">如果尚未修改此值，則會取出原始值。</span><span class="sxs-lookup"><span data-stu-id="59014-134">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="59014-135">如此一來，在插入或更新記錄的作業期間，可能會取出尚未插入或更新的值。</span><span class="sxs-lookup"><span data-stu-id="59014-135">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-136">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="59014-136">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="59014-137">此選項可用來從索引取出資料行值（如果可能的話），而不需要存取記錄。</span><span class="sxs-lookup"><span data-stu-id="59014-137">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="59014-138">如此一來，當索引項目本身有需要的資料時，就可以避免不必要的記錄載入。</span><span class="sxs-lookup"><span data-stu-id="59014-138">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="59014-139">在無法從索引中取出原始資料行值的情況下，因為無法復原的轉換或資料截斷，將會存取記錄，並以一般方式抓取資料。</span><span class="sxs-lookup"><span data-stu-id="59014-139">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="59014-140">這是效能選項，只有在可能會從索引中抓取資料行值時才會指定。</span><span class="sxs-lookup"><span data-stu-id="59014-140">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="59014-141">如果目前的索引是叢集索引，則不應指定此選項，因為叢集或主要索引的索引項目目是記錄本身。</span><span class="sxs-lookup"><span data-stu-id="59014-141">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="59014-142">如果也設定 JET_bitRetrieveFromPrimaryBookmark，則無法設定此位。</span><span class="sxs-lookup"><span data-stu-id="59014-142">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-143">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="59014-143">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="59014-144">此選項是用來從索引書簽中取出資料行值，而且當資料行同時出現在主要索引和目前索引中時，可能會與索引值不同。</span><span class="sxs-lookup"><span data-stu-id="59014-144">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="59014-145">如果目前的索引是叢集或主要索引，則不應指定此選項。</span><span class="sxs-lookup"><span data-stu-id="59014-145">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="59014-146">如果也設定 JET_bitRetrieveFromIndex，則無法設定此位。</span><span class="sxs-lookup"><span data-stu-id="59014-146">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-147">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="59014-147">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="59014-148">此選項可用來取出 pretinfo-itagSequence 中多重值資料行值的序號 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="59014-148">This option is used to retrieve the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="59014-149">ItagSequence 欄位通常是用來從記錄中取出多重值資料行值的輸入。</span><span class="sxs-lookup"><span data-stu-id="59014-149">The itagSequence field is commonly an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="59014-150">不過，從索引中抓取值時，您也可以將索引項目與特定序號建立關聯，並取出此序號。</span><span class="sxs-lookup"><span data-stu-id="59014-150">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="59014-151">抓取序號可能是成本高昂的作業，而且只在必要時才執行。</span><span class="sxs-lookup"><span data-stu-id="59014-151">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-152">JET_bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="59014-152">JET_bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="59014-153">此選項可用來取出多值資料行 <strong>Null</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="59014-153">This option is used to retrieve multi-valued column <strong>NULL</strong> values.</span></span> <span data-ttu-id="59014-154">如果未指定此選項，則會自動略過多重值資料行的 <strong>Null</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="59014-154">If this option is not specified, multi-valued column <strong>NULL</strong> values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-155">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="59014-155">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="59014-156">此選項只會影響多重值資料行，而且當要求的序號為1，而且記錄中的資料行沒有設定值時，就會傳回 <strong>Null</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="59014-156">This option affects only multi-valued columns and causes a <strong>NULL</strong> value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-157">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="59014-157">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="59014-158">此旗標僅供內部使用，不適合在您的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="59014-158">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-159">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="59014-159">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="59014-160">此旗標僅供內部使用，不適合在您的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="59014-160">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-161">JET_bitRetrieveTuple</span><span class="sxs-lookup"><span data-stu-id="59014-161">JET_bitRetrieveTuple</span></span></p></td>
<td><p><span data-ttu-id="59014-162">此旗標將允許抓取索引的元組區段。</span><span class="sxs-lookup"><span data-stu-id="59014-162">This flag will allow the retrieval of a tuple segment of the index.</span></span> <span data-ttu-id="59014-163">您必須使用 JET_bitRetrieveFromIndex 指定此位。</span><span class="sxs-lookup"><span data-stu-id="59014-163">This bit must be specified with JET_bitRetrieveFromIndex.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="59014-164">*pretinfo*</span><span class="sxs-lookup"><span data-stu-id="59014-164">*pretinfo*</span></span>

<span data-ttu-id="59014-165">如果 *pretinfo* 為 **Null** ，則函式的行為就如同 *ItagSequence* 為1，而 *ibLongValue* 為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="59014-165">If *pretinfo* is give as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="59014-166">這會導致資料行抓取抓取多重值資料行的第一個值，並在位移 0 (零) 取出長資料。</span><span class="sxs-lookup"><span data-stu-id="59014-166">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

<span data-ttu-id="59014-167">這個參數是用來提供下列一或多項：</span><span class="sxs-lookup"><span data-stu-id="59014-167">This parameter is used to provide one or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59014-168">值</span><span class="sxs-lookup"><span data-stu-id="59014-168">Value</span></span></p></th>
<th><p><span data-ttu-id="59014-169">意義</span><span class="sxs-lookup"><span data-stu-id="59014-169">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59014-170">ibLongValue</span><span class="sxs-lookup"><span data-stu-id="59014-170">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="59014-171">在抓取資料行值的一部分時，將二進位位移提供給 long 資料行值。</span><span class="sxs-lookup"><span data-stu-id="59014-171">Gives a binary offset into a long column value when retrieving a portion of a column value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-172">itagSequence</span><span class="sxs-lookup"><span data-stu-id="59014-172">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="59014-173">提供所需多重值資料行值的序號。</span><span class="sxs-lookup"><span data-stu-id="59014-173">Gives the sequence number of the desired multi-valued column value.</span></span> <span data-ttu-id="59014-174">請注意，只有在指定 JET_bitRetrieveTag 時，才會設定此欄位。</span><span class="sxs-lookup"><span data-stu-id="59014-174">Note that this field is only set if the JET_bitRetrieveTag is specified.</span></span> <span data-ttu-id="59014-175">否則，它不會修改。</span><span class="sxs-lookup"><span data-stu-id="59014-175">Otherwise, it is unmodified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-176">columnidNextTagged</span><span class="sxs-lookup"><span data-stu-id="59014-176">columnidNextTagged</span></span></p></td>
<td><p><span data-ttu-id="59014-177">當使用傳遞 <em>columnid</em> 0 (零) 來抓取所有標記、稀疏和多重值的資料行時，傳回所傳回之資料行值的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="59014-177">Returns the column ID of the returned column value when retrieving all tagged, sparse and multi-valued, columns using passing <em>columnid</em> of 0 (zero).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="59014-178">傳回值</span><span class="sxs-lookup"><span data-stu-id="59014-178">Return Value</span></span>

<span data-ttu-id="59014-179">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="59014-179">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="59014-180">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="59014-180">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59014-181">傳回碼</span><span class="sxs-lookup"><span data-stu-id="59014-181">Return code</span></span></p></th>
<th><p><span data-ttu-id="59014-182">Description</span><span class="sxs-lookup"><span data-stu-id="59014-182">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59014-183">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="59014-183">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="59014-184">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="59014-184">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-185">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="59014-185">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="59014-186">提供的資料行識別碼超出資料行識別碼的合法限制。</span><span class="sxs-lookup"><span data-stu-id="59014-186">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-187">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="59014-187">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="59014-188">傳遞了不正確多重值資料行序號值給 pretinfo- &gt; itagSequence。</span><span class="sxs-lookup"><span data-stu-id="59014-188">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="59014-189">多重值資料行值序號的有效值為1或更大。</span><span class="sxs-lookup"><span data-stu-id="59014-189">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="59014-190">值為 0 (零) 對此函數無效。</span><span class="sxs-lookup"><span data-stu-id="59014-190">A value of 0 (zero) is invalid for this function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="59014-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="59014-192">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="59014-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-193">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="59014-193">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="59014-194">給定 <em>columnid</em> 所描述的資料行不存在於資料表中。</span><span class="sxs-lookup"><span data-stu-id="59014-194">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-195">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="59014-195">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="59014-196">無法從索引中取出索引為子字串的資料行，因為只有資料行的一小部分通常會出現在每個索引項目目中。</span><span class="sxs-lookup"><span data-stu-id="59014-196">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-197">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="59014-197">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="59014-198">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="59014-198">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="59014-199">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="59014-199">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-200">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="59014-200">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="59014-201">在某些情況下，為抓取資料行提供的緩衝區必須夠大，才能傳回任何數量的資料行值。</span><span class="sxs-lookup"><span data-stu-id="59014-201">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="59014-202">例如，將可更新的可更新資料行調整為在呼叫會話的交易內容中保持一致，而且這項調整需要呼叫端所提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="59014-202">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="59014-203">如果提供的緩衝區空間不足，則會傳回 JET_errInvalidBufferSize，且不會傳回任何資料行資料。</span><span class="sxs-lookup"><span data-stu-id="59014-203">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-204">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="59014-204">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="59014-205">指定的一個或多個參數不正確。</span><span class="sxs-lookup"><span data-stu-id="59014-205">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="59014-206">如果 retinfo 的大小小於 <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>的大小，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="59014-206">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-207">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="59014-207">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="59014-208">提供的選項未知，或已知位設定的不合法組合。</span><span class="sxs-lookup"><span data-stu-id="59014-208">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-209">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="59014-209">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="59014-210">資料指標未放置在記錄上。</span><span class="sxs-lookup"><span data-stu-id="59014-210">The cursor is not positioned on a record.</span></span> <span data-ttu-id="59014-211">此情況具有許多不同的原因。</span><span class="sxs-lookup"><span data-stu-id="59014-211">This can happen for many different reasons.</span></span> <span data-ttu-id="59014-212">例如，如果資料指標目前位於目前索引的最後一筆記錄之後，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="59014-212">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-213">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="59014-213">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="59014-214">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="59014-214">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-215">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="59014-215">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="59014-216">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="59014-216">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-217">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="59014-217">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="59014-218">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="59014-218">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="59014-219"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="59014-219"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-220">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="59014-220">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="59014-221">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="59014-221">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-222">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="59014-222">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="59014-223">無法取出整個資料行值，因為指定的緩衝區小於資料行的大小。</span><span class="sxs-lookup"><span data-stu-id="59014-223">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-224">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="59014-224">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="59014-225">取出的資料行值為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="59014-225">The column value retrieved is <strong>NULL</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="59014-226">成功時，會將指定資料行的資料行值複製到指定的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="59014-226">On success, the column value for the given column, is copied into the given buffer.</span></span> <span data-ttu-id="59014-227">會傳回小於所有資料行值，並傳回警告 JET_wrnBufferTruncated。</span><span class="sxs-lookup"><span data-stu-id="59014-227">Less than all of the column value is copied with the warning JET_wrnBufferTruncated is returned.</span></span> <span data-ttu-id="59014-228">如果指定了 *pcbActual* ，則會傳回資料行值的實際大小。</span><span class="sxs-lookup"><span data-stu-id="59014-228">If the *pcbActual* was given, the actual size of the column value is returned.</span></span> <span data-ttu-id="59014-229">請注意， **Null** 值具有 0 (零) 長度，因此會將傳回的大小設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="59014-229">Note that **NULL** values have 0 (zero) length and will thus set the returned size to 0 (zero).</span></span> <span data-ttu-id="59014-230">如果取出的資料行是多重值資料行，而且已指定 *pretinfo* ，而且 JET_bitReturnTag 設定為選項，則會在 pretinfo-itagSequence 中傳回資料行值的序號 \> 。</span><span class="sxs-lookup"><span data-stu-id="59014-230">If the column retrieved was a multi-valued column, and *pretinfo* was given, and JET_bitReturnTag was set as an option, then the sequence number of the column value is returned in pretinfo-\>itagSequence.</span></span>

<span data-ttu-id="59014-231">失敗時，資料指標位置會保持不變，且不會將任何資料複製到提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="59014-231">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="59014-232">備註</span><span class="sxs-lookup"><span data-stu-id="59014-232">Remarks</span></span>

<span data-ttu-id="59014-233">此呼叫只會用來針對非多重值資料行取出固定或已知大小的資料。</span><span class="sxs-lookup"><span data-stu-id="59014-233">This call is used just once to retrieve data of fixed or known size for non-multi-valued columns.</span></span> <span data-ttu-id="59014-234">不過，當資料行資料的大小不明時，通常會使用這兩次呼叫。</span><span class="sxs-lookup"><span data-stu-id="59014-234">However, when column data is of unknown size, this call is typically used twice.</span></span> <span data-ttu-id="59014-235">首先會呼叫它來判斷資料的大小，讓它可以配置所需的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="59014-235">It is called first to determine the size of the data so it can allocate the necessary storage space.</span></span> <span data-ttu-id="59014-236">然後，再次進行相同的呼叫，以取得資料行資料。</span><span class="sxs-lookup"><span data-stu-id="59014-236">Then, the same call is made again to retrieve the column data.</span></span> <span data-ttu-id="59014-237">當實際的值數目未知時，因為資料行是多重值，所以呼叫通常會使用三次。</span><span class="sxs-lookup"><span data-stu-id="59014-237">When the actual number of values is unknown, because a column is multi-valued, the call is typically used three times.</span></span> <span data-ttu-id="59014-238">首先，取得值的數目，然後再按兩次，以配置儲存體並取出實際的資料。</span><span class="sxs-lookup"><span data-stu-id="59014-238">First to get the number of values and then twice more to allocate storage and retrieve the actual data.</span></span>

<span data-ttu-id="59014-239">您可以使用 \> 從1開始的 pretinfo-itagSequence 值（從1開始，並在每個後續的呼叫中增加），來取得多重值資料行的所有值。</span><span class="sxs-lookup"><span data-stu-id="59014-239">Retrieving all the values for a multi-valued column can be done by repeatedly calling this function with a pretinfo-\>itagSequence value beginning at 1 and increasing on each subsequent call.</span></span> <span data-ttu-id="59014-240">從函式傳回 JET_wrnColumnNull 時，已知會取出最後一個資料行值。</span><span class="sxs-lookup"><span data-stu-id="59014-240">The last column value is known to be retrieved when a JET_wrnColumnNull is returned from the function.</span></span> <span data-ttu-id="59014-241">請注意，如果多重值資料行的值序列中設定了明確的 **Null** 值，則無法完成這個方法，因為這些值會被略過。</span><span class="sxs-lookup"><span data-stu-id="59014-241">Note that this method cannot be done if the multi-value column has explicit **NULL** values set in its value sequence, since these values would be skipped.</span></span> <span data-ttu-id="59014-242">如果應用程式想要取出所有多重值的資料行值（包括明確設定為 **Null** 的值），則必須使用 [JetRetrieveColumns](./jetretrievecolumns-function.md) ，而不是 **JetRetrieveColumn**。</span><span class="sxs-lookup"><span data-stu-id="59014-242">If an application desires to retrieve all multi-valued column values, including those explicitly set to **NULL**, then [JetRetrieveColumns](./jetretrievecolumns-function.md) must be used instead of **JetRetrieveColumn**.</span></span> <span data-ttu-id="59014-243">請注意，當 *itagSequence* 值為 0 (零) 時，此函數不會傳回多重值函數的值數目。</span><span class="sxs-lookup"><span data-stu-id="59014-243">Note that this function does not return the number of values for a multi-valued function when an *itagSequence* value of 0 (zero) is given.</span></span> <span data-ttu-id="59014-244">當 *itagSequence* 值為 0 (零) 時，只有 [JetRetrieveColumns](./jetretrievecolumns-function.md)會傳回資料行值的數目。</span><span class="sxs-lookup"><span data-stu-id="59014-244">Only [JetRetrieveColumns](./jetretrievecolumns-function.md) will return the number of values of a column value when an *itagSequence* value of 0 (zero) is passed.</span></span>

<span data-ttu-id="59014-245">如果在交易層級0呼叫這個函式 (零) （例如，呼叫會話本身不在交易中），則會在函式中開啟和關閉交易。</span><span class="sxs-lookup"><span data-stu-id="59014-245">If this function is called at transaction level 0 (zero), for example, the calling session is not itself in a transaction, then a transaction is opened and closed within the function.</span></span> <span data-ttu-id="59014-246">這項功能的目的是要傳回一致的結果，以防長數值跨越資料庫頁面。</span><span class="sxs-lookup"><span data-stu-id="59014-246">The purpose of this is to return consistent results in the case that a long value spans database pages.</span></span> <span data-ttu-id="59014-247">請注意，當會話不在交易中時，此交易會在函式呼叫和一系列的呼叫之間釋出，而交易中的會話可能會在第一次呼叫這個函數之後傳回資料更新。</span><span class="sxs-lookup"><span data-stu-id="59014-247">Note that the transaction is released between function calls and a series of calls to this function when the session is not in a transaction may return data updated after the first call to this function.</span></span>

<span data-ttu-id="59014-248">除非設定了 JET_bitRetrieveIgnoreDefault 選項，否則當資料行尚未明確設定為另一個值時，將會取出預設資料行值。</span><span class="sxs-lookup"><span data-stu-id="59014-248">The default column value will be retrieved when the column has not been set explicitly to another value, unless the JET_bitRetrieveIgnoreDefault option is set.</span></span>

<span data-ttu-id="59014-249">在插入之前從複製緩衝區取出自動遞增資料行值，是在將正規化的資料插入多個資料表時，唯一用來識別連結之記錄的常見方式。</span><span class="sxs-lookup"><span data-stu-id="59014-249">Retrieving the autoincrement column value from the copy buffer prior to insert is a common means of identifying a record uniquely for linkage when inserting normalized data into multiple tables.</span></span> <span data-ttu-id="59014-250">自動遞增值是在插入作業開始時配置，而且可以在更新完成之前，隨時從複製緩衝區中取出。</span><span class="sxs-lookup"><span data-stu-id="59014-250">The autoincrement value is allocated when the insert operation begins and can be retrieved from the copy buffer at any time until the update is complete.</span></span>

<span data-ttu-id="59014-251">當您藉由將 *columnid* 設定為 0 (零) 來抓取所有標記、多重值和稀疏資料行時，資料行會以 *columnid* 順序從最低 *columnid* 到最高 *columnid* 進行取出。</span><span class="sxs-lookup"><span data-stu-id="59014-251">When retrieving all tagged, multi-valued, and sparse columns, by setting *columnid* to 0 (zero), columns are retrieved in *columnid* order from lowest *columnid* to highest *columnid*.</span></span> <span data-ttu-id="59014-252">每次抓取資料行值時，就會傳回相同的資料行值順序。</span><span class="sxs-lookup"><span data-stu-id="59014-252">The same order of column values is returned each time column values are retrieved.</span></span> <span data-ttu-id="59014-253">順序具決定性。</span><span class="sxs-lookup"><span data-stu-id="59014-253">The order is deterministic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="59014-254">規格需求</span><span class="sxs-lookup"><span data-stu-id="59014-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59014-255"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="59014-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="59014-256">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="59014-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-257"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="59014-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="59014-258">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="59014-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-259"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="59014-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="59014-260">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="59014-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59014-261"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="59014-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="59014-262">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="59014-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59014-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="59014-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="59014-264">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="59014-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="59014-265">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59014-265">See Also</span></span>

[<span data-ttu-id="59014-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="59014-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="59014-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="59014-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="59014-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="59014-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="59014-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="59014-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="59014-270">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="59014-270">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="59014-271">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="59014-271">JetSetColumn</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="59014-272">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="59014-272">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
