---
description: 本主題是 DirectShow 中音訊/影片播放教學課程的步驟5。
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 步驟5：新增影片功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968c35916f90f226305eb987058d14cc7891d250961e2b8a41a1756ec3794b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951777"
---
# <a name="step-5-add-video-functionality"></a>步驟5：新增影片功能

本主題是[DirectShow 中音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟5。 完整的程式碼會顯示在[DirectShow 播放範例](directshow-playback-example.md)的主題中。

為確保影片正確顯示，應用程式必須回應 [**wm \_ 油漆**](../gdi/wm-paint.md)、 [**WM \_ 大小**](../winmsg/wm-size.md)和 [**wm \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) 訊息，如下所示。

### <a name="handle-wm_paint-messages"></a>處理 WM \_ 油漆訊息

當應用程式收到 [**WM \_ 油漆**](../gdi/wm-paint.md) 訊息時，影片轉譯器可能需要重繪最後的影片畫面。 如需 [**增強型影片**](enhanced-video-renderer-filter.md) 轉譯器 (EVR) 篩選準則，請呼叫 [**IMFVideoDisplayControl：： RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo)。


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



若為 [影片混合轉譯器篩選 9](video-mixing-renderer-filter-9.md) (VMR-9) ，請呼叫 [**IVMRWindowlessControl9：： RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo)。


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



若為 [影片混合轉譯器篩選 7](video-mixing-renderer-filter-7.md) (VMR-7) ，請呼叫 [**IVMRWindowlessControl：： RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo)。


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



### <a name="handle-wm_size-messages"></a>處理 WM \_ 大小訊息

如果影片視窗的大小變更，請通知影片轉譯器調整影片的大小。 若為 EVR，請呼叫 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)。


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



若為 VMR-9，請呼叫 [**IVMRWindowlessControl9：： SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition)。


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



若為 VMR-7，請呼叫 [**IVMRWindowlessControl：： SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition)。


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



### <a name="handle-wm_displaychange-messages"></a>處理 WM \_ DISPLAYCHANGE 訊息

如果顯示模式變更，您必須通知 VMR-9 或 VMR 7 篩選。 若為 VMR-9，請呼叫 [**IVMRWindowlessControl9：:D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged)。


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



若為 VMR-7，請呼叫 [**IVMRWindowlessControl：:D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged)。


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



當顯示模式變更時，不需要通知 EVR。

下一[步：步驟6：處理 Graph 事件](step-6--handle-graph-events.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的音訊/影片播放](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow播放範例](directshow-playback-example.md)
</dt> <dt>

[使用 DirectShow EVR 篩選](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[使用影片混合轉譯器](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
