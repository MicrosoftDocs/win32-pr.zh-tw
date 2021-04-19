---
description: CBaseOutputPin 類別是一種抽象基類，可實作為輸出的釘選。
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: 'CBaseOutputPin 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993446"
---
# <a name="cbaseoutputpin-class"></a><span data-ttu-id="b2b6b-103">CBaseOutputPin 類別</span><span class="sxs-lookup"><span data-stu-id="b2b6b-103">CBaseOutputPin class</span></span>

![cbaseoutputpin 類別階層](images/filter06.png)

<span data-ttu-id="b2b6b-105">`CBaseOutputPin`類別是一種抽象基類，可實作為輸出的釘選。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-105">The `CBaseOutputPin` class is an abstract base class that implements an output pin.</span></span>

<span data-ttu-id="b2b6b-106">這個類別衍生自 [**CBasePin**](cbasepin.md)。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-106">This class derives from [**CBasePin**](cbasepin.md).</span></span> <span data-ttu-id="b2b6b-107">這與 **CBasePin** 的差異在於下列各方面：</span><span class="sxs-lookup"><span data-stu-id="b2b6b-107">It differs from **CBasePin** in the following respects:</span></span>

-   <span data-ttu-id="b2b6b-108">它只會連線到支援 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-108">It connects only to input pins that support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="b2b6b-109">它支援透過 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的本機記憶體傳輸。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-109">It supports local memory transport through the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>
-   <span data-ttu-id="b2b6b-110">它會拒絕資料流程結束、排清和新區段的通知。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-110">It rejects end-of-stream, flush, and new-segment notifications.</span></span> <span data-ttu-id="b2b6b-111"> (不應將這些傳送至輸出釘選。 ) </span><span class="sxs-lookup"><span data-stu-id="b2b6b-111">(These should not be sent to an output pin.)</span></span>
-   <span data-ttu-id="b2b6b-112">它提供了提供下游範例的方法。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-112">It provides methods for delivering samples downstream.</span></span>

