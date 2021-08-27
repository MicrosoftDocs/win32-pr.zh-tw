---
description: 重疊 Mixer 篩選器
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: 重疊 Mixer 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475726607f282ce4b7885ec6c5aea562c0380cb0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476984"
---
# <a name="overlay-mixer-filter"></a>重疊 Mixer 篩選器

覆迭 Mixer 篩選器是一種影片轉譯器，專為 DVD 播放和廣播影片串流（具有第21行的隱藏式輔助字幕）所設計。 覆迭 Mixer 也支援 (VPEs) 的影片埠擴充功能，讓它能夠使用硬體 mpeg-2 解碼器或類比 TV 調諧器，直接將影片傳送至圖形配接器，而不是透過 PCI 匯流排。

> [!Note]  
> 除非在 VPE 案例中，否則[影片混合](video-mixing-renderer-filter-9.md)轉譯器9現在優先于覆迭 Mixer 濾波器。

 

覆迭 Mixer 會使用 DirectDraw 來呈現。 圖形配接器上需要有重迭表面。 主要影片資料流程應連接到 pin 0。 次要串流 (隱藏式輔助字幕圖形或 DVD subpictures) 連接到圖釘1和更新版本。 覆迭 Mixer 將次要資料流程直接 blits 至主要 suface;它不會混搭或使用 Alpha blend。

覆迭 Mixer 使用影片轉譯器進行視窗管理。 影片轉譯器會連接到覆迭 Mixer 的輸出圖釘。

當應用程式使用 [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) 和 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面建立圖形時，會自動將此篩選新增至篩選圖形。 篩選 Graph 管理員將不會自動將重迭 Mixer 新增至圖形。

> [!Note]  
> 在下表中，輸入 pin 0 上接受的媒體子類型與硬體相依。 覆迭 Mixer 無法判斷是否支援特定的子類型，直到它建立 DirectDraw 介面為止。 因此，上游篩選器用來判斷是否支援子類型的唯一方法，是嘗試與該子類型的連接。

 




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>、 <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>、 <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>、 <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | |輸入 Pin 媒體類型 |主要類型： MEDIATYPE_Video<br /> 亞：<br /><ul><li>MEDIASUBTYPE_Overlay 只 (針腳 0) </li><li>DirectDraw YUV 格式 (僅限針腳 0) </li><li>DirectDraw 影片加速格式 (僅限針腳 0) </li><li> (所有輸入圖釘的 DirectDraw RGB 格式) </li></ul>格式類型：<br /><ul><li>Format_VIDEOINFO</li><li>Format_VIDEOINFO2</li></ul> | |輸入 Pin 介面 | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>、 <a href="ikspin.md"><strong>IKsPin</strong></a>、 <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig</strong></a>、 <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (引腳 0 only) 、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>、 <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | |輸出釘選媒體類型 |MEDIATYPE_Video，MEDIASUBTYPE_Overlay | |輸出 Pin 介面 | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |篩選 CLSID |CLSID_OverlayMixer | |屬性頁 CLSID |沒有屬性頁。 | |可執行檔 |qdvd.dll | | <a href="merit.md">業績</a> |MERIT_DO_NOT_USE | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>備註

覆迭 Mixer 使用目的地色彩金鑰組合來混合具有重迭的影片表面。 它會將色彩索引鍵和次要影片 blits 至主要表面，並將主要影片傳送至重迭表面。 然後，圖形配接器會將這兩個表面合成至其框架緩衝區。

若要測試圖形驅動程式是否支援硬體重迭，請呼叫 **IDirectDraw7：： GetCaps**。 如果 **DDCAPS** 結構中的 **dwMaxVisibleOverlays** 欄位大於零，驅動程式就會支援硬體重迭。

應用程式可以透過 [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2)介面控制重迭 Mixer 上的一些行為。 遊戲開發人員可以使用重迭 Mixer，以 DirectDraw 獨佔模式顯示影片，如本節稍後所述。 不過， [影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9) 現在可為遊戲中的影片提供更好的支援。 如需詳細資訊，請參閱 [使用影片混合](using-the-video-mixing-renderer.md)轉譯器。

下列資訊提供給篩選開發人員的優點，以及想要在 DirectDraw 獨佔模式中使用覆迭 Mixer 的遊戲開發人員。

**Mixer 內部作業重迭**

