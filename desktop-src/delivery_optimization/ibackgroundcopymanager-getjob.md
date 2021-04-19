---
title: 'IBackgroundCopyManager GetJob 方法 (>deliveryoptimization .h) '
description: 從傳送佇列中抓取指定的工作。 一般來說，您的應用程式會保存工作識別碼，讓您稍後可以從佇列中取得工作。
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- GetJob 方法
- GetJob 方法，IBackgroundCopyManager 介面
- IBackgroundCopyManager 介面，GetJob 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a59956e68b5b656e7182e62969b3212c2ef6732c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965090"
---
# <a name="ibackgroundcopymanagergetjob-method"></a><span data-ttu-id="8f902-107">IBackgroundCopyManager：： GetJob 方法</span><span class="sxs-lookup"><span data-stu-id="8f902-107">IBackgroundCopyManager::GetJob method</span></span>

<span data-ttu-id="8f902-108">從傳送佇列中抓取指定的工作。</span><span class="sxs-lookup"><span data-stu-id="8f902-108">Retrieves a specified job from the transfer queue.</span></span> <span data-ttu-id="8f902-109">一般來說，您的應用程式會保存工作識別碼，讓您稍後可以從佇列中取得工作。</span><span class="sxs-lookup"><span data-stu-id="8f902-109">Typically, your application persists the job identifier, so you can later retrieve the job from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f902-110">語法</span><span class="sxs-lookup"><span data-stu-id="8f902-110">Syntax</span></span>


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="8f902-111">參數</span><span class="sxs-lookup"><span data-stu-id="8f902-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f902-112">*JobID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f902-112">*JobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f902-113">識別要從傳送佇列中取出的作業。</span><span class="sxs-lookup"><span data-stu-id="8f902-113">Identifies the job to retrieve from the transfer queue.</span></span> <span data-ttu-id="8f902-114">[**>batchclient.joboperations.createjob**](ibackgroundcopymanager-createjob.md)方法會傳回作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f902-114">The [**CreateJob**](ibackgroundcopymanager-createjob.md) method returns the job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8f902-115">*ppJob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f902-115">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f902-116">*JobID* 所指定之作業的 [**IBackgroundCopyJob**](ibackgroundcopyjob-.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="8f902-116">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer to the job specified by *JobID*.</span></span> <span data-ttu-id="8f902-117">完成時，發行 *ppJob*。</span><span class="sxs-lookup"><span data-stu-id="8f902-117">When done, release *ppJob*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f902-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f902-118">Return value</span></span>

<span data-ttu-id="8f902-119">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="8f902-119">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="8f902-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8f902-120">Return code</span></span>                                                                                      | <span data-ttu-id="8f902-121">Description</span><span class="sxs-lookup"><span data-stu-id="8f902-121">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f902-122"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="8f902-122"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>         | <span data-ttu-id="8f902-123">已成功從傳送佇列中取出作業。</span><span class="sxs-lookup"><span data-stu-id="8f902-123">Job was successfully retrieved from the transfer queue.</span></span><br/> |
| <dl> <span data-ttu-id="8f902-124"><dt>**DO_E_NOT_FOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="8f902-124"><dt>**DO_E_NOT_FOUND**</dt></span></span> </dl> | <span data-ttu-id="8f902-125">在佇列中找不到作業。</span><span class="sxs-lookup"><span data-stu-id="8f902-125">The job was not found in the queue.</span></span><br/>                     |
| <dl> <span data-ttu-id="8f902-126"><dt>**E_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8f902-126"><dt>**E_ACCESSDENIED**</dt></span></span> </dl>   | <span data-ttu-id="8f902-127">使用者沒有取得工作的許可權。</span><span class="sxs-lookup"><span data-stu-id="8f902-127">User does not have permission to retrieve the job.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="8f902-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f902-128">Requirements</span></span>



| <span data-ttu-id="8f902-129">需求</span><span class="sxs-lookup"><span data-stu-id="8f902-129">Requirement</span></span> | <span data-ttu-id="8f902-130">值</span><span class="sxs-lookup"><span data-stu-id="8f902-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f902-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f902-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8f902-132">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f902-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8f902-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f902-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8f902-134">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f902-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8f902-135">標頭</span><span class="sxs-lookup"><span data-stu-id="8f902-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f902-136"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f902-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f902-137">Idl</span><span class="sxs-lookup"><span data-stu-id="8f902-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8f902-138"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f902-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="8f902-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="8f902-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f902-140"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f902-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="8f902-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8f902-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f902-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f902-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="8f902-143">IID</span><span class="sxs-lookup"><span data-stu-id="8f902-143">IID</span></span><br/>                      | <span data-ttu-id="8f902-144">IID_IBackgroundCopyManager 定義為5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="8f902-144">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8f902-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f902-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f902-146">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="8f902-146">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="8f902-147">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="8f902-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="8f902-148">**IBackgroundCopyJob：： GetId**</span><span class="sxs-lookup"><span data-stu-id="8f902-148">**IBackgroundCopyJob::GetId**</span></span>](ibackgroundcopyjob-getid.md)
</dt> <dt>

[<span data-ttu-id="8f902-149">**IBackgroundCopyManager：： >batchclient.joboperations.createjob**</span><span class="sxs-lookup"><span data-stu-id="8f902-149">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





