---
title: 'IBackgroundCopyJob >getstate 方法 (>deliveryoptimization .h) '
description: 捕獲作業的狀態。
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- '>getstate 方法'
- '>getstate 方法，IBackgroundCopyJob 介面'
- IBackgroundCopyJob 介面，>getstate 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685962"
---
# <a name="ibackgroundcopyjobgetstate-method"></a><span data-ttu-id="7c5d2-106">IBackgroundCopyJob：： >getstate 方法</span><span class="sxs-lookup"><span data-stu-id="7c5d2-106">IBackgroundCopyJob::GetState method</span></span>

<span data-ttu-id="7c5d2-107">捕獲作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-107">Retrieves the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c5d2-108">語法</span><span class="sxs-lookup"><span data-stu-id="7c5d2-108">Syntax</span></span>


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a><span data-ttu-id="7c5d2-109">參數</span><span class="sxs-lookup"><span data-stu-id="7c5d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c5d2-110">*pJobState* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7c5d2-110">*pJobState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c5d2-111">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-111">The state of the job.</span></span> <span data-ttu-id="7c5d2-112">例如，此狀態會反映作業是錯誤、傳送資料還是暫停。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-112">For example, the state reflects whether the job is in error, transferring data, or suspended.</span></span> <span data-ttu-id="7c5d2-113">如需作業狀態的清單，請參閱 [**BG_JOB_STATE**](bg-job-state-.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-113">For a list of job states, see the [**BG_JOB_STATE**](bg-job-state-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c5d2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c5d2-114">Return value</span></span>

<span data-ttu-id="7c5d2-115">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="7c5d2-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7c5d2-116">Return code</span></span>                                                                              | <span data-ttu-id="7c5d2-117">Description</span><span class="sxs-lookup"><span data-stu-id="7c5d2-117">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="7c5d2-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="7c5d2-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="7c5d2-119">已成功抓取作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-119">The state of the job was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c5d2-120">備註</span><span class="sxs-lookup"><span data-stu-id="7c5d2-120">Remarks</span></span>

<span data-ttu-id="7c5d2-121">如果您想要知道作業發生錯誤或已傳送作業中的所有檔案，您可以使用這個方法來輪詢作業的狀態，或您可以註冊在事件發生時收到通知。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-121">If you want to know when a job is in error or has transferred all the files in the job, you can use this method to poll for the state of the job or you can register to receive notification when events occur.</span></span> <span data-ttu-id="7c5d2-122">如需註冊以接收事件通知的詳細資訊，請參閱 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="7c5d2-122">For details on registering to receive event notification, see the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c5d2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c5d2-123">Requirements</span></span>



| <span data-ttu-id="7c5d2-124">需求</span><span class="sxs-lookup"><span data-stu-id="7c5d2-124">Requirement</span></span> | <span data-ttu-id="7c5d2-125">值</span><span class="sxs-lookup"><span data-stu-id="7c5d2-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c5d2-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c5d2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7c5d2-127">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c5d2-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7c5d2-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c5d2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7c5d2-129">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c5d2-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7c5d2-130">標頭</span><span class="sxs-lookup"><span data-stu-id="7c5d2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c5d2-131"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c5d2-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c5d2-132">Idl</span><span class="sxs-lookup"><span data-stu-id="7c5d2-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c5d2-133"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c5d2-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="7c5d2-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="7c5d2-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c5d2-135"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c5d2-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="7c5d2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7c5d2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c5d2-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c5d2-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="7c5d2-138">IID</span><span class="sxs-lookup"><span data-stu-id="7c5d2-138">IID</span></span><br/>                      | <span data-ttu-id="7c5d2-139">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="7c5d2-139">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7c5d2-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c5d2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c5d2-141">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="7c5d2-141">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="7c5d2-142">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="7c5d2-142">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="7c5d2-143">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="7c5d2-143">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> </dl>

 

 





