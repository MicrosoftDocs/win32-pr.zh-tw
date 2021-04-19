---
description: Receive 方法會接收資料流程中的下一個媒體範例。
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: 'CBaseRenderer 的 Receive 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983256"
---
# <a name="cbaserendererreceive-method"></a><span data-ttu-id="70f91-103">CBaseRenderer 接收方法</span><span class="sxs-lookup"><span data-stu-id="70f91-103">CBaseRenderer.Receive method</span></span>

<span data-ttu-id="70f91-104">`Receive`方法會接收資料流程中的下一個媒體範例。</span><span class="sxs-lookup"><span data-stu-id="70f91-104">The `Receive` method receives the next media sample in the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="70f91-105">語法</span><span class="sxs-lookup"><span data-stu-id="70f91-105">Syntax</span></span>


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="70f91-106">參數</span><span class="sxs-lookup"><span data-stu-id="70f91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70f91-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="70f91-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="70f91-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="70f91-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70f91-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="70f91-109">Return value</span></span>

<span data-ttu-id="70f91-110">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="70f91-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="70f91-111">備註</span><span class="sxs-lookup"><span data-stu-id="70f91-111">Remarks</span></span>

<span data-ttu-id="70f91-112">輸入 pin 會在從上游篩選器收到範例時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="70f91-112">The input pin calls this method when it receives a sample from the upstream filter.</span></span>

<span data-ttu-id="70f91-113">如果篩選器正在執行，這個方法會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="70f91-113">If the filter is running, this method performs the following steps:</span></span>

1.  <span data-ttu-id="70f91-114">排定轉譯 ([**CBaseRenderer：:P reparereceive**](cbaserenderer-preparereceive.md)) 的範例。</span><span class="sxs-lookup"><span data-stu-id="70f91-114">Schedules the sample for rendering ([**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md)).</span></span>
2.  <span data-ttu-id="70f91-115">等候排程的時間 ([**CBaseRenderer：： WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) 。</span><span class="sxs-lookup"><span data-stu-id="70f91-115">Waits for the scheduled time ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span></span>
3.  <span data-ttu-id="70f91-116">轉譯 ([**CBaseRenderer：： Render**](cbaserenderer-render.md)) 的範例。</span><span class="sxs-lookup"><span data-stu-id="70f91-116">Renders the sample ([**CBaseRenderer::Render**](cbaserenderer-render.md)).</span></span>
4.  <span data-ttu-id="70f91-117">釋放範例 ([**CBaseRenderer：： ClearPendingSample**](cbaserenderer-clearpendingsample.md)) 。</span><span class="sxs-lookup"><span data-stu-id="70f91-117">Releases the sample ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span></span>

<span data-ttu-id="70f91-118">如果已暫停篩選，則方法會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="70f91-118">If the filter is paused, the method performs the following steps:</span></span>

1.  <span data-ttu-id="70f91-119">通知衍生類別 ([**CBaseRenderer：： OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)) 提供範例。</span><span class="sxs-lookup"><span data-stu-id="70f91-119">Notifies the derived class that a sample is available ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span></span>
2.  <span data-ttu-id="70f91-120">等候排程的時間。</span><span class="sxs-lookup"><span data-stu-id="70f91-120">Waits for the scheduled time.</span></span>
3.  <span data-ttu-id="70f91-121">呈現範例。</span><span class="sxs-lookup"><span data-stu-id="70f91-121">Renders the sample.</span></span>
4.  <span data-ttu-id="70f91-122">釋放範例。</span><span class="sxs-lookup"><span data-stu-id="70f91-122">Releases the sample.</span></span>

<span data-ttu-id="70f91-123">暫停時，方法會在步驟2中等候，直到篩選切換到執行中狀態。</span><span class="sxs-lookup"><span data-stu-id="70f91-123">While paused, the method waits in step 2 until the filter switches to a running state.</span></span> <span data-ttu-id="70f91-124">在該時間點，篩選會排定範例。</span><span class="sxs-lookup"><span data-stu-id="70f91-124">At that point, the filter schedules the sample.</span></span>

<span data-ttu-id="70f91-125">在基類中， **OnReceiveFirstSample** 方法不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="70f91-125">In the base class, the **OnReceiveFirstSample** method does nothing.</span></span> <span data-ttu-id="70f91-126">衍生的類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="70f91-126">The derived class can override it.</span></span> <span data-ttu-id="70f91-127">例如，當影片轉譯器暫停時，會將第一個範例顯示為靜止影像。</span><span class="sxs-lookup"><span data-stu-id="70f91-127">For example, when a video renderer is paused, it displays the first sample as a still image.</span></span>

## <a name="requirements"></a><span data-ttu-id="70f91-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="70f91-128">Requirements</span></span>



| <span data-ttu-id="70f91-129">需求</span><span class="sxs-lookup"><span data-stu-id="70f91-129">Requirement</span></span> | <span data-ttu-id="70f91-130">值</span><span class="sxs-lookup"><span data-stu-id="70f91-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f91-131">標頭</span><span class="sxs-lookup"><span data-stu-id="70f91-131">Header</span></span><br/>  | <dl> <span data-ttu-id="70f91-132"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="70f91-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="70f91-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="70f91-133">Library</span></span><br/> | <dl> <span data-ttu-id="70f91-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="70f91-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70f91-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70f91-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70f91-136">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="70f91-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




