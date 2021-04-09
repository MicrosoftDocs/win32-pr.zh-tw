---
description: 深入瞭解： JetGetInstanceInfo 函數
title: JetGetInstanceInfo 函式
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850708"
---
# <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="754d9-103">JetGetInstanceInfo 函式</span><span class="sxs-lookup"><span data-stu-id="754d9-103">JetGetInstanceInfo Function</span></span>


<span data-ttu-id="754d9-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="754d9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="754d9-105">JetGetInstanceInfo 函式</span><span class="sxs-lookup"><span data-stu-id="754d9-105">JetGetInstanceInfo Function</span></span>

<span data-ttu-id="754d9-106">**JetGetInstanceInfo** 函數會抓取正在執行之實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="754d9-106">The **JetGetInstanceInfo** function retrieves information about the instances that are running.</span></span>

<span data-ttu-id="754d9-107">**Windows xp： JetGetInstanceInfo** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="754d9-107">**Windows XP:  JetGetInstanceInfo** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="754d9-108">參數</span><span class="sxs-lookup"><span data-stu-id="754d9-108">Parameters</span></span>

<span data-ttu-id="754d9-109">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="754d9-109">*pcInstanceInfo*</span></span>

<span data-ttu-id="754d9-110">緩衝區的指標，此緩衝區會接收儲存在 *paInstanceInfo* 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="754d9-110">A pointer to a buffer which will receive the number of elements stored in *paInstanceInfo*.</span></span>

<span data-ttu-id="754d9-111">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="754d9-111">*paInstanceInfo*</span></span>

<span data-ttu-id="754d9-112">緩衝區的指標，此緩衝區會接收結構陣列第一個元素的位址。</span><span class="sxs-lookup"><span data-stu-id="754d9-112">A pointer to a buffer which will receive the address of the first element of an array of structures.</span></span>

### <a name="return-value"></a><span data-ttu-id="754d9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="754d9-113">Return Value</span></span>

<span data-ttu-id="754d9-114">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="754d9-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="754d9-115">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="754d9-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="754d9-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="754d9-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="754d9-117">Description</span><span class="sxs-lookup"><span data-stu-id="754d9-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="754d9-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="754d9-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="754d9-119">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="754d9-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d9-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="754d9-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="754d9-121">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="754d9-121">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="754d9-122"><strong>JetGetInstanceInfo</strong>會在下列情況傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="754d9-122">This error will be returned by <strong>JetGetInstanceInfo</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="754d9-123"><em>pcInstanceInfo</em> 或 <em>paInstanceInfo</em> 為 Null。</span><span class="sxs-lookup"><span data-stu-id="754d9-123"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> are NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d9-124">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="754d9-124">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="754d9-125">記憶體不足，無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="754d9-125">There is insufficient memory to process the request.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="754d9-126">備註</span><span class="sxs-lookup"><span data-stu-id="754d9-126">Remarks</span></span>

<span data-ttu-id="754d9-127">資料庫引擎會配置 [JET_INSTANCE_INFO](./jet-instance-info-structure.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="754d9-127">The database engine will allocate an array of [JET_INSTANCE_INFO](./jet-instance-info-structure.md) structures.</span></span> <span data-ttu-id="754d9-128">呼叫端負責使用 [JetFreeBuffer](./jetfreebuffer-function.md)釋出此記憶體。</span><span class="sxs-lookup"><span data-stu-id="754d9-128">The caller is responsible for freeing this memory with [JetFreeBuffer](./jetfreebuffer-function.md).</span></span>

<span data-ttu-id="754d9-129">如果沒有使用中的實例， **JetGetInstanceInfo** 會傳回 JET_errSuccess，而 *pcInstanceInfo* 會收到值為0的值。</span><span class="sxs-lookup"><span data-stu-id="754d9-129">If there are no active instances, **JetGetInstanceInfo** will return JET_errSuccess, and *pcInstanceInfo* will receive a value of 0.</span></span>

#### <a name="requirements"></a><span data-ttu-id="754d9-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="754d9-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="754d9-131"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="754d9-131"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="754d9-132">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="754d9-132">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d9-133"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="754d9-133"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="754d9-134">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="754d9-134">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d9-135"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="754d9-135"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="754d9-136">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="754d9-136">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d9-137"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="754d9-137"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="754d9-138">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="754d9-138">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="754d9-139"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="754d9-139"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="754d9-140">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="754d9-140">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="754d9-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="754d9-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="754d9-142">實作為 <strong>JetGetInstanceInfoW</strong> (Unicode) 和 <strong>JetGetInstanceInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="754d9-142">Implemented as <strong>JetGetInstanceInfoW</strong> (Unicode) and <strong>JetGetInstanceInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="754d9-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="754d9-143">See Also</span></span>

[<span data-ttu-id="754d9-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="754d9-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="754d9-145">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="754d9-145">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="754d9-146">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="754d9-146">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="754d9-147">JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="754d9-147">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)
