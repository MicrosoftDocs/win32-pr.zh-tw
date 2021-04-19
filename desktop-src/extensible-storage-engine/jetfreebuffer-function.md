---
description: 深入瞭解： JetFreeBuffer 函數
title: JetFreeBuffer 函式
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe638e2aab1d37324a6fd6bf477a578f02b9ac58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987768"
---
# <a name="jetfreebuffer-function"></a><span data-ttu-id="b59b5-103">JetFreeBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="b59b5-103">JetFreeBuffer Function</span></span>


<span data-ttu-id="b59b5-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b59b5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetfreebuffer-function"></a><span data-ttu-id="b59b5-105">JetFreeBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="b59b5-105">JetFreeBuffer Function</span></span>

<span data-ttu-id="b59b5-106">**JetFreeBuffer** 函式會釋出由 database engine 呼叫所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b59b5-106">The **JetFreeBuffer** function frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="b59b5-107">**Windows xp： JetFreeBuffer** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="b59b5-107">**Windows XP:  JetFreeBuffer** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a><span data-ttu-id="b59b5-108">參數</span><span class="sxs-lookup"><span data-stu-id="b59b5-108">Parameters</span></span>

<span data-ttu-id="b59b5-109">*pbBuf*</span><span class="sxs-lookup"><span data-stu-id="b59b5-109">*pbBuf*</span></span>

<span data-ttu-id="b59b5-110">先前由資料庫引擎的呼叫所配置的記憶體區域指標。</span><span class="sxs-lookup"><span data-stu-id="b59b5-110">Pointer to a region of memory that was previously allocated by a call to the database engine.</span></span> <span data-ttu-id="b59b5-111">**Null** 是可接受的，將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="b59b5-111">**NULL** is acceptable, and will be ignored.</span></span>

### <a name="return-value"></a><span data-ttu-id="b59b5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b59b5-112">Return Value</span></span>

<span data-ttu-id="b59b5-113">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="b59b5-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b59b5-114">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="b59b5-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b59b5-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b59b5-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="b59b5-116">Description</span><span class="sxs-lookup"><span data-stu-id="b59b5-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b59b5-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b59b5-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b59b5-118">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="b59b5-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b59b5-119">備註</span><span class="sxs-lookup"><span data-stu-id="b59b5-119">Remarks</span></span>

<span data-ttu-id="b59b5-120">未定義的行為會將資料庫引擎未配置的記憶體傳遞給 *pbBuf*。</span><span class="sxs-lookup"><span data-stu-id="b59b5-120">It is undefined behavior to pass memory that was not allocated by the database engine in to *pbBuf*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b59b5-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b59b5-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b59b5-122"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="b59b5-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b59b5-123">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="b59b5-123">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59b5-124"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="b59b5-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b59b5-125">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="b59b5-125">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59b5-126"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="b59b5-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b59b5-127">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="b59b5-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59b5-128"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="b59b5-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b59b5-129">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="b59b5-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59b5-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b59b5-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b59b5-131">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="b59b5-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b59b5-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b59b5-132">See Also</span></span>

[<span data-ttu-id="b59b5-133">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b59b5-133">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b59b5-134">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="b59b5-134">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)
