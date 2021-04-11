---
title: 'IBackgroundCopyJob SetNotifyInterface 方法 (>deliveryoptimization .h) '
description: 識別要執行之 IBackgroundCopyCallback 介面的實作為。 您可以使用 IBackgroundCopyCallback 介面來接收作業相關事件的通知。
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- SetNotifyInterface 方法
- SetNotifyInterface 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，SetNotifyInterface 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317224"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a><span data-ttu-id="694a3-107">IBackgroundCopyJob：： SetNotifyInterface 方法</span><span class="sxs-lookup"><span data-stu-id="694a3-107">IBackgroundCopyJob::SetNotifyInterface method</span></span>

<span data-ttu-id="694a3-108">識別要執行之 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="694a3-108">Identifies your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to DO.</span></span> <span data-ttu-id="694a3-109">您可以使用 **IBackgroundCopyCallback** 介面來接收作業相關事件的通知。</span><span class="sxs-lookup"><span data-stu-id="694a3-109">Use the **IBackgroundCopyCallback** interface to receive notification of job-related events.</span></span>

## <a name="syntax"></a><span data-ttu-id="694a3-110">語法</span><span class="sxs-lookup"><span data-stu-id="694a3-110">Syntax</span></span>


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="694a3-111">參數</span><span class="sxs-lookup"><span data-stu-id="694a3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="694a3-112">*pNotifyInterface*</span><span class="sxs-lookup"><span data-stu-id="694a3-112">*pNotifyInterface*</span></span> 
</dt> <dd>

<span data-ttu-id="694a3-113">[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="694a3-113">An [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface pointer.</span></span> <span data-ttu-id="694a3-114">若要移除目前的回呼介面指標，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="694a3-114">To remove the current callback interface pointer, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="694a3-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="694a3-115">Return value</span></span>

<span data-ttu-id="694a3-116">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="694a3-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="694a3-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="694a3-117">Return code</span></span>                                                                              | <span data-ttu-id="694a3-118">Description</span><span class="sxs-lookup"><span data-stu-id="694a3-118">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="694a3-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="694a3-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="694a3-120">已成功設定通知介面指標。</span><span class="sxs-lookup"><span data-stu-id="694a3-120">Notification interface pointer was successfully set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="694a3-121">備註</span><span class="sxs-lookup"><span data-stu-id="694a3-121">Remarks</span></span>

<span data-ttu-id="694a3-122">只有在您執行 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面時，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="694a3-122">Call this method only if you implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="694a3-123">使用 **SetNotifyInterface** 方法搭配 [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) 方法，以指定您想要接收的通知類型。</span><span class="sxs-lookup"><span data-stu-id="694a3-123">Use the **SetNotifyInterface** method in conjunction with the [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to specify the type of notification that you want to receive.</span></span>

<span data-ttu-id="694a3-124">當您的應用程式終止時，通知介面會變成無效;請勿保存通知介面。</span><span class="sxs-lookup"><span data-stu-id="694a3-124">The notification interface becomes invalid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="694a3-125">如此一來，應用程式的初始化程式應該在您要接收通知的現有工作上呼叫 **SetNotifyInterface** 方法。</span><span class="sxs-lookup"><span data-stu-id="694a3-125">As a result, your application's initialization process should call the **SetNotifyInterface** method on those existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="694a3-126">如果您需要捕獲自上一次執行應用程式之後發生的狀態和進度資訊，請在應用程式初始化期間輪詢狀態和進度資訊。</span><span class="sxs-lookup"><span data-stu-id="694a3-126">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="694a3-127">只有作業擁有者/建立者或系統管理員可以註冊通知。</span><span class="sxs-lookup"><span data-stu-id="694a3-127">Only the job owner/creator or an administrator can register for notifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="694a3-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="694a3-128">Requirements</span></span>



| <span data-ttu-id="694a3-129">需求</span><span class="sxs-lookup"><span data-stu-id="694a3-129">Requirement</span></span> | <span data-ttu-id="694a3-130">值</span><span class="sxs-lookup"><span data-stu-id="694a3-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="694a3-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="694a3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="694a3-132">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="694a3-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="694a3-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="694a3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="694a3-134">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="694a3-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="694a3-135">標頭</span><span class="sxs-lookup"><span data-stu-id="694a3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="694a3-136"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="694a3-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="694a3-137">Idl</span><span class="sxs-lookup"><span data-stu-id="694a3-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="694a3-138"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="694a3-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="694a3-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="694a3-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="694a3-140"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="694a3-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="694a3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="694a3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="694a3-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="694a3-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="694a3-143">IID</span><span class="sxs-lookup"><span data-stu-id="694a3-143">IID</span></span><br/>                      | <span data-ttu-id="694a3-144">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="694a3-144">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="694a3-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="694a3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="694a3-146">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="694a3-146">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="694a3-147">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="694a3-147">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="694a3-148">**IBackgroundCopyJob::GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="694a3-148">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="694a3-149">**IBackgroundCopyJob::SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="694a3-149">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





