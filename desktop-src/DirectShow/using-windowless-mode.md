---
description: 使用無視窗模式
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: 使用無視窗模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850332"
---
# <a name="using-windowless-mode"></a>使用無視窗模式

[影片混合轉譯器篩選 7](video-mixing-renderer-filter-7.md) (VMR-7) 和 [影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9) 支援 *無視窗模式*，這代表 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)介面上的重大改進。 本主題說明無視窗模式和視窗模式之間的差異，以及如何使用無視窗模式。

為了維持與現有應用程式的回溯相容性，VMR 預設為視窗模式。 在視窗模式中，轉譯器會建立自己的視窗來顯示影片。 一般而言，應用程式會將影片視窗設定為應用程式視窗的子系。 有個別的影片視窗會造成一些問題，不過：

-   最重要的是，如果線上程之間傳送視窗訊息，則可能會發生鎖死。
-   篩選圖形管理員必須將某些視窗訊息（例如 WM \_ 油漆）轉寄給影片轉譯器。 應用程式必須使用篩選圖形管理員的 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (，而不是影片轉譯器的) ，如此篩選圖形管理員就會維持正確的內部狀態。
-   若要從影片視窗接收滑鼠或鍵盤事件，應用程式必須設定 *訊息清空*，使影片視窗將這些訊息轉送到應用程式。
-   若要防止裁剪問題，影片視窗必須有正確的視窗樣式。

無視窗模式可避免這些問題，方法是讓 VMR 直接在應用程式視窗的工作區上進行繪製，並使用 DirectDraw 來裁剪影片矩形。 無視窗模式可大幅減少鎖死的機會。 此外，應用程式不需要設定擁有者視窗或視窗樣式。 事實上，當 VMR 處於無視窗模式時，它甚至不會公開不再需要的 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面。

若要使用無視窗模式，您必須明確設定 VMR。 不過，您會發現更具彈性且更容易使用的視窗模式。

VMR-7 篩選和 VMR-9 篩選器會公開不同的介面，但每個都有相同的步驟。

## <a name="configure-the-vmr-for-windowless-mode"></a>設定無視窗模式的 VMR

若要覆寫 VMR 的預設行為，請在建立篩選圖形之前設定 VMR：

**VMR-7**

1.  建立篩選圖形管理員。
2.  建立 VMR-7 並將它新增至篩選圖形。
3.  使用 **VMRMode \_ 無視窗** 旗標，在 VMR-7 上呼叫 [**IVMRFilterConfig：： SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) 。
4.  針對 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) 介面查詢 VMR-7。
5.  在 VMR-7 上呼叫 [**IVMRWindowlessControl：： SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) 。 指定應顯示影片的視窗控制碼。

**VMR-9**

1.  建立篩選圖形管理員。
2.  建立 VMR-9 並將它新增至篩選圖形。
3.  使用 **VMR9Mode \_ 無視窗** 旗標，在 VMR-9 上呼叫 [**IVMRFilterConfig9：： SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) 。
4.  針對 [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) 介面查詢 VMR-9。
5.  在 VMR-9 上呼叫 [**IVMRWindowlessControl9：： SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) 。 指定應顯示影片的視窗控制碼。

現在請呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 或其他圖形建立方法，以建立篩選圖形的其餘部分。 篩選圖形管理員會自動使用您新增至圖形的 VMR 實例。  (如需發生此情況的詳細資訊，請參閱 [智慧型連接](intelligent-connect.md)。 ) 

下列程式碼顯示 helper 函式，此函式會建立 VMR-7、將它新增至圖形，並設定無視窗模式。


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



此函式假設只會顯示一個影片資料流程，而不會在影片上混用靜態點陣圖。 如需詳細資訊，請參閱 [VMR 無視窗模式](vmr-windowless-mode.md)。 您會呼叫此函式，如下所示：


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a>定位影片

