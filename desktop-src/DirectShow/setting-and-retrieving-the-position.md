---
description: 設定和取出位置
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: 設定和取出位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687383"
---
# <a name="setting-and-retrieving-the-position"></a><span data-ttu-id="b771d-103">設定和取出位置</span><span class="sxs-lookup"><span data-stu-id="b771d-103">Setting and Retrieving the Position</span></span>

<span data-ttu-id="b771d-104">篩選圖形會維護兩個位置值：目前的位置和停止位置。</span><span class="sxs-lookup"><span data-stu-id="b771d-104">The filter graph maintains two position values, current position and stop position.</span></span> <span data-ttu-id="b771d-105">這些定義如下：</span><span class="sxs-lookup"><span data-stu-id="b771d-105">These are defined as follows:</span></span>

-   <span data-ttu-id="b771d-106">當圖形正在執行時，目前的位置會是目前的播放位置（相對於來源的開頭）。</span><span class="sxs-lookup"><span data-stu-id="b771d-106">When the graph is running, the current position is the current playback position, relative to the beginning of the source.</span></span> <span data-ttu-id="b771d-107">當圖形停止或暫停時，目前的位置是串流將開始于下一個執行命令的時間點。</span><span class="sxs-lookup"><span data-stu-id="b771d-107">When the graph is stopped or paused, the current position is the point where streaming will begin on the next run command.</span></span>
-   <span data-ttu-id="b771d-108">停止位置是資料流程將結束的點。</span><span class="sxs-lookup"><span data-stu-id="b771d-108">The stop position is the point where the stream will end.</span></span> <span data-ttu-id="b771d-109">當圖形到達停止位置時，就不會再串流處理任何資料，而篩選圖形管理員會張貼 [**EC \_ 完成**](ec-complete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="b771d-109">When the graph reaches the stop position, no more data is streamed, and the filter graph manager posts an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="b771d-110">但圖形 (不會自動切換為已停止狀態。</span><span class="sxs-lookup"><span data-stu-id="b771d-110">(The graph does not automatically switch to a stopped state, however.</span></span> <span data-ttu-id="b771d-111">如需詳細資訊，請參閱 [回應事件](responding-to-events.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="b771d-111">For more information, see [Responding to Events](responding-to-events.md).)</span></span>

<span data-ttu-id="b771d-112">若要取出這些值，請呼叫 [**IMediaSeeking：： GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) 方法。</span><span class="sxs-lookup"><span data-stu-id="b771d-112">To retrieve these values, call the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span> <span data-ttu-id="b771d-113">傳回的值一律相對於原始媒體來源。</span><span class="sxs-lookup"><span data-stu-id="b771d-113">The returned values are always relative to the original media source.</span></span> <span data-ttu-id="b771d-114">依預設，值為參考時間單位。</span><span class="sxs-lookup"><span data-stu-id="b771d-114">By default, the values are in reference time units.</span></span> <span data-ttu-id="b771d-115">在某些情況下，您可以變更時間單位;如需詳細資訊，請參閱 [搜尋命令的時間格式](time-formats-for-seek-commands.md)。</span><span class="sxs-lookup"><span data-stu-id="b771d-115">In some cases, you can change the time units; for more information, see [Time Formats For Seek Commands](time-formats-for-seek-commands.md).</span></span>

<span data-ttu-id="b771d-116">若要搜尋新位置或設定新的停止位置，請呼叫 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="b771d-116">To seek to a new position or set a new stop position, call the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method, as shown in the following example:</span></span>


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> <span data-ttu-id="b771d-117">一秒是10000000的參考時間單位。</span><span class="sxs-lookup"><span data-stu-id="b771d-117">One second is 10,000,000 units of reference time.</span></span> <span data-ttu-id="b771d-118">為了方便起見，此範例會將此值定義為一 \_ 秒。</span><span class="sxs-lookup"><span data-stu-id="b771d-118">For convenience, the example defines this value as ONE\_SECOND.</span></span> <span data-ttu-id="b771d-119">如果您使用的是 DirectShow 基類程式庫，常數單位會有相同的值。</span><span class="sxs-lookup"><span data-stu-id="b771d-119">If you are using the DirectShow base-class library, the constant UNITS has the same value.</span></span>

 

<span data-ttu-id="b771d-120">*RtNow* 參數會指定新的目前位置。</span><span class="sxs-lookup"><span data-stu-id="b771d-120">The *rtNow* parameter specifies the new current position.</span></span> <span data-ttu-id="b771d-121">第二個參數是定義如何解讀 *rtNow* 的旗標。</span><span class="sxs-lookup"><span data-stu-id="b771d-121">The second parameter is a flag that defines how to interpret *rtNow*.</span></span> <span data-ttu-id="b771d-122">在此範例中，AM \_ 搜尋 \_ AbsolutePositioning 旗標指出 *rtNow* 在來源中指定絕對位置。</span><span class="sxs-lookup"><span data-stu-id="b771d-122">In this example, the AM\_SEEKING\_AbsolutePositioning flag indicates that *rtNow* specifies an absolute position in the source.</span></span> <span data-ttu-id="b771d-123">因此，篩選圖形將會從資料流程的開頭開始搜尋兩秒鐘的位置。</span><span class="sxs-lookup"><span data-stu-id="b771d-123">Therefore, the filter graph will seek to a position two seconds from the start of the stream.</span></span> <span data-ttu-id="b771d-124">*RtStop* 參數會提供停止時間。</span><span class="sxs-lookup"><span data-stu-id="b771d-124">The *rtStop* parameter gives the stop time.</span></span> <span data-ttu-id="b771d-125">最後一個參數指定 *rtStop* 也是絕對位置。</span><span class="sxs-lookup"><span data-stu-id="b771d-125">The last parameter specifies that *rtStop* is also an absolute position.</span></span>

<span data-ttu-id="b771d-126">若要指定相對於先前位置值的位置，請使用 AM \_ 搜尋 \_ RelativePositioning 旗標。</span><span class="sxs-lookup"><span data-stu-id="b771d-126">To specify a position relative to the previous position value, use the AM\_SEEKING\_RelativePositioning flag.</span></span> <span data-ttu-id="b771d-127">若要讓其中一個位置值保持不變，請使用 AM \_ 搜尋 \_ NoPositioning 旗標。</span><span class="sxs-lookup"><span data-stu-id="b771d-127">To leave one of the position values unchanged, use the AM\_SEEKING\_NoPositioning flag.</span></span> <span data-ttu-id="b771d-128">在該情況下，對應的 time 參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b771d-128">The corresponding time parameter can be **NULL** in that case.</span></span> <span data-ttu-id="b771d-129">下列範例會向前搜尋10秒，但不會讓停止位置保持不變：</span><span class="sxs-lookup"><span data-stu-id="b771d-129">The following example seeks forward by 10 seconds but leaves the stop position unchanged:</span></span>


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



<span data-ttu-id="b771d-130">如果篩選圖形已停止，則影片轉譯器不會在搜尋作業之後更新影像。</span><span class="sxs-lookup"><span data-stu-id="b771d-130">If the filter graph is stopped, the video renderer does not update the image after a seek operation.</span></span> <span data-ttu-id="b771d-131">對使用者而言，它會顯示為搜尋未發生。</span><span class="sxs-lookup"><span data-stu-id="b771d-131">To the user, it will appear as if the seek did not happen.</span></span> <span data-ttu-id="b771d-132">若要更新影像，請在搜尋作業之後暫停圖形。</span><span class="sxs-lookup"><span data-stu-id="b771d-132">To update the image, pause the graph after the seek operation.</span></span> <span data-ttu-id="b771d-133">暫停圖形會提示影片轉譯器的新影片畫面。</span><span class="sxs-lookup"><span data-stu-id="b771d-133">Pausing the graph cues a new video frame for the video renderer.</span></span> <span data-ttu-id="b771d-134">您可以使用 [**IMediaControl：： StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) 方法，它會暫停圖形，然後將它停止。</span><span class="sxs-lookup"><span data-stu-id="b771d-134">You can use the [**IMediaControl::StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) method, which pauses the graph and then stops it.</span></span>

 

 