<span data-ttu-id="b2b6b-113">當 pin 連接時，它會向輸入 pin 要求記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-113">When the pin connects, it requests a memory allocator from the input pin.</span></span> <span data-ttu-id="b2b6b-114">若失敗，則會建立新的配置器物件。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-114">Failing that, it creates a new allocator object.</span></span> <span data-ttu-id="b2b6b-115">輸出針腳負責設定配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-115">The output pin is responsible for setting the allocator properties.</span></span> <span data-ttu-id="b2b6b-116">它會透過純虛擬方法 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md)。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-116">It does this through the pure virtual method [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span> <span data-ttu-id="b2b6b-117">在您的衍生類別中覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-117">Override this method in your derived class.</span></span> <span data-ttu-id="b2b6b-118">如果輸入 pin 具有任何緩衝區需求，則會將它們傳遞給 **DecideBufferSize** 方法。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-118">If the input pin has any buffer requirements, they are passed to the **DecideBufferSize** method.</span></span>

<span data-ttu-id="b2b6b-119">呼叫 [**CBaseOutputPin：： GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) 方法以取得空白媒體範例。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-119">Call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain an empty media sample.</span></span> <span data-ttu-id="b2b6b-120">呼叫 [**CBaseOutputPin：:D eliver**](cbaseoutputpin-deliver.md) 方法以傳遞下游範例。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-120">Call the [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) method to deliver samples downstream.</span></span>

<span data-ttu-id="b2b6b-121">您的衍生類別必須覆寫純虛擬 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法，以在 pin 連接期間驗證媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-121">Your derived class must override the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to validate the media type during pin connections.</span></span>



| <span data-ttu-id="b2b6b-122">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="b2b6b-122">Protected Member Variables</span></span>                                      | <span data-ttu-id="b2b6b-123">Description</span><span class="sxs-lookup"><span data-stu-id="b2b6b-123">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="b2b6b-124">**m \_ pAllocator**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-124">**m\_pAllocator**</span></span>](cbaseoutputpin-m-pallocator.md)            | <span data-ttu-id="b2b6b-125">記憶體配置器的指標。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-125">Pointer to the memory allocator.</span></span>                                           |
| [<span data-ttu-id="b2b6b-126">**m \_ pInputPin**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-126">**m\_pInputPin**</span></span>](cbaseoutputpin-m-pinputpin.md)              | <span data-ttu-id="b2b6b-127">連接到此 pin 之輸入連接的指標。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-127">Pointer to the input pin connected to this pin.</span></span>                            |
| <span data-ttu-id="b2b6b-128">公用方法</span><span class="sxs-lookup"><span data-stu-id="b2b6b-128">Public Methods</span></span>                                                  | <span data-ttu-id="b2b6b-129">Description</span><span class="sxs-lookup"><span data-stu-id="b2b6b-129">Description</span></span>                                                                |
| [<span data-ttu-id="b2b6b-130">**CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-130">**CBaseOutputPin**</span></span>](cbaseoutputpin-cbaseoutputpin.md)         | <span data-ttu-id="b2b6b-131">函式方法。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-131">Constructor method.</span></span>                                                        |
| [<span data-ttu-id="b2b6b-132">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-132">**CompleteConnect**</span></span>](cbaseoutputpin-completeconnect.md)       | <span data-ttu-id="b2b6b-133">完成輸入 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-133">Completes a connection to an input pin.</span></span> <span data-ttu-id="b2b6b-134">虛擬。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-134">Virtual.</span></span>                           |
| [<span data-ttu-id="b2b6b-135">**DecideAllocator**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-135">**DecideAllocator**</span></span>](cbaseoutputpin-decideallocator.md)       | <span data-ttu-id="b2b6b-136">選取記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-136">Selects a memory allocator.</span></span> <span data-ttu-id="b2b6b-137">虛擬。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-137">Virtual.</span></span>                                       |
| [<span data-ttu-id="b2b6b-138">**GetDeliveryBuffer**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-138">**GetDeliveryBuffer**</span></span>](cbaseoutputpin-getdeliverybuffer.md)   | <span data-ttu-id="b2b6b-139">抓取包含空緩衝區的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-139">Retrieves a media sample that contains an empty buffer.</span></span> <span data-ttu-id="b2b6b-140">虛擬。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-140">Virtual.</span></span>           |
| [<span data-ttu-id="b2b6b-141">**提供**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-141">**Deliver**</span></span>](cbaseoutputpin-deliver.md)                       | <span data-ttu-id="b2b6b-142">將媒體範例傳遞至連線的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-142">Delivers a media sample to the connected input pin.</span></span> <span data-ttu-id="b2b6b-143">虛擬。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-143">Virtual.</span></span>               |
| [<span data-ttu-id="b2b6b-144">**InitAllocator**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-144">**InitAllocator**</span></span>](cbaseoutputpin-initallocator.md)           | <span data-ttu-id="b2b6b-145">建立記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-145">Creates a memory allocator.</span></span> <span data-ttu-id="b2b6b-146">虛擬。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-146">Virtual.</span></span>                                       |
| [<span data-ttu-id="b2b6b-147">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-147">**CheckConnect**</span></span>](cbaseoutputpin-checkconnect.md)             | <span data-ttu-id="b2b6b-148">判斷 pin 連接是否合適。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-148">Determines whether a pin connection is suitable.</span></span>                           |
| [<span data-ttu-id="b2b6b-149">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-149">**BreakConnect**</span></span>](cbaseoutputpin-breakconnect.md)             | <span data-ttu-id="b2b6b-150">釋放連接的 pin。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-150">Releases the pin from a connection.</span></span>                                        |
| [<span data-ttu-id="b2b6b-151">**使用中**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-151">**Active**</span></span>](cbaseoutputpin-active.md)                         | <span data-ttu-id="b2b6b-152">通知釘選篩選現在已啟用。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-152">Notifies the pin that the filter is now active.</span></span>                            |
| [<span data-ttu-id="b2b6b-153">**非使用中**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-153">**Inactive**</span></span>](cbaseoutputpin-inactive.md)                     | <span data-ttu-id="b2b6b-154">通知 pin 此篩選已不再有效。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-154">Notifies the pin that the filter is no longer active.</span></span>                      |
| [<span data-ttu-id="b2b6b-155">**DeliverEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-155">**DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md) | <span data-ttu-id="b2b6b-156">將資料流程結束通知傳遞至連線的輸入 pin。虛擬。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-156">Delivers an end-of-stream notification to the connected input pin.Virtual.</span></span> |
| [<span data-ttu-id="b2b6b-157">**DeliverBeginFlush**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-157">**DeliverBeginFlush**</span></span>](cbaseoutputpin-deliverbeginflush.md)   | <span data-ttu-id="b2b6b-158">要求連接的輸入 pin 以開始清除作業。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-158">Requests the connected input pin to begin a flush operation.</span></span> <span data-ttu-id="b2b6b-159">虛擬。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-159">Virtual.</span></span>      |
| [<span data-ttu-id="b2b6b-160">**DeliverEndFlush**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-160">**DeliverEndFlush**</span></span>](cbaseoutputpin-deliverendflush.md)       | <span data-ttu-id="b2b6b-161">要求連接的輸入 pin 以結束排清操作。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-161">Requests the connected input pin to end a flush operation.</span></span> <span data-ttu-id="b2b6b-162">虛擬。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-162">Virtual.</span></span>        |
| [<span data-ttu-id="b2b6b-163">**DeliverNewSegment**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-163">**DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)   | <span data-ttu-id="b2b6b-164">將新區段通知傳遞至連線的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-164">Delivers a new-segment notification to the connected input pin.</span></span> <span data-ttu-id="b2b6b-165">虛擬。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-165">Virtual.</span></span>   |
| <span data-ttu-id="b2b6b-166">純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="b2b6b-166">Pure Virtual Methods</span></span>                                            | <span data-ttu-id="b2b6b-167">Description</span><span class="sxs-lookup"><span data-stu-id="b2b6b-167">Description</span></span>                                                                |
| [<span data-ttu-id="b2b6b-168">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-168">**DecideBufferSize**</span></span>](cbaseoutputpin-decidebuffersize.md)     | <span data-ttu-id="b2b6b-169">設定緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-169">Sets the buffer requirements.</span></span>                                              |
| <span data-ttu-id="b2b6b-170">IPin 方法</span><span class="sxs-lookup"><span data-stu-id="b2b6b-170">IPin Methods</span></span>                                                    | <span data-ttu-id="b2b6b-171">Description</span><span class="sxs-lookup"><span data-stu-id="b2b6b-171">Description</span></span>                                                                |
| [<span data-ttu-id="b2b6b-172">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-172">**BeginFlush**</span></span>](cbaseoutputpin-beginflush.md)                 | <span data-ttu-id="b2b6b-173">開始清除作業。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-173">Begins a flush operation.</span></span>                                                  |
| [<span data-ttu-id="b2b6b-174">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-174">**EndFlush**</span></span>](cbaseoutputpin-endflush.md)                     | <span data-ttu-id="b2b6b-175">結束清除操作。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-175">Ends a flush operation.</span></span>                                                    |
| [<span data-ttu-id="b2b6b-176">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="b2b6b-176">**EndOfStream**</span></span>](cbaseoutputpin-endofstream.md)               | <span data-ttu-id="b2b6b-177">通知 pin，不需要額外的資料。</span><span class="sxs-lookup"><span data-stu-id="b2b6b-177">Notifies the pin that no additional data is expected.</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="b2b6b-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2b6b-178">Requirements</span></span>



| <span data-ttu-id="b2b6b-179">需求</span><span class="sxs-lookup"><span data-stu-id="b2b6b-179">Requirement</span></span> | <span data-ttu-id="b2b6b-180">值</span><span class="sxs-lookup"><span data-stu-id="b2b6b-180">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b6b-181">標頭</span><span class="sxs-lookup"><span data-stu-id="b2b6b-181">Header</span></span><br/>  | <dl> <span data-ttu-id="b2b6b-182"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b2b6b-182"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b2b6b-183">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2b6b-183">Library</span></span><br/> | <dl> <span data-ttu-id="b2b6b-184"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b2b6b-184"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