覆迭 Mixer 會公開每個內送資料流程的輸入 pin。 通常有三個輸入圖釘：適用于影片資料的 pin 0，以及第21行和 DVD 子圖片資料的針腳1和2。 就內部而言，重迭 Mixer 會建立包含整個桌面之主要介面的 DirectDraw 物件，再加上其矩形是由 Pin 0 上的影片資料流程大小定義的重迭表面。 如果此解碼器未指定色彩索引鍵，則重迭 Mixer 會使用預設色彩索引鍵：較新的圖形配接器為深色灰色，較舊的256色卡則為洋紅。

> [!Note]  
> 如果解碼器在重迭表面上的相同位置同時提供兩個次要影片串流，則結果為未定義。  (這種情況有時會發生在包含子圖片和第21行串流的 Dvd 中。 ) 影片可能會閃爍，或只顯示其中一個串流。

 

在 Windows Vista 或更新版本上，如果顯示器驅動程式支援硬體重迭，重迭 Mixer 會停用桌面視窗管理員 (DWM) 組合。 應用程式應該避免使用覆迭 Mixer 篩選;改為使用 VMR-9 或增強型影片轉譯器 (EVR) 。

**使用影片解碼的上游連線**

一般而言，重迭 Mixer 的輸入針腳會連接到上游視頻解碼器。 主要影片串流必須連接到 pin 0。 第21行或子圖片資料流程連接到 pin 1 或更大。 如果解碼器是僅使用主機 CPU 的軟體解碼器，則解碼器與 Pin 0 之間的連接是 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 連接。 如果此解碼器使用硬體加速，則 Pin 0 的連接必須使用 [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) 介面。 這兩種連線類型互斥。

如果此解碼器直接繪製在重迭表面上，它應該使用 pin 0 上的 [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) 介面，並執行 [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) 介面。

透過影片埠包裝硬體解碼器並連接到重迭 Mixer 的篩選準則，必須執行 [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)介面。 覆迭 Mixer 會實 [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify)介面。 這兩個介面可讓您指定所需的重迭表面，並可讓覆迭 Mixer 在視訊記憶體中通知這些表面位置的解碼器。

重迭 Mixer 也可確保影片矩形會正確地縮放。 影片捕獲牽涉到調整預覽影像和捕捉交錯的影片畫面方面的特定問題。 如果您正在開發硬體影片捕獲裝置的篩選或 WDM 驅動程式，請參閱 [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) 和 [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) 參考頁面，以取得有關這些主題的詳細資訊。

1394或 USB 捕獲案例中不會使用重迭 Mixer。 它會透過 PCI 匯流排在影片捕獲中使用。

**使用影片轉譯器的下游連接**

覆迭 Mixer 具有連接至[影片](video-renderer-filter.md)轉譯器篩選器的輸出 pin。 在此情況下，影片轉譯器不會轉譯影片;它只會管理影片視窗。

Pin 連接會使用 [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) 介面，而不是 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面。 影片轉譯器會透過覆迭 Mixer 將其視窗控制碼傳遞至 DirectDraw，以管理矩形剪輯。 應用程式可以透過篩選 Graph 管理員上的 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)和 [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2)介面，控制影片轉譯器。

**DirectDraw 獨佔模式**

覆迭 Mixer 的 DirectDraw 獨佔模式，可讓遊戲在螢幕的某個部分顯示影片。 在此模式中，重迭 Mixer 會將影片直接轉譯為遊戲應用程式所建立的 DirectDraw 介面，而不是影片轉譯器所提供的視窗。 這可讓遊戲控制色彩索引鍵。 覆迭 Mixer 在 DirectDraw 獨佔模式中只公開一個輸入 pin，這表示不能在此模式下執行行21或 DVD 子圖片的混合。

若要在 DirectDraw 獨佔模式中使用覆迭 Mixer，請建立重迭 Mixer 的實例，並在建立篩選圖形之前，針對 [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo)介面進行查詢。 然後呼叫 [**IDDrawExclModeVideo：： SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) 來指定用於轉譯的 DirectDraw 介面。 這種模式的一個重大限制是，遊戲無法存取實際的影片位。 如果您使用 **IDDrawExclModeVideo**，您的應用程式會建立主要介面，而重迭 Mixer 會建立重迭表面。

您也可以使用 DirectDraw 專屬模式來執行無視窗轉譯（例如，在網頁中），但不建議這樣做，因為覆迭 Mixer 不會在此模式中執行任何混合。 這表示不會顯示任何行21或子圖片資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




