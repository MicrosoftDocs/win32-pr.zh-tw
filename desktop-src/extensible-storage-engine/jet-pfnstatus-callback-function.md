---
description: 深入瞭解： JET_PFNSTATUS 回呼函數
title: JET_PFNSTATUS 回呼函數
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
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
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193801"
---
# <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="3304e-103">JET_PFNSTATUS 回呼函數</span><span class="sxs-lookup"><span data-stu-id="3304e-103">JET_PFNSTATUS Callback Function</span></span>


<span data-ttu-id="3304e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3304e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="3304e-105">JET_PFNSTATUS 回呼函數</span><span class="sxs-lookup"><span data-stu-id="3304e-105">JET_PFNSTATUS Callback Function</span></span>

<span data-ttu-id="3304e-106">**JET_PFNSTATUS** 回呼函式會接收長時間執行之作業進度的相關資訊，例如磁碟重組、備份或還原作業。</span><span class="sxs-lookup"><span data-stu-id="3304e-106">The **JET_PFNSTATUS** callback function receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="3304e-107">在這類作業期間，資料庫引擎會呼叫此回呼函數，以提供作業進度的更新。</span><span class="sxs-lookup"><span data-stu-id="3304e-107">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a><span data-ttu-id="3304e-108">參數</span><span class="sxs-lookup"><span data-stu-id="3304e-108">Parameters</span></span>

<span data-ttu-id="3304e-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3304e-109">*sesid*</span></span>

<span data-ttu-id="3304e-110">呼叫長時間執行之函式 [JET_SESID](./jet-sesid.md) 類型的會話。</span><span class="sxs-lookup"><span data-stu-id="3304e-110">The session of type [JET_SESID](./jet-sesid.md) with which the long-running function was called.</span></span>

<span data-ttu-id="3304e-111">*Snp*</span><span class="sxs-lookup"><span data-stu-id="3304e-111">*snp*</span></span>

<span data-ttu-id="3304e-112">[JET_SNP](./jet-snp.md)中指定的作業類型。</span><span class="sxs-lookup"><span data-stu-id="3304e-112">The type of operation as specified in [JET_SNP](./jet-snp.md).</span></span> <span data-ttu-id="3304e-113">作業類型包括修復、壓縮、還原、備份、更新、清除和更新記錄格式。</span><span class="sxs-lookup"><span data-stu-id="3304e-113">Types of operations include repair, compact, restore, backup, update, scrub, and update the record format.</span></span>

<span data-ttu-id="3304e-114">*snt*</span><span class="sxs-lookup"><span data-stu-id="3304e-114">*snt*</span></span>

<span data-ttu-id="3304e-115">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3304e-115">The status of an operation.</span></span> <span data-ttu-id="3304e-116">狀態類型包括開始、進行中、完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="3304e-116">Status types include beginning, in progress, completion, or failure.</span></span> <span data-ttu-id="3304e-117">狀態會以 [JET_SNT](./jet-snt.md)類型的第三個參數來指定。</span><span class="sxs-lookup"><span data-stu-id="3304e-117">The status will be specified with the third parameter of type [JET_SNT](./jet-snt.md).</span></span>

<span data-ttu-id="3304e-118">*光伏*</span><span class="sxs-lookup"><span data-stu-id="3304e-118">*pv*</span></span>

<span data-ttu-id="3304e-119">[JET_SNPROG](./jet-snprog-structure.md)類型之結構的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="3304e-119">An optional pointer to a structure of type [JET_SNPROG](./jet-snprog-structure.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="3304e-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="3304e-120">Return Value</span></span>

<span data-ttu-id="3304e-121">此函式會傳回具有其中一個可延伸[儲存引擎錯誤碼](./extensible-storage-engine-error-codes.md)的[JET_ERR](./jet-err.md)資料類型。</span><span class="sxs-lookup"><span data-stu-id="3304e-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="3304e-122">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="3304e-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="3304e-123">成功時，發出回呼的作業可以正常執行。</span><span class="sxs-lookup"><span data-stu-id="3304e-123">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="3304e-124">在某些情況下，回呼可能會傳回會影響該作業的警告。</span><span class="sxs-lookup"><span data-stu-id="3304e-124">In some cases, the callback might return a warning that influences that operation.</span></span>

<span data-ttu-id="3304e-125">失敗時，發出回呼的作業可能會正常進行，或可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="3304e-125">On failure, the operation that issued the callback might proceed normally or might fail.</span></span>

### <a name="remarks"></a><span data-ttu-id="3304e-126">備註</span><span class="sxs-lookup"><span data-stu-id="3304e-126">Remarks</span></span>

<span data-ttu-id="3304e-127">這個回呼函式將用於進度通知，其中結構會指出進度的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="3304e-127">This callback function will be used in a progress notification in which the structure will indicate the current state of the progress.</span></span> <span data-ttu-id="3304e-128">請注意，您可能會針對作業的進度多次呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="3304e-128">Note that the callback function might be called multiple times for the progress of the operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="3304e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="3304e-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3304e-130"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="3304e-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3304e-131">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="3304e-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3304e-132"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="3304e-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3304e-133">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="3304e-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3304e-134"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="3304e-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3304e-135">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="3304e-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3304e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3304e-136">See Also</span></span>

[<span data-ttu-id="3304e-137">可擴充儲存引擎錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3304e-137">Extensible Storage Engine error codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="3304e-138">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="3304e-138">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="3304e-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3304e-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3304e-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="3304e-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="3304e-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="3304e-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="3304e-142">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="3304e-142">JET_SNT</span></span>](./jet-snt.md)
