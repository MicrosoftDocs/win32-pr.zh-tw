---
description: CBaseInputPin 類別是用來執行輸入圖釘的抽象基類。 除了 CBasePin 提供的 IPin 介面支援之外，此類別還新增了 IMemInputPin 介面的支援。
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: 'CBaseInputPin 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994315"
---
# <a name="cbaseinputpin-class"></a><span data-ttu-id="cdfbd-104">CBaseInputPin 類別</span><span class="sxs-lookup"><span data-stu-id="cdfbd-104">CBaseInputPin class</span></span>

![cbaseinputpin 類別階層](images/filter07.png)

<span data-ttu-id="cdfbd-106">`CBaseInputPin`類別是用來執行輸入圖釘的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-106">The `CBaseInputPin` class is an abstract base class for implementing input pins.</span></span> <span data-ttu-id="cdfbd-107">除了 [**CBasePin**](cbasepin.md)提供的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面支援之外，此類別還新增了 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)介面的支援。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-107">This class adds support for the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, in addition to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface support provided by [**CBasePin**](cbasepin.md).</span></span>

<span data-ttu-id="cdfbd-108">若要使用此類別，請衍生新的類別，並至少覆寫下列方法：</span><span class="sxs-lookup"><span data-stu-id="cdfbd-108">To use this class, derive a new class and override at least the following methods:</span></span>

