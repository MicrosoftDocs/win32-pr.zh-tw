---
description: 增強型影片轉譯器 (EVR) 是在使用者監視器上顯示影片的元件。
ms.assetid: 1c985558-d25d-4f51-978a-58c05943dab9
title: 增強的影片轉譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0881da0827e6cc757a0ea855bcb51864dd98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317972"
---
# <a name="enhanced-video-renderer"></a>增強的影片轉譯器

增強型影片轉譯器 (EVR) 是在使用者的監視器上顯示影片的元件。 有兩個版本的 EVR 存在：

-   EVR 媒體接收，適用于媒體基礎應用程式。
-   EVR 篩選器，適用于 DirectShow 應用程式。

這兩個版本都使用相同的內建物件來轉譯影片，並共用許多相同的介面。

EVR 最多可以混合16個影片串流。 第一個輸入資料流程稱為 *參考資料流*。 參考資料流一律會先出現在 z 順序中。 任何額外的資料流程都稱為 *子串流*，而且會在參考資料流上方混合。 應用程式可以變更子串流的迭置順序，但不能先以迭置順序來進行子流。

圖形驅動程式會決定支援的影片格式，但通常僅限於下列各項：

-   參考資料流：不含每圖元 Alpha (（例如 NV12 或 YUY2) ;）的漸進式或交錯式 YUV或漸進式 RGB。
-   子串流：每圖元 Alpha 的漸進 YUV，例如 AYUV 或 AI44。

可用的子資料流程格式可能取決於參考資料流的格式。 如需詳細資訊，請參閱 [EVR 媒體類型的協商](evr-media-type-negotiation.md)。

就內部而言，EVR 會使用稱為「 *混音* 器」的物件，將輸入資料流程中的畫面合成至一個介面以進行轉譯。 混音器也會執行去交錯和色彩校正。 混音器的輸出是最後一個合成的影片畫面。 第二個物件，稱為「展示 *者* 」會將影片畫面轉譯為顯示畫面。 展示者會在轉譯和管理 Direct3D 裝置時進行排程。 應用程式可以提供混音器或展示者的自訂執行。

輸出畫面播放速率會鎖定到參考資料流。 每當子串流收到新的框架時，混音器就會保留在其上。 當參考資料流收到新的框架時，會以子資料流程框架組成的混音器複合。  (如果參考資料流是交錯的，則完整的參考框架可能需要一個以上的媒體範例 ) 。當混音器等待參考框架時，子資料流程可能會接收多個框架。 在這種情況下，混音器只會捨棄先前的子串流框架。

由於展示者會建立 Direct3D 裝置，因此它也會負責與其他需要存取 DirectX Video 加速 (DXVA) 服務的管線物件共用裝置。 尤其是，EVR 混音器會使用 DXVA video 處理服務來逐行處理和混合影片。 在 EVR 的外部，軟體解碼器可能會使用 DXVA 來進行加速影片解碼。 展示者透過 [direct3d 裝置管理員](direct3d-device-manager.md)共用 direct3d 裝置。 下圖顯示 EVR 的內部架構。  (軟體解碼器（以灰色陰影呈現）不屬於 EVR。 ) 

![顯示 evr 的架構圖表。](images/5d4a1fd9-25ff-4cc5-a486-0d22f34bbfd7.gif)

## <a name="evr-interfaces"></a>EVR 介面

EVR 支援下列介面。 這些介面中有些是由混音器或展示者所執行。 針對每個介面，參考主題描述如何取得介面的指標。

| 介面                                                    | 描述                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)                 | 將 EVR 篩選器上的輸入圖釘數目設定 (DirectShow 僅) 。                                |
| [**IEVRFilterConfigEx**](/windows/desktop/api/evr/nn-evr-ievrfilterconfigex)             | 將 EVR 濾波器設定 (DirectShow 僅) 。                                                      |
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin)     | 讓 EVR 外掛程式轉譯受保護的影片。                                                 |
| [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)                 | 讓 EVR 展示者向混音器要求特定的畫面格。                             |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                 | 可讓品質管制員調整 EVR 的影片品質。                                      |
| [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) | 讓自訂混音器或展示者從 EVR 取得介面指標。                       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                 | 傳回 EVR 混音器或展示者的裝置識別碼。                                       |
| [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)     | 控制 EVR 顯示影片的方式。                                                              |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)           | Alpha-將靜態點陣圖影像與影片混合。                                                |
| [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)         | 控制增強型影片轉譯器 (EVR) 如何混合影片子串流。                            |
| [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2)       | 控制影片去交錯的喜好設定。                                                     |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)     | 將輸入影片串流上的位置對應到輸出影片資料流程上的對應位置。 |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)               | 由 EVR 展示者公開。                                                                     |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)               | 控制影片處理，包括調整、雜訊篩選和詳細資料篩選。               |
| [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)                 | 在 EVR 上設定混音器或展示者。                                                             |
| [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)   | 配置影片範例。                                                                          |



 

## <a name="in-this-section"></a>本節內容



| 主題                                                                    | 描述                                                                           |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [使用 DirectShow EVR 篩選器](using-the-directshow-evr-filter.md)   | 如何在 DirectShow 應用程式中使用 EVR。                                       |
| [使用 EVR 媒體接收](using-the-evr-media-sink.md)                 | 如何在媒體基礎應用程式中使用 EVR。                                 |
| [使用影片顯示控制項](using-the-video-display-controls.md) | 如何控制 EVR 在應用程式視窗內顯示影片的方式。 |
| [使用影片混音器控制項](using-the-video-mixer-controls.md)     | 如何控制 EVR 混音器的運作方式。                               |
| [EVR 媒體類型的協商](evr-media-type-negotiation.md)             | 描述 EVR 如何決定可接受哪些影片格式做為輸入。          |
| [自訂 Mixers](custom-mixers.md)                                       | 如何為 EVR 撰寫自訂混音器。                                              |
| [如何撰寫 EVR 展示者](how-to-write-an-evr-presenter.md)       | 如何撰寫 EVR 的自訂展示者。                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> </dl>

 

 



