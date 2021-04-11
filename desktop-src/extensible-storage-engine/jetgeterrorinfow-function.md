---
description: 深入瞭解： JetGetErrorInfoW 函數
title: JetGetErrorInfoW 函式
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104116320"
---
# <a name="jetgeterrorinfow-function"></a><span data-ttu-id="298e0-103">JetGetErrorInfoW 函式</span><span class="sxs-lookup"><span data-stu-id="298e0-103">JetGetErrorInfoW Function</span></span>


<span data-ttu-id="298e0-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="298e0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgeterrorinfow-function"></a><span data-ttu-id="298e0-105">JetGetErrorInfoW 函式</span><span class="sxs-lookup"><span data-stu-id="298e0-105">JetGetErrorInfoW Function</span></span>

<span data-ttu-id="298e0-106">資料庫引擎的 **JetGetErrorInfoW** 函數 BAS_。</span><span class="sxs-lookup"><span data-stu-id="298e0-106">The **JetGetErrorInfoW** function BAS_ of the database engine.</span></span>

<span data-ttu-id="298e0-107">注意：本檔是以可延伸儲存引擎的初步發行版本為基礎。</span><span class="sxs-lookup"><span data-stu-id="298e0-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="298e0-108">此資訊可能隨時變更。</span><span class="sxs-lookup"><span data-stu-id="298e0-108">This information is subject to change.</span></span>

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a><span data-ttu-id="298e0-109">參數</span><span class="sxs-lookup"><span data-stu-id="298e0-109">Parameters</span></span>

<span data-ttu-id="298e0-110">*pvCoNtext*</span><span class="sxs-lookup"><span data-stu-id="298e0-110">*pvContext*</span></span>

<span data-ttu-id="298e0-111">需要擴充錯誤資訊的內容或錯誤值。</span><span class="sxs-lookup"><span data-stu-id="298e0-111">The context or error value for which the extended error information is needed.</span></span> <span data-ttu-id="298e0-112">傳入的值取決於 *InfoLevel* 參數值。</span><span class="sxs-lookup"><span data-stu-id="298e0-112">The value passed in depends on the *InfoLevel* parameter value.</span></span>

<span data-ttu-id="298e0-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="298e0-113">*pvResult*</span></span>

<span data-ttu-id="298e0-114">將接收資訊的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="298e0-114">A pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="298e0-115">緩衝區的類型取決於 *InfoLevel* 參數值。</span><span class="sxs-lookup"><span data-stu-id="298e0-115">The type of the buffer depends on the *InfoLevel* parameter value.</span></span> <span data-ttu-id="298e0-116">呼叫端必須設定為適當地對齊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="298e0-116">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="298e0-117">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="298e0-117">*cbMax*</span></span>

<span data-ttu-id="298e0-118">傳入的 *pvResult* 結構大小上限。</span><span class="sxs-lookup"><span data-stu-id="298e0-118">The maximum size of the *pvResult* structure that is passed in.</span></span>

<span data-ttu-id="298e0-119">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="298e0-119">*InfoLevel*</span></span>

<span data-ttu-id="298e0-120">將針對錯誤資訊/內容抓取的資訊類型是由 *pvCoNtext* 參數指定。</span><span class="sxs-lookup"><span data-stu-id="298e0-120">The type of information that will be retrieved for the error info/context is specified by the *pvContext* parameter.</span></span> <span data-ttu-id="298e0-121">儲存在 *pvResult* 中的資料格式取決於 *InfoLevel*。</span><span class="sxs-lookup"><span data-stu-id="298e0-121">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="298e0-122">下表列出此參數的可能值。</span><span class="sxs-lookup"><span data-stu-id="298e0-122">The following table lists the possible values for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="298e0-123">值</span><span class="sxs-lookup"><span data-stu-id="298e0-123">Value</span></span></p></th>
<th><p><span data-ttu-id="298e0-124">意義</span><span class="sxs-lookup"><span data-stu-id="298e0-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="298e0-125">JET_ErrorInfoSpecificErr</span><span class="sxs-lookup"><span data-stu-id="298e0-125">JET_ErrorInfoSpecificErr</span></span></p></td>
<td><p><span data-ttu-id="298e0-126"><em>pvCoNtext</em> 會被視為 <a href="gg269297(v=exchg.10).md">JET_ERR</a>/Error 程式碼， <em>pvResult</em> 會被視為 <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>，而 <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> 結構的欄位則會適當地填入。</span><span class="sxs-lookup"><span data-stu-id="298e0-126"><em>pvContext</em> is interpreted as a <a href="gg269297(v=exchg.10).md">JET_ERR</a>/error code, <em>pvResult</em> is interpreted as a <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>, and the fields of the <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> structure are filled in appropriately.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="298e0-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="298e0-127">*grbit*</span></span>

<span data-ttu-id="298e0-128">保留的。</span><span class="sxs-lookup"><span data-stu-id="298e0-128">Reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="298e0-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="298e0-129">Return Value</span></span>

