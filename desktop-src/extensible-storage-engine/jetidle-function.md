---
description: 深入瞭解： JetIdle 函數
title: JetIdle 函式
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850704"
---
# <a name="jetidle-function"></a><span data-ttu-id="6be1a-103">JetIdle 函式</span><span class="sxs-lookup"><span data-stu-id="6be1a-103">JetIdle Function</span></span>


<span data-ttu-id="6be1a-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6be1a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetidle-function"></a><span data-ttu-id="6be1a-105">JetIdle 函式</span><span class="sxs-lookup"><span data-stu-id="6be1a-105">JetIdle Function</span></span>

<span data-ttu-id="6be1a-106">**JetIdle** 函式已無用，且僅供測試用途使用。</span><span class="sxs-lookup"><span data-stu-id="6be1a-106">The **JetIdle** function is defunct, and should only be used for testing purposes.</span></span> <span data-ttu-id="6be1a-107">**JetIdle** 可以用來執行閒置清除工作，或檢查 ESE 中的版本存放區狀態。</span><span class="sxs-lookup"><span data-stu-id="6be1a-107">**JetIdle** can be used to perform idle cleanup tasks or check the version store status in ESE.</span></span>

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="6be1a-108">參數</span><span class="sxs-lookup"><span data-stu-id="6be1a-108">Parameters</span></span>

<span data-ttu-id="6be1a-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6be1a-109">*sesid*</span></span>

<span data-ttu-id="6be1a-110">此呼叫將使用的會話。</span><span class="sxs-lookup"><span data-stu-id="6be1a-110">The session that will be used for this call.</span></span>

<span data-ttu-id="6be1a-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6be1a-111">*grbit*</span></span>

<span data-ttu-id="6be1a-112">位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列位：</span><span class="sxs-lookup"><span data-stu-id="6be1a-112">A group of bits that contain the options to be used for this call, which include zero or more of the following bits:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6be1a-113">值</span><span class="sxs-lookup"><span data-stu-id="6be1a-113">Value</span></span></p></th>
<th><p><span data-ttu-id="6be1a-114">意義</span><span class="sxs-lookup"><span data-stu-id="6be1a-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6be1a-115">JET_bitIdleCompact</span><span class="sxs-lookup"><span data-stu-id="6be1a-115">JET_bitIdleCompact</span></span></p></td>
<td><p><span data-ttu-id="6be1a-116">觸發版本存放區的清除。</span><span class="sxs-lookup"><span data-stu-id="6be1a-116">Triggers cleanup of the version store.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be1a-117">JET_bitIdleFlushBuffers</span><span class="sxs-lookup"><span data-stu-id="6be1a-117">JET_bitIdleFlushBuffers</span></span></p></td>
<td><p><span data-ttu-id="6be1a-118">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="6be1a-118">Reserved for future use.</span></span> <span data-ttu-id="6be1a-119">如果指定此旗標，則 API 會傳回 JET_errInvalidgrbit。</span><span class="sxs-lookup"><span data-stu-id="6be1a-119">If this flag is specified, the API will return JET_errInvalidgrbit.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be1a-120">JET_bitIdleStatus</span><span class="sxs-lookup"><span data-stu-id="6be1a-120">JET_bitIdleStatus</span></span></p></td>
<td><p><span data-ttu-id="6be1a-121">如果版本存放區已滿一半，則會傳回 JET_wrnIdleFull。</span><span class="sxs-lookup"><span data-stu-id="6be1a-121">Returns JET_wrnIdleFull if version store is more than half full.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6be1a-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="6be1a-122">Return Value</span></span>

<span data-ttu-id="6be1a-123">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="6be1a-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6be1a-124">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="6be1a-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6be1a-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6be1a-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="6be1a-126">Description</span><span class="sxs-lookup"><span data-stu-id="6be1a-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6be1a-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6be1a-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6be1a-128">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="6be1a-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be1a-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6be1a-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6be1a-130">提供給 API 的 <em>grbit</em> 參數無效。</span><span class="sxs-lookup"><span data-stu-id="6be1a-130">A <em>grbit</em> parameter that was provided to the API was not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6be1a-131">如果此函式成功，則會觸發適當的作業，或使用錯誤碼指出版本存放區根據提供的 *grbit* 的填滿程度。</span><span class="sxs-lookup"><span data-stu-id="6be1a-131">If this function succeeds, the appropriate operation will be triggered, or an error code indicating how full the version store is depending on the *grbit* provided.</span></span>

<span data-ttu-id="6be1a-132">如果此函式失敗，則要求的作業將不會順利完成。</span><span class="sxs-lookup"><span data-stu-id="6be1a-132">If this function fails, the requested operation will not have completed successfully.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6be1a-133">備註</span><span class="sxs-lookup"><span data-stu-id="6be1a-133">Remarks</span></span>

<span data-ttu-id="6be1a-134">版本存放區會維護 ESE 的快照集隔離機制。</span><span class="sxs-lookup"><span data-stu-id="6be1a-134">The version store maintains ESE's snapshot isolation mechanism.</span></span> <span data-ttu-id="6be1a-135">如果版本存放區的長度超過一半，則程式可能會關閉長時間執行的交易。</span><span class="sxs-lookup"><span data-stu-id="6be1a-135">If the version store is more than half full, the program might close long-running transactions.</span></span> <span data-ttu-id="6be1a-136">如果長時間執行的交易耗盡版本存放區，ESE 將會停止允許對資料庫進行寫入作業。</span><span class="sxs-lookup"><span data-stu-id="6be1a-136">If a long-running transaction exhausts the version store, ESE will stop allowing write operations to the database.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6be1a-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="6be1a-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6be1a-138"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="6be1a-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6be1a-139">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="6be1a-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be1a-140"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="6be1a-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6be1a-141">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="6be1a-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be1a-142"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="6be1a-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6be1a-143">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="6be1a-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be1a-144"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="6be1a-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6be1a-145">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="6be1a-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be1a-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6be1a-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6be1a-147">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="6be1a-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6be1a-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6be1a-148">See Also</span></span>

[<span data-ttu-id="6be1a-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6be1a-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6be1a-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6be1a-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6be1a-151">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6be1a-151">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6be1a-152">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="6be1a-152">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
