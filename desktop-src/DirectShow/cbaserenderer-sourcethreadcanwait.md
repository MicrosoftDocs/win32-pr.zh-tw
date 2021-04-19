---
description: SourceThreadCanWait 方法會保存或釋放串流執行緒。
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: 'CBaseRenderer. SourceThreadCanWait 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001203"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a><span data-ttu-id="055a4-103">CBaseRenderer. SourceThreadCanWait 方法</span><span class="sxs-lookup"><span data-stu-id="055a4-103">CBaseRenderer.SourceThreadCanWait method</span></span>

<span data-ttu-id="055a4-104">`SourceThreadCanWait`方法會保存或釋放串流執行緒。</span><span class="sxs-lookup"><span data-stu-id="055a4-104">The `SourceThreadCanWait` method holds or releases the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="055a4-105">語法</span><span class="sxs-lookup"><span data-stu-id="055a4-105">Syntax</span></span>


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a><span data-ttu-id="055a4-106">參數</span><span class="sxs-lookup"><span data-stu-id="055a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="055a4-107">*bCanWait*</span><span class="sxs-lookup"><span data-stu-id="055a4-107">*bCanWait*</span></span> 
</dt> <dd>

<span data-ttu-id="055a4-108">指出是否要保存串流執行緒的布林值。</span><span class="sxs-lookup"><span data-stu-id="055a4-108">Boolean value indicating whether to hold the streaming thread.</span></span> <span data-ttu-id="055a4-109">若 **為 TRUE**，則會在篩選等候轉譯下一個範例時封鎖串流執行緒。</span><span class="sxs-lookup"><span data-stu-id="055a4-109">If **TRUE**, the streaming thread is blocked while the filter waits to render the next samples.</span></span> <span data-ttu-id="055a4-110">如果 **為 FALSE**，則會釋放串流處理執行緒。</span><span class="sxs-lookup"><span data-stu-id="055a4-110">If **FALSE**, the streaming thread is released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="055a4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="055a4-111">Return value</span></span>

<span data-ttu-id="055a4-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="055a4-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="055a4-113">備註</span><span class="sxs-lookup"><span data-stu-id="055a4-113">Remarks</span></span>

<span data-ttu-id="055a4-114">`SourceThreadCanWait`使用值 **FALSE** 來呼叫方法，會強制篩選從封鎖的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="055a4-114">Calling the `SourceThreadCanWait` method with the value **FALSE** forces the filter to return from a blocked [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call.</span></span> <span data-ttu-id="055a4-115">當篩選準則正在執行時，它會封鎖 **接收** 呼叫，直到目前樣本的呈現時間為止。</span><span class="sxs-lookup"><span data-stu-id="055a4-115">When the filter is running, it blocks **Receive** calls until the current sample's presentation time.</span></span> <span data-ttu-id="055a4-116">當篩選暫停時，它會無限期地封鎖 **接收** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="055a4-116">When the filter is paused, it blocks **Receive** calls indefinitely.</span></span> <span data-ttu-id="055a4-117">此行為會控制資料流程中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="055a4-117">This behavior regulates the flow of data in the stream.</span></span> <span data-ttu-id="055a4-118">不過，當篩選準則停止或清除時，不應封鎖。</span><span class="sxs-lookup"><span data-stu-id="055a4-118">When the filter is stopped or flushing, however, it should not block.</span></span>

<span data-ttu-id="055a4-119">封鎖是由 [**CBaseRenderer：： WaitForRenderTime**](cbaserenderer-waitforrendertime.md) 方法所控制，它會等候兩個事件： [**CBaseRenderer：： m \_ RenderEvent**](cbaserenderer-m-renderevent.md) 和 [**CBaseRenderer：： m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md)。</span><span class="sxs-lookup"><span data-stu-id="055a4-119">The blocking is controlled by the [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method, which waits on two events: [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) and [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md).</span></span> <span data-ttu-id="055a4-120">當呈現時間到達時， **m \_ RenderEvent** 事件就會收到信號。</span><span class="sxs-lookup"><span data-stu-id="055a4-120">The **m\_RenderEvent** event is signaled when the presentation time arrives.</span></span> <span data-ttu-id="055a4-121">以 FALSE 值呼叫時，會發出 **m \_ ThreadSignal** 事件的信號 `SourceThreadCanWait` 。 </span><span class="sxs-lookup"><span data-stu-id="055a4-121">The **m\_ThreadSignal** event is signaled when `SourceThreadCanWait` is called with the value **FALSE**.</span></span> <span data-ttu-id="055a4-122">`SourceThreadCanWait`使用值 **TRUE** 來呼叫會重設事件。</span><span class="sxs-lookup"><span data-stu-id="055a4-122">Calling `SourceThreadCanWait` with the value **TRUE** resets the event.</span></span>

<span data-ttu-id="055a4-123">[**CBaseRenderer：： Stop**](cbaserenderer-stop.md)和 [**CBaseRenderer：： BeginFlush**](cbaserenderer-beginflush.md)方法呼叫 `SourceThreadCanWait` 值 **為 FALSE** (釋放串流執行緒) 。</span><span class="sxs-lookup"><span data-stu-id="055a4-123">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call `SourceThreadCanWait` with the value **FALSE** (releasing the streaming thread).</span></span> <span data-ttu-id="055a4-124">[**CBaseRenderer：:P ause**](cbaserenderer-pause.md)、 [**CBaseRenderer：： Run**](cbaserenderer-run.md)和 [**CBaseRenderer：： EndFlush**](cbaserenderer-endflush.md)方法會 `SourceThreadCanWait` 使用值 **TRUE** 來呼叫。</span><span class="sxs-lookup"><span data-stu-id="055a4-124">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md), [**CBaseRenderer::Run**](cbaserenderer-run.md), and [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) methods call `SourceThreadCanWait` with the value **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="055a4-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="055a4-125">Requirements</span></span>



| <span data-ttu-id="055a4-126">需求</span><span class="sxs-lookup"><span data-stu-id="055a4-126">Requirement</span></span> | <span data-ttu-id="055a4-127">值</span><span class="sxs-lookup"><span data-stu-id="055a4-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="055a4-128">標頭</span><span class="sxs-lookup"><span data-stu-id="055a4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="055a4-129"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="055a4-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="055a4-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="055a4-130">Library</span></span><br/> | <dl> <span data-ttu-id="055a4-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="055a4-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="055a4-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="055a4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="055a4-133">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="055a4-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




