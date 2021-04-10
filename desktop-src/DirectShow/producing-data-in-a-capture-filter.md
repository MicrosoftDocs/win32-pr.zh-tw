---
description: 本主題描述自訂的 DirectShow capture 篩選器應該如何產生輸出資料。
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: 在 Capture 篩選器中產生資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935877"
---
# <a name="producing-data-in-a-capture-filter"></a><span data-ttu-id="ac07f-103">在 Capture 篩選器中產生資料</span><span class="sxs-lookup"><span data-stu-id="ac07f-103">Producing Data in a Capture Filter</span></span>

<span data-ttu-id="ac07f-104">本主題描述自訂的 DirectShow capture 篩選器應該如何產生輸出資料。</span><span class="sxs-lookup"><span data-stu-id="ac07f-104">This topic describes how a custom DirectShow capture filter should generate output data.</span></span>

## <a name="filter-state-changes"></a><span data-ttu-id="ac07f-105">篩選狀態變更</span><span class="sxs-lookup"><span data-stu-id="ac07f-105">Filter State Changes</span></span>

<span data-ttu-id="ac07f-106">只有在執行篩選時，才會產生資料的捕獲篩選。</span><span class="sxs-lookup"><span data-stu-id="ac07f-106">A capture filter should produce data only when the filter is running.</span></span> <span data-ttu-id="ac07f-107">當篩選暫停時，請勿從您的 pin 傳送資料。</span><span class="sxs-lookup"><span data-stu-id="ac07f-107">Do not send data from your pins when the filter is paused.</span></span> <span data-ttu-id="ac07f-108">此外，當篩選暫停時，傳回 VFW 無法從 [**CBaseFilter：： >getstate**](cbasefilter-getstate.md)方法 **\_ \_ \_ 提示**。</span><span class="sxs-lookup"><span data-stu-id="ac07f-108">Also, return **VFW\_S\_CANT\_CUE** from the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method when the filter is paused.</span></span> <span data-ttu-id="ac07f-109">此傳回值會告知篩選圖形管理員，在篩選暫停時，不應該等候篩選中的任何資料。</span><span class="sxs-lookup"><span data-stu-id="ac07f-109">This return value informs the Filter Graph Manager that it should not wait for any data from your filter while the filter is paused.</span></span> <span data-ttu-id="ac07f-110">如需詳細資訊，請參閱 [篩選狀態](filter-states.md)。</span><span class="sxs-lookup"><span data-stu-id="ac07f-110">For more information, see [Filter States](filter-states.md).</span></span>

<span data-ttu-id="ac07f-111">下列程式碼顯示如何執行 [**IMediaFilter：： >getstate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) 方法：</span><span class="sxs-lookup"><span data-stu-id="ac07f-111">The following code shows how to implement the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method:</span></span>


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a><span data-ttu-id="ac07f-112">控制個別資料流程</span><span class="sxs-lookup"><span data-stu-id="ac07f-112">Controlling Individual Streams</span></span>

<span data-ttu-id="ac07f-113">捕捉篩選器的輸出圖釘應支援 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) 介面，讓應用程式可以個別開啟或關閉每個 pin。</span><span class="sxs-lookup"><span data-stu-id="ac07f-113">A capture filter's output pins should support the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, so that an application can turn each pin on or off individually.</span></span> <span data-ttu-id="ac07f-114">例如，應用程式可以在不進行捕捉的情況下預覽，然後切換到 [capture] 模式，而不需重建篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="ac07f-114">For example, an application can preview without capturing, and then switch to capture mode without rebuilding the filter graph.</span></span> <span data-ttu-id="ac07f-115">您可以使用 [**CBaseStreamControl**](cbasestreamcontrol.md) 類別來執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="ac07f-115">You can use the [**CBaseStreamControl**](cbasestreamcontrol.md) class to implement this interface.</span></span>

## <a name="time-stamps"></a><span data-ttu-id="ac07f-116">時間戳記</span><span class="sxs-lookup"><span data-stu-id="ac07f-116">Time Stamps</span></span>

<span data-ttu-id="ac07f-117">當篩選器捕捉到範例時，請使用目前的資料流程時間來為範例加上時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ac07f-117">When the filter captures a sample, time stamp the sample with the current stream time.</span></span> <span data-ttu-id="ac07f-118">結束時間是開始時間加上持續時間。</span><span class="sxs-lookup"><span data-stu-id="ac07f-118">The end time is the start time plus the duration.</span></span> <span data-ttu-id="ac07f-119">例如，如果篩選器是以每秒10個樣本來進行，而且當篩選器捕捉到樣本時，資料流程時間為200000000個單位，則時間戳記應該是200000000和201000000。</span><span class="sxs-lookup"><span data-stu-id="ac07f-119">For example, if the filter is capturing at ten samples per second, and the stream time is 200,000,000 units when the filter captures the sample, the time stamps should be 200000000 and 201000000.</span></span> <span data-ttu-id="ac07f-120"> (每秒10000000個單位。 ) </span><span class="sxs-lookup"><span data-stu-id="ac07f-120">(There are 10,000,000 units per second.)</span></span>

