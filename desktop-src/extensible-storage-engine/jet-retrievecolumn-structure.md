---
description: 深入瞭解： JET_RETRIEVECOLUMN 結構
title: JET_RETRIEVECOLUMN 結構
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
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
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974527"
---
# <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="28f83-103">JET_RETRIEVECOLUMN 結構</span><span class="sxs-lookup"><span data-stu-id="28f83-103">JET_RETRIEVECOLUMN Structure</span></span>


<span data-ttu-id="28f83-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="28f83-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="28f83-105">JET_RETRIEVECOLUMN 結構</span><span class="sxs-lookup"><span data-stu-id="28f83-105">JET_RETRIEVECOLUMN Structure</span></span>

<span data-ttu-id="28f83-106">**JET_RETRIEVECOLUMN** 結構包含 [JetRetrieveColumns](./jetretrievecolumns-function.md)的輸入和輸出參數。</span><span class="sxs-lookup"><span data-stu-id="28f83-106">The **JET_RETRIEVECOLUMN** structure contains input and output parameters for [JetRetrieveColumns](./jetretrievecolumns-function.md).</span></span> <span data-ttu-id="28f83-107">結構中的欄位描述要取出的資料行值、如何取出它，以及要儲存結果的位置。</span><span class="sxs-lookup"><span data-stu-id="28f83-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a><span data-ttu-id="28f83-108">成員</span><span class="sxs-lookup"><span data-stu-id="28f83-108">Members</span></span>

<span data-ttu-id="28f83-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="28f83-109">**columnid**</span></span>

<span data-ttu-id="28f83-110">要取得之資料行的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="28f83-110">The column identifier for the column to retrieve.</span></span>

<span data-ttu-id="28f83-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="28f83-111">**pvData**</span></span>

<span data-ttu-id="28f83-112">開始儲存從資料行值取出之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="28f83-112">A pointer to begin storing data that is retrieved from the column value.</span></span>

<span data-ttu-id="28f83-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="28f83-113">**cbData**</span></span>

<span data-ttu-id="28f83-114">從 **pvData** 開始的配置大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="28f83-114">The size of allocation beginning at **pvData**, in bytes.</span></span> <span data-ttu-id="28f83-115">抓取資料行作業將不會在 **pvData** 上儲存比 **cbData** 更多的資料。</span><span class="sxs-lookup"><span data-stu-id="28f83-115">The retrieve column operation will not store more data at **pvData** than **cbData**.</span></span>

<span data-ttu-id="28f83-116">**cbActual**</span><span class="sxs-lookup"><span data-stu-id="28f83-116">**cbActual**</span></span>

<span data-ttu-id="28f83-117">抓取資料行作業取出的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="28f83-117">The size, in bytes, of data that is retrieved by a retrieve column operation.</span></span>

<span data-ttu-id="28f83-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="28f83-118">**grbit**</span></span>

