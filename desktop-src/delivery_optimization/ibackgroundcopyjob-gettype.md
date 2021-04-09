---
title: 'IBackgroundCopyJob GetType 方法 (>deliveryoptimization .h) '
description: 抓取正在執行的傳輸類型，例如檔案下載或上傳。
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- GetType 方法
- GetType 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetType 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024741"
---
# <a name="ibackgroundcopyjobgettype-method"></a><span data-ttu-id="c255a-106">IBackgroundCopyJob：： GetType 方法</span><span class="sxs-lookup"><span data-stu-id="c255a-106">IBackgroundCopyJob::GetType method</span></span>

<span data-ttu-id="c255a-107">抓取正在執行的傳輸類型，例如檔案下載或上傳。</span><span class="sxs-lookup"><span data-stu-id="c255a-107">Retrieves the type of transfer being performed, such as a file download or upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="c255a-108">語法</span><span class="sxs-lookup"><span data-stu-id="c255a-108">Syntax</span></span>


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a><span data-ttu-id="c255a-109">參數</span><span class="sxs-lookup"><span data-stu-id="c255a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c255a-110">*pJobType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c255a-110">*pJobType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c255a-111">要執行的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="c255a-111">Type of transfer being performed.</span></span> <span data-ttu-id="c255a-112">如需傳輸類型的清單，請參閱 [**BG_JOB_TYPE**](bg-job-type.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="c255a-112">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c255a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c255a-113">Return value</span></span>

<span data-ttu-id="c255a-114">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="c255a-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="c255a-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c255a-115">Return code</span></span>                                                                              | <span data-ttu-id="c255a-116">Description</span><span class="sxs-lookup"><span data-stu-id="c255a-116">Description</span></span>                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="c255a-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="c255a-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="c255a-118">已成功取出傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="c255a-118">Transfer type was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c255a-119">備註</span><span class="sxs-lookup"><span data-stu-id="c255a-119">Remarks</span></span>

<span data-ttu-id="c255a-120">指定建立作業時的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="c255a-120">Specify the type of transfer when you create the job.</span></span>

## <a name="requirements"></a><span data-ttu-id="c255a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c255a-121">Requirements</span></span>



| <span data-ttu-id="c255a-122">需求</span><span class="sxs-lookup"><span data-stu-id="c255a-122">Requirement</span></span> | <span data-ttu-id="c255a-123">值</span><span class="sxs-lookup"><span data-stu-id="c255a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c255a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c255a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c255a-125">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c255a-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c255a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c255a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c255a-127">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c255a-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c255a-128">標頭</span><span class="sxs-lookup"><span data-stu-id="c255a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c255a-129"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="c255a-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c255a-130">Idl</span><span class="sxs-lookup"><span data-stu-id="c255a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c255a-131"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c255a-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c255a-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="c255a-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="c255a-133"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c255a-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c255a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c255a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c255a-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c255a-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c255a-136">IID</span><span class="sxs-lookup"><span data-stu-id="c255a-136">IID</span></span><br/>                      | <span data-ttu-id="c255a-137">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="c255a-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c255a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c255a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c255a-139">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="c255a-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="c255a-140">**BG_JOB_TYPE**</span><span class="sxs-lookup"><span data-stu-id="c255a-140">**BG_JOB_TYPE**</span></span>](bg-job-type.md)
</dt> <dt>

[<span data-ttu-id="c255a-141">**IBackgroundCopyManager：： >batchclient.joboperations.createjob**</span><span class="sxs-lookup"><span data-stu-id="c255a-141">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





