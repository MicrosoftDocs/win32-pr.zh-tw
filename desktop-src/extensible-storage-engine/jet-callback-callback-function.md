---
description: 深入瞭解： JET_CALLBACK 回呼函數
title: JET_CALLBACK 回呼函數
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
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
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986393"
---
# <a name="jet_callback-callback-function"></a><span data-ttu-id="95b67-103">JET_CALLBACK 回呼函數</span><span class="sxs-lookup"><span data-stu-id="95b67-103">JET_CALLBACK Callback Function</span></span>


<span data-ttu-id="95b67-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="95b67-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_callback-callback-function"></a><span data-ttu-id="95b67-105">JET_CALLBACK 回呼函數</span><span class="sxs-lookup"><span data-stu-id="95b67-105">JET_CALLBACK Callback Function</span></span>

<span data-ttu-id="95b67-106">**JET_CALLBACK** 函式是一種多用途的回呼函式，由資料庫引擎用來通知應用程式涉及線上磁碟重組和資料指標狀態通知。</span><span class="sxs-lookup"><span data-stu-id="95b67-106">The **JET_CALLBACK** function is a multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="95b67-107">請參閱 [JET_CBTYP](./jet-cbtyp.md) ，以取得此函式的參數所使用的特定設定，因為這些設定會根據在 *CBTYP* 參數中選取要使用的 **JET_CBTYP** 選項而有所不同。</span><span class="sxs-lookup"><span data-stu-id="95b67-107">See [JET_CBTYP](./jet-cbtyp.md) for specific settings to use for the parameters of this function, as these settings will differ depending upon the **JET_CBTYP** option that is selected for use in the *cbtyp* parameter.</span></span>

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a><span data-ttu-id="95b67-108">參數</span><span class="sxs-lookup"><span data-stu-id="95b67-108">Parameters</span></span>

<span data-ttu-id="95b67-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="95b67-109">*sesid*</span></span>

<span data-ttu-id="95b67-110">正在進行回呼的會話。</span><span class="sxs-lookup"><span data-stu-id="95b67-110">The session for which the callback is being made.</span></span>

<span data-ttu-id="95b67-111">*dbid*</span><span class="sxs-lookup"><span data-stu-id="95b67-111">*dbid*</span></span>

<span data-ttu-id="95b67-112">正在進行回呼的資料庫。</span><span class="sxs-lookup"><span data-stu-id="95b67-112">The database for which the callback is being made.</span></span>

<span data-ttu-id="95b67-113">*tableid*</span><span class="sxs-lookup"><span data-stu-id="95b67-113">*tableid*</span></span>

<span data-ttu-id="95b67-114">正在進行回呼的資料指標。</span><span class="sxs-lookup"><span data-stu-id="95b67-114">The cursor for which the callback is being made.</span></span>

<span data-ttu-id="95b67-115">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="95b67-115">*cbtyp*</span></span>

<span data-ttu-id="95b67-116">執行回呼的作業中的點。</span><span class="sxs-lookup"><span data-stu-id="95b67-116">The point in the operation at which the callback is being made.</span></span> <span data-ttu-id="95b67-117">請參閱 [JET_CBTYP](./jet-cbtyp.md) ，以取得值清單和每個案例中下列參數的意義。</span><span class="sxs-lookup"><span data-stu-id="95b67-117">See [JET_CBTYP](./jet-cbtyp.md) for a list of values and the meaning of the following parameters in each case.</span></span>

<span data-ttu-id="95b67-118">*pvArg1*</span><span class="sxs-lookup"><span data-stu-id="95b67-118">*pvArg1*</span></span>

<span data-ttu-id="95b67-119">用來與使用回呼的應用程式通訊的參數。</span><span class="sxs-lookup"><span data-stu-id="95b67-119">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="95b67-120">如需有關此參數的使用方式，請參閱 database engine 所支援的每個回呼的詳細資訊 [JET_CBTYP](./jet-cbtyp.md) 。</span><span class="sxs-lookup"><span data-stu-id="95b67-120">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="95b67-121">*pvArg2*</span><span class="sxs-lookup"><span data-stu-id="95b67-121">*pvArg2*</span></span>

<span data-ttu-id="95b67-122">用來與使用回呼的應用程式通訊的參數。</span><span class="sxs-lookup"><span data-stu-id="95b67-122">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="95b67-123">如需有關此參數的使用方式，請參閱 database engine 所支援的每個回呼的詳細資訊 [JET_CBTYP](./jet-cbtyp.md) 。</span><span class="sxs-lookup"><span data-stu-id="95b67-123">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="95b67-124">*pvCoNtext*</span><span class="sxs-lookup"><span data-stu-id="95b67-124">*pvContext*</span></span>

