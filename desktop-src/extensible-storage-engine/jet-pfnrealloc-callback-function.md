---
description: 深入瞭解： JET_PFNREALLOC 回呼函數
title: JET_PFNREALLOC 回呼函數
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195338"
---
# <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="adbed-103">JET_PFNREALLOC 回呼函數</span><span class="sxs-lookup"><span data-stu-id="adbed-103">JET_PFNREALLOC Callback Function</span></span>


<span data-ttu-id="adbed-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="adbed-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="adbed-105">JET_PFNREALLOC 回呼函數</span><span class="sxs-lookup"><span data-stu-id="adbed-105">JET_PFNREALLOC Callback Function</span></span>

<span data-ttu-id="adbed-106">JET_PFNREALLOC 函式是[JetEnumerateColumns](./jetenumeratecolumns-function.md)用來為其輸出緩衝區配置記憶體的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼。</span><span class="sxs-lookup"><span data-stu-id="adbed-106">The JET_PFNREALLOC function is a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback used by [JetEnumerateColumns](./jetenumeratecolumns-function.md) to allocate memory for its output buffers.</span></span>

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a><span data-ttu-id="adbed-107">參數</span><span class="sxs-lookup"><span data-stu-id="adbed-107">Parameters</span></span>

<span data-ttu-id="adbed-108">*pvCoNtext*</span><span class="sxs-lookup"><span data-stu-id="adbed-108">*pvContext*</span></span>

<span data-ttu-id="adbed-109">提供給 [JetEnumerateColumns](./jetenumeratecolumns-function.md)的內容指標。</span><span class="sxs-lookup"><span data-stu-id="adbed-109">The context pointer given to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span> <span data-ttu-id="adbed-110">此內容指標可用來將 [JetEnumerateColumns](./jetenumeratecolumns-function.md) 呼叫端的狀態，傳遞給這個回呼的實作為。</span><span class="sxs-lookup"><span data-stu-id="adbed-110">This context pointer can be used to convey state from the caller of [JetEnumerateColumns](./jetenumeratecolumns-function.md) to the implementation of this callback.</span></span>

<span data-ttu-id="adbed-111">*光伏*</span><span class="sxs-lookup"><span data-stu-id="adbed-111">*pv*</span></span>

<span data-ttu-id="adbed-112">如果非 Null，則指定此回呼先前配置之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="adbed-112">If non-NULL, specifies a pointer to a memory block previously allocated by this callback.</span></span> <span data-ttu-id="adbed-113">如果是 Null，則會配置所要求大小的新記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="adbed-113">If NULL, a new memory block of the requested size will be allocated.</span></span>

<span data-ttu-id="adbed-114">*Cb*</span><span class="sxs-lookup"><span data-stu-id="adbed-114">*cb*</span></span>

<span data-ttu-id="adbed-115">記憶體區塊的新大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="adbed-115">The new size of the memory block in bytes.</span></span> <span data-ttu-id="adbed-116">如果這個參數是 0 (零) 而且指定了記憶體區塊，就會釋放該記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="adbed-116">If this parameter is 0 (zero) and a memory block is specified, that memory block will be freed.</span></span>

### <a name="return-value"></a><span data-ttu-id="adbed-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="adbed-117">Return Value</span></span>

<span data-ttu-id="adbed-118">因為呼叫此函式，所以系統可能會產生成功或失敗的代碼。</span><span class="sxs-lookup"><span data-stu-id="adbed-118">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="adbed-119">如需如何將這些程式碼傳回為 Hresult 的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="adbed-119">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adbed-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="adbed-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="adbed-121">描述</span><span class="sxs-lookup"><span data-stu-id="adbed-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adbed-122">Success</span><span class="sxs-lookup"><span data-stu-id="adbed-122">Success</span></span></p></td>
<td><p><span data-ttu-id="adbed-123">如果指定了先前配置的記憶體區塊，且指定了新的大小為零，則會釋放該區塊，並傳回 Null。</span><span class="sxs-lookup"><span data-stu-id="adbed-123">If a previously allocated memory block was specified and a new size of zero was specified then that block is freed and NULL will be returned.</span></span> <span data-ttu-id="adbed-124">如果指定了先前配置的記憶體區塊，但指定了非零的新大小，則會傳回重新配置的記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="adbed-124">If a previously allocated memory block was specified and a non-zero new size was specified then the reallocated memory block is returned.</span></span> <span data-ttu-id="adbed-125">如果未指定記憶體區塊，則會傳回指定大小的新配置記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="adbed-125">If no memory block was specified then a newly allocated memory block of the specified size is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adbed-126">失敗</span><span class="sxs-lookup"><span data-stu-id="adbed-126">Failure</span></span></p></td>
<td><p><span data-ttu-id="adbed-127">將會傳回 Null。</span><span class="sxs-lookup"><span data-stu-id="adbed-127">NULL will be returned.</span></span> <span data-ttu-id="adbed-128">如果提供了先前配置的記憶體區塊，該區塊將維持配置狀態。</span><span class="sxs-lookup"><span data-stu-id="adbed-128">If a previously allocated memory block was provided then that block will remain allocated.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="adbed-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="adbed-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adbed-130"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="adbed-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="adbed-131">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="adbed-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adbed-132"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="adbed-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="adbed-133">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="adbed-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adbed-134"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="adbed-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="adbed-135">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="adbed-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="adbed-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adbed-136">See Also</span></span>

[<span data-ttu-id="adbed-137">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="adbed-137">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
