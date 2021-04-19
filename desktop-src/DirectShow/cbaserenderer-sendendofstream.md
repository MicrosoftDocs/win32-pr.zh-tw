---
description: 如果已到達資料流程結尾，SendEndOfStream 方法會 \_ 為篩選圖形管理員排程 EC 完成事件。
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: 'CBaseRenderer. SendEndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998760"
---
# <a name="cbaserenderersendendofstream-method"></a><span data-ttu-id="38fac-103">CBaseRenderer. SendEndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="38fac-103">CBaseRenderer.SendEndOfStream method</span></span>

<span data-ttu-id="38fac-104">如果已到達資料流程結尾，則方法會排程 `SendEndOfStream` \_ 篩選圖形管理員的 EC 完成事件。</span><span class="sxs-lookup"><span data-stu-id="38fac-104">If end-of-stream was reached, the `SendEndOfStream` method schedules an EC\_COMPLETE event for the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="38fac-105">語法</span><span class="sxs-lookup"><span data-stu-id="38fac-105">Syntax</span></span>


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="38fac-106">參數</span><span class="sxs-lookup"><span data-stu-id="38fac-106">Parameters</span></span>

<span data-ttu-id="38fac-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="38fac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38fac-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="38fac-108">Return value</span></span>

<span data-ttu-id="38fac-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="38fac-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="38fac-110">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="38fac-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="38fac-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="38fac-111">Return code</span></span>                                                                             | <span data-ttu-id="38fac-112">Description</span><span class="sxs-lookup"><span data-stu-id="38fac-112">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38fac-113"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="38fac-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="38fac-114">篩選圖形管理員不接受事件通知。</span><span class="sxs-lookup"><span data-stu-id="38fac-114">The filter graph manager is not accepting event notifications.</span></span><br/> |
| <dl> <span data-ttu-id="38fac-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="38fac-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="38fac-116">成功。</span><span class="sxs-lookup"><span data-stu-id="38fac-116">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="38fac-117">備註</span><span class="sxs-lookup"><span data-stu-id="38fac-117">Remarks</span></span>

<span data-ttu-id="38fac-118">篩選可能會在目前範例的停止時間之前接收資料流程結束通知。</span><span class="sxs-lookup"><span data-stu-id="38fac-118">The filter might receive an end-of-stream notification before the current sample's stop time.</span></span> <span data-ttu-id="38fac-119">如果是這樣，篩選器應該在將 [**EC \_ 完成**](ec-complete.md) 通知張貼至篩選圖形管理員之前等候。</span><span class="sxs-lookup"><span data-stu-id="38fac-119">If so, the filter should wait before posting an [**EC\_COMPLETE**](ec-complete.md) notification to the filter graph manager.</span></span>

<span data-ttu-id="38fac-120">因此：</span><span class="sxs-lookup"><span data-stu-id="38fac-120">Therefore:</span></span>

-   <span data-ttu-id="38fac-121">如果篩選已收到早期的資料流程結尾 (EOS) 通知，這個方法會排定計時器事件。</span><span class="sxs-lookup"><span data-stu-id="38fac-121">If the filter has received an early end-of-stream (EOS) notification, this method schedules a timer event.</span></span> <span data-ttu-id="38fac-122">當計時器事件啟動時，篩選會張貼 EC \_ COMPLETE 事件。</span><span class="sxs-lookup"><span data-stu-id="38fac-122">When the timer event is activated, the filter posts the EC\_COMPLETE event.</span></span>
-   <span data-ttu-id="38fac-123">如果篩選器收到非早期的 EOS 通知，這個方法會立即張貼 EC \_ 完成事件。</span><span class="sxs-lookup"><span data-stu-id="38fac-123">If the filter has received an EOS notification that was not early, this method posts the EC\_COMPLETE event immediately.</span></span>
-   <span data-ttu-id="38fac-124">如果篩選沒有任何擱置中的 EOS 通知，則方法會傳回而不會執行任何作業。</span><span class="sxs-lookup"><span data-stu-id="38fac-124">If the filter does not have any pending EOS notification, the method returns without doing anything.</span></span>

<span data-ttu-id="38fac-125">計時器回呼方法是 [**CBaseRenderer：： TimerCallback**](cbaserenderer-timercallback.md)。</span><span class="sxs-lookup"><span data-stu-id="38fac-125">The timer callback method is [**CBaseRenderer::TimerCallback**](cbaserenderer-timercallback.md).</span></span> <span data-ttu-id="38fac-126">為了傳遞 EC \_ COMPLETE 事件，篩選準則會呼叫 [**CBaseRenderer：： NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="38fac-126">To deliver the EC\_COMPLETE event, the filter calls the [**CBaseRenderer::NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="38fac-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="38fac-127">Requirements</span></span>



| <span data-ttu-id="38fac-128">需求</span><span class="sxs-lookup"><span data-stu-id="38fac-128">Requirement</span></span> | <span data-ttu-id="38fac-129">值</span><span class="sxs-lookup"><span data-stu-id="38fac-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38fac-130">標頭</span><span class="sxs-lookup"><span data-stu-id="38fac-130">Header</span></span><br/>  | <dl> <span data-ttu-id="38fac-131"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="38fac-131"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="38fac-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="38fac-132">Library</span></span><br/> | <dl> <span data-ttu-id="38fac-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="38fac-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38fac-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38fac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38fac-135">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="38fac-135">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