-   [<span data-ttu-id="cdfbd-109">**CBaseInputPin::BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-109">**CBaseInputPin::BeginFlush**</span></span>](cbaseinputpin-beginflush.md)
-   [<span data-ttu-id="cdfbd-110">**CBaseInputPin::EndFlush**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-110">**CBaseInputPin::EndFlush**</span></span>](cbaseinputpin-endflush.md)
-   [<span data-ttu-id="cdfbd-111">**CBaseInputPin：： Receive**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-111">**CBaseInputPin::Receive**</span></span>](cbaseinputpin-receive.md)
-   [<span data-ttu-id="cdfbd-112">**CBasePin::CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-112">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="cdfbd-113">**CBasePin::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-113">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="cdfbd-114">根據 pin 的函式，您可能需要覆寫或 CBasePin 中的其他 `CBaseInputPin` 方法。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-114">Depending on the function of the pin, you might need to override additional methods in `CBaseInputPin` or **CBasePin**.</span></span>



| <span data-ttu-id="cdfbd-115">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="cdfbd-115">Protected Member Variables</span></span>                                                 | <span data-ttu-id="cdfbd-116">Description</span><span class="sxs-lookup"><span data-stu-id="cdfbd-116">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdfbd-117">**m \_ pAllocator**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-117">**m\_pAllocator**</span></span>](cbaseinputpin-m-pallocator.md)                        | <span data-ttu-id="cdfbd-118">記憶體配置器的指標。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-118">Pointer to the memory allocator.</span></span>                                                                            |
| [<span data-ttu-id="cdfbd-119">**m \_ bReadOnly**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-119">**m\_bReadOnly**</span></span>](cbaseinputpin-m-breadonly.md)                          | <span data-ttu-id="cdfbd-120">指出配置器是否會產生唯讀媒體範例的旗標。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-120">Flag that indicates whether the allocator produces read-only media samples.</span></span>                                 |
| [<span data-ttu-id="cdfbd-121">**m \_ bFlushing**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-121">**m\_bFlushing**</span></span>](cbaseinputpin-m-bflushing.md)                          | <span data-ttu-id="cdfbd-122">指出釘選是否正在排清的旗標。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-122">Flag that indicates whether the pin is currently flushing.</span></span>                                                  |
| [<span data-ttu-id="cdfbd-123">**m \_ SampleProps**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-123">**m\_SampleProps**</span></span>](cbaseinputpin-m-sampleprops.md)                      | <span data-ttu-id="cdfbd-124">最新範例的屬性。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-124">Properties of the most recent sample.</span></span>                                                                       |
| <span data-ttu-id="cdfbd-125">公用方法</span><span class="sxs-lookup"><span data-stu-id="cdfbd-125">Public Methods</span></span>                                                             | <span data-ttu-id="cdfbd-126">Description</span><span class="sxs-lookup"><span data-stu-id="cdfbd-126">Description</span></span>                                                                                                 |
| [<span data-ttu-id="cdfbd-127">**CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-127">**CBaseInputPin**</span></span>](cbaseinputpin-cbaseinputpin.md)                       | <span data-ttu-id="cdfbd-128">函式方法。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-128">Constructor method.</span></span>                                                                                         |
| [<span data-ttu-id="cdfbd-129">**~ CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-129">**~CBaseInputPin**</span></span>](cbaseinputpin--cbaseinputpin.md)                     | <span data-ttu-id="cdfbd-130">函式方法。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-130">Destructor method.</span></span>                                                                                          |
| [<span data-ttu-id="cdfbd-131">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-131">**BreakConnect**</span></span>](cbaseinputpin-breakconnect.md)                         | <span data-ttu-id="cdfbd-132">釋放連接的 pin。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-132">Releases the pin from a connection.</span></span>                                                                         |
| [<span data-ttu-id="cdfbd-133">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-133">**IsReadOnly**</span></span>](cbaseinputpin-isreadonly.md)                             | <span data-ttu-id="cdfbd-134">查詢配置器是否使用唯讀媒體範例。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-134">Queries whether the allocator uses read-only media samples.</span></span>                                                 |
| [<span data-ttu-id="cdfbd-135">**IsFlushing**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-135">**IsFlushing**</span></span>](cbaseinputpin-isflushing.md)                             | <span data-ttu-id="cdfbd-136">查詢篩選目前是否正在排清。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-136">Queries whether the filter is currently flushing.</span></span>                                                           |
| [<span data-ttu-id="cdfbd-137">**CheckStreaming**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-137">**CheckStreaming**</span></span>](cbaseinputpin-checkstreaming.md)                     | <span data-ttu-id="cdfbd-138">判斷 pin 是否可以接受範例。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-138">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="cdfbd-139">虛擬。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-139">Virtual.</span></span>                                                     |
| [<span data-ttu-id="cdfbd-140">**PassNotify**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-140">**PassNotify**</span></span>](cbaseinputpin-passnotify.md)                             | <span data-ttu-id="cdfbd-141">將品質控制訊息傳遞至適當的物件。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-141">Passes a quality-control message to the appropriate object.</span></span>                                                 |
| [<span data-ttu-id="cdfbd-142">**非使用中**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-142">**Inactive**</span></span>](cbaseinputpin-inactive.md)                                 | <span data-ttu-id="cdfbd-143">通知 pin 此篩選已不再有效。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-143">Notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="cdfbd-144">虛擬。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-144">Virtual.</span></span>                                              |
| [<span data-ttu-id="cdfbd-145">**SampleProps**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-145">**SampleProps**</span></span>](cbaseinputpin-sampleprops.md)                           | <span data-ttu-id="cdfbd-146">抓取最新範例的屬性。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-146">Retrieves the properties of the most recent sample.</span></span>                                                         |
| <span data-ttu-id="cdfbd-147">IPin 方法</span><span class="sxs-lookup"><span data-stu-id="cdfbd-147">IPin Methods</span></span>                                                               | <span data-ttu-id="cdfbd-148">Description</span><span class="sxs-lookup"><span data-stu-id="cdfbd-148">Description</span></span>                                                                                                 |
| [<span data-ttu-id="cdfbd-149">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-149">**BeginFlush**</span></span>](cbaseinputpin-beginflush.md)                             | <span data-ttu-id="cdfbd-150">開始清除作業。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-150">Begins a flush operation.</span></span>                                                                                   |
| [<span data-ttu-id="cdfbd-151">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-151">**EndFlush**</span></span>](cbaseinputpin-endflush.md)                                 | <span data-ttu-id="cdfbd-152">結束清除操作。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-152">Ends a flush operation.</span></span>                                                                                     |
| <span data-ttu-id="cdfbd-153">IMemInputPin 方法</span><span class="sxs-lookup"><span data-stu-id="cdfbd-153">IMemInputPin Methods</span></span>                                                       | <span data-ttu-id="cdfbd-154">Description</span><span class="sxs-lookup"><span data-stu-id="cdfbd-154">Description</span></span>                                                                                                 |
| [<span data-ttu-id="cdfbd-155">**GetAllocator**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-155">**GetAllocator**</span></span>](cbaseinputpin-getallocator.md)                         | <span data-ttu-id="cdfbd-156">抓取此 pin 提議的記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-156">Retrieves the memory allocator proposed by this pin.</span></span>                                                        |
| [<span data-ttu-id="cdfbd-157">**NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-157">**NotifyAllocator**</span></span>](cbaseinputpin-notifyallocator.md)                   | <span data-ttu-id="cdfbd-158">指定連接的配置器。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-158">Specifies an allocator for the connection.</span></span>                                                                  |
| [<span data-ttu-id="cdfbd-159">**GetAllocatorRequirements**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-159">**GetAllocatorRequirements**</span></span>](cbaseinputpin-getallocatorrequirements.md) | <span data-ttu-id="cdfbd-160">抓取輸入 pin 所要求的配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-160">Retrieves the allocator properties requested by the input pin.</span></span>                                              |
| [<span data-ttu-id="cdfbd-161">**收到**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-161">**Receive**</span></span>](cbaseinputpin-receive.md)                                   | <span data-ttu-id="cdfbd-162">接收資料流程中的下一個媒體範例。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-162">Receives the next media sample in the stream.</span></span>                                                               |
| [<span data-ttu-id="cdfbd-163">**ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-163">**ReceiveMultiple**</span></span>](cbaseinputpin-receivemultiple.md)                   | <span data-ttu-id="cdfbd-164">接收資料流程中的多個範例。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-164">Receives multiple samples in the stream.</span></span>                                                                    |
| [<span data-ttu-id="cdfbd-165">**ReceiveCanBlock**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-165">**ReceiveCanBlock**</span></span>](cbaseinputpin-receivecanblock.md)                   | <span data-ttu-id="cdfbd-166">判斷 [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法的呼叫是否可能封鎖。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-166">Determines whether calls to the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method might block.</span></span> |
| <span data-ttu-id="cdfbd-167">IQualityControl 方法</span><span class="sxs-lookup"><span data-stu-id="cdfbd-167">IQualityControl Methods</span></span>                                                    | <span data-ttu-id="cdfbd-168">Description</span><span class="sxs-lookup"><span data-stu-id="cdfbd-168">Description</span></span>                                                                                                 |
| [<span data-ttu-id="cdfbd-169">**Notify**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-169">**Notify**</span></span>](cbaseinputpin-notify.md)                                     | <span data-ttu-id="cdfbd-170">接收品質控制訊息。</span><span class="sxs-lookup"><span data-stu-id="cdfbd-170">Receives a quality-control message.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="cdfbd-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdfbd-171">Requirements</span></span>



| <span data-ttu-id="cdfbd-172">需求</span><span class="sxs-lookup"><span data-stu-id="cdfbd-172">Requirement</span></span> | <span data-ttu-id="cdfbd-173">值</span><span class="sxs-lookup"><span data-stu-id="cdfbd-173">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdfbd-174">標頭</span><span class="sxs-lookup"><span data-stu-id="cdfbd-174">Header</span></span><br/>  | <dl> <span data-ttu-id="cdfbd-175"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cdfbd-175"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cdfbd-176">程式庫</span><span class="sxs-lookup"><span data-stu-id="cdfbd-176">Library</span></span><br/> | <dl> <span data-ttu-id="cdfbd-177"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cdfbd-177"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




