---
description: 深入瞭解： JetGetInstanceMiscInfo 函數
title: JetGetInstanceMiscInfo 函式
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027140"
---
# <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="0aaa8-103">JetGetInstanceMiscInfo 函式</span><span class="sxs-lookup"><span data-stu-id="0aaa8-103">JetGetInstanceMiscInfo Function</span></span>


<span data-ttu-id="0aaa8-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0aaa8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="0aaa8-105">JetGetInstanceMiscInfo 函式</span><span class="sxs-lookup"><span data-stu-id="0aaa8-105">JetGetInstanceMiscInfo Function</span></span>

<span data-ttu-id="0aaa8-106">當實例在線上時， **JetGetInstanceMiscInfo** 函式會抓取實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-106">The **JetGetInstanceMiscInfo** function retrieves information about the instance, while the instance is online.</span></span>

<span data-ttu-id="0aaa8-107">**Windows vista： JetGetInstanceMiscInfo** 是在 windows vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-107">**Windows Vista:  JetGetInstanceMiscInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="0aaa8-108">參數</span><span class="sxs-lookup"><span data-stu-id="0aaa8-108">Parameters</span></span>

<span data-ttu-id="0aaa8-109">*實例*</span><span class="sxs-lookup"><span data-stu-id="0aaa8-109">*instance*</span></span>

<span data-ttu-id="0aaa8-110">識別將用於 API 呼叫的資料庫實例。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-110">Identifies the database instance that will be used for the API call.</span></span>

<span data-ttu-id="0aaa8-111">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="0aaa8-111">*pvResult*</span></span>

<span data-ttu-id="0aaa8-112">將接收資訊的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-112">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="0aaa8-113">緩衝區的類型取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-113">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="0aaa8-114">呼叫端會負責適當地對齊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-114">The caller is responsible for aligning the buffer appropriately.</span></span>

<span data-ttu-id="0aaa8-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="0aaa8-115">*cbMax*</span></span>

<span data-ttu-id="0aaa8-116">傳入 *pvResult* 的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-116">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="0aaa8-117">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="0aaa8-117">*InfoLevel*</span></span>

<span data-ttu-id="0aaa8-118">判斷針對 *實例* 指定的實例，將會抓取何種類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-118">Determines what type of information will be retrieved for the instance specified by *instance*.</span></span> <span data-ttu-id="0aaa8-119">*PvResult* 中儲存的資料格式取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-119">The format of the data stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="0aaa8-120">下列選項可用於此參數。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-120">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0aaa8-121">值</span><span class="sxs-lookup"><span data-stu-id="0aaa8-121">Value</span></span></p></th>
<th><p><span data-ttu-id="0aaa8-122">意義</span><span class="sxs-lookup"><span data-stu-id="0aaa8-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0aaa8-123">JET_InstanceMiscInfoLogSignature</span><span class="sxs-lookup"><span data-stu-id="0aaa8-123">JET_InstanceMiscInfoLogSignature</span></span></p></td>
<td><p><span data-ttu-id="0aaa8-124"><em>pvResult</em> 會被視為與此實例相關聯之交易記錄順序的 <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-124"><em>pvResult</em> is interpreted as a <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> structure of the transaction log sequence associated with this instance.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0aaa8-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="0aaa8-125">Return Value</span></span>

<span data-ttu-id="0aaa8-126">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0aaa8-127">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0aaa8-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0aaa8-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="0aaa8-129">Description</span><span class="sxs-lookup"><span data-stu-id="0aaa8-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0aaa8-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0aaa8-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0aaa8-131">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0aaa8-132">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="0aaa8-132">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="0aaa8-133">緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-133">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0aaa8-134">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0aaa8-134">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0aaa8-135">不正確 <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> 或指定的 <em>InfoLevel</em> 無效。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-135">Either an invalid <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> or an invalid <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="0aaa8-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="0aaa8-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0aaa8-137"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="0aaa8-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0aaa8-138">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0aaa8-139"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="0aaa8-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0aaa8-140">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0aaa8-141"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="0aaa8-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0aaa8-142">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0aaa8-143"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="0aaa8-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0aaa8-144">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0aaa8-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0aaa8-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0aaa8-146">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-146">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0aaa8-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0aaa8-147">See Also</span></span>

[<span data-ttu-id="0aaa8-148">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0aaa8-148">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0aaa8-149">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0aaa8-149">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="0aaa8-150">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="0aaa8-150">JET_SIGNATURE</span></span>](./jet-signature-structure.md)