<span data-ttu-id="28f83-119">包含資料行抓取選項的位群組，其中包含零或多個下列值。</span><span class="sxs-lookup"><span data-stu-id="28f83-119">A group of bits that contain the options for column retrieval, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28f83-120">值</span><span class="sxs-lookup"><span data-stu-id="28f83-120">Value</span></span></p></th>
<th><p><span data-ttu-id="28f83-121">意義</span><span class="sxs-lookup"><span data-stu-id="28f83-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28f83-122">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="28f83-122">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="28f83-123">抓取修改過的值，而不是原始的值。</span><span class="sxs-lookup"><span data-stu-id="28f83-123">Retrieves the modified value instead of the original value.</span></span> <span data-ttu-id="28f83-124">如果尚未修改此值，則會取出原始值。</span><span class="sxs-lookup"><span data-stu-id="28f83-124">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="28f83-125">如此一來，插入或更新記錄時，即可抓取尚未插入或更新的值。</span><span class="sxs-lookup"><span data-stu-id="28f83-125">In this way, a value that has not yet been inserted or updated can be retrieved when a record is inserted or updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f83-126">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="28f83-126">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="28f83-127">盡可能從索引中抓取資料行值，而不存取記錄。</span><span class="sxs-lookup"><span data-stu-id="28f83-127">Retrieves column values from the index without accessing the record, if possible.</span></span> <span data-ttu-id="28f83-128">如此一來，當索引項目本身有需要的資料時，就可以避免不必要的記錄載入。</span><span class="sxs-lookup"><span data-stu-id="28f83-128">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="28f83-129">在無法從索引中取出原始資料行值的情況下，因為無法復原的轉換或資料截斷，將會存取記錄，並以一般方式抓取資料。</span><span class="sxs-lookup"><span data-stu-id="28f83-129">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="28f83-130">這是效能選項，只有在可能會從索引中抓取資料行值時才會指定。</span><span class="sxs-lookup"><span data-stu-id="28f83-130">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="28f83-131">如果目前的索引是叢集索引，則不應指定此選項，因為叢集或主要索引的索引項目目是記錄本身。</span><span class="sxs-lookup"><span data-stu-id="28f83-131">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="28f83-132">如果也設定 JET_bitRetrieveFromPrimaryBookmark，則無法設定此位。</span><span class="sxs-lookup"><span data-stu-id="28f83-132">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f83-133">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="28f83-133">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="28f83-134">從索引書簽抓取資料行值，而且當資料行同時出現在主要索引和目前索引中時，可以與索引值不同。</span><span class="sxs-lookup"><span data-stu-id="28f83-134">Retrieves column values from the index bookmark, and can differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="28f83-135">如果目前的索引是叢集或主要索引，則不應指定此選項。</span><span class="sxs-lookup"><span data-stu-id="28f83-135">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="28f83-136">如果也設定 JET_bitRetrieveFromIndex，則無法設定此位。</span><span class="sxs-lookup"><span data-stu-id="28f83-136">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f83-137">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="28f83-137">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="28f83-138">捕獲 pretinfo-itagSequence 中多重值資料行值的序號 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="28f83-138">Retrieves the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="28f83-139">ItagSequence 欄位通常是用來從記錄中取出多值資料行值的輸入。</span><span class="sxs-lookup"><span data-stu-id="28f83-139">The itagSequence field is often used an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="28f83-140">不過，從索引中抓取值時，您也可以將索引項目與特定序號建立關聯，並取出此序號。</span><span class="sxs-lookup"><span data-stu-id="28f83-140">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="28f83-141">抓取序號可能是成本高昂的作業，而且只在必要時才執行。</span><span class="sxs-lookup"><span data-stu-id="28f83-141">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f83-142">JET_ bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="28f83-142">JET_ bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="28f83-143">捕獲多重值資料行 Null 值。</span><span class="sxs-lookup"><span data-stu-id="28f83-143">Retrieves multi-valued column NULL values.</span></span> <span data-ttu-id="28f83-144">如果未指定此選項，則會自動略過多重值資料行的 Null 值。</span><span class="sxs-lookup"><span data-stu-id="28f83-144">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f83-145">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="28f83-145">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="28f83-146">當要求的序號為1，而且記錄中的資料行沒有設定值時，會傳回 Null 值。</span><span class="sxs-lookup"><span data-stu-id="28f83-146">Causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span> <span data-ttu-id="28f83-147">此選項只會影響多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="28f83-147">This option affects only multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f83-148">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="28f83-148">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="28f83-149">此旗標僅供內部使用，不適合在您的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="28f83-149">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f83-150">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="28f83-150">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="28f83-151">此旗標僅供內部使用，不適合在您的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="28f83-151">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="28f83-152">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="28f83-152">**ibLongValue**</span></span>

<span data-ttu-id="28f83-153">要從類型 [JET_coltypLongBinary](./jet-coltyp.md) 或 [JET_coltypLongText](./jet-coltyp.md)的資料行中抓取之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="28f83-153">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="28f83-154">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="28f83-154">**itagSequence**</span></span>

<span data-ttu-id="28f83-155">多值資料行中所包含之值的序號。</span><span class="sxs-lookup"><span data-stu-id="28f83-155">The sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="28f83-156">**JET_RETRIEVECOLUMN** 中的 **itagSequence** 可以是0。</span><span class="sxs-lookup"><span data-stu-id="28f83-156">**itagSequence** here in the **JET_RETRIEVECOLUMN** can be 0.</span></span> <span data-ttu-id="28f83-157">如果 **itagSequence** 為0，則會傳回多重值資料行的實例數目，而不是任何資料行資料。</span><span class="sxs-lookup"><span data-stu-id="28f83-157">If the **itagSequence** is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span> <span data-ttu-id="28f83-158">**ItagSequence** 值0不能用在 [JetRetrieveColumn](./jetretrievecolumn-function.md)的呼叫中。</span><span class="sxs-lookup"><span data-stu-id="28f83-158">An **itagSequence** value of 0 cannot be used in calls to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="28f83-159">**columnidNextTagged**</span><span class="sxs-lookup"><span data-stu-id="28f83-159">**columnidNextTagged**</span></span>

<span data-ttu-id="28f83-160">當所有標記的資料行都透過傳遞0做為 [JetRetrieveColumn](./jetretrievecolumn-function.md)的 **columnid** 時，已標記、多重值或稀疏資料行的 **columnid** 。</span><span class="sxs-lookup"><span data-stu-id="28f83-160">The **columnid** of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the **columnid** to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="28f83-161">**犯 錯**</span><span class="sxs-lookup"><span data-stu-id="28f83-161">**err**</span></span>

<span data-ttu-id="28f83-162">從資料行抓取傳回的錯誤碼和警告。</span><span class="sxs-lookup"><span data-stu-id="28f83-162">Error codes and warnings returned from the retrieval of the column.</span></span>

### <a name="requirements"></a><span data-ttu-id="28f83-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="28f83-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28f83-164"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="28f83-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="28f83-165">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="28f83-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f83-166"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="28f83-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="28f83-167">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="28f83-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f83-168"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="28f83-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="28f83-169">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="28f83-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="28f83-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28f83-170">See Also</span></span>

[<span data-ttu-id="28f83-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="28f83-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="28f83-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="28f83-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="28f83-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="28f83-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="28f83-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="28f83-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="28f83-175">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="28f83-175">JET_RETRIEVECOLUMN</span></span>]()  
[<span data-ttu-id="28f83-176">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="28f83-176">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="28f83-177">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="28f83-177">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
