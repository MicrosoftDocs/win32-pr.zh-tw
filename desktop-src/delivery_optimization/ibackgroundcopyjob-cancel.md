---
title: 'IBackgroundCopyJob Cancel 方法 (>deliveryoptimization) '
description: 從傳送佇列刪除工作，並從用戶端移除相關的暫存檔案 (下載) 和伺服器 (上傳) 。
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Cancel 方法
- Cancel 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，Cancel 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843456"
---
# <a name="ibackgroundcopyjobcancel-method"></a><span data-ttu-id="fb64e-106">IBackgroundCopyJob：： Cancel 方法</span><span class="sxs-lookup"><span data-stu-id="fb64e-106">IBackgroundCopyJob::Cancel method</span></span>

<span data-ttu-id="fb64e-107">從傳送佇列刪除工作，並從用戶端移除相關的暫存檔案 (下載) 和伺服器 (上傳) 。</span><span class="sxs-lookup"><span data-stu-id="fb64e-107">Deletes the job from the transfer queue and removes related temporary files from the client (downloads) and server (uploads).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb64e-108">語法</span><span class="sxs-lookup"><span data-stu-id="fb64e-108">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="fb64e-109">參數</span><span class="sxs-lookup"><span data-stu-id="fb64e-109">Parameters</span></span>

<span data-ttu-id="fb64e-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fb64e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb64e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb64e-111">Return value</span></span>

<span data-ttu-id="fb64e-112">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="fb64e-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="fb64e-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fb64e-113">Return code</span></span>                                                                                          | <span data-ttu-id="fb64e-114">Description</span><span class="sxs-lookup"><span data-stu-id="fb64e-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb64e-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="fb64e-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="fb64e-116">已成功取消作業。</span><span class="sxs-lookup"><span data-stu-id="fb64e-116">Job was successfully canceled.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="fb64e-117"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="fb64e-117"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="fb64e-118">無法取消其狀態為 BG_JOB_STATE_CANCELLED 或 BG_JOB_STATE_ACKNOWLEDGED 的作業。</span><span class="sxs-lookup"><span data-stu-id="fb64e-118">Cannot cancel a job whose state is BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb64e-119">備註</span><span class="sxs-lookup"><span data-stu-id="fb64e-119">Remarks</span></span>

<span data-ttu-id="fb64e-120">您可以隨時取消作業;不過，無法在作業取消之後復原。</span><span class="sxs-lookup"><span data-stu-id="fb64e-120">You can cancel a job at any time; however, the job cannot be recovered after it is canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb64e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb64e-121">Requirements</span></span>



| <span data-ttu-id="fb64e-122">需求</span><span class="sxs-lookup"><span data-stu-id="fb64e-122">Requirement</span></span> | <span data-ttu-id="fb64e-123">值</span><span class="sxs-lookup"><span data-stu-id="fb64e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb64e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb64e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fb64e-125">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb64e-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fb64e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb64e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fb64e-127">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb64e-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fb64e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="fb64e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb64e-129"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb64e-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb64e-130">Idl</span><span class="sxs-lookup"><span data-stu-id="fb64e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb64e-131"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb64e-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="fb64e-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="fb64e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb64e-133"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb64e-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="fb64e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fb64e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb64e-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb64e-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="fb64e-136">IID</span><span class="sxs-lookup"><span data-stu-id="fb64e-136">IID</span></span><br/>                      | <span data-ttu-id="fb64e-137">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="fb64e-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fb64e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb64e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb64e-139">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="fb64e-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="fb64e-140">**IBackgroundCopyJob：： Complete**</span><span class="sxs-lookup"><span data-stu-id="fb64e-140">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="fb64e-141">**IBackgroundCopyJob：： Resume**</span><span class="sxs-lookup"><span data-stu-id="fb64e-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> <dt>

[<span data-ttu-id="fb64e-142">**IBackgroundCopyJob：：暫止**</span><span class="sxs-lookup"><span data-stu-id="fb64e-142">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





