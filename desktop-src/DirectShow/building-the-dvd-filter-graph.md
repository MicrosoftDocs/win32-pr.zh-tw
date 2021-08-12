---
description: 建立 DVD 篩選器 Graph
ms.assetid: 1d2f8284-2deb-4207-b067-24a54d6b286c
title: 建立 DVD 篩選器 Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049c8bc52fd382be863cdf5a0e6b124534e0b9280d28536abc58a6f4e64e81e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662644"
---
# <a name="building-the-dvd-filter-graph"></a>建立 DVD 篩選器 Graph

如同任何 DirectShow 的應用程式，DVD 播放應用程式一開始會先建立篩選圖形。 DirectShow 為 DVD 播放提供下列元件：

-   [DVD Graph Builder](dvd-graph-builder.md)。 建立篩選圖形的 helper 物件。 它會公開 [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) 介面。
-   [DVD 流覽](dvd-navigator-filter.md) 器篩選。 處理 DVD 播放、流覽和其他命令的 DirectShow 篩選。

DVD 播放也需要 MPEG-2 解碼器。 硬體和軟體 MPEG-2 解碼器可從協力廠商取得。 首先，建立 DVD Graph Builder 物件的實例。


```C++
IDvdGraphBuilder *pBuild = NULL;
hr = CoCreateInstance(CLSID_DvdGraphBuilder, NULL, 
    CLSCTX_INPROC_SERVER, IID_IDvdGraphBuilder, (void **)&pBuild);
```



至此，您可以在建立圖形的其餘部分之前，先選取並設定影片轉譯器。 此步驟是選擇性的，在下一節中會更詳細地說明。 如果您省略這個步驟，DVD Graph Builder 會選取預設轉譯器。 接下來，藉由呼叫 [**IDvdGraphBuilder：： RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) 方法來建立圖形。


```C++
AM_DVD_RENDERSTATUS buildStatus;
hr = pBuild->RenderDvdVideoVolume(L"Z:\\video_ts", 0, &buildStatus);
```



第一個參數是包含 DVD 檔案的目錄名稱。 在 DVD 光碟上，這些檔案位於名為 VIDEO TS 的目錄中 \_ 。 如果第一個參數是 **Null**，則 dvd Graph 產生器會使用第一個包含 DVD 磁片區的磁片磁碟機。

第二個參數包含各種選擇性旗標，可用於選擇 (硬體或軟體) 和其他選項的解碼器類型。

第三個參數是可接收狀態資訊的 [**AM \_ DVD \_ RENDERSTATUS**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) 結構。 如果 [**RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) 方法傳回 \_ FALSE，則表示呼叫部分成功 (或部分失敗，如果您是 pessimist) 。 例如，即使已成功轉譯其他資料流程，方法還是可能無法轉譯子圖片資料流程。 如果 **RenderDvdVideoVolume** 方法傳回錯誤碼或值 \_ FALSE，您可以檢查 **AM \_ DVD \_ RENDERSTATUS** 結構，以取得錯誤的詳細資料。

接下來，藉由呼叫 [**IDvdGraphBuilder：： GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph)來取得篩選 Graph 管理員的指標。 這個方法會傳回篩選 Graph 管理員 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)介面的指標。


```C++
IGraphBuilder *pGraph = NULL;
hr =  pBuild->GetFiltergraph(&m_pGraph);
```



使用 [**IDvdGraphBuilder：： GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) 方法來取出 DVD 相關的介面，包括下列各項：

-   [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)。 控制播放和 DVD 命令
-   [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)。 傳回 DVD 導覽器目前狀態的相關資訊。
-   [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder)。 控制隱藏式輔助字幕顯示。 預設會啟用隱藏式輔助字幕顯示。 若要停用它[](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) ，請使用 AM \_ L21 \_ CCSTATE \_ Off 旗標來呼叫 IAMLine21Decoder：： SetServiceState。
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)。 控制音訊音量和餘額。

例如，下列程式碼會傳回 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 介面。


```C++
IDvdControl2 *pDvdControl = NULL;
hr = pBuild->GetDvdInterface(IID_IDvdControl2, (void**)&pDvdControl);
```



建立 dvd 播放篩選圖形的建議方式是讓[dvd Graph Builder](dvd-graph-builder.md)物件自動為您進行。 這種方法在下面和 DVD 範例應用程式中示範。 如果您需要手動建立 DVD 篩選圖形，您可以遵循 DirectShow 檔中其他位置所討論之圖形建築物的基本規則來進行。 一般而言，您不應該手動新增、移除、連接或中斷 DVD Graph 產生器所建立之圖形中的個別篩選器，因為這樣做可能會使清除程式碼混淆。

設定影片轉譯器

DirectShow 提供數個影片轉譯器篩選器。 建立圖形之前，您可以選擇您偏好的影片轉譯器。 藉由呼叫 [**IDvdGraphBuilder：： GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) 並要求該轉譯器的特定介面，來選取轉譯器：

