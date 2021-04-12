---
title: 'IBackgroundCopyCallback JobTransferred 方法 (>deliveryoptimization .h) '
description: 當作業中的所有檔案都已成功傳輸時，傳遞最佳化 () 會呼叫 JobTransferred 方法的執行。
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- JobTransferred 方法
- JobTransferred 方法，IBackgroundCopyCallback 介面
- IBackgroundCopyCallback 介面，JobTransferred 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094463"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a><span data-ttu-id="44d34-106">IBackgroundCopyCallback：： JobTransferred 方法</span><span class="sxs-lookup"><span data-stu-id="44d34-106">IBackgroundCopyCallback::JobTransferred method</span></span>

<span data-ttu-id="44d34-107">當作業中的所有檔案都已成功傳輸時，傳遞最佳化 () 會呼叫 **JobTransferred** 方法的執行。</span><span class="sxs-lookup"><span data-stu-id="44d34-107">Delivery Optimization (DO) calls your implementation of the **JobTransferred** method when all of the files in the job have been successfully transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d34-108">語法</span><span class="sxs-lookup"><span data-stu-id="44d34-108">Syntax</span></span>


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a><span data-ttu-id="44d34-109">參數</span><span class="sxs-lookup"><span data-stu-id="44d34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d34-110">*pJob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44d34-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d34-111">包含作業的相關資訊，例如工作完成時間、傳輸的位元組數，以及傳輸的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="44d34-111">Contains job-related information, such as the time the job completed, the number of bytes transferred, and the number of files transferred.</span></span> <span data-ttu-id="44d34-112">請勿發行 *pJob*;當方法傳回時，請釋放介面。</span><span class="sxs-lookup"><span data-stu-id="44d34-112">Do not release *pJob*; DO releases the interface when the method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d34-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="44d34-113">Return value</span></span>

<span data-ttu-id="44d34-114">這個方法應該會傳回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="44d34-114">This method should return S_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d34-115">備註</span><span class="sxs-lookup"><span data-stu-id="44d34-115">Remarks</span></span>

<span data-ttu-id="44d34-116">一般而言，您的執行應該呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法，以確認已成功傳輸檔案。</span><span class="sxs-lookup"><span data-stu-id="44d34-116">Typically, your implementation should call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that DO successfully transferred the files.</span></span> <span data-ttu-id="44d34-117">除非您呼叫 **Complete** 方法，否則不會在用戶端上提供下載檔案和回復檔案。</span><span class="sxs-lookup"><span data-stu-id="44d34-117">Download files and the reply file are not available on the client until you call the **Complete** method.</span></span>

<span data-ttu-id="44d34-118">如果您未呼叫 [**Complete**](ibackgroundcopyjob-complete.md) 方法，或 [**IBackgroundCopyJob：： Cancel**](ibackgroundcopyjob-cancel.md) 方法在30天后取消作業，並刪除不完整的檔案。</span><span class="sxs-lookup"><span data-stu-id="44d34-118">If you do not call the [**Complete**](ibackgroundcopyjob-complete.md) method or the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method DO cancels the job after 30 days and deletes the incomplete files.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d34-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="44d34-119">Requirements</span></span>



| <span data-ttu-id="44d34-120">需求</span><span class="sxs-lookup"><span data-stu-id="44d34-120">Requirement</span></span> | <span data-ttu-id="44d34-121">值</span><span class="sxs-lookup"><span data-stu-id="44d34-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44d34-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44d34-122">Minimum supported client</span></span><br/> | <span data-ttu-id="44d34-123">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44d34-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="44d34-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44d34-124">Minimum supported server</span></span><br/> | <span data-ttu-id="44d34-125">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44d34-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="44d34-126">標頭</span><span class="sxs-lookup"><span data-stu-id="44d34-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="44d34-127"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="44d34-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="44d34-128">Idl</span><span class="sxs-lookup"><span data-stu-id="44d34-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44d34-129"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="44d34-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="44d34-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="44d34-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="44d34-131"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="44d34-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="44d34-132">DLL</span><span class="sxs-lookup"><span data-stu-id="44d34-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44d34-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44d34-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="44d34-134">IID</span><span class="sxs-lookup"><span data-stu-id="44d34-134">IID</span></span><br/>                      | <span data-ttu-id="44d34-135">IID_IBackgroundCopyCallback 定義為97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="44d34-135">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="44d34-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44d34-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d34-137">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="44d34-137">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="44d34-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="44d34-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="44d34-139">**IBackgroundCopyJob：： Complete**</span><span class="sxs-lookup"><span data-stu-id="44d34-139">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="44d34-140">**IBackgroundCopyJob：： Cancel**</span><span class="sxs-lookup"><span data-stu-id="44d34-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





