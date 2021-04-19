---
description: CPosPassThru 類別會處理轉換篩選的搜尋命令，方法是將它們傳遞給下一個篩選準則。
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: 'CPosPassThru 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984075"
---
# <a name="cpospassthru-class"></a><span data-ttu-id="85bd3-103">CPosPassThru 類別</span><span class="sxs-lookup"><span data-stu-id="85bd3-103">CPosPassThru class</span></span>

![cpospassthru 基類階層](images/cutil14.png)

<span data-ttu-id="85bd3-105">`CPosPassThru`類別會處理轉換篩選的搜尋命令，方法是將它們傳遞給下一個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="85bd3-105">The `CPosPassThru` class handles seek commands for transform filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="85bd3-106">當應用程式搜尋篩選圖形時，篩選圖形管理員會向轉譯器篩選提供搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="85bd3-106">When an application seeks the filter graph, the Filter Graph Manager gives the seek command to the renderer filters.</span></span> <span data-ttu-id="85bd3-107">此命令會透過每個篩選器的輸出釘選上游傳遞，直到達到可執行命令 (的篩選準則（如果有任何) ）。</span><span class="sxs-lookup"><span data-stu-id="85bd3-107">The command is passed upstream, through each filter's output pin, until it reaches a filter that can execute the command (if any).</span></span> <span data-ttu-id="85bd3-108">如需詳細資訊，請參閱 [搜尋](seeking.md)。</span><span class="sxs-lookup"><span data-stu-id="85bd3-108">For details, see [Seeking](seeking.md).</span></span> <span data-ttu-id="85bd3-109">類別會將 `CPosPassThru` 所有搜尋命令傳遞至上游篩選器上的輸出圖釘，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="85bd3-109">The `CPosPassThru` class passes all seek commands to the output pin on the upstream filter, as shown in the following diagram.</span></span>

![cpospassthru 類別會傳送上游的搜尋命令。](images/cpospassthru.png)

<span data-ttu-id="85bd3-111">雖然此類別是在基類庫中提供的，但 DirectShow 也會在 Quartz.dll 中提供相同的類別。</span><span class="sxs-lookup"><span data-stu-id="85bd3-111">Although this class is provided in the base class library, DirectShow also provides the same class in Quartz.dll.</span></span> <span data-ttu-id="85bd3-112">使用 Quartz.dll 版本可以稍微減少篩選中的程式碼大小，因為類別是在執行時間從 DLL 載入的。</span><span class="sxs-lookup"><span data-stu-id="85bd3-112">Using the Quartz.dll version can reduce the code size in your filter somewhat, because the class is loaded at run-time from the DLL.</span></span> <span data-ttu-id="85bd3-113">若要使用該版本，請呼叫 [**CreatePosPassThru**](createpospassthru.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="85bd3-113">To use that version, call the [**CreatePosPassThru**](createpospassthru.md) function.</span></span>

<span data-ttu-id="85bd3-114">在輸出釘選的 **NonDelegatingQueryInterface** 方法中，每當要求的介面是 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)或 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)時，委派給 **CPosPassThru** 物件，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="85bd3-114">In your output pin's **NonDelegatingQueryInterface** method, delegate to the **CPosPassThru** object whenever the requested interface is [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) or [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), as shown in the following code:</span></span>


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



