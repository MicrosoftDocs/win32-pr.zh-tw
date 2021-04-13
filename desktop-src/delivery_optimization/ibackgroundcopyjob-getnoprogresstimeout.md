---
title: 'IBackgroundCopyJob GetNoProgressTimeout 方法 (>deliveryoptimization .h) '
description: 抓取在暫時性錯誤狀況發生之後，服務嘗試傳送檔案的時間長度。 如果有進度，則會重設計時器。
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- GetNoProgressTimeout 方法
- GetNoProgressTimeout 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetNoProgressTimeout 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ccd236c17612aa03a28e07a08d087454f8db6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465520"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a><span data-ttu-id="06014-107">IBackgroundCopyJob：： GetNoProgressTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="06014-107">IBackgroundCopyJob::GetNoProgressTimeout method</span></span>

<span data-ttu-id="06014-108">抓取在暫時性錯誤狀況發生之後，服務嘗試傳送檔案的時間長度。</span><span class="sxs-lookup"><span data-stu-id="06014-108">Retrieves the length of time that the service tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="06014-109">如果有進度，則會重設計時器。</span><span class="sxs-lookup"><span data-stu-id="06014-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="06014-110">語法</span><span class="sxs-lookup"><span data-stu-id="06014-110">Syntax</span></span>


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="06014-111">參數</span><span class="sxs-lookup"><span data-stu-id="06014-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06014-112">*pRetryPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06014-112">*pRetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06014-113">發生暫時性錯誤之後，服務嘗試傳送檔案的時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="06014-113">Length of time, in seconds, that the service tries to transfer the file after a transient error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06014-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="06014-114">Return value</span></span>

<span data-ttu-id="06014-115">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="06014-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="06014-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="06014-116">Return code</span></span>                                                                              | <span data-ttu-id="06014-117">Description</span><span class="sxs-lookup"><span data-stu-id="06014-117">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="06014-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="06014-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="06014-119">已成功取出超時時間。</span><span class="sxs-lookup"><span data-stu-id="06014-119">Time-out was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="06014-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="06014-120">Requirements</span></span>



| <span data-ttu-id="06014-121">需求</span><span class="sxs-lookup"><span data-stu-id="06014-121">Requirement</span></span> | <span data-ttu-id="06014-122">值</span><span class="sxs-lookup"><span data-stu-id="06014-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06014-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06014-123">Minimum supported client</span></span><br/> | <span data-ttu-id="06014-124">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06014-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06014-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06014-125">Minimum supported server</span></span><br/> | <span data-ttu-id="06014-126">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06014-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="06014-127">標頭</span><span class="sxs-lookup"><span data-stu-id="06014-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="06014-128"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="06014-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="06014-129">Idl</span><span class="sxs-lookup"><span data-stu-id="06014-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06014-130"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="06014-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="06014-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="06014-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="06014-132"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="06014-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="06014-133">DLL</span><span class="sxs-lookup"><span data-stu-id="06014-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06014-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06014-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="06014-135">IID</span><span class="sxs-lookup"><span data-stu-id="06014-135">IID</span></span><br/>                      | <span data-ttu-id="06014-136">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="06014-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="06014-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06014-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06014-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="06014-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="06014-139">**IBackgroundCopyJob::SetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="06014-139">**IBackgroundCopyJob::SetNoProgressTimeout**</span></span>](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





