---
description: VMR 無視窗模式
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: VMR 無視窗模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193f672e0fc1e3dced4bdff16da0e85123079eb94f2ac3c5fdb302b67c9432b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830580"
---
# <a name="vmr-windowless-mode"></a>VMR 無視窗模式

無視窗模式是應用程式在應用程式視窗內轉譯影片的慣用方式。 在無視窗模式中，影片混合轉譯器不會載入其視窗管理員元件，因此不支援 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 或 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面。 相反地，應用程式會提供播放視窗，並在工作區中設定目的地矩形，讓 VMR 繪製影片。 VMR 會使用 DirectDraw 的 clipper 物件，以確保影片會裁剪到應用程式的視窗，且不會出現在任何其他視窗上。 VMR 不會將應用程式的視窗子類別化，也不會安裝任何系統/進程勾點。

在無視窗模式中，連接期間的事件順序以及轉換至執行狀態的順序如下：

-   上游篩選器會提出 VMR 可接受或拒絕的媒體類型。
-   如果媒體類型為 [已接受]，VMR 會呼叫配置器提供者來取得 DirectDraw 表面。 如果介面已成功建立，則圖釘會連線，而且 VMR 已準備好轉換成執行狀態。
-   當篩選圖形執行時，此解碼器會呼叫 **GetBuffer** 以從配置器取得媒體範例。 VMR 會查詢配置器提供者，以確保其 DirectDraw 介面上的圖元深度、矩形大小和其他參數與內送影片相容。 如果相容，VMR 會將 DirectDraw 介面傳回給解碼器。 在解碼器解碼成介面之後，VMR 的核心同步處理單位會驗證時間戳記。 此單元會封鎖 **接收** 呼叫，直到呈現時間到達為止。 此時，VMR 會在配置器顯示器上呼叫 **PresentImage** ，以呈現圖形配接器的介面。

下圖顯示具有多個輸入資料流程的無視窗模式 VMR。

![以無視窗模式 vmr](images/vmr-windowless-mult-streams.png)

**設定無視窗模式的 VMR-7**

若要設定無視窗模式的 VMR-7，請在連接任何 VMR 的輸入圖釘之前，執行下列所有步驟：

1.  建立篩選器，並將它新增至圖形。
2.  使用 VMRMode 無視窗旗標呼叫 [**IVMRFilterConfig：： SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) 方法 \_ 。
3.  （選擇性）藉由呼叫 [**IVMRFilterConfig：： SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams)，設定多個輸入資料流程的 VMR。 VMR 會建立每個資料流程的輸入 pin。 您可以使用 [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) 介面來設定資料流程的迭置順序和其他參數。 如需詳細資訊，請參閱 [使用多個資料流程 (混合模式) 的 VMR ](vmr-with-multiple-streams--mixing-mode.md)。

    如果您未呼叫 **SetNumberOfStreams**，VMR-7 會預設為一個輸入的 pin。 連接輸入連接之後，就無法變更 pin 數目。

4.  呼叫 [**IVMRWindowlessControl：： SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) ，以指定將出現轉譯影片的視窗。

完成這些步驟之後，您就可以連接 VMR 篩選器的輸入接點。 建立圖形的方式有很多種，例如直接連接釘選、使用智慧型連線方法（例如 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)），或使用 Capture Graph Builder 的 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法。 如需詳細資訊，請參閱 [一般 Graph-Building 技術](general-graph-building-techniques.md)。

若要設定影片在應用程式視窗中的位置，請呼叫 [**IVMRWindowlessControl：： SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) 方法。 [**IVMRWindowlessControl：： GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize)方法會傳回原生影片大小。 在播放期間，應用程式應該通知 VMR 下列 Windows 訊息：

-   WM \_ 油漆：呼叫 [**IVMRWindowlessControl：： RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) 來重新繪製影像。
-   WM \_ DISPLAYCHANGE： Call [**IVMRWindowlessControl：:D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged)。 VMR 會採取任何必要動作，以在新的解析度或色彩深度顯示影片。
-   WM \_ 大小：重新計算影片的位置，然後視需要再次呼叫 [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) 。

> [!Note]  
> MFC 應用程式必須定義空的 WM \_ ERASEBKGND 訊息處理常式，否則影片顯示區域將無法正確地重新繪製。

 

**設定無視窗模式的 VMR-9**

若要設定無視窗模式的 VMR-9，請使用針對無視窗模式 VMR-7 所述的步驟，但使用 [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) 和 [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) 介面。 唯一的差別在於 VMR-9 預設會建立四個輸入圖釘，而不是一個輸入 pin。 因此，如果您要混合四個以上的視頻串流，則只需要呼叫 **SetNumberOfStreams** 。

**範例程式碼**

下列程式碼示範如何建立 VMR-7 篩選器、將它新增至 DirectShow 篩選圖形，然後讓 VMR 進入無視窗模式。 若為 VMR-9，請使用 \_ **CoCreateInstance** 中的 CLSID VideoMixingRenderer9 和對應的 VMR-9 介面。


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用無視窗模式](using-windowless-mode.md)
</dt> </dl>

 

 



