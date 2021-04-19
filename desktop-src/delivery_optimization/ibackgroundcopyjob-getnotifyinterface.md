---
title: 'IBackgroundCopyJob GetNotifyInterface 方法 (>deliveryoptimization .h) '
description: 抓取 IBackgroundCopyCallback 介面的實介面指標。
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- GetNotifyInterface 方法
- GetNotifyInterface 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetNotifyInterface 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967368"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a><span data-ttu-id="6dbd7-106">IBackgroundCopyJob：： GetNotifyInterface 方法</span><span class="sxs-lookup"><span data-stu-id="6dbd7-106">IBackgroundCopyJob::GetNotifyInterface method</span></span>

<span data-ttu-id="6dbd7-107">抓取 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面的實介面指標。</span><span class="sxs-lookup"><span data-stu-id="6dbd7-107">Retrieves the interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dbd7-108">語法</span><span class="sxs-lookup"><span data-stu-id="6dbd7-108">Syntax</span></span>


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="6dbd7-109">參數</span><span class="sxs-lookup"><span data-stu-id="6dbd7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dbd7-110">*ppNotifyInterface* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6dbd7-110">*ppNotifyInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dbd7-111">[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)介面的實介面指標。</span><span class="sxs-lookup"><span data-stu-id="6dbd7-111">Interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="6dbd7-112">完成時，發行 *ppNotifyInterface*。</span><span class="sxs-lookup"><span data-stu-id="6dbd7-112">When done, release *ppNotifyInterface*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dbd7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6dbd7-113">Return value</span></span>

<span data-ttu-id="6dbd7-114">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="6dbd7-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="6dbd7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6dbd7-115">Return code</span></span>                                                                              | <span data-ttu-id="6dbd7-116">Description</span><span class="sxs-lookup"><span data-stu-id="6dbd7-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="6dbd7-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6dbd7-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="6dbd7-118">已成功抓取通知介面指標。</span><span class="sxs-lookup"><span data-stu-id="6dbd7-118">Notification interface pointer was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6dbd7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dbd7-119">Requirements</span></span>



| <span data-ttu-id="6dbd7-120">需求</span><span class="sxs-lookup"><span data-stu-id="6dbd7-120">Requirement</span></span> | <span data-ttu-id="6dbd7-121">值</span><span class="sxs-lookup"><span data-stu-id="6dbd7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dbd7-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6dbd7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6dbd7-123">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dbd7-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6dbd7-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6dbd7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6dbd7-125">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dbd7-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6dbd7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6dbd7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dbd7-127"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="6dbd7-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="6dbd7-128">Idl</span><span class="sxs-lookup"><span data-stu-id="6dbd7-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6dbd7-129"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6dbd7-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="6dbd7-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="6dbd7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="6dbd7-131"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6dbd7-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="6dbd7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6dbd7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dbd7-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dbd7-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="6dbd7-134">IID</span><span class="sxs-lookup"><span data-stu-id="6dbd7-134">IID</span></span><br/>                      | <span data-ttu-id="6dbd7-135">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="6dbd7-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6dbd7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6dbd7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dbd7-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="6dbd7-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="6dbd7-138">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="6dbd7-138">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="6dbd7-139">**IBackgroundCopyJob::GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="6dbd7-139">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="6dbd7-140">**IBackgroundCopyJob::SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="6dbd7-140">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





