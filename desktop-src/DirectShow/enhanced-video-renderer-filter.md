---
description: 增強型影片轉譯器 (EVR) 濾波器是16通道的視頻混音器和轉譯器。 它具有與媒體基礎 EVR 媒體接收相同的核心功能和外掛程式模型。
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: 增強的影片轉譯器篩選
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed63ba80864f98012a178ed775e5812ee5abe88
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475524"
---
# <a name="enhanced-video-renderer-filter"></a>增強的影片轉譯器篩選

> [!Note]  
> 本主題適用于 Windows Vista 和更新版本。

 

增強型影片轉譯器 (EVR) 濾波器是16通道的視頻混音器和轉譯器。 它具有與媒體基礎 EVR 媒體接收相同的核心功能和外掛程式模型。

DirectShow EVR 篩選器記載于媒體基礎 SDK 檔;如需詳細資訊，請參閱[增強型影片](../medfound/enhanced-video-renderer.md)轉譯器。




| | |透過<strong>QueryInterface</strong> (篩選介面) |DirectShow 介面：<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li></ul>媒體基礎介面：<br /><ul><li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></li></ul> | |輸入 Pin 媒體類型 |變數，視圖形驅動程式而定。 | |輸入 Pin 介面 (透過<strong>QueryInterface</strong>) |DirectShow 介面：<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul>媒體基礎介面：<br /><ul><li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></li><li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li></ul> | |輸出釘選媒體類型 |不適用。 | |輸出 Pin 介面 |不適用。 | |篩選 CLSID |CLSID_EnhancedVideoRenderer | |可執行檔 |evr.dll | | <a href="merit.md">業績</a> |MERIT_DO_NOT_USE | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>備註

除了透過 **QueryInterface** 公開的介面之外，EVR 還會透過 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 方法公開其他介面。 其中一些介面是由 EVR 展示者或 EVR 混音器所執行，而不是 EVR 本身。 如果應用程式在 EVR 上設定自訂的簡報者或混音器，自訂版本可能會公開一組不同的介面。



| Object     | 服務識別碼                                              | 介面                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVR 篩選 | MR \_ 影片 \_ 轉譯 \_ 服務 (查詢 EVR 或簡報者) <br/> | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| EVR 篩選 | MR \_ 影片 \_ 加速 \_ 服務 (查詢展示者) <br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| EVR 篩選 | MR \_ 影片 \_ 混音器 \_ 服務 (查詢混音器) <br/>             | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| 輸入 pin | MR \_ 影片 \_ 加速 \_ 服務                                | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

EVR 最多可以混合16個影片串流。 第一個輸入資料流程 (針腳 0) 稱為 *參考資料流*。 參考資料流一律會先出現在 z 順序中。 任何額外的資料流程都稱為子串流，而且會在參考資料流上方混合。 應用程式可以變更子串流的迭置順序，但不能先以迭置順序來進行子流。

圖形驅動程式會決定支援的影片格式，但通常僅限於下列各項：

-   參考資料流：不含每圖元 Alpha (（例如 NV12 或 YUY2) ;）的漸進式或交錯式 YUV或漸進式 RGB。
-   子串流：每圖元 Alpha 的漸進 YUV，例如 AYUV 或 AI44。

可用的子資料流程格式可能取決於參考資料流的格式。

EVR 會透過 pin 0 轉送向上游搜尋命令。 子流釘選不會轉寄搜尋命令。 來源或分隔器篩選準則的責任是讓子串流與參考資料流保持同步。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