-   覆迭 Mixer 篩選： [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo)。
-   影片混合轉譯器 7 (VMR-7) ： [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig)。
-   影片混合轉譯器 9 (VMR-9) ： [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9)。
-   增強的影片轉譯器 (EVR) ： [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)。

如果您在建立篩選圖形之前要求這些介面中的任何一項，DVD Graph Builder 會建立對應的影片轉譯器。 之後，當您建立圖形時，DVD Graph Builder 會嘗試使用該轉譯器。 但是，如果無法使用您選取的轉譯器來建立圖形，它可能會切換至另一個轉譯器。 例如，您的 mpeg-2 解碼器可能與 VMR 篩選器不相容，在這種情況下，DVD Graph Builder 會預設為重迭 Mixer。

這些介面也會讓您有機會在連接至解碼器之前，先設定轉譯器。 例如，您可以將 VMR 設定為使用無視窗模式，而不是預設的視窗模式。 如需影片轉譯器的詳細資訊，請參閱[DirectShow 中的影片](about-video-rendering-in-directshow.md)轉譯主題。

在 Windows XP 和更新版本上，除非下列情況，否則 DVD Graph Builder 一律會使用[影片混合](video-mixing-renderer-filter-7.md)轉譯器 7 (VMR-7) 

-   呼叫端查詢介面只會找到覆迭 [Mixer](overlay-mixer-filter.md)，例如 [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2)。 這會將提示傳送給 DVD Graph 產生器，讓應用程式想要使用重迭 Mixer 而不是 VMR。 Windows Media Player 也有一個對話方塊選項，可強制使用重迭 Mixer。
-   安裝的解碼器與 VMR 不相容。 在圖形建立期間，會使用新的 [**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) 介面來檢查解碼器的 VMR 支援。 如果不存在，則 DVD Graph Builder 將會使用重迭 Mixer。
-   使用硬體解碼器時，解碼器無法連線到 [影片埠管理員](video-port-manager.md) (VPM) 。 如果硬體解碼器無法使用 VPM，則它無法使用 VMR，因此 DVD Graph Builder 接著會嘗試使用重迭 Mixer 來建立圖形。
-   已知顯示配接器的資源和/或功能不足，無法支援 VMR，但無法在驅動程式中正確地報告。  (某些已知案例是由 DVD Graph 產生器明確排除。 ) 
-   基於任何原因，解碼器與 VMR 之間的連接失敗，通常是因為缺乏 VRAM 來建立必要的表面。 在這些情況下，DVD Graph Builder 會關閉 VMR 使用，並嘗試使用重迭 Mixer 來建立圖形。

視窗模式

在視窗模式中 (重迭 Mixer 或 VMR) ，轉譯器會建立自己的影片視窗。 若要將此視窗設為應用程式視窗的子系，請使用應用程式的控制碼來呼叫 [**IVideoWindow：:p 的 ui \_ 擁有**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) 者。 此外，也請呼叫 [**IVideoWindow：:p 的 \_ system.windows.window.windowstyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) ， \_ 在轉譯器的影片視窗上設定 WS 子系和 ws \_ CLIPSIBLINGS 樣式。 若要從轉譯器的影片視窗取得滑鼠訊息，請使用應用程式視窗的控制碼來呼叫 [**IVideoWindow：:p 的 \_ MessageDrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) 。 這個方法會設定「訊息清空」—影片視窗會將接收到的任何滑鼠訊息轉寄至「訊息清空」視窗。


```C++
pVideoWindow->put_Owner((OAHWND)hwnd);
pVideoWindow->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
pVideoWindow->put_MessageDrain((OAHWND)hwnd) ;
```



郵件清空讓選取 DVD 功能表按鈕稍微複雜一點。 假設影片視窗未填滿應用程式的整個工作區，則有些滑鼠事件會落在影片視窗之外。 當您從影片視窗 *內* 取得滑鼠事件時，您應該處理它以進行 DVD 功能表導覽。 不應處理影片視窗 *外* 的滑鼠事件。 在訊息清空的情況下，沒有辦法區分兩者。 此外，影片視窗中滑鼠事件的座標是相對於影片視窗的工作區。但從影片視窗外部的滑鼠事件是相對於應用程式的工作區。

無視窗模式

無視窗模式可避免整個滑鼠訊息的問題。 因為 VMR (或 EVR) 不會在無視窗模式中建立自己的視窗，所以不需要訊息清空。 相反地，它會直接在您的應用程式視窗上進行繪製。 如果目的地矩形小於應用程式工作區，則在計算 DVD 按鈕位置時，DVD 導覽器會將此納入考慮。 因此，當您取得滑鼠訊息時，可以將座標直接傳遞至 DVD 導覽器，如一節的功能表導覽所述。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 
