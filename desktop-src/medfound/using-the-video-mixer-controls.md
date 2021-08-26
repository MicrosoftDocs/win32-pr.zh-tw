---
description: 使用影片 Mixer 控制項
ms.assetid: 475996c6-a205-4133-8882-f55beaf9f8fd
title: 使用影片 Mixer 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72506a69cb1e3a8584a92cc7052541ffc210cd307073dece61f3a9d76a4c35d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887140"
---
# <a name="using-the-video-mixer-controls"></a>使用影片 Mixer 控制項

EVR 混音器提供數個介面，可讓應用程式用來控制混音器處理影片的方式。 這些介面可以在 DirectShow 或媒體基礎中使用。



| 介面                                                      | 描述                                                                                                                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) 介面   | Alpha-將靜態點陣圖影像混合到影片上。                                                                                                                                                                                          |
| [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) 介面 | 控制 EVR 混合影片子串流的方式。                                                                                                                                                                                                |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) 介面       | 控制色彩調整、影像篩選和其他影片處理功能。 這個介面可讓您存取圖形驅動程式所執行的功能，因此確切的功能將取決於使用者的圖形驅動程式。 |



 

取得這些介面指標的正確方式，取決於您使用的是 DirectShow 版本的 EVR 或媒體基礎版本。 針對媒體基礎 EVR，它也取決於您是直接使用 EVR 或透過 [媒體會話](media-session.md)使用。  (，應用程式通常會透過媒體會話使用 EVR，而不是直接) 。

若要取得這些介面的指標，請執行下列動作：

1.  取得 EVR 上 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面的指標。

    -   如果您使用 DirectShow EVR 篩選器，請在篩選器上呼叫 **QueryInterface** 。

    -   如果您直接使用 EVR 媒體接收，請在媒體接收器上呼叫 **QueryInterface** 。

    -   如果您使用媒體會話，請呼叫媒體會話上的 **QueryInterface** 。

2.  如果您使用媒體會話，請等候媒體會話傳送 [MESessionTopologyStatus](mesessiontopologystatus.md) 事件，其狀態值為 [已就緒的 MF TOPOSTATUS] \_ \_ 。 如果您不是使用媒體會話， (略過此步驟。 ) 

3.  呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 以取得混音器介面。 使用服務識別碼 MR 的 \_ 影片 \_ 混音器 \_ 服務。

## <a name="alpha-blending-a-bitmap-onto-the-video"></a>將點陣圖混合到影片上的 Alpha

您可以在播放期間使用 [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) 介面，將靜態點陣圖帶到影片上。 您可以在 Direct3D 介面中儲存點陣圖，並將其指定為 **IDirect3DSurface9** 指標，或使用 GDI 點陣圖。

如果您使用適用于點陣圖的 Direct3D 介面，此介面可包含每圖元的 Alpha 資料，而這會在混音器 Alpha-混合影像時使用。 或者，您可以定義色彩索引鍵，也就是在點陣圖中出現的任何地方都是透明的單一色彩。 此外，您也可以指定將套用至整個影像的 Alpha 值。 您也可以設定來源矩形來裁剪點陣圖，並設定目的地矩形以將點陣圖放置於影片框架內。

若要設定點陣圖，請呼叫 [**IMFVideoMixerBitmap：： SetAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap)。 這個方法會採用 [**MFVideoAlphaBitmap**](/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap) 結構的指標，此結構會指定點陣圖和 Alpha 混合參數。 如需範例程式碼，請參閱 **SetAlphaBitmap** 方法的參考主題。

設定點陣圖之後，您可以藉由呼叫 [**IMFVideoMixerBitmap：： UpdateAlphaBitmapParameters**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters)來更新混合參數，包括來源和目的地 recangles。 更新會在下一個影片畫面上生效。 必須播放影片，才能進行更新。 您可以使用這個方法，在點陣圖上執行簡單的動畫。  (如果您需要更複雜的效果，請考慮撰寫自訂的 EVR 混音器。 ) 

若要清除點陣圖，請呼叫 [**IMFVideoMixerBitmap：： ClearAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-clearalphabitmap)。

## <a name="controlling-substreams"></a>控制子串流

EVR 可將一或多個影片子串流混合到主要影片串流。 若要控制子流混合，請使用 [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) 介面。

-   呼叫 [**IMFVideoMixerControl：： SetStreamOutputRect**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamoutputrect) ，在複合的影片框架內設定子串流的位置。

-   呼叫 [**IMFVideoMixerControl：： SetStreamZOrder**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamzorder) 來設定子串流的迭置順序。 EVR 會以其 z 順序值的順序（從零開始）繪製影片串流。 主要影片資料流程一律會先以 z 順序排列。

## <a name="video-processor-settings"></a>影片處理器設定

