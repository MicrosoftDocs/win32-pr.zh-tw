---
description: 深入瞭解： JetSetCursorFilter 函數
title: JetSetCursorFilter 函式
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad589fecb190ad0f0676325b78adc7c96028a3fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112517"
---
# <a name="jetsetcursorfilter-function"></a><span data-ttu-id="33f3d-103">JetSetCursorFilter 函式</span><span class="sxs-lookup"><span data-stu-id="33f3d-103">JetSetCursorFilter Function</span></span>


<span data-ttu-id="33f3d-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="33f3d-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="33f3d-105">**JetSetCursorFilter** 函式會設定 [JetMove](./jetmove-function.md)函數的簡單篩選陣列。</span><span class="sxs-lookup"><span data-stu-id="33f3d-105">The **JetSetCursorFilter** function sets an array of simple filters for the [JetMove](./jetmove-function.md) function.</span></span>

<span data-ttu-id="33f3d-106">**JetSetCursorFilter** 函式是在 Windows 8 作業系統中引進的。</span><span class="sxs-lookup"><span data-stu-id="33f3d-106">The **JetSetCursorFilter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="33f3d-107">參數</span><span class="sxs-lookup"><span data-stu-id="33f3d-107">Parameters</span></span>

<span data-ttu-id="33f3d-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="33f3d-108">*sesid*</span></span>

<span data-ttu-id="33f3d-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="33f3d-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="33f3d-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="33f3d-110">*tableid*</span></span>

<span data-ttu-id="33f3d-111">要放置的游標。</span><span class="sxs-lookup"><span data-stu-id="33f3d-111">The cursor to position.</span></span>

<span data-ttu-id="33f3d-112">*rgFilters*</span><span class="sxs-lookup"><span data-stu-id="33f3d-112">*rgFilters*</span></span>

<span data-ttu-id="33f3d-113">簡單的記錄篩選。</span><span class="sxs-lookup"><span data-stu-id="33f3d-113">The simple record filters.</span></span>

<span data-ttu-id="33f3d-114">*cFilters*</span><span class="sxs-lookup"><span data-stu-id="33f3d-114">*cFilters*</span></span>

<span data-ttu-id="33f3d-115">篩選的數目。</span><span class="sxs-lookup"><span data-stu-id="33f3d-115">The number of filters.</span></span>

<span data-ttu-id="33f3d-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="33f3d-116">*grbit*</span></span>

<span data-ttu-id="33f3d-117">一組位，指定下表所列的零或多個移動選項。</span><span class="sxs-lookup"><span data-stu-id="33f3d-117">A group of bits that specifies zero or more of the move options listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33f3d-118">值</span><span class="sxs-lookup"><span data-stu-id="33f3d-118">Value</span></span></p></th>
<th><p><span data-ttu-id="33f3d-119">意義</span><span class="sxs-lookup"><span data-stu-id="33f3d-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33f3d-120">None</span><span class="sxs-lookup"><span data-stu-id="33f3d-120">None</span></span></p></td>
<td><p><span data-ttu-id="33f3d-121">預設選項。</span><span class="sxs-lookup"><span data-stu-id="33f3d-121">Default option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="33f3d-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="33f3d-122">Return value</span></span>

<span data-ttu-id="33f3d-123">此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="33f3d-123">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="33f3d-124">如需可能的可延伸儲存引擎 (ESE) 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="33f3d-124">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33f3d-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="33f3d-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="33f3d-126">Description</span><span class="sxs-lookup"><span data-stu-id="33f3d-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33f3d-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="33f3d-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="33f3d-128">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="33f3d-128">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="33f3d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="33f3d-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33f3d-130"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="33f3d-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="33f3d-131">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="33f3d-131">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33f3d-132"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="33f3d-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="33f3d-133">需要 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="33f3d-133">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33f3d-134"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="33f3d-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="33f3d-135">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="33f3d-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33f3d-136"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="33f3d-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="33f3d-137">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="33f3d-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33f3d-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="33f3d-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="33f3d-139">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="33f3d-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="33f3d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33f3d-140">See also</span></span>

[<span data-ttu-id="33f3d-141">JetMove</span><span class="sxs-lookup"><span data-stu-id="33f3d-141">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="33f3d-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="33f3d-142">JET_ERR</span></span>](./jet-err.md)
