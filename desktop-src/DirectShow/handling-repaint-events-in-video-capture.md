---
description: 處理影片捕獲中的重新繪製事件
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: 處理影片捕獲中的重新繪製事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935974"
---
# <a name="handling-repaint-events-in-video-capture"></a><span data-ttu-id="b6ab8-103">處理影片捕獲中的重新繪製事件</span><span class="sxs-lookup"><span data-stu-id="b6ab8-103">Handling Repaint Events in Video Capture</span></span>

<span data-ttu-id="b6ab8-104">如果您在不使用 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面的情況下建立影片捕獲圖形，而且您使用舊的影片轉譯器篩選器來預覽影片，則應該覆寫 [**EC 重新 \_ 繪製**](ec-repaint.md) 事件的預設處理。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-104">If you build a video capture graph without using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, and you preview the video using the old Video Renderer filter, then you should override the default handling for [**EC\_REPAINT**](ec-repaint.md) events.</span></span> <span data-ttu-id="b6ab8-105">查詢 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) 介面的 [篩選圖形管理員]，並使用 [EC] 值來呼叫 [**IMediaEvent：： CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) 方法 \_ ：</span><span class="sxs-lookup"><span data-stu-id="b6ab8-105">Query the Filter Graph Manager for the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface and call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the value EC\_REPAINT:</span></span>


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



<span data-ttu-id="b6ab8-106">這可防止可能會損毀您的捕獲檔案的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-106">This prevents a possible error that can corrupt your capture file.</span></span> <span data-ttu-id="b6ab8-107">如果使用者涵蓋並暴露預覽視窗，則影片轉譯器篩選器會接收 WM \_ 油漆訊息。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-107">If the user covers and uncovers the preview window, the Video Renderer filter receives a WM\_PAINT message.</span></span> <span data-ttu-id="b6ab8-108">根據預設，影片轉譯器會要求新的框架，而篩選圖形管理員會暫停圖形，以提示另一個影片畫面。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-108">By default, the Video Renderer requests a new frame, and the Filter Graph Manager pauses the graph in order to cue another video frame.</span></span> <span data-ttu-id="b6ab8-109">如果在圖形寫入檔案時發生這種情況，就會損毀檔案。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-109">If that happens while the graph is writing a file, it will corrupt the file.</span></span> <span data-ttu-id="b6ab8-110">覆寫預設的 EC 重新 \_ 繪製行為，可防止轉譯器要求新的框架。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-110">Overriding the default EC\_REPAINT behavior prevents the renderer from requesting a new frame.</span></span>

<span data-ttu-id="b6ab8-111">如果您使用的是 **ICaptureGraphBuilder2** 介面，則不需要執行此步驟，因為「捕獲圖形產生器」會自動為您執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-111">You do not have to perform this step if you are using the **ICaptureGraphBuilder2** interface, because the Capture Graph Builder does it for you automatically.</span></span> <span data-ttu-id="b6ab8-112">此外，如果您使用影片混合轉譯器 (VMR) 進行預覽，則不需要此項。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-112">Also, it is not required if you are using the Video Mixing Renderer (VMR) for preview.</span></span> <span data-ttu-id="b6ab8-113">VMR 一律具有最新的可用畫面，因此不會傳送 EC 重新 \_ 繪製事件。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-113">The VMR always has the most recent frame available, so it does not send EC\_REPAINT events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6ab8-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="b6ab8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6ab8-115">Advanced Capture 主題</span><span class="sxs-lookup"><span data-stu-id="b6ab8-115">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="b6ab8-116">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="b6ab8-116">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



