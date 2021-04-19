---
description: CTransInPlaceFilter 類別是針對就地轉換篩選所設計，而篩選準則會修改輸入資料，而不是跨緩衝區複製資料。若要使用此類別，請從 CTransInPlaceFilter 衍生新的類別，並執行下列方法：
ms.assetid: 3d6d5436-f280-4e36-96e4-40161e8115c2
title: 'CTransInPlaceFilter 類別 (Transip) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f59dd312adbb95797caf695aecea082f296df5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983135"
---
# <a name="ctransinplacefilter-class"></a><span data-ttu-id="3c945-103">CTransInPlaceFilter 類別</span><span class="sxs-lookup"><span data-stu-id="3c945-103">CTransInPlaceFilter class</span></span>

![ctransinplacefilter 類別階層](images/tsip03.png)

<span data-ttu-id="3c945-105">`CTransInPlaceFilter`類別是針對就地轉換篩選所設計，而這些篩選準則是修改輸入資料的篩選，而不是跨緩衝區複製資料。若要使用這個類別，請從衍生新的類別， `CTransInPlaceFilter` 並執行下列方法：</span><span class="sxs-lookup"><span data-stu-id="3c945-105">The `CTransInPlaceFilter` class is designed for in-place transform filters, which are filters that modify the input data rather than copying the data across buffers.To use this class, derive a new class from `CTransInPlaceFilter` and implement the following methods:</span></span>

-   [<span data-ttu-id="3c945-106">**CTransformFilter::CheckInputType**</span><span class="sxs-lookup"><span data-stu-id="3c945-106">**CTransformFilter::CheckInputType**</span></span>](ctransformfilter-checkinputtype.md)
-   [<span data-ttu-id="3c945-107">**CTransInPlaceFilter：： Transform**</span><span class="sxs-lookup"><span data-stu-id="3c945-107">**CTransInPlaceFilter::Transform**</span></span>](ctransinplacefilter-transform.md)

