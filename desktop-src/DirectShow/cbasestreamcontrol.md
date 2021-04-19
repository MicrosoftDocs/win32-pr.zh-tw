---
description: 這個類別會為輸入和輸出的釘選 IAMStreamControl 介面。
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: 'CBaseStreamControl 類別 (Strmctl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978669"
---
# <a name="cbasestreamcontrol-class"></a><span data-ttu-id="bb95e-103">CBaseStreamControl 類別</span><span class="sxs-lookup"><span data-stu-id="bb95e-103">CBaseStreamControl class</span></span>

![cbasestreamcontrol 類別階層](images/strmctl1.png)

<span data-ttu-id="bb95e-105">這個類別會為輸入和輸出的釘選 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="bb95e-105">This class implements the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface for input and output pins.</span></span> <span data-ttu-id="bb95e-106">它可讓您控制在篩選器上啟動及停止個別的 pin。</span><span class="sxs-lookup"><span data-stu-id="bb95e-106">It provides control over starting and stopping an individual pin on the filter.</span></span> <span data-ttu-id="bb95e-107">支援 **IAMStreamControl** 的 pin 應該繼承自這個基類。</span><span class="sxs-lookup"><span data-stu-id="bb95e-107">A pin that supports **IAMStreamControl** should inherit from this base class.</span></span> <span data-ttu-id="bb95e-108">以下是輸入 pin 的一般宣告：</span><span class="sxs-lookup"><span data-stu-id="bb95e-108">The following is a typical declaration for an input pin:</span></span>

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

<span data-ttu-id="bb95e-109">務必覆寫 **NonDelegatingQueryInteface** 以公開 **IAMStreamControl**。</span><span class="sxs-lookup"><span data-stu-id="bb95e-109">Be sure to override **NonDelegatingQueryInteface** to expose **IAMStreamControl**.</span></span> <span data-ttu-id="bb95e-110">如需詳細資訊，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="bb95e-110">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>



| <span data-ttu-id="bb95e-111">公用方法</span><span class="sxs-lookup"><span data-stu-id="bb95e-111">Public Methods</span></span>                                                        | <span data-ttu-id="bb95e-112">Description</span><span class="sxs-lookup"><span data-stu-id="bb95e-112">Description</span></span>                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb95e-113">**CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="bb95e-113">**CBaseStreamControl**</span></span>](cbasestreamcontrol-cbasestreamcontrol.md)   | <span data-ttu-id="bb95e-114">函式方法。</span><span class="sxs-lookup"><span data-stu-id="bb95e-114">Constructor method.</span></span>                                                                                  |
| [<span data-ttu-id="bb95e-115">**~ CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="bb95e-115">**~CBaseStreamControl**</span></span>](cbasestreamcontrol--cbasestreamcontrol.md) | <span data-ttu-id="bb95e-116">函式方法。</span><span class="sxs-lookup"><span data-stu-id="bb95e-116">Destructor method.</span></span>                                                                                   |
| [<span data-ttu-id="bb95e-117">**CheckStreamState**</span><span class="sxs-lookup"><span data-stu-id="bb95e-117">**CheckStreamState**</span></span>](cbasestreamcontrol-checkstreamstate.md)       | <span data-ttu-id="bb95e-118">決定是否應該傳遞或捨棄媒體範例。</span><span class="sxs-lookup"><span data-stu-id="bb95e-118">Determines whether a media sample should be delivered or discarded.</span></span>                                  |
| [<span data-ttu-id="bb95e-119">**沖洗**</span><span class="sxs-lookup"><span data-stu-id="bb95e-119">**Flushing**</span></span>](cbasestreamcontrol-flushing.md)                       | <span data-ttu-id="bb95e-120">通知基類： pin 已啟動或停止排清。</span><span class="sxs-lookup"><span data-stu-id="bb95e-120">Notifies the base class that the pin has started or stopped flushing.</span></span>                                |
| [<span data-ttu-id="bb95e-121">**NotifyFilterState**</span><span class="sxs-lookup"><span data-stu-id="bb95e-121">**NotifyFilterState**</span></span>](cbasestreamcontrol-notifyfilterstate.md)     | <span data-ttu-id="bb95e-122">當篩選準則的狀態變更時，通知 pin。</span><span class="sxs-lookup"><span data-stu-id="bb95e-122">Notifies the pin when the filter's state changes.</span></span>                                                    |
| [<span data-ttu-id="bb95e-123">**SetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="bb95e-123">**SetFilterGraph**</span></span>](cbasestreamcontrol-setfiltergraph.md)           | <span data-ttu-id="bb95e-124">指定資料流程控制事件的事件接收器。</span><span class="sxs-lookup"><span data-stu-id="bb95e-124">Specifies the event sink for stream control events.</span></span>                                                  |
| [<span data-ttu-id="bb95e-125">**SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="bb95e-125">**SetSyncSource**</span></span>](cbasestreamcontrol-setsyncsource.md)             | <span data-ttu-id="bb95e-126">通知目前參考時鐘的基類。</span><span class="sxs-lookup"><span data-stu-id="bb95e-126">Notifies the base class of the current reference clock.</span></span>                                              |
| <span data-ttu-id="bb95e-127">IAMStreamControl 方法</span><span class="sxs-lookup"><span data-stu-id="bb95e-127">IAMStreamControl Methods</span></span>                                              | <span data-ttu-id="bb95e-128">Description</span><span class="sxs-lookup"><span data-stu-id="bb95e-128">Description</span></span>                                                                                          |
| [<span data-ttu-id="bb95e-129">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="bb95e-129">**GetInfo**</span></span>](cbasestreamcontrol-getinfo.md)                         | <span data-ttu-id="bb95e-130">抓取目前資料流程控制設定的相關資訊，包括開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="bb95e-130">Retrieves information about the current stream-control settings, including the start and stop times.</span></span> |
| [<span data-ttu-id="bb95e-131">**StartAt**</span><span class="sxs-lookup"><span data-stu-id="bb95e-131">**StartAt**</span></span>](cbasestreamcontrol-startat.md)                         | <span data-ttu-id="bb95e-132">通知 pin 何時開始傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="bb95e-132">Informs the pin when to start delivering data.</span></span>                                                       |
| [<span data-ttu-id="bb95e-133">**StopAt**</span><span class="sxs-lookup"><span data-stu-id="bb95e-133">**StopAt**</span></span>](cbasestreamcontrol-stopat.md)                           | <span data-ttu-id="bb95e-134">通知 pin 何時停止傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="bb95e-134">Informs the pin when to stop delivering data.</span></span>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="bb95e-135">備註</span><span class="sxs-lookup"><span data-stu-id="bb95e-135">Remarks</span></span>

