---
title: 'IBackgroundCopyCallback JobModification 方法 (>deliveryoptimization .h) '
description: 傳遞最佳化 (在修改工作時，) 呼叫 JobModification 方法的執行。
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- JobModification 方法
- JobModification 方法，IBackgroundCopyCallback 介面
- IBackgroundCopyCallback 介面，JobModification 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968958"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a><span data-ttu-id="b5527-106">IBackgroundCopyCallback：： JobModification 方法</span><span class="sxs-lookup"><span data-stu-id="b5527-106">IBackgroundCopyCallback::JobModification method</span></span>

<span data-ttu-id="b5527-107">傳遞最佳化 (在修改工作時，) 呼叫 [**JobModification**](https://www.bing.com/search?q=**JobModification**) 方法的執行。</span><span class="sxs-lookup"><span data-stu-id="b5527-107">Delivery Optimization (DO) calls your implementation of the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method when the job has been modified.</span></span> <span data-ttu-id="b5527-108">當傳送位元組、將檔案新增至作業、屬性已修改，或作業狀態已變更時，服務就會產生此事件。</span><span class="sxs-lookup"><span data-stu-id="b5527-108">The service generates this event when bytes are transferred, files have been added to the job, properties have been modified, or the state of the job has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5527-109">語法</span><span class="sxs-lookup"><span data-stu-id="b5527-109">Syntax</span></span>


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="b5527-110">參數</span><span class="sxs-lookup"><span data-stu-id="b5527-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5527-111">*pJob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5527-111">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5527-112">包含存取作業之屬性、進度和狀態資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="b5527-112">Contains the methods for accessing property, progress, and state information of the job.</span></span> <span data-ttu-id="b5527-113">請勿發行 *pJob*;當 [**JobModification**](https://www.bing.com/search?q=**JobModification**) 方法傳回時，請釋放介面。</span><span class="sxs-lookup"><span data-stu-id="b5527-113">Do not release *pJob*; DO releases the interface when the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="b5527-114">*>dwreserved* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5527-114">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5527-115">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="b5527-115">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5527-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5527-116">Return value</span></span>

<span data-ttu-id="b5527-117">這個方法應該會傳回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="b5527-117">This method should return S_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5527-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5527-118">Requirements</span></span>



| <span data-ttu-id="b5527-119">需求</span><span class="sxs-lookup"><span data-stu-id="b5527-119">Requirement</span></span> | <span data-ttu-id="b5527-120">值</span><span class="sxs-lookup"><span data-stu-id="b5527-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5527-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5527-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b5527-122">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5527-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b5527-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5527-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b5527-124">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5527-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b5527-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b5527-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5527-126"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="b5527-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5527-127">Idl</span><span class="sxs-lookup"><span data-stu-id="b5527-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5527-128"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5527-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b5527-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="b5527-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5527-130"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5527-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b5527-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b5527-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5527-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5527-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b5527-133">IID</span><span class="sxs-lookup"><span data-stu-id="b5527-133">IID</span></span><br/>                      | <span data-ttu-id="b5527-134">IID_IBackgroundCopyCallback 定義為97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="b5527-134">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b5527-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5527-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5527-136">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="b5527-136">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="b5527-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="b5527-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