<span data-ttu-id="3c945-108">這個類別會針對其輸入的 pin 使用 [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) 類別，並使用其輸出圖釘的 [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="3c945-108">This class uses the [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) class for its input pin, and the [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) class for its output pin.</span></span> <span data-ttu-id="3c945-109">一般而言，您不需要覆寫這些釘選類別。</span><span class="sxs-lookup"><span data-stu-id="3c945-109">Typically, you do not need to override these pin classes.</span></span> <span data-ttu-id="3c945-110">此篩選器會在 [**CTransInPlaceFilter：： GetPin**](ctransinplacefilter-getpin.md) 方法中建立這兩個 pin。</span><span class="sxs-lookup"><span data-stu-id="3c945-110">The filter creates both pins in the [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method.</span></span> <span data-ttu-id="3c945-111">如果您確實覆寫了釘選類別，則必須覆寫 **GetPin** 以建立自訂 pin。</span><span class="sxs-lookup"><span data-stu-id="3c945-111">If you do override the pin classes, you must override **GetPin** to create your custom pins.</span></span>

<span data-ttu-id="3c945-112">此類別的設計目的是讓輸入類型永遠符合輸出類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-112">This class is designed so the input type always matches the output type.</span></span> <span data-ttu-id="3c945-113">如果可能的話，篩選器會針對這兩個 pin 連接使用單一配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-113">Whenever possible, the filter uses a single allocator for both pin connections.</span></span>

## <a name="preferred-media-types"></a><span data-ttu-id="3c945-114">慣用的媒體類型</span><span class="sxs-lookup"><span data-stu-id="3c945-114">Preferred Media Types</span></span>

<span data-ttu-id="3c945-115">如果輸出釘選已連接，則輸入 pin 會提供下游篩選器的慣用類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-115">If the output pin is already connected, the input pin offers the downstream filter's preferred types.</span></span> <span data-ttu-id="3c945-116"> (事實上，它只會傳回下游篩選器的列舉值物件 ) 。否則，就不會有任何慣用的類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-116">(In fact it simply returns the downstream filter's enumerator object.) Otherwise, it has no preferred types.</span></span> <span data-ttu-id="3c945-117">輸出 pin 具有相同的行為，但反向：如果輸入的連接已連接，則輸出 pin 會提供上游篩選器的慣用類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-117">The output pin has the same behavior, but in reverse: If the input pin is already connected, the output pin offers the upstream filter's preferred types.</span></span> <span data-ttu-id="3c945-118">否則，它沒有慣用的類型</span><span class="sxs-lookup"><span data-stu-id="3c945-118">Otherwise, it has no preferred types</span></span>

## <a name="pin-connections"></a><span data-ttu-id="3c945-119">Pin 連接</span><span class="sxs-lookup"><span data-stu-id="3c945-119">Pin Connections</span></span>

<span data-ttu-id="3c945-120">當一個 pin 連線時，篩選通常會重新連接其他 pin，以確定這兩個 pin 都使用相同的媒體類型和相同的配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-120">When one pin connects, the filter generally reconnects the other pin, to make sure that both pins use the same media type and the same allocator.</span></span> <span data-ttu-id="3c945-121"> (重新連接的 [pin](reconnecting-pins.md)會描述重新連接 pin 的機制 ) 。可能的方法有兩種：輸入 pin 會先連接，或輸出 pin 會先連接。</span><span class="sxs-lookup"><span data-stu-id="3c945-121">(The mechanism for reconnecting pins is described in [Reconnecting Pins](reconnecting-pins.md).) Two scenarios are possible: Either the input pin connects first, or the output pin connects first.</span></span>

<span data-ttu-id="3c945-122">假設輸入 pin 會先連接。</span><span class="sxs-lookup"><span data-stu-id="3c945-122">Suppose the input pin connects first.</span></span> <span data-ttu-id="3c945-123">會進行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="3c945-123">The following steps occur:</span></span>

1.  <span data-ttu-id="3c945-124">輸入的 pin 會呼叫篩選器的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-124">The input pin calls the filter's [**CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span>
2.  <span data-ttu-id="3c945-125">上游篩選器會選取配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-125">The upstream filter selects an allocator.</span></span> <span data-ttu-id="3c945-126">此時，輸入 pin 沒有配置器需求，而且會接受連接的任何配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-126">At this point, the input pin has no allocator requirements, and it accepts any allocator for the connection.</span></span> <span data-ttu-id="3c945-127">如果上游篩選要求配置器，則 pin 會建立一個新的配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-127">If the upstream filter requests an allocator, the pin creates a new one.</span></span> <span data-ttu-id="3c945-128">基於稍後所述的原因，此配置器將不會用於最終連接。</span><span class="sxs-lookup"><span data-stu-id="3c945-128">For reasons described shortly, this allocator will not be used in the final connection.</span></span> <span data-ttu-id="3c945-129">它僅提供協助完成此連接程式階段。</span><span class="sxs-lookup"><span data-stu-id="3c945-129">It is provided only to help finish this stage of the connection process.</span></span>

<span data-ttu-id="3c945-130">稍後，當輸出 pin 連接時：</span><span class="sxs-lookup"><span data-stu-id="3c945-130">Later, when the output pin connects:</span></span>

1.  <span data-ttu-id="3c945-131">輸出圖釘會呼叫篩選器的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-131">The output pin calls the filter's [**CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="3c945-132">它也會呼叫上游篩選器上的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。</span><span class="sxs-lookup"><span data-stu-id="3c945-132">It also calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream filter.</span></span> <span data-ttu-id="3c945-133">這可確保輸入 pin 可以變更其媒體類型以符合。</span><span class="sxs-lookup"><span data-stu-id="3c945-133">This ensures that the input pin can change its media type to match.</span></span>
2.  <span data-ttu-id="3c945-134">輸出圖釘會呼叫篩選器的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-134">The output pin calls the filter's [**CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="3c945-135">它也會呼叫上游篩選器上的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。</span><span class="sxs-lookup"><span data-stu-id="3c945-135">It also calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream filter.</span></span> <span data-ttu-id="3c945-136">這可確保輸入 pin 可以變更其媒體類型以符合。</span><span class="sxs-lookup"><span data-stu-id="3c945-136">This ensures that the input pin can change its media type to match.</span></span>
3.  <span data-ttu-id="3c945-137">輸出圖釘會呼叫篩選器的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-137">The output pin calls the filter's [**CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="3c945-138">它也會呼叫上游篩選器上的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。</span><span class="sxs-lookup"><span data-stu-id="3c945-138">It also calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream filter.</span></span> <span data-ttu-id="3c945-139">這可確保輸入 pin 可以變更其媒體類型以符合。</span><span class="sxs-lookup"><span data-stu-id="3c945-139">This ensures that the input pin can change its media type to match.</span></span>
4.  <span data-ttu-id="3c945-140">這次，輸入 pin 的 [**GetAllocator**](ctransinplaceinputpin-getallocator.md) 方法會傳回下游配置器，而 [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) 會傳回下游篩選器的配置器需求。</span><span class="sxs-lookup"><span data-stu-id="3c945-140">This time, the input pin's [**GetAllocator**](ctransinplaceinputpin-getallocator.md) method returns the downstream allocator, and [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) returns the downstream filter's allocator requirements.</span></span> <span data-ttu-id="3c945-141">輸入 pin 會接受上游篩選器選擇的任何配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-141">The input pin accepts whatever allocator the upstream filter chooses.</span></span>
5.  <span data-ttu-id="3c945-142">這次，輸入 pin 的 [**GetAllocator**](ctransinplaceinputpin-getallocator.md) 方法會傳回下游配置器，而 [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) 會傳回下游篩選器的配置器需求。</span><span class="sxs-lookup"><span data-stu-id="3c945-142">This time, the input pin's [**GetAllocator**](ctransinplaceinputpin-getallocator.md) method returns the downstream allocator, and [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) returns the downstream filter's allocator requirements.</span></span> <span data-ttu-id="3c945-143">輸入 pin 會接受上游篩選器選擇的任何配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-143">The input pin accepts whatever allocator the upstream filter chooses.</span></span>

<span data-ttu-id="3c945-144">現在請考慮相反的案例，其中的輸出圖釘是要連接的第一個 pin。</span><span class="sxs-lookup"><span data-stu-id="3c945-144">Now consider the opposite scenario, where the output pin is the first pin to connect.</span></span>

1.  <span data-ttu-id="3c945-145">輸出圖釘會呼叫篩選器的 [**CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-145">The output pin calls the filter's [**CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span>
2.  <span data-ttu-id="3c945-146">它會選取配置器，並偏好使用下游篩選器的配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-146">It selects an allocator, preferring to use the downstream filter's allocator.</span></span>

<span data-ttu-id="3c945-147">然後，當輸入 pin 連接時：</span><span class="sxs-lookup"><span data-stu-id="3c945-147">Then, when the input pin connects:</span></span>

1.  <span data-ttu-id="3c945-148">輸入 pin 會藉由在篩選上呼叫 [**CheckInputType**](ctransformfilter-checkinputtype.md) ，以及在下游篩選器的輸出圖釘上呼叫 [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) ，來檢查媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-148">The input pin checks the media type by calling [**CheckInputType**](ctransformfilter-checkinputtype.md) on the filter, and by calling [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the downstream filter's output pin.</span></span>
2.  <span data-ttu-id="3c945-149">如果輸入類型與輸出類型不符，則篩選會重新連接輸出的釘選。</span><span class="sxs-lookup"><span data-stu-id="3c945-149">If the input type does not match the output type, the filter reconnects the output pin.</span></span>
3.  <span data-ttu-id="3c945-150">上游篩選器會選取配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-150">The upstream filter selects an allocator.</span></span> <span data-ttu-id="3c945-151">輸入 pin 的 [**GetAllocator**](ctransinplaceinputpin-getallocator.md) 方法會傳回下游配置器，而輸入 pin 會接受上游篩選器所選取的任何配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-151">The input pin's [**GetAllocator**](ctransinplaceinputpin-getallocator.md) method returns the downstream allocator, and the input pin accepts whatever allocator the upstream filter selects.</span></span>
4.  <span data-ttu-id="3c945-152">此篩選器會使用相同的配置器進行下游連接，可能會覆寫原始的下游配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-152">The filter uses the same allocator for the downstream connection, possibly overriding the original downstream allocator.</span></span>

<span data-ttu-id="3c945-153">如果任何相關的配置器是唯讀的，這一系列的事件就會稍微變更，因為下游配置器必須是可寫入的。</span><span class="sxs-lookup"><span data-stu-id="3c945-153">This sequence of events changes slightly if any of the allocators involved are read-only, because the downstream allocator must be writable.</span></span> <span data-ttu-id="3c945-154">在此情況下，篩選可能會使用兩個不同的配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-154">In that case, the filter might use two separate allocators.</span></span>

<span data-ttu-id="3c945-155">如需使用這個類別的詳細資訊，請參閱 [寫入轉換篩選](writing-transform-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="3c945-155">For more information about using this class, see [Writing Transform Filters](writing-transform-filters.md).</span></span>



| <span data-ttu-id="3c945-156">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="3c945-156">Protected Member Variables</span></span>                                                        | <span data-ttu-id="3c945-157">Description</span><span class="sxs-lookup"><span data-stu-id="3c945-157">Description</span></span>                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="3c945-158">**m \_ bModifiesData**</span><span class="sxs-lookup"><span data-stu-id="3c945-158">**m\_bModifiesData**</span></span>](ctransinplacefilter-m-bmodifiesdata.md)                   | <span data-ttu-id="3c945-159">指出篩選準則是否修改範例資料。</span><span class="sxs-lookup"><span data-stu-id="3c945-159">Indicates whether the filter modifies the sample data.</span></span>                           |
| <span data-ttu-id="3c945-160">保護方法</span><span class="sxs-lookup"><span data-stu-id="3c945-160">Protected Methods</span></span>                                                                 | <span data-ttu-id="3c945-161">Description</span><span class="sxs-lookup"><span data-stu-id="3c945-161">Description</span></span>                                                                      |
| [<span data-ttu-id="3c945-162">**複製**</span><span class="sxs-lookup"><span data-stu-id="3c945-162">**Copy**</span></span>](ctransinplacefilter-copy.md)                                          | <span data-ttu-id="3c945-163">複製媒體範例。</span><span class="sxs-lookup"><span data-stu-id="3c945-163">Copies a media sample.</span></span>                                                           |
| [<span data-ttu-id="3c945-164">**InputPin**</span><span class="sxs-lookup"><span data-stu-id="3c945-164">**InputPin**</span></span>](ctransinplacefilter-inputpin.md)                                  | <span data-ttu-id="3c945-165">抓取篩選的輸入圖釘指標。</span><span class="sxs-lookup"><span data-stu-id="3c945-165">Retrieves a pointer to the filter's input pin.</span></span>                                   |
| [<span data-ttu-id="3c945-166">**OutputPin**</span><span class="sxs-lookup"><span data-stu-id="3c945-166">**OutputPin**</span></span>](ctransinplacefilter-outputpin.md)                                | <span data-ttu-id="3c945-167">抓取篩選的輸出圖釘指標。</span><span class="sxs-lookup"><span data-stu-id="3c945-167">Retrieves a pointer to the filter's output pin.</span></span>                                  |
| [<span data-ttu-id="3c945-168">**TypesMatch**</span><span class="sxs-lookup"><span data-stu-id="3c945-168">**TypesMatch**</span></span>](ctransinplacefilter-typesmatch.md)                              | <span data-ttu-id="3c945-169">判斷輸入媒體類型是否符合輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-169">Determines whether the input media type matches the output media type.</span></span>           |
| [<span data-ttu-id="3c945-170">**UsingDifferentAllocators**</span><span class="sxs-lookup"><span data-stu-id="3c945-170">**UsingDifferentAllocators**</span></span>](ctransinplacefilter--usingdifferentallocators.md) | <span data-ttu-id="3c945-171">判斷輸入和輸出圖釘是否使用不同的配置器。</span><span class="sxs-lookup"><span data-stu-id="3c945-171">Determines whether the input and output pins are using different allocators.</span></span>     |
| <span data-ttu-id="3c945-172">公用方法</span><span class="sxs-lookup"><span data-stu-id="3c945-172">Public Methods</span></span>                                                                    | <span data-ttu-id="3c945-173">Description</span><span class="sxs-lookup"><span data-stu-id="3c945-173">Description</span></span>                                                                      |
| [<span data-ttu-id="3c945-174">**CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="3c945-174">**CTransInPlaceFilter**</span></span>](ctransinplacefilter-ctransinplacefilter.md)            | <span data-ttu-id="3c945-175">函式方法。</span><span class="sxs-lookup"><span data-stu-id="3c945-175">Constructor method.</span></span>                                                              |
| [<span data-ttu-id="3c945-176">**GetPin**</span><span class="sxs-lookup"><span data-stu-id="3c945-176">**GetPin**</span></span>](ctransinplacefilter-getpin.md)                                      | <span data-ttu-id="3c945-177">捕獲 pin。</span><span class="sxs-lookup"><span data-stu-id="3c945-177">Retrieves a pin.</span></span>                                                                 |
| [<span data-ttu-id="3c945-178">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="3c945-178">**GetMediaType**</span></span>](ctransinplacefilter-getmediatype.md)                          | <span data-ttu-id="3c945-179">抓取輸出圖釘的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c945-179">Retrieves a preferred media type for the output pin.</span></span>                             |
| [<span data-ttu-id="3c945-180">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3c945-180">**DecideBufferSize**</span></span>](ctransinplacefilter-decidebuffersize.md)                  | <span data-ttu-id="3c945-181">設定輸出釘選的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="3c945-181">Sets the output pin's buffer requirements.</span></span>                                       |
| [<span data-ttu-id="3c945-182">**CheckTransform**</span><span class="sxs-lookup"><span data-stu-id="3c945-182">**CheckTransform**</span></span>](ctransinplacefilter-checktransform.md)                      | <span data-ttu-id="3c945-183">檢查輸入媒體類型是否與輸出媒體類型相容。</span><span class="sxs-lookup"><span data-stu-id="3c945-183">Checks whether an input media type is compatible with an output media type.</span></span>      |
| [<span data-ttu-id="3c945-184">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="3c945-184">**CompleteConnect**</span></span>](ctransinplacefilter-completeconnect.md)                    | <span data-ttu-id="3c945-185">完成 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="3c945-185">Completes a pin connection.</span></span>                                                      |
| [<span data-ttu-id="3c945-186">**收到**</span><span class="sxs-lookup"><span data-stu-id="3c945-186">**Receive**</span></span>](ctransinplacefilter-receive.md)                                    | <span data-ttu-id="3c945-187">接收媒體範例、進行處理，並將其傳遞至下游篩選器。</span><span class="sxs-lookup"><span data-stu-id="3c945-187">Receives a media sample, processes it, and delivers it to the downstream filter.</span></span> |
| <span data-ttu-id="3c945-188">純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="3c945-188">Pure Virtual Methods</span></span>                                                              | <span data-ttu-id="3c945-189">Description</span><span class="sxs-lookup"><span data-stu-id="3c945-189">Description</span></span>                                                                      |
| [<span data-ttu-id="3c945-190">**Transform**</span><span class="sxs-lookup"><span data-stu-id="3c945-190">**Transform**</span></span>](ctransinplacefilter-transform.md)                                | <span data-ttu-id="3c945-191">就地轉換範例。</span><span class="sxs-lookup"><span data-stu-id="3c945-191">Transforms a sample in place.</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="3c945-192">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c945-192">Requirements</span></span>



| <span data-ttu-id="3c945-193">需求</span><span class="sxs-lookup"><span data-stu-id="3c945-193">Requirement</span></span> | <span data-ttu-id="3c945-194">值</span><span class="sxs-lookup"><span data-stu-id="3c945-194">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c945-195">標頭</span><span class="sxs-lookup"><span data-stu-id="3c945-195">Header</span></span><br/>  | <dl> <span data-ttu-id="3c945-196"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3c945-196"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c945-197">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c945-197">Library</span></span><br/> | <dl> <span data-ttu-id="3c945-198"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3c945-198"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