<span data-ttu-id="bb95e-136">此類別需要 pin 和擁有篩選準則，以在發生各種事件時通知類別，例如加入圖形或接收新的參考時鐘的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="bb95e-136">This class requires the pin and the owning filter to notify the class when various events occur, such as the filter joining the graph or receiving a new reference clock.</span></span> <span data-ttu-id="bb95e-137">您應該呼叫下列類別方法：</span><span class="sxs-lookup"><span data-stu-id="bb95e-137">You should call the following class methods:</span></span>

-   <span data-ttu-id="bb95e-138">在篩選的 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) 方法中，呼叫 [**CBaseStreamControl：： SetSyncSource**](cbasestreamcontrol-setsyncsource.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bb95e-138">In the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method, call the [**CBaseStreamControl::SetSyncSource**](cbasestreamcontrol-setsyncsource.md) method.</span></span> <span data-ttu-id="bb95e-139">這個方法會通知目前參考時鐘的類別。</span><span class="sxs-lookup"><span data-stu-id="bb95e-139">This method notifies the class of the current reference clock.</span></span>
-   <span data-ttu-id="bb95e-140">在篩選的 [**CBaseFilter：： JoinFilterGraph**](cbasefilter-joinfiltergraph.md) 方法中，呼叫 [**CBaseStreamControl：： SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bb95e-140">In the filter's [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, call the [**CBaseStreamControl::SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) method.</span></span> <span data-ttu-id="bb95e-141">這個方法會為類別提供篩選圖形管理員的指標，讓類別可以傳送正確的資料流程控制事件。</span><span class="sxs-lookup"><span data-stu-id="bb95e-141">This method gives the class a pointer to the Filter Graph Manager, so that the class can send the right stream-control events.</span></span>
-   <span data-ttu-id="bb95e-142">每當篩選變更狀態 (為 [執行中]、[已暫停] 或 [已停止]) 時，請呼叫 [**CBaseStreamControl：： NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bb95e-142">Whenever the filter changes state (to running, paused, or stopped), call the [**CBaseStreamControl::NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) method.</span></span>
-   <span data-ttu-id="bb95e-143">在釘選的 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 和 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法中，呼叫 [**CBaseStreamControl：：**](cbasestreamcontrol-flushing.md) 排清方法。</span><span class="sxs-lookup"><span data-stu-id="bb95e-143">In the pin's [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods, call the [**CBaseStreamControl::Flushing**](cbasestreamcontrol-flushing.md) method.</span></span>

<span data-ttu-id="bb95e-144">`CBaseStreamControl`類別會使用篩選圖形的參考時鐘來決定要傳遞的範例，以及應捨棄的範例。</span><span class="sxs-lookup"><span data-stu-id="bb95e-144">The `CBaseStreamControl` class uses the filter graph's reference clock to determine which samples the filter should be deliver, and which it should discard.</span></span> <span data-ttu-id="bb95e-145">在您的 pin [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法中，以連入媒體範例的指標呼叫 [**CBaseStreamControl：： CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bb95e-145">In your pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, call the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method with a pointer to the incoming media sample.</span></span> <span data-ttu-id="bb95e-146">如果方法傳回資料流程 \_ 流動值，請傳遞範例下游。</span><span class="sxs-lookup"><span data-stu-id="bb95e-146">If the method returns the value STREAM\_FLOWING, deliver the sample downstream.</span></span> <span data-ttu-id="bb95e-147">否則，請捨棄它。</span><span class="sxs-lookup"><span data-stu-id="bb95e-147">Otherwise, discard it.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb95e-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb95e-148">Requirements</span></span>



| <span data-ttu-id="bb95e-149">需求</span><span class="sxs-lookup"><span data-stu-id="bb95e-149">Requirement</span></span> | <span data-ttu-id="bb95e-150">值</span><span class="sxs-lookup"><span data-stu-id="bb95e-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb95e-151">標頭</span><span class="sxs-lookup"><span data-stu-id="bb95e-151">Header</span></span><br/>  | <dl> <span data-ttu-id="bb95e-152"><dt>Strmctl (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bb95e-152"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bb95e-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="bb95e-153">Library</span></span><br/> | <dl> <span data-ttu-id="bb95e-154"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bb95e-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




