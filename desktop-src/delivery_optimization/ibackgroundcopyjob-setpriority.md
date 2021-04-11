---
title: 'IBackgroundCopyJob SetPriority 方法 (>deliveryoptimization .h) '
description: 指定作業的優先權層級。 優先權層級會決定您的作業相對於傳送佇列中其他作業的處理時間。
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- SetPriority 方法
- SetPriority 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，SetPriority 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685961"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a><span data-ttu-id="201fd-107">IBackgroundCopyJob：： SetPriority 方法</span><span class="sxs-lookup"><span data-stu-id="201fd-107">IBackgroundCopyJob::SetPriority method</span></span>

<span data-ttu-id="201fd-108">指定作業的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="201fd-108">Specifies the priority level of your job.</span></span> <span data-ttu-id="201fd-109">優先權層級會決定您的作業相對於傳送佇列中其他作業的處理時間。</span><span class="sxs-lookup"><span data-stu-id="201fd-109">The priority level determines when your job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="201fd-110">語法</span><span class="sxs-lookup"><span data-stu-id="201fd-110">Syntax</span></span>


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a><span data-ttu-id="201fd-111">參數</span><span class="sxs-lookup"><span data-stu-id="201fd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="201fd-112">*優先順序* \[在\]</span><span class="sxs-lookup"><span data-stu-id="201fd-112">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="201fd-113">指定作業相對於傳送佇列中其他作業的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="201fd-113">Specifies the priority level of your job relative to other jobs in the transfer queue.</span></span> <span data-ttu-id="201fd-114">預設值為 BG_JOB_PRIORITY_NORMAL。</span><span class="sxs-lookup"><span data-stu-id="201fd-114">The default is BG_JOB_PRIORITY_NORMAL.</span></span> <span data-ttu-id="201fd-115">如需優先權層級的清單，請參閱 [**BG_JOB_PRIORITY**](bg-job-priority-.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="201fd-115">For a list of priority levels, see the [**BG_JOB_PRIORITY**](bg-job-priority-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="201fd-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="201fd-116">Return value</span></span>

<span data-ttu-id="201fd-117">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="201fd-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="201fd-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="201fd-118">Return code</span></span>                                                                              | <span data-ttu-id="201fd-119">Description</span><span class="sxs-lookup"><span data-stu-id="201fd-119">Description</span></span>                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="201fd-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="201fd-121">已成功設定作業優先順序。</span><span class="sxs-lookup"><span data-stu-id="201fd-121">Job priority was successfully set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="201fd-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="201fd-122">Requirements</span></span>



| <span data-ttu-id="201fd-123">需求</span><span class="sxs-lookup"><span data-stu-id="201fd-123">Requirement</span></span> | <span data-ttu-id="201fd-124">值</span><span class="sxs-lookup"><span data-stu-id="201fd-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="201fd-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="201fd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="201fd-126">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="201fd-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="201fd-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="201fd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="201fd-128">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="201fd-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="201fd-129">標頭</span><span class="sxs-lookup"><span data-stu-id="201fd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="201fd-130"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="201fd-131">Idl</span><span class="sxs-lookup"><span data-stu-id="201fd-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="201fd-132"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="201fd-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="201fd-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="201fd-134"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="201fd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="201fd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="201fd-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="201fd-137">IID</span><span class="sxs-lookup"><span data-stu-id="201fd-137">IID</span></span><br/>                      | <span data-ttu-id="201fd-138">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="201fd-138">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="201fd-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="201fd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="201fd-140">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="201fd-140">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="201fd-141">**BG_JOB_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="201fd-141">**BG_JOB_PRIORITY**</span></span>](bg-job-priority-.md)
</dt> <dt>

[<span data-ttu-id="201fd-142">**IBackgroundCopyJob：： GetPriority**</span><span class="sxs-lookup"><span data-stu-id="201fd-142">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