<span data-ttu-id="95b67-125">用來與使用回呼的應用程式通訊的參數。</span><span class="sxs-lookup"><span data-stu-id="95b67-125">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="95b67-126">如需有關此參數的使用方式，請參閱 database engine 所支援的每個回呼的詳細資訊 [JET_CBTYP](./jet-cbtyp.md) 。</span><span class="sxs-lookup"><span data-stu-id="95b67-126">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="95b67-127">*ulUnused*</span><span class="sxs-lookup"><span data-stu-id="95b67-127">*ulUnused*</span></span>

<span data-ttu-id="95b67-128">用來與使用回呼的應用程式通訊的參數。</span><span class="sxs-lookup"><span data-stu-id="95b67-128">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="95b67-129">如需有關此參數的使用方式，請參閱 database engine 所支援的每個回呼的詳細資訊 [JET_CBTYP](./jet-cbtyp.md) 。</span><span class="sxs-lookup"><span data-stu-id="95b67-129">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

#### <a name="return-value"></a><span data-ttu-id="95b67-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="95b67-130">Return Value</span></span>

<span data-ttu-id="95b67-131">函數會傳回其中一個可延伸的 [儲存引擎錯誤碼](./extensible-storage-engine-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="95b67-131">The function returns one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="95b67-132">如需如何將這些程式碼傳回為 Hresult 的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="95b67-132">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="95b67-133">成功時，發出回呼的作業可以正常執行。</span><span class="sxs-lookup"><span data-stu-id="95b67-133">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="95b67-134">在某些情況下，回呼可能會傳回會影響該作業的警告。</span><span class="sxs-lookup"><span data-stu-id="95b67-134">In some cases, the callback may return a warning that influences that operation.</span></span> <span data-ttu-id="95b67-135">如需作業使用這些警告的詳細資訊，請參閱 [JET_CBTYP](./jet-cbtyp.md) 。</span><span class="sxs-lookup"><span data-stu-id="95b67-135">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of these warnings by the operation.</span></span>

<span data-ttu-id="95b67-136">失敗時，發出回呼的作業可能會正常進行，或可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="95b67-136">On failure, the operation that issued the callback may proceed normally or may fail.</span></span> <span data-ttu-id="95b67-137">如需作業使用錯誤碼的詳細資訊，請參閱 [JET_CBTYP](./jet-cbtyp.md) 。</span><span class="sxs-lookup"><span data-stu-id="95b67-137">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of the error code by the operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="95b67-138">備註</span><span class="sxs-lookup"><span data-stu-id="95b67-138">Remarks</span></span>

<span data-ttu-id="95b67-139">如果回呼將資料指標傳遞至應用程式，請務必知道此資料指標刻意限制為較小的一組功能，以避免遞迴和其他 ugliness。</span><span class="sxs-lookup"><span data-stu-id="95b67-139">If the callback passes a cursor to the application then it is important to know that this cursor is intentionally limited to a smaller set of functionality to avoid recursion and other ugliness.</span></span> <span data-ttu-id="95b67-140">允許下列作業：</span><span class="sxs-lookup"><span data-stu-id="95b67-140">The following operations are allowed:</span></span>

  - [<span data-ttu-id="95b67-141">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="95b67-141">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="95b67-142">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="95b67-142">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="95b67-143">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="95b67-143">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="95b67-144">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="95b67-144">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)

  - [<span data-ttu-id="95b67-145">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="95b67-145">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="95b67-146">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="95b67-146">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="95b67-147">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="95b67-147">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)

  - [<span data-ttu-id="95b67-148">JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="95b67-148">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)

  - [<span data-ttu-id="95b67-149">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="95b67-149">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)

  - [<span data-ttu-id="95b67-150">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="95b67-150">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)

  - [<span data-ttu-id="95b67-151">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="95b67-151">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="95b67-152">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="95b67-152">JetRegisterCallback</span></span>](./jetregistercallback-function.md)

  - [<span data-ttu-id="95b67-153">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="95b67-153">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="95b67-154">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="95b67-154">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="95b67-155">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="95b67-155">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="95b67-156">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="95b67-156">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="95b67-157">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="95b67-157">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="95b67-158">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="95b67-158">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="95b67-159">JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="95b67-159">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)

<span data-ttu-id="95b67-160">當您設計回呼時，請考慮即使有這些限制，回呼仍可能失敗。</span><span class="sxs-lookup"><span data-stu-id="95b67-160">When you design your callback, take into account that even with these restrictions, it is still possible for the callback to fail.</span></span>

#### <a name="requirements"></a><span data-ttu-id="95b67-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="95b67-161">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95b67-162"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="95b67-162"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="95b67-163">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="95b67-163">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b67-164"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="95b67-164"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="95b67-165">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="95b67-165">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b67-166"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="95b67-166"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="95b67-167">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="95b67-167">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="95b67-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95b67-168">See Also</span></span>

[<span data-ttu-id="95b67-169">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="95b67-169">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="95b67-170">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="95b67-170">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="95b67-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="95b67-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="95b67-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="95b67-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="95b67-173">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="95b67-173">JET_CBTYP</span></span>](./jet-cbtyp.md)
