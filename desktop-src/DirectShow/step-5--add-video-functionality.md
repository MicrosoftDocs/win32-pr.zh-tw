---
description: 本主題是在 DirectShow 中進行音訊/影片播放教學課程的步驟5。
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 步驟5：新增影片功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f5ccf1ae3ca24a705506bc41620ac53a13d7e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194226"
---
# <a name="step-5-add-video-functionality"></a><span data-ttu-id="f8918-103">步驟5：新增影片功能</span><span class="sxs-lookup"><span data-stu-id="f8918-103">Step 5: Add Video Functionality</span></span>

<span data-ttu-id="f8918-104">本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟5。</span><span class="sxs-lookup"><span data-stu-id="f8918-104">This topic is step 5 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="f8918-105">完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="f8918-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="f8918-106">為確保影片正確顯示，應用程式必須回應 [**wm \_ 油漆**](../gdi/wm-paint.md)、 [**WM \_ 大小**](../winmsg/wm-size.md)和 [**wm \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) 訊息，如下所示。</span><span class="sxs-lookup"><span data-stu-id="f8918-106">To ensure that video displays correctly, the application must respond to [**WM\_PAINT**](../gdi/wm-paint.md), [**WM\_SIZE**](../winmsg/wm-size.md), and [**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md) messages as follows.</span></span>

### <a name="handle-wm_paint-messages"></a><span data-ttu-id="f8918-107">處理 WM \_ 油漆訊息</span><span class="sxs-lookup"><span data-stu-id="f8918-107">Handle WM\_PAINT Messages</span></span>

<span data-ttu-id="f8918-108">當應用程式收到 [**WM \_ 油漆**](../gdi/wm-paint.md) 訊息時，影片轉譯器可能需要重繪最後的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="f8918-108">When the application receives a [**WM\_PAINT**](../gdi/wm-paint.md) message, the video renderer might need to redraw the last video frame.</span></span> <span data-ttu-id="f8918-109">如需 [**增強型影片**](enhanced-video-renderer-filter.md) 轉譯器 (EVR) 篩選準則，請呼叫 [**IMFVideoDisplayControl：： RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo)。</span><span class="sxs-lookup"><span data-stu-id="f8918-109">For the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter, call [**IMFVideoDisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>


```C++
HRESULT CEVR::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="f8918-110">若為 [影片混合轉譯器篩選 9](video-mixing-renderer-filter-9.md) (VMR-9) ，請呼叫 [**IVMRWindowlessControl9：： RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo)。</span><span class="sxs-lookup"><span data-stu-id="f8918-110">For the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9), call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span>


```C++
HRESULT CVMR9::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="f8918-111">若為 [影片混合轉譯器篩選 7](video-mixing-renderer-filter-7.md) (VMR-7) ，請呼叫 [**IVMRWindowlessControl：： RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo)。</span><span class="sxs-lookup"><span data-stu-id="f8918-111">For the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7), call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span>


```C++
HRESULT CVMR7::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



### <a name="handle-wm_size-messages"></a><span data-ttu-id="f8918-112">處理 WM \_ 大小訊息</span><span class="sxs-lookup"><span data-stu-id="f8918-112">Handle WM\_SIZE Messages</span></span>

<span data-ttu-id="f8918-113">如果影片視窗的大小變更，請通知影片轉譯器調整影片的大小。</span><span class="sxs-lookup"><span data-stu-id="f8918-113">If the size of the video window changes, notify the video renderer to resize the video.</span></span> <span data-ttu-id="f8918-114">若為 EVR，請呼叫 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)。</span><span class="sxs-lookup"><span data-stu-id="f8918-114">For the EVR, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>


```C++
HRESULT CEVR::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pVideoDisplay == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pVideoDisplay->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pVideoDisplay->SetVideoPosition(NULL, &rc);
    }
}
```



<span data-ttu-id="f8918-115">若為 VMR-9，請呼叫 [**IVMRWindowlessControl9：： SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition)。</span><span class="sxs-lookup"><span data-stu-id="f8918-115">For the VMR-9, call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span></span>


```C++
HRESULT CVMR9::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



<span data-ttu-id="f8918-116">若為 VMR-7，請呼叫 [**IVMRWindowlessControl：： SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition)。</span><span class="sxs-lookup"><span data-stu-id="f8918-116">For the VMR-7, call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span></span>


```C++
HRESULT CVMR7::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {
        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



### <a name="handle-wm_displaychange-messages"></a><span data-ttu-id="f8918-117">處理 WM \_ DISPLAYCHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="f8918-117">Handle WM\_DISPLAYCHANGE Messages</span></span>

<span data-ttu-id="f8918-118">如果顯示模式變更，您必須通知 VMR-9 或 VMR 7 篩選。</span><span class="sxs-lookup"><span data-stu-id="f8918-118">If the display mode changes, you must notify the VMR-9 or VMR-7 filter.</span></span> <span data-ttu-id="f8918-119">若為 VMR-9，請呼叫 [**IVMRWindowlessControl9：:D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged)。</span><span class="sxs-lookup"><span data-stu-id="f8918-119">For the VMR-9, call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span>


```C++
HRESULT CVMR9::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="f8918-120">若為 VMR-7，請呼叫 [**IVMRWindowlessControl：:D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged)。</span><span class="sxs-lookup"><span data-stu-id="f8918-120">For the VMR-7, call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span>


```C++
HRESULT CVMR7::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="f8918-121">當顯示模式變更時，不需要通知 EVR。</span><span class="sxs-lookup"><span data-stu-id="f8918-121">The EVR does not need to be notified when the display mode changes.</span></span>

<span data-ttu-id="f8918-122">下一 [步：步驟6：處理圖形事件](step-6--handle-graph-events.md)。</span><span class="sxs-lookup"><span data-stu-id="f8918-122">Next: [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8918-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8918-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8918-124">在 DirectShow 播放音訊/影片</span><span class="sxs-lookup"><span data-stu-id="f8918-124">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="f8918-125">DirectShow 播放範例</span><span class="sxs-lookup"><span data-stu-id="f8918-125">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="f8918-126">使用 DirectShow EVR 篩選器</span><span class="sxs-lookup"><span data-stu-id="f8918-126">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="f8918-127">使用影片混合轉譯器</span><span class="sxs-lookup"><span data-stu-id="f8918-127">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
