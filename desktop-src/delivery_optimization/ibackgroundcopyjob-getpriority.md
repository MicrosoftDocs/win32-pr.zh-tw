---
title: 'IBackgroundCopyJob GetPriority 方法 (>deliveryoptimization .h) '
description: 抓取作業的優先權層級。 優先權層級會決定作業的處理方式相對於傳送佇列中的其他作業。
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- GetPriority 方法
- GetPriority 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetPriority 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967970"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a><span data-ttu-id="a2d85-107">IBackgroundCopyJob：： GetPriority 方法</span><span class="sxs-lookup"><span data-stu-id="a2d85-107">IBackgroundCopyJob::GetPriority method</span></span>

<span data-ttu-id="a2d85-108">抓取作業的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="a2d85-108">Retrieves the priority level for the job.</span></span> <span data-ttu-id="a2d85-109">優先權層級會決定作業的處理方式相對於傳送佇列中的其他作業。</span><span class="sxs-lookup"><span data-stu-id="a2d85-109">The priority level determines when the job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d85-110">語法</span><span class="sxs-lookup"><span data-stu-id="a2d85-110">Syntax</span></span>


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="a2d85-111">參數</span><span class="sxs-lookup"><span data-stu-id="a2d85-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2d85-112">*pPriority* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a2d85-112">*pPriority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2d85-113">相對於傳送佇列中其他作業的作業優先順序。</span><span class="sxs-lookup"><span data-stu-id="a2d85-113">Priority of the job relative to other jobs in the transfer queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2d85-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2d85-114">Return value</span></span>

<span data-ttu-id="a2d85-115">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="a2d85-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="a2d85-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a2d85-116">Return code</span></span>                                                                              | <span data-ttu-id="a2d85-117">Description</span><span class="sxs-lookup"><span data-stu-id="a2d85-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="a2d85-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a2d85-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="a2d85-119">已成功抓取優先權層級。</span><span class="sxs-lookup"><span data-stu-id="a2d85-119">Priority level was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a2d85-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2d85-120">Requirements</span></span>



| <span data-ttu-id="a2d85-121">需求</span><span class="sxs-lookup"><span data-stu-id="a2d85-121">Requirement</span></span> | <span data-ttu-id="a2d85-122">值</span><span class="sxs-lookup"><span data-stu-id="a2d85-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d85-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2d85-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2d85-124">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2d85-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a2d85-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2d85-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2d85-126">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2d85-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a2d85-127">標頭</span><span class="sxs-lookup"><span data-stu-id="a2d85-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2d85-128"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2d85-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2d85-129">Idl</span><span class="sxs-lookup"><span data-stu-id="a2d85-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2d85-130"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2d85-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a2d85-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2d85-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2d85-132"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2d85-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a2d85-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a2d85-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2d85-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2d85-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a2d85-135">IID</span><span class="sxs-lookup"><span data-stu-id="a2d85-135">IID</span></span><br/>                      | <span data-ttu-id="a2d85-136">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="a2d85-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a2d85-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2d85-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d85-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="a2d85-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="a2d85-139">**IBackgroundCopyJob：： SetPriority**</span><span class="sxs-lookup"><span data-stu-id="a2d85-139">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