設定 VMR 後，下一個步驟是設定影片的位置。 有兩個要考慮的矩形： *來源* 矩形和 *目的地* 矩形。 來源矩形會定義影片中要顯示的部分。 目的地矩形會在視窗的工作區中指定將包含影片的區域。 VMR 會將影片影像裁剪至來源矩形，並伸展裁剪影像以符合目的地矩形。

**VMR-7**

1.  呼叫 [**IVMRWindowlessControl：： SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) 方法來指定這兩個矩形。
2.  來源矩形必須等於或小於原生影片大小;您可以使用 [**IVMRWindowlessControl：： GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) 方法來取得原生影片大小。

**VMR-9**

1.  呼叫 [**IVMRWindowlessControl9：： SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) 方法來指定這兩個矩形。
2.  來源矩形必須等於或小於原生影片大小;您可以使用 [**IVMRWindowlessControl9：： GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) 方法來取得原生影片大小。

例如，下列程式碼會設定 VMR-7 的來源和目的地矩形。 它會將來源矩形設定為與整個影片影像相等，而目的地矩形等於整個視窗工作區：


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



如果您想要讓影片佔用工作區的較小部分，請修改 *rcDest* 參數。 如果您想要裁剪影片影像，請修改 *rcSrc* 參數。

## <a name="handle-window-messages"></a>處理視窗訊息

因為 VMR 沒有自己的視窗，所以如果需要重新繪製或調整影片的大小，就必須通知它。 藉由呼叫所列出的 VMR 方法來回應下列視窗訊息。

**VMR-7**

1.  [**WM \_繪製**](../gdi/wm-paint.md)。 呼叫 [**IVMRWindowlessControl：： RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo)。 這個方法會導致 VMR-7 重新繪製最新的影片畫面。
2.  [**WM \_DISPLAYCHANGE**](../gdi/wm-displaychange.md)： Call [**IVMRWindowlessControl：:D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged)。 這個方法會通知 VMR-7 影片必須在新的解析度或色彩深度上顯示。
3.  [**WM \_大小**](../winmsg/wm-size.md) 或 [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md)：重新計算影片的位置並呼叫 [**IVMRWindowlessControl：： SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) ，以更新位置（如有需要）。

**VMR-9**

1.  [**WM \_繪製**](../gdi/wm-paint.md)。 呼叫 [**IVMRWindowlessControl9：： RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo)。 這個方法會導致 VMR-9 重新繪製最新的影片畫面。
2.  [**WM \_DISPLAYCHANGE**](../gdi/wm-displaychange.md)： Call [**IVMRWindowlessControl9：:D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged)。 這個方法會通知 VMR-9 影片必須以新的解析度或色彩深度顯示。
3.  [**WM \_大小**](../winmsg/wm-size.md) 或 [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md)：重新計算影片的位置並呼叫 [**IVMRWindowlessControl9：： SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) ，以更新位置（如有需要）。

> [!Note]  
> [**Wm \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md)訊息的預設處理常式會傳送 [**wm \_ 大小**](../winmsg/wm-size.md)的訊息。 但是，如果您的應用程式會攔截 **wm \_ WINDOWPOSCHANGED** ，而不將它傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，您應該在 **Wm \_ WINDOWPOSCHANGED** 處理常式中呼叫 **SetVideoPosition** ，除了您的 **wm \_ 大小** 處理常式。

 

下列範例顯示 [**WM \_ 油漆**](../gdi/wm-paint.md) 訊息處理常式。 它會繪製用戶端矩形所定義的區域減去影片矩形。 請勿在影片矩形上繪製，因為 VMR 會在其上繪製，導致閃爍。 基於相同的原因，請勿在視窗類別中設定背景筆刷。


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



雖然您必須回應 [**wm \_ 油漆**](../gdi/wm-paint.md) 訊息，但您不需要在 **wm \_ 油漆** 訊息之間執行任何動作來更新影片。 如這個範例所示，無視窗模式可讓您將影片影像視為視窗上的自我繪圖區域。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片混合轉譯器](using-the-video-mixing-renderer.md)
</dt> <dt>

[影片轉譯](video-rendering.md)
</dt> </dl>

 

 