<span data-ttu-id="298e0-130">此函數會傳回 [JET_ERR](./extensible-storage-engine-error-codes.md) 資料類型，其中包含下表所列的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="298e0-130">This function returns the [JET_ERR](./extensible-storage-engine-error-codes.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="298e0-131">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="298e0-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="298e0-132">傳回碼</span><span class="sxs-lookup"><span data-stu-id="298e0-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="298e0-133">Description</span><span class="sxs-lookup"><span data-stu-id="298e0-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="298e0-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="298e0-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="298e0-135">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="298e0-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298e0-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="298e0-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="298e0-137">提供的其中一個參數包含未預期的值，或包含與另一個參數的值結合時沒有意義的值。</span><span class="sxs-lookup"><span data-stu-id="298e0-137">One of the parameters provided contains an unexpected value or contains a value that does not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="298e0-138">發生下列情況時， <strong>JetGetErrorInfo</strong> 可能會發生這種情況：</span><span class="sxs-lookup"><span data-stu-id="298e0-138">This can happen for <strong>JetGetErrorInfo</strong> when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="298e0-139">指定的 <em>InfoLevel</em> 參數值無效。</span><span class="sxs-lookup"><span data-stu-id="298e0-139">The specified <em>InfoLevel</em> parameter value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="298e0-140">指定的 <em>grbit</em> 值無效。</span><span class="sxs-lookup"><span data-stu-id="298e0-140">The specified <em>grbit</em> value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="298e0-141">指定的 <em>pvResult</em> 參數緩衝區的 <em>cbMax</em> 值小於這個 <em>InfoLevel</em> 參數的輸出所需的大小。</span><span class="sxs-lookup"><span data-stu-id="298e0-141">The specified <em>pvResult</em> parameter buffer’s <em>cbMax</em> value is less than the required size for output of this <em>InfoLevel</em> parameter.</span></span></p></li>
<li><p><span data-ttu-id="298e0-142">針對 <em>InfoLevel</em> = JET_ErrorInfoSpecificErr，傳入的 <a href="gg294092(v=exchg.10).md">JET_ERR</a> 值對引擎而言是未知的。</span><span class="sxs-lookup"><span data-stu-id="298e0-142">For <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, the <a href="gg294092(v=exchg.10).md">JET_ERR</a> value passed in is unknown to the engine.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298e0-143">JET_errDisabledFunctionality</span><span class="sxs-lookup"><span data-stu-id="298e0-143">JET_errDisabledFunctionality</span></span></p></td>
<td><p><span data-ttu-id="298e0-144">如果此 windows SKU 不支援此功能，將會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="298e0-144">If this SKU of windows doesn’t support this function, this error will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="298e0-145">成功時，適用于要求之錯誤內容/值的輸出緩衝區將會設定為所要求的擴充錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="298e0-145">On success, the output buffer that is appropriate for the requested error context/value will be set to the extended error info requested.</span></span>

<span data-ttu-id="298e0-146">失敗時，輸出緩衝區的狀態將會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="298e0-146">On failure, the state of the output buffers will be undefined.</span></span>

### <a name="remarks"></a><span data-ttu-id="298e0-147">備註</span><span class="sxs-lookup"><span data-stu-id="298e0-147">Remarks</span></span>

<span data-ttu-id="298e0-148">[JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md)函式和 [JET_ERRCAT](./jet-errcat.md)的常數群組包含 *InfoLevel* = JET_ErrorInfoSpecificErr 所傳回之擴充錯誤資訊的相關檔。</span><span class="sxs-lookup"><span data-stu-id="298e0-148">The [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) function and [JET_ERRCAT](./jet-errcat.md) group of constants contain documentation about the extended error information that is returned for *InfoLevel* = JET_ErrorInfoSpecificErr.</span></span>

### <a name="requirements"></a><span data-ttu-id="298e0-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="298e0-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="298e0-150"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="298e0-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="298e0-151">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="298e0-151">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298e0-152"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="298e0-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="298e0-153">需要 Windows 8 Server。</span><span class="sxs-lookup"><span data-stu-id="298e0-153">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298e0-154"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="298e0-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="298e0-155">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="298e0-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298e0-156"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="298e0-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="298e0-157">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="298e0-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298e0-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="298e0-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="298e0-159">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="298e0-159">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298e0-160"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="298e0-160"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="298e0-161">注意：只會執行 <strong>JetGetErrorInfoW</strong> (Unicode) 。</span><span class="sxs-lookup"><span data-stu-id="298e0-161">Note: Only the <strong>JetGetErrorInfoW</strong> (Unicode) is implemented.</span></span> <span data-ttu-id="298e0-162">此 API 沒有 (ANSI) 版本。</span><span class="sxs-lookup"><span data-stu-id="298e0-162">This API does not have an A (ANSI) version.</span></span></p></td>
</tr>
</tbody>
</table>
