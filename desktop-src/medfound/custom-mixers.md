---
description: 自訂 Mixers
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: 自訂 Mixers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7e56c578a7081de7c71ae3abaf9fc45d085827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999842"
---
# <a name="custom-mixers"></a>自訂 Mixers

本主題說明如何撰寫增強型影片轉譯器的自訂混音器 (EVR) 。 您可以使用自訂混音器搭配媒體基礎 EVR 媒體接收器或 DirectShow EVR 篩選器。 如需 mixers 和展示者的詳細資訊，請參閱 [增強型影片](enhanced-video-renderer.md)轉譯器。

混音器是一種媒體基礎轉換 (MFT) ，其中包含一或多個輸入 (參考資料流以及子串流) 和一個輸出。 輸入資料流程從上游接收樣本。 輸出資料流程會將範例提供給展示者。 EVR 負責呼叫混音器上的 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ，而展示者負責呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。

EVR 混音器至少必須執行下列介面：



| 介面                                                                | 描述                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | 提供基底 MFT 功能。                                                                 |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | 讓混音器從 EVR 取得介面。                                                |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | 讓混音器從 EVR 取得介面。                                                |
| [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | 用來將 [**MF \_ SA \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md) 屬性公開給 EVR。 |



 

（選擇性） MFT 可以執行下列任何介面：



| 介面                                                | 描述                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | 播放受保護的內容時需要。                                                                                                                  |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | 將介面（例如 [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) 和 [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) ）公開給應用程式。 |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | 可讓品質管制員調整影片品質。                                                                                             |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | 讓應用程式將靜態點陣圖混合到影片上。                                                                                       |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | 將輸出影片畫面上的座標組應到輸入影片畫面上的座標。                                                                  |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | 將部分 DXVA 的影片處理功能公開給應用程式。                                                                                      |



 

使用混音器的格式協調運作方式如下：

1.  EVR 會設定參考資料流上的媒體類型。
2.  EVR 會使用 **MFVP \_ MESSAGE \_ INVALIDATEMEDIATYPE** 訊息來呼叫展示者上的 [**IMFVideoPresenter：:P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) 。

3.  展示者會設定混音器輸出資料流程上的媒體類型。
4.  EVR 會設定子串流上的媒體類型。

如果參考資料流上的媒體類型變更，則混音器的其他媒體類型將不再有效。 混音器的 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法將會失敗，並傳回 **MF \_ E \_ 轉換 \_ 資料流程 \_ 變更**。 目前，展示者不應該在此時進行任何動作。 EVR 會再次起始格式的協商處理。

當任何輸入資料流程到達資料流程的結尾時，EVR 會在 rocessMessage 上呼叫 [**IMFTransform：:P**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) ，並以 [**MFT \_ 訊息 \_ 通知 \_ 結尾 \_ \_**](mft-message-notify-end-of-stream.md)。

混音器會使用 EVR 的 [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) 介面，將下列事件傳送至 EVR。 此介面記載于 DirectShow SDK 檔中。



| 事件                                            | 描述                            |
|--------------------------------------------------|----------------------------------------|
| [**\_需要 EC 範例 \_**](../directshow/ec-sample-needed.md) | 混音器需要新的輸入範例。 |



 

EVR 可能會在串流處理開始之前，于混音器上呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。 混音器不應該讓這些呼叫失敗。 相反地，它應該以黑色圖元填滿輸出介面。 混音器應該會繼續以色彩填滿輸出範例，直到它收到 [**MFT \_ 訊息 \_ 通知 \_ 開始 \_ 串流**](mft-message-notify-begin-streaming.md) 訊息或呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 方法為止。 如果混音器收到 [**MFT \_ 訊息 \_ 通知 \_ 結束 \_ 串流**](mft-message-notify-end-streaming.md) 訊息，則應該切換回色彩填滿模式。

## <a name="implementing-imfvideodeviceid"></a>執行 IMFVideoDeviceID

[**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)介面包含一個方法 [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)，它會傳回裝置 GUID。 裝置 GUID 可確保展示者和混音器使用相容的技術。 如果裝置 Guid 不符，EVR 將無法初始化。

標準混音器和展示者都使用 Direct3D 9，且裝置 GUID 等於 IID \_ IDirect3DDevice9。 如果您想要將您的自訂展示者與標準混音器搭配使用，則展示者的裝置 GUID 必須是 IID \_ IDirect3DDevice9。 如果您取代這兩個元件，則可以定義新的裝置 GUID。

## <a name="implementing-imftopologyservicelookupclient"></a>執行 IMFTopologyServiceLookupClient

混音器必須執行 [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) 介面。 開始串流之前，EVR 會呼叫 [**IMFTopologyServiceLookupClient：： InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) ，並將指標傳入 EVR 的 [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) 介面。 混音器會使用這個指標從 EVR 取得介面指標。

混音器至少必須查詢下列介面：

-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

當 EVR 呼叫 [**IMFTopologyServiceLookupClient：： ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers)時，混音器必須釋放從呼叫取得的任何指標至 [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)。

## <a name="mixer-attributes"></a>混音器屬性

混音器應該支援下列屬性。



| 屬性                                                                        | 描述                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ SA \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md)                          | 指定混音器是否支援 (DXVA) 的 DirectX Video 加速。                                                                                                                                                                               |
| [**MF \_ SA \_ 需求 \_ 範例 \_ 計數**](mf-sa-required-sample-count-attribute.md) | EVR 應該為每個混音器串流配置的影片樣本數。 這個屬性會套用至個別資料流程;使用 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)所傳回的屬性存放區。 |



 

## <a name="setting-the-mixer-on-the-evr"></a>在 EVR 上設定混音器

若要在 EVR 上設定自訂混音器，請呼叫 [**IMFVideoRenderer：： InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)。 DirectShow EVR 濾波器和 EVR 媒體接收器都會執行此方法。

**EVR 啟用物件**。 如果您使用 EVR 啟始物件，您可以在 EVR 啟用物件上設定下列其中一個屬性，以提供自訂混音器：



| 屬性                                                                                                 | 描述                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ 啟用**](mf-activate-custom-video-mixer-activate-attribute.md) | 混音器之啟用物件的指標。 啟用物件必須執行 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面。 |
| [**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)       | 混音器的 CLSID。                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> </dl>

 

 