EVR 混音器使用 DirectX Video 加速 (DXVA) 在輸入串流上執行影片處理。 確切的處理功能取決於圖形驅動程式。 影片處理功能是使用 [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) 結構來描述。 一組特定的功能稱為「 *影片處理模式*」，每個模式都是由 GUID 所識別。 如需預先定義的 Guid 清單，請參閱 [**IDirectXVideoProcessorService：： GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids)。 驅動程式可能會定義其他廠商專屬的 Guid，以代表不同的功能組合。

若要尋找支援的模式及每種模式的功能，請執行下列動作：

1.  呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，以取得混音器 [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) 介面的指標。

2.  呼叫 [**IMFVideoProcessor：： GetAvailableVideoProcessorModes**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes)。 這個方法會傳回 Guid 陣列，識別可用的視頻處理器模式。 清單會以遞減的品質順序傳回，最高品質的模式會先出現在清單中。 清單可以根據影片的格式而變更。

3.  針對清單中的每個 GUID，呼叫 [**IMFVideoProcessor：： GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) 以找出對應的視頻處理器模式的功能。 方法會以功能的描述填入 [**DXVA2 的 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) 結構。

4.  若要選取模式，請呼叫 [**IMFVideoProcessor：： SetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode)。 否則，EVR 會在串流處理開始時自動選取模式。 在這種情況下，您可以呼叫 [**IMFVideoProcessor：： GetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessormode) 來找出選取的模式。

[**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps)結構中大部分的欄位都會描述低層級的驅動程式行為，而且在一般應用程式中並不感興趣。 以下是最有可能感興趣的欄位：

-   **DeviceCaps**。 此欄位指出影片處理是否在硬體或軟體中執行，以及圖形驅動程式是否為較舊的 DXVA 1.0 驅動程式。

-   **DeinterlaceTechnology**。 如果來源影片是交錯的，則此欄位可提供您預期的去交錯品質層級的指示。

-   **ProcAmpControlCaps**。 此欄位會指定可用的色彩調整控制項。 如需可能的色彩調整清單，請參閱[ProcAmp 設定](procamp-settings.md)。 如果驅動程式無法執行色彩調整，則此欄位為零。

-   **VideoProcessorOperations**。 此欄位包含描述其他影片處理功能的旗標。 特定重要性的兩個旗標是 DXVA2 \_ VideoProcess \_ 子串流旗標和 DXVA2 \_ VideoProcess \_ 子串流旗標。 EVR 必須至少有其中一個旗標，才能將子串流混合到參考影片串流。 如果兩個旗標都不存在，則 EVR 會限制為一個影片串流。

-   **NoiseFilterTechnology**。 此欄位指出圖形驅動程式支援哪些雜訊篩選。 如果驅動程式不支援雜訊篩選，則此值為不 \_ 支援的 DXVA2 NoiseFilterTech \_ 。

-   **DetailFilterTechnology**。 此欄位會指出圖形驅動程式支援的詳細資料篩選。 如果驅動程式不支援雜訊篩選，則此值為不 \_ 支援的 DXVA2 DetailFilterTech \_ 。

## <a name="color-adjustment-and-image-filtering"></a>色彩調整和影像篩選

圖形驅動程式可能支援色彩調整 (也稱為「 *處理放大* 」或單純 *ProcAmp*) 和影像篩選。 當 GPU 執行時，可以即時完成色彩調整和影像篩選，而不會產生 CPU 額外負荷。

若要使用這些功能，請執行下列步驟：

1.  選取影片處理模式，如上一節所述。

2.  如前一節所述，呼叫 [**IMFVideoProcessor：： GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) 來尋找影片處理功能。 方法會填入描述功能的 [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) 結構，包括驅動程式是否支援色彩調整和影像篩選。

3.  針對驅動程式所支援的每個色彩調整，呼叫 [**IMFVideoProcessor：： GetProcAmpRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange) 來尋找該設定的可能值範圍。 這個方法也會傳回設定的預設值。 呼叫 [**IMFVideoProcessor：： GetProcAmpValues**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocampvalues) 來尋找設定的目前值。 值沒有指定的單位。 驅動程式是由驅動程式來定義值的範圍。

4.  呼叫 [**IMFVideoProcessor：： SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue) 來設定色彩調整值。

5.  如果驅動程式支援影像篩選，則每個篩選器類型 (雜訊和詳細資料) 支援三個設定（層級、半徑和臨界值），兩者都是在色度和 luma 中。  (參閱 [DXVA 影像篩選設定](dxva-image-filter-settings.md)) 。針對每個設定，請呼叫 [**IMFVideoProcessor：： GetFilteringRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange)以取得可能值的範圍，並呼叫 [**IMFVideoProcessor：： GetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringvalue)來取得目前的值。

6.  若要變更影像篩選設定，請呼叫 [**IMFVideoProcessor：： SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> </dl>

 

 