<span data-ttu-id="ac07f-121">若要計算資料流程時間，請呼叫 [**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) 方法來取得目前的參考時間，然後減法原始的開始時間。</span><span class="sxs-lookup"><span data-stu-id="ac07f-121">To calculate the stream time, call the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method to get the current reference time, and then substract the original start time.</span></span> <span data-ttu-id="ac07f-122">或者，呼叫 [**CBaseFilter：： StreamTime**](cbasefilter-streamtime.md) 方法，它會執行相同的計算。</span><span class="sxs-lookup"><span data-stu-id="ac07f-122">Alternatively, call the [**CBaseFilter::StreamTime**](cbasefilter-streamtime.md) method, which performs the same calculation.</span></span> <span data-ttu-id="ac07f-123">若要設定範例的時間戳記，請呼叫 [**IMediaSample：： SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) 方法。</span><span class="sxs-lookup"><span data-stu-id="ac07f-123">To set the time stamp on a sample, call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

<span data-ttu-id="ac07f-124">不過，如果篩選具有預覽 pin，則來自預覽 pin 的範例不應該有時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ac07f-124">If the filter has a preview pin, however, samples from the preview pin should not have time stamps.</span></span> <span data-ttu-id="ac07f-125">原因是，在捕捉時間之後，範例一律會稍微觸及轉譯器。</span><span class="sxs-lookup"><span data-stu-id="ac07f-125">The reason is that samples will always reach the renderer slightly after the time of capture.</span></span> <span data-ttu-id="ac07f-126">如果樣本有時間戳記，轉譯器會將它們視為延遲，而且可能會藉由卸載樣本來嘗試趕上。</span><span class="sxs-lookup"><span data-stu-id="ac07f-126">If the samples are time stamped, the renderer will treat them as late, and it may try to catch up by dropping samples.</span></span> <span data-ttu-id="ac07f-127"> (需詳細資訊，請參閱 [DirectShow 影片捕獲篩選器](directshow-video-capture-filters.md)。 ) 請注意， [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) 介面需要 pin 才能追蹤取樣時間。</span><span class="sxs-lookup"><span data-stu-id="ac07f-127">(For more information, see [DirectShow Video Capture Filters](directshow-video-capture-filters.md).) Note that the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface requires the pin to keep track of sample times.</span></span> <span data-ttu-id="ac07f-128">針對預覽釘選，您可能需要修改執行，使其不依賴時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ac07f-128">For a preview pin, you might need to modify the implementation so that it does not rely on time stamps.</span></span>

<span data-ttu-id="ac07f-129">時間戳記必須永遠從一個樣本增加到下一個樣本。</span><span class="sxs-lookup"><span data-stu-id="ac07f-129">Time stamps must always increase from one sample to the next.</span></span> <span data-ttu-id="ac07f-130">即使在篩選暫停時也是如此。</span><span class="sxs-lookup"><span data-stu-id="ac07f-130">This is true even when the filter pauses.</span></span> <span data-ttu-id="ac07f-131">如果篩選執行、暫停，然後再次執行，則暫停之後的第一個範例必須具有比暫停前最後一個樣本更大的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ac07f-131">If the filter runs, pauses, and then runs again, the first sample after the pause must have a larger time stamp than the last sample before the pause.</span></span>

<span data-ttu-id="ac07f-132">視您要捕捉的資料而定，可能會有適當的設定範例媒體時間。</span><span class="sxs-lookup"><span data-stu-id="ac07f-132">Depending on the data you are capturing, it might be appropriate to set the media time on the samples.</span></span>

<span data-ttu-id="ac07f-133">如需詳細資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="ac07f-133">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac07f-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac07f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac07f-135">DirectShow 影片捕獲篩選</span><span class="sxs-lookup"><span data-stu-id="ac07f-135">DirectShow Video Capture Filters</span></span>](directshow-video-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="ac07f-136">DirectShow 中的時間和時鐘</span><span class="sxs-lookup"><span data-stu-id="ac07f-136">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="ac07f-137">寫入捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="ac07f-137">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



