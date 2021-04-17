---
title: 'IBackgroundCopyJob GetTimes 方法 (>deliveryoptimization .h) '
description: 抓取作業相關的時間戳記，例如作業的建立時間或上次修改時間。
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- GetTimes 方法
- GetTimes 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetTimes 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04e779b59e0976e77b287bc575f3b08f8d39340a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465517"
---
# <a name="ibackgroundcopyjobgettimes-method"></a><span data-ttu-id="e6462-106">IBackgroundCopyJob：： GetTimes 方法</span><span class="sxs-lookup"><span data-stu-id="e6462-106">IBackgroundCopyJob::GetTimes method</span></span>

<span data-ttu-id="e6462-107">抓取作業相關的時間戳記，例如作業的建立時間或上次修改時間。</span><span class="sxs-lookup"><span data-stu-id="e6462-107">Retrieves job-related time stamps, such as the time that the job was created or last modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6462-108">語法</span><span class="sxs-lookup"><span data-stu-id="e6462-108">Syntax</span></span>


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a><span data-ttu-id="e6462-109">參數</span><span class="sxs-lookup"><span data-stu-id="e6462-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6462-110">*pTimes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e6462-110">*pTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6462-111">包含作業相關的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e6462-111">Contains job-related time stamps.</span></span> <span data-ttu-id="e6462-112">如需可用的時間戳記，請參閱 [**BG_JOB_TIMES**](bg-job-times.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="e6462-112">For available time stamps, see the [**BG_JOB_TIMES**](bg-job-times.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6462-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6462-113">Return value</span></span>

<span data-ttu-id="e6462-114">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="e6462-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="e6462-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e6462-115">Return code</span></span>                                                                              | <span data-ttu-id="e6462-116">Description</span><span class="sxs-lookup"><span data-stu-id="e6462-116">Description</span></span>                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="e6462-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e6462-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="e6462-118">已成功取出時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e6462-118">Time stamps were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e6462-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6462-119">Requirements</span></span>



| <span data-ttu-id="e6462-120">需求</span><span class="sxs-lookup"><span data-stu-id="e6462-120">Requirement</span></span> | <span data-ttu-id="e6462-121">值</span><span class="sxs-lookup"><span data-stu-id="e6462-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6462-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6462-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e6462-123">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6462-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e6462-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6462-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e6462-125">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6462-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e6462-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e6462-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6462-127"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6462-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6462-128">Idl</span><span class="sxs-lookup"><span data-stu-id="e6462-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e6462-129"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6462-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e6462-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="e6462-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6462-131"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6462-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e6462-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e6462-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6462-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6462-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e6462-134">IID</span><span class="sxs-lookup"><span data-stu-id="e6462-134">IID</span></span><br/>                      | <span data-ttu-id="e6462-135">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="e6462-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e6462-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6462-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6462-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="e6462-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="e6462-138">**BG_JOB_TIMES**</span><span class="sxs-lookup"><span data-stu-id="e6462-138">**BG_JOB_TIMES**</span></span>](bg-job-times.md)
</dt> </dl>

 

 





