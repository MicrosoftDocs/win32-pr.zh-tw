---
title: 'IDeliveryOptimizationJob AddFileWithRanges 方法 (>deliveryoptimization .h) '
description: 將檔案新增至下載作業，並指定您想要下載的檔案範圍。
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- AddFileWithRanges 方法
- AddFileWithRanges 方法，IDeliveryOptimizationJob 介面
- IDeliveryOptimizationJob 介面，AddFileWithRanges 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965329"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a><span data-ttu-id="9930d-106">IDeliveryOptimizationJob：： AddFileWithRanges 方法</span><span class="sxs-lookup"><span data-stu-id="9930d-106">IDeliveryOptimizationJob::AddFileWithRanges method</span></span>

<span data-ttu-id="9930d-107">將檔案新增至下載作業，並指定您想要下載的檔案範圍。</span><span class="sxs-lookup"><span data-stu-id="9930d-107">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="9930d-108">語法</span><span class="sxs-lookup"><span data-stu-id="9930d-108">Syntax</span></span>


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a><span data-ttu-id="9930d-109">參數</span><span class="sxs-lookup"><span data-stu-id="9930d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9930d-110">*fileId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9930d-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9930d-111">以 Null 終止的字串，表示已發佈內容的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9930d-111">Null terminated string that s an unique identifier of the published content.</span></span> <span data-ttu-id="9930d-112">針對未發佈的內容，這可以是任何唯一的字串，呼叫者可以用來識別作業內的檔案。</span><span class="sxs-lookup"><span data-stu-id="9930d-112">For non-published content, this can be any unique string that caller can use to identify files within a job.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-113">*remoteUrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9930d-113">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9930d-114">以 Null 終止的字串，其中包含伺服器上的檔案名。</span><span class="sxs-lookup"><span data-stu-id="9930d-114">Null-terminated string that contains the name of the file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-115">*localName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9930d-115">*localName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9930d-116">以 Null 終止的字串，其中包含用戶端上的檔案名。</span><span class="sxs-lookup"><span data-stu-id="9930d-116">Null-terminated string that contains the name of the file on the client.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-117">*rangeCount* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9930d-117">*rangeCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9930d-118">*範圍* 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="9930d-118">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-119">*範圍* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9930d-119">*ranges* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9930d-120">一或多個 [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) 結構的陣列，指定要下載的範圍。</span><span class="sxs-lookup"><span data-stu-id="9930d-120">Array of one or more [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) structures that specify the ranges to download.</span></span> <span data-ttu-id="9930d-121">請勿指定重複或重迭的範圍。</span><span class="sxs-lookup"><span data-stu-id="9930d-121">Do not specify duplicate or overlapping ranges.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-122">*fileSize* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9930d-122">*fileSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9930d-123">檔案大小，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="9930d-123">Size of the file in bytes.</span></span> <span data-ttu-id="9930d-124">如果呼叫端應用程式不知道大小，請傳入 **DO_UNKNOWN_FILE_SIZE** 。</span><span class="sxs-lookup"><span data-stu-id="9930d-124">Pass in **DO_UNKNOWN_FILE_SIZE** if size is not known to the caller application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9930d-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="9930d-125">Return value</span></span>

<span data-ttu-id="9930d-126">這個方法會傳回下列傳回值以及其他值。</span><span class="sxs-lookup"><span data-stu-id="9930d-126">This method returns the following return values, as well as others.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9930d-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9930d-127">Return code</span></span></th>
<th><span data-ttu-id="9930d-128">Description</span><span class="sxs-lookup"><span data-stu-id="9930d-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="9930d-129"><dt><strong><strong>S_OK</strong></strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9930d-129"><dt><strong><strong>S_OK</strong></strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9930d-130">成功。</span><span class="sxs-lookup"><span data-stu-id="9930d-130">Success.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9930d-131"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9930d-131"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9930d-132">本機檔案名為 Null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="9930d-132">The local file name is NULL or empty string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9930d-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9930d-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9930d-134">使用者沒有許可權可寫入至用戶端上指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="9930d-134">User does not have permission to write to the specified directory on the client.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9930d-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9930d-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9930d-136">其中一個範圍無效。</span><span class="sxs-lookup"><span data-stu-id="9930d-136">One of the ranges is invalid.</span></span> <span data-ttu-id="9930d-137">例如，InitialOffset 會設定為 <strong>BG_LENGTH_TO_EOF</strong>。</span><span class="sxs-lookup"><span data-stu-id="9930d-137">For example, InitialOffset is set to <strong>BG_LENGTH_TO_EOF</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9930d-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9930d-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9930d-139">您無法指定重複或重迭的範圍。</span><span class="sxs-lookup"><span data-stu-id="9930d-139">You cannot specify duplicate or overlapping ranges.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9930d-140">範圍是依值的位移（而不是長度）來排序。</span><span class="sxs-lookup"><span data-stu-id="9930d-140">The ranges are sorted by the offset of the value, not the length.</span></span> <span data-ttu-id="9930d-141">如果輸入的範圍具有相同的位移，但順序相反，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9930d-141">If ranges are entered that have the same offset, but are in reverse order, then this error will be returned.</span></span> <span data-ttu-id="9930d-142">例如，如果以該順序輸入100.5 和100.0，您將無法將檔案新增至作業。</span><span class="sxs-lookup"><span data-stu-id="9930d-142">For example, if 100.5 and 100.0 are entered in that order, then you will not be able to add the file to the job.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9930d-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9930d-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9930d-144">無法 <strong>BG_JOB_STATE_CANCELLED</strong> 或 <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="9930d-144">The state of the job cannot be <strong>BG_JOB_STATE_CANCELLED</strong> or <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9930d-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="9930d-145">Requirements</span></span>



| <span data-ttu-id="9930d-146">需求</span><span class="sxs-lookup"><span data-stu-id="9930d-146">Requirement</span></span> | <span data-ttu-id="9930d-147">值</span><span class="sxs-lookup"><span data-stu-id="9930d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9930d-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9930d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9930d-149">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9930d-149">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9930d-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9930d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9930d-151">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9930d-151">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9930d-152">標頭</span><span class="sxs-lookup"><span data-stu-id="9930d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="9930d-153"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="9930d-153"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9930d-154">Idl</span><span class="sxs-lookup"><span data-stu-id="9930d-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9930d-155"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9930d-155"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9930d-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="9930d-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="9930d-157"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9930d-157"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9930d-158">DLL</span><span class="sxs-lookup"><span data-stu-id="9930d-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9930d-159"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9930d-159"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9930d-160">IID</span><span class="sxs-lookup"><span data-stu-id="9930d-160">IID</span></span><br/>                      | <span data-ttu-id="9930d-161">IID_IDeliveryOptimizationJob 定義為 EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="9930d-161">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="9930d-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9930d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9930d-163">**IDeliveryOptimizationJob**</span><span class="sxs-lookup"><span data-stu-id="9930d-163">**IDeliveryOptimizationJob**</span></span>](ideliveryoptimizationjob.md)
</dt> </dl>

 

