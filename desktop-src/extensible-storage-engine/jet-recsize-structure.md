---
description: 深入瞭解： JET_RECSIZE 結構
title: JET_RECSIZE 結構
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
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
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689604"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="aad65-103">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="aad65-103">JET_RECSIZE Structure</span></span>


<span data-ttu-id="aad65-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="aad65-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize-structure"></a><span data-ttu-id="aad65-105">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="aad65-105">JET_RECSIZE Structure</span></span>

<span data-ttu-id="aad65-106">[JetGetRecordSize](./jetgetrecordsize-function.md)會使用 **JET_RECSIZE** 結構來傳回有關使用者資料空間、集合資料行數目、值數目，以及 ESE 記錄結構額外空間之記錄使用需求的資訊。</span><span class="sxs-lookup"><span data-stu-id="aad65-106">The **JET_RECSIZE** structure is used by [JetGetRecordSize](./jetgetrecordsize-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="aad65-107">**Windows Vista：** 在 Windows Vista 中引進 **JET_RECSIZE** 結構。</span><span class="sxs-lookup"><span data-stu-id="aad65-107">**Windows Vista:** The **JET_RECSIZE** structure is introduced in Windows Vista.</span></span>

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
    } JET_RECSIZE;
```

### <a name="members"></a><span data-ttu-id="aad65-108">成員</span><span class="sxs-lookup"><span data-stu-id="aad65-108">Members</span></span>

<span data-ttu-id="aad65-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="aad65-109">**cbData**</span></span>

<span data-ttu-id="aad65-110">記錄中的使用者資料集。</span><span class="sxs-lookup"><span data-stu-id="aad65-110">User data set in the record.</span></span>

<span data-ttu-id="aad65-111">**注意**  金鑰大小並未包含在此中。</span><span class="sxs-lookup"><span data-stu-id="aad65-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="aad65-112">**cbLongValueData**</span><span class="sxs-lookup"><span data-stu-id="aad65-112">**cbLongValueData**</span></span>

<span data-ttu-id="aad65-113">與記錄相關聯但儲存在長值樹狀結構中的使用者資料。</span><span class="sxs-lookup"><span data-stu-id="aad65-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="aad65-114">**注意**  這不會計算內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="aad65-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="aad65-115">**cbOverhead**</span><span class="sxs-lookup"><span data-stu-id="aad65-115">**cbOverhead**</span></span>

<span data-ttu-id="aad65-116">此記錄的 ESE 記錄結構的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="aad65-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="aad65-117">這包括記錄的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="aad65-117">This includes the record's key size.</span></span>

<span data-ttu-id="aad65-118">**cbLongValueOverhead**</span><span class="sxs-lookup"><span data-stu-id="aad65-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="aad65-119">長數值資料的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="aad65-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="aad65-120">**注意**  這不會計算內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="aad65-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="aad65-121">**cNonTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="aad65-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="aad65-122">此記錄中設定的固定和變數資料行總數。</span><span class="sxs-lookup"><span data-stu-id="aad65-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="aad65-123">**cTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="aad65-123">**cTaggedColumns**</span></span>

<span data-ttu-id="aad65-124">此記錄中設定的標記資料行總數。</span><span class="sxs-lookup"><span data-stu-id="aad65-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="aad65-125">**cLongValues**</span><span class="sxs-lookup"><span data-stu-id="aad65-125">**cLongValues**</span></span>

<span data-ttu-id="aad65-126">此記錄的長值樹狀結構中儲存的完整值總數。</span><span class="sxs-lookup"><span data-stu-id="aad65-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="aad65-127">**注意**  這不會計算內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="aad65-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="aad65-128">**cMultiValues**</span><span class="sxs-lookup"><span data-stu-id="aad65-128">**cMultiValues**</span></span>

<span data-ttu-id="aad65-129">記錄中所有資料行之第一個資料行的總值總數。</span><span class="sxs-lookup"><span data-stu-id="aad65-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

### <a name="remarks"></a><span data-ttu-id="aad65-130">備註</span><span class="sxs-lookup"><span data-stu-id="aad65-130">Remarks</span></span>

<span data-ttu-id="aad65-131">記錄中的值總數會是 **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**。</span><span class="sxs-lookup"><span data-stu-id="aad65-131">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

### <a name="requirements"></a><span data-ttu-id="aad65-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="aad65-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aad65-133"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="aad65-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aad65-134">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="aad65-134">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aad65-135"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="aad65-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aad65-136">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="aad65-136">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aad65-137"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="aad65-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aad65-138">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="aad65-138">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="aad65-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aad65-139">See Also</span></span>

[<span data-ttu-id="aad65-140">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="aad65-140">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)