<span data-ttu-id="85bd3-115">除非有注明，否則這個類別中的所有 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 和 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 方法都會呼叫連接的釘選上的對應方法，並傳回結果。</span><span class="sxs-lookup"><span data-stu-id="85bd3-115">Except where noted, all [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods in this class call the corresponding method on the connected pin and return the result.</span></span>



| <span data-ttu-id="85bd3-116">公用方法</span><span class="sxs-lookup"><span data-stu-id="85bd3-116">Public Methods</span></span>                                                    | <span data-ttu-id="85bd3-117">Description</span><span class="sxs-lookup"><span data-stu-id="85bd3-117">Description</span></span>                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85bd3-118">**CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="85bd3-118">**CPosPassThru**</span></span>](cpospassthru-cpospassthru.md)                 | <span data-ttu-id="85bd3-119">函式方法。</span><span class="sxs-lookup"><span data-stu-id="85bd3-119">Constructor method.</span></span>                                                                                 |
| [<span data-ttu-id="85bd3-120">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="85bd3-120">**ForceRefresh**</span></span>](cpospassthru-forcerefresh.md)                 | <span data-ttu-id="85bd3-121">已過時。</span><span class="sxs-lookup"><span data-stu-id="85bd3-121">Obsolete.</span></span>                                                                                           |
| [<span data-ttu-id="85bd3-122">**GetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="85bd3-122">**GetMediaTime**</span></span>](cpospassthru-getmediatime.md)                 | <span data-ttu-id="85bd3-123">抓取目前樣本上的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="85bd3-123">Retrieves the time stamps on the current sample.</span></span> <span data-ttu-id="85bd3-124">虛擬。</span><span class="sxs-lookup"><span data-stu-id="85bd3-124">Virtual.</span></span>                                           |
| <span data-ttu-id="85bd3-125">IMediaPosition 方法</span><span class="sxs-lookup"><span data-stu-id="85bd3-125">IMediaPosition Methods</span></span>                                            | <span data-ttu-id="85bd3-126">Description</span><span class="sxs-lookup"><span data-stu-id="85bd3-126">Description</span></span>                                                                                         |
| [<span data-ttu-id="85bd3-127">**取得 \_ 持續時間**</span><span class="sxs-lookup"><span data-stu-id="85bd3-127">**get\_Duration**</span></span>](cpospassthru-get-duration.md)                | <span data-ttu-id="85bd3-128">捕獲資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="85bd3-128">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="85bd3-129">**put \_ CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="85bd3-129">**put\_CurrentPosition**</span></span>](cpospassthru-put-currentposition.md)  | <span data-ttu-id="85bd3-130">設定目前的位置，相對於資料流程的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="85bd3-130">Sets the current position, relative to the total duration of the stream.</span></span>                            |
| [<span data-ttu-id="85bd3-131">**取得 \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="85bd3-131">**get\_StopTime**</span></span>](cpospassthru-get-stoptime.md)                | <span data-ttu-id="85bd3-132">抓取將停止播放的時間（相對於資料流程的持續時間）。</span><span class="sxs-lookup"><span data-stu-id="85bd3-132">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="85bd3-133">**put \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="85bd3-133">**put\_StopTime**</span></span>](cpospassthru-put-stoptime.md)                | <span data-ttu-id="85bd3-134">設定播放將停止的時間，相對於資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="85bd3-134">Sets the time at which the playback will stop, relative to the duration of the stream.</span></span>              |
| [<span data-ttu-id="85bd3-135">**取得 \_ PrerollTime**</span><span class="sxs-lookup"><span data-stu-id="85bd3-135">**get\_PrerollTime**</span></span>](cpospassthru-get-prerolltime.md)          | <span data-ttu-id="85bd3-136">抓取在開始位置之前將排入佇列的資料量。</span><span class="sxs-lookup"><span data-stu-id="85bd3-136">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="85bd3-137">**put \_ PrerollTime**</span><span class="sxs-lookup"><span data-stu-id="85bd3-137">**put\_PrerollTime**</span></span>](cpospassthru-put-prerolltime.md)          | <span data-ttu-id="85bd3-138">設定要在開始位置之前排入佇列的資料量。</span><span class="sxs-lookup"><span data-stu-id="85bd3-138">Sets the amount of data that will be queued before the start position.</span></span>                              |
| [<span data-ttu-id="85bd3-139">**取得 \_ 率**</span><span class="sxs-lookup"><span data-stu-id="85bd3-139">**get\_Rate**</span></span>](cpospassthru-get-rate.md)                        | <span data-ttu-id="85bd3-140">捕獲播放速率。</span><span class="sxs-lookup"><span data-stu-id="85bd3-140">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="85bd3-141">**put \_ 率**</span><span class="sxs-lookup"><span data-stu-id="85bd3-141">**put\_Rate**</span></span>](cpospassthru-put-rate.md)                        | <span data-ttu-id="85bd3-142">設定播放速率。</span><span class="sxs-lookup"><span data-stu-id="85bd3-142">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="85bd3-143">**取得 \_ CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="85bd3-143">**get\_CurrentPosition**</span></span>](cpospassthru-get-currentposition.md)  | <span data-ttu-id="85bd3-144">抓取目前的位置，相對於資料流程的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="85bd3-144">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="85bd3-145">**CanSeekForward**</span><span class="sxs-lookup"><span data-stu-id="85bd3-145">**CanSeekForward**</span></span>](cpospassthru-canseekforward.md)             | <span data-ttu-id="85bd3-146">判斷資料流程是否可以向後 seeked。</span><span class="sxs-lookup"><span data-stu-id="85bd3-146">Determines whether the stream can be seeked backward.</span></span>                                               |
| [<span data-ttu-id="85bd3-147">**CanSeekBackward**</span><span class="sxs-lookup"><span data-stu-id="85bd3-147">**CanSeekBackward**</span></span>](cpospassthru-canseekbackward.md)           | <span data-ttu-id="85bd3-148">判斷資料流程是否可以向前 seeked。</span><span class="sxs-lookup"><span data-stu-id="85bd3-148">Determines whether the stream can be seeked forward.</span></span>                                                |
| <span data-ttu-id="85bd3-149">IMediaSeeking 方法</span><span class="sxs-lookup"><span data-stu-id="85bd3-149">IMediaSeeking Methods</span></span>                                             | <span data-ttu-id="85bd3-150">Description</span><span class="sxs-lookup"><span data-stu-id="85bd3-150">Description</span></span>                                                                                         |
| [<span data-ttu-id="85bd3-151">**CheckCapabilities**</span><span class="sxs-lookup"><span data-stu-id="85bd3-151">**CheckCapabilities**</span></span>](cpospassthru-checkcapabilities.md)       | <span data-ttu-id="85bd3-152">查詢資料流程是否已指定搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="85bd3-152">Queries whether a stream has specified seeking capabilities.</span></span>                                        |
| [<span data-ttu-id="85bd3-153">**ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="85bd3-153">**ConvertTimeFormat**</span></span>](cpospassthru-converttimeformat.md)       | <span data-ttu-id="85bd3-154">從一種時間格式轉換成另一種格式。</span><span class="sxs-lookup"><span data-stu-id="85bd3-154">Converts from one time format to another.</span></span>                                                           |
| [<span data-ttu-id="85bd3-155">**GetAvailable**</span><span class="sxs-lookup"><span data-stu-id="85bd3-155">**GetAvailable**</span></span>](cpospassthru-getavailable.md)                 | <span data-ttu-id="85bd3-156">抓取搜尋有效的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="85bd3-156">Retrieves the range of times in which seeking is efficient.</span></span>                                         |
| [<span data-ttu-id="85bd3-157">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="85bd3-157">**GetCapabilities**</span></span>](cpospassthru-getcapabilities.md)           | <span data-ttu-id="85bd3-158">抓取資料流程的所有搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="85bd3-158">Retrieves all the seeking capabilities of the stream.</span></span>                                               |
| [<span data-ttu-id="85bd3-159">**GetCurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="85bd3-159">**GetCurrentPosition**</span></span>](cpospassthru-getcurrentposition.md)     | <span data-ttu-id="85bd3-160">抓取目前的位置，相對於資料流程的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="85bd3-160">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="85bd3-161">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="85bd3-161">**GetDuration**</span></span>](cpospassthru-getduration.md)                   | <span data-ttu-id="85bd3-162">捕獲資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="85bd3-162">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="85bd3-163">**GetPositions**</span><span class="sxs-lookup"><span data-stu-id="85bd3-163">**GetPositions**</span></span>](cpospassthru-getpositions.md)                 | <span data-ttu-id="85bd3-164">抓取目前的位置和停止位置，相對於資料流程的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="85bd3-164">Retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> |
| [<span data-ttu-id="85bd3-165">**GetPreroll**</span><span class="sxs-lookup"><span data-stu-id="85bd3-165">**GetPreroll**</span></span>](cpospassthru-getpreroll.md)                     | <span data-ttu-id="85bd3-166">抓取在開始位置之前將排入佇列的資料量。</span><span class="sxs-lookup"><span data-stu-id="85bd3-166">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="85bd3-167">**GetRate**</span><span class="sxs-lookup"><span data-stu-id="85bd3-167">**GetRate**</span></span>](cpospassthru-getrate.md)                           | <span data-ttu-id="85bd3-168">捕獲播放速率。</span><span class="sxs-lookup"><span data-stu-id="85bd3-168">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="85bd3-169">**GetStopPosition**</span><span class="sxs-lookup"><span data-stu-id="85bd3-169">**GetStopPosition**</span></span>](cpospassthru-getstopposition.md)           | <span data-ttu-id="85bd3-170">抓取將停止播放的時間（相對於資料流程的持續時間）。</span><span class="sxs-lookup"><span data-stu-id="85bd3-170">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="85bd3-171">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="85bd3-171">**GetTimeFormat**</span></span>](cpospassthru-gettimeformat.md)               | <span data-ttu-id="85bd3-172">抓取目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="85bd3-172">Retrieves the current time format.</span></span>                                                                  |
| [<span data-ttu-id="85bd3-173">**IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="85bd3-173">**IsFormatSupported**</span></span>](cpospassthru-isformatsupported.md)       | <span data-ttu-id="85bd3-174">判斷是否支援指定的時間格式。</span><span class="sxs-lookup"><span data-stu-id="85bd3-174">Determines whether a specified time format is supported.</span></span>                                            |
| [<span data-ttu-id="85bd3-175">**IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="85bd3-175">**IsUsingTimeFormat**</span></span>](cpospassthru-isusingtimeformat.md)       | <span data-ttu-id="85bd3-176">判斷指定的時間格式是否為目前使用中的格式。</span><span class="sxs-lookup"><span data-stu-id="85bd3-176">Determines whether a specified time format is the format currently in use.</span></span>                          |
| [<span data-ttu-id="85bd3-177">**QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="85bd3-177">**QueryPreferredFormat**</span></span>](cpospassthru-querypreferredformat.md) | <span data-ttu-id="85bd3-178">抓取資料流程的慣用時間格式。</span><span class="sxs-lookup"><span data-stu-id="85bd3-178">Retrieves the preferred time format for the stream.</span></span>                                                 |
| [<span data-ttu-id="85bd3-179">**SetPositions**</span><span class="sxs-lookup"><span data-stu-id="85bd3-179">**SetPositions**</span></span>](cpospassthru-setpositions.md)                 | <span data-ttu-id="85bd3-180">設定目前的位置和停止位置。</span><span class="sxs-lookup"><span data-stu-id="85bd3-180">Sets the current position and the stop position.</span></span>                                                    |
| [<span data-ttu-id="85bd3-181">**SetRate**</span><span class="sxs-lookup"><span data-stu-id="85bd3-181">**SetRate**</span></span>](cpospassthru-setrate.md)                           | <span data-ttu-id="85bd3-182">設定播放速率。</span><span class="sxs-lookup"><span data-stu-id="85bd3-182">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="85bd3-183">**SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="85bd3-183">**SetTimeFormat**</span></span>](cpospassthru-settimeformat.md)               | <span data-ttu-id="85bd3-184">設定時間格式。</span><span class="sxs-lookup"><span data-stu-id="85bd3-184">Sets the time format.</span></span>                                                                               |
| <span data-ttu-id="85bd3-185">輔助函式</span><span class="sxs-lookup"><span data-stu-id="85bd3-185">Helper Functions</span></span>                                                  | <span data-ttu-id="85bd3-186">Description</span><span class="sxs-lookup"><span data-stu-id="85bd3-186">Description</span></span>                                                                                         |
| [<span data-ttu-id="85bd3-187">**CreatePosPassThru**</span><span class="sxs-lookup"><span data-stu-id="85bd3-187">**CreatePosPassThru**</span></span>](createpospassthru.md)                    | <span data-ttu-id="85bd3-188">建立 `CPosPassThru` 或 [**CRendererPosPassThru**](crendererpospassthru.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="85bd3-188">Creates a `CPosPassThru` or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="85bd3-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="85bd3-189">Requirements</span></span>



| <span data-ttu-id="85bd3-190">需求</span><span class="sxs-lookup"><span data-stu-id="85bd3-190">Requirement</span></span> | <span data-ttu-id="85bd3-191">值</span><span class="sxs-lookup"><span data-stu-id="85bd3-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85bd3-192">標頭</span><span class="sxs-lookup"><span data-stu-id="85bd3-192">Header</span></span><br/>  | <dl> <span data-ttu-id="85bd3-193"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="85bd3-193"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85bd3-194">程式庫</span><span class="sxs-lookup"><span data-stu-id="85bd3-194">Library</span></span><br/> | <dl> <span data-ttu-id="85bd3-195"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="85bd3-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




