---
description: 深入瞭解： JET_RECSIZE2 結構
title: JET_RECSIZE2 結構
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991890"
---
# <a name="jet_recsize2-structure"></a><span data-ttu-id="14608-103">JET_RECSIZE2 結構</span><span class="sxs-lookup"><span data-stu-id="14608-103">JET_RECSIZE2 Structure</span></span>


<span data-ttu-id="14608-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="14608-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize2-structure"></a><span data-ttu-id="14608-105">JET_RECSIZE2 結構</span><span class="sxs-lookup"><span data-stu-id="14608-105">JET_RECSIZE2 Structure</span></span>

<span data-ttu-id="14608-106">[JetGetRecordSize2](./jetgetrecordsize2-function.md)會使用 **JET_RECSIZE2** 結構來傳回有關使用者資料空間、集合資料行數目、值數目，以及 ESE 記錄結構額外空間之記錄使用需求的資訊。</span><span class="sxs-lookup"><span data-stu-id="14608-106">The **JET_RECSIZE2** structure is used by [JetGetRecordSize2](./jetgetrecordsize2-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="14608-107">**Windows 7：** 在 Windows 7 作業系統中引進 **JET_RECSIZE2** 結構。</span><span class="sxs-lookup"><span data-stu-id="14608-107">**Windows 7:** The **JET_RECSIZE2** structure is introduced in the Windows 7 operating system.</span></span>

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
```

### <a name="members"></a><span data-ttu-id="14608-108">成員</span><span class="sxs-lookup"><span data-stu-id="14608-108">Members</span></span>

<span data-ttu-id="14608-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="14608-109">**cbData**</span></span>

<span data-ttu-id="14608-110">記錄中的使用者資料集。</span><span class="sxs-lookup"><span data-stu-id="14608-110">User data set in the record.</span></span>

<span data-ttu-id="14608-111">**注意**  金鑰大小並未包含在此中。</span><span class="sxs-lookup"><span data-stu-id="14608-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="14608-112">**cbLongValueData**</span><span class="sxs-lookup"><span data-stu-id="14608-112">**cbLongValueData**</span></span>

<span data-ttu-id="14608-113">與記錄相關聯但儲存在長值樹狀結構中的使用者資料。</span><span class="sxs-lookup"><span data-stu-id="14608-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="14608-114">**注意**  這不會計算內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="14608-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="14608-115">**cbOverhead**</span><span class="sxs-lookup"><span data-stu-id="14608-115">**cbOverhead**</span></span>

<span data-ttu-id="14608-116">此記錄的 ESE 記錄結構的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="14608-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="14608-117">這包括記錄的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="14608-117">This includes the record's key size.</span></span>

<span data-ttu-id="14608-118">**cbLongValueOverhead**</span><span class="sxs-lookup"><span data-stu-id="14608-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="14608-119">長數值資料的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="14608-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="14608-120">**注意**  這不會計算內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="14608-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="14608-121">**cNonTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="14608-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="14608-122">此記錄中設定的固定和變數資料行總數。</span><span class="sxs-lookup"><span data-stu-id="14608-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="14608-123">**cTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="14608-123">**cTaggedColumns**</span></span>

<span data-ttu-id="14608-124">此記錄中設定的標記資料行總數。</span><span class="sxs-lookup"><span data-stu-id="14608-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="14608-125">**cLongValues**</span><span class="sxs-lookup"><span data-stu-id="14608-125">**cLongValues**</span></span>

<span data-ttu-id="14608-126">此記錄的長值樹狀結構中儲存的完整值總數。</span><span class="sxs-lookup"><span data-stu-id="14608-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="14608-127">**注意**  這不會計算內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="14608-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="14608-128">**cMultiValues**</span><span class="sxs-lookup"><span data-stu-id="14608-128">**cMultiValues**</span></span>

<span data-ttu-id="14608-129">記錄中所有資料行之第一個資料行的總值總數。</span><span class="sxs-lookup"><span data-stu-id="14608-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

<span data-ttu-id="14608-130">**cCompressedColumns**</span><span class="sxs-lookup"><span data-stu-id="14608-130">**cCompressedColumns**</span></span>

<span data-ttu-id="14608-131">壓縮的資料行總數。</span><span class="sxs-lookup"><span data-stu-id="14608-131">The total number of compressed columns.</span></span>

<span data-ttu-id="14608-132">**cbDataCompressed**</span><span class="sxs-lookup"><span data-stu-id="14608-132">**cbDataCompressed**</span></span>

<span data-ttu-id="14608-133">此記錄中使用者資料的壓縮大小。</span><span class="sxs-lookup"><span data-stu-id="14608-133">The compressed size of user data in this record.</span></span> <span data-ttu-id="14608-134">如果沒有壓縮內建的 long 值，這就會與 cbData 相同。</span><span class="sxs-lookup"><span data-stu-id="14608-134">This is the same as cbData if no intrinsic long-values are compressed.</span></span>

<span data-ttu-id="14608-135">**cbLongValueDataCompressed**</span><span class="sxs-lookup"><span data-stu-id="14608-135">**cbLongValueDataCompressed**</span></span>

<span data-ttu-id="14608-136">完整值樹狀目錄中的使用者資料壓縮大小。</span><span class="sxs-lookup"><span data-stu-id="14608-136">The compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="14608-137">如果沒有壓縮分隔的 long 值，就會與 cbLongValue 資料相同。</span><span class="sxs-lookup"><span data-stu-id="14608-137">This is the same as cbLongValue data if no separated long values are compressed.</span></span>

### <a name="remarks"></a><span data-ttu-id="14608-138">備註</span><span class="sxs-lookup"><span data-stu-id="14608-138">Remarks</span></span>

<span data-ttu-id="14608-139">記錄中的值總數會是 **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**。</span><span class="sxs-lookup"><span data-stu-id="14608-139">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

<span data-ttu-id="14608-140">記錄中的邏輯資料是 (cbData + cbLongValueData) ，而資料的實際大小 (cbDataCompressed + cbLongValueDataCompressed) 。</span><span class="sxs-lookup"><span data-stu-id="14608-140">The logical data in the record is (cbData+cbLongValueData) and the physical size of the data is (cbDataCompressed+cbLongValueDataCompressed).</span></span> <span data-ttu-id="14608-141">這可以用來計算儲存資料的壓縮比率。</span><span class="sxs-lookup"><span data-stu-id="14608-141">This can be used to calculate the compression ratio of stored data.</span></span>

### <a name="requirements"></a><span data-ttu-id="14608-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="14608-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14608-143"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="14608-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="14608-144">需要 Windows Vista 作業系統。</span><span class="sxs-lookup"><span data-stu-id="14608-144">Requires Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14608-145"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="14608-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="14608-146">需要 Windows Server 2008 作業系統。</span><span class="sxs-lookup"><span data-stu-id="14608-146">Requires Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14608-147"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="14608-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="14608-148">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="14608-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="14608-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14608-149">See Also</span></span>

[<span data-ttu-id="14608-150">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="14608-150">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)  
[<span data-ttu-id="14608-151">JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="14608-151">JetGetRecordSize2</span></span>](./jetgetrecordsize2-function.md)
