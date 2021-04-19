---
description: 服務介面
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: 服務介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31687cc1c1283eb59c7731743eaf4ece0127b392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976786"
---
# <a name="service-interfaces"></a>服務介面

媒體基礎中的某些介面必須藉由呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得，而不是呼叫 **QueryInterface**。 [**GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)方法的運作方式類似于 QueryInterface，但有下列差異：

-   除了介面識別碼之外，還會採用服務識別碼 GUID。
-   它可以傳回另一個物件的指標，該物件會實介面，而不是傳回所查詢之原始物件的指標。

> [!Note]  
> [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)介面非常類似于一些其他 api 中使用的 **IServiceProvider** 介面。

 

*服務* 是透過 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)介面從特定物件類別取得的特定介面。 定義了下列服務。



| 服務識別碼                          | 介面                                                                                                                                | 可能公開此服務的物件                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| MF \_ 中繼資料 \_ 提供者 \_ 服務             | [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | 媒體來源                                                                                                                                     |
| MF \_ MEDIASOURCE \_ 服務                    | [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | 在 Windows 8.1 和更新版本中支援。<br/>                                                                                                    |
| MF \_ PMP \_ 伺服器 \_ 內容                    | [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     |  (PMP) 媒體會話的受保護媒體路徑。                                                                                                         |
| MF \_ 品質 \_ 服務                       | [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | 媒體來源。                                                                                                                                    |
| MF \_ 速率 \_ 控制 \_ 服務                  | [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | 媒體來源、媒體會話                                                                                                                      |
| MF \_ 速率 \_ 控制 \_ 服務                  | [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | 媒體來源、媒體接收器、媒體會話                                                                                                         |
| MF \_ 遠端 \_ PROXY                           | [**IMFRemoteProxy**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | 遠端物件的 proxy。                                                                                                                       |
| MF \_ 薩米文 \_ 服務                           | [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | 已同步的可存取媒體交換 (薩米) 媒體來源。                                                                                    |
| MF \_ 來源 \_ 表示 \_ 提供者 \_ 服務 | [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Sequencer 來源                                                                                                                                  |
| MF 時間 \_ 碼 \_ 服務                       | [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | ASF 媒體來源。                                                                                                                                 |
| MF \_ TOPONODE \_ 屬性 \_ 編輯器 \_ 服務    | [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | 媒體工作階段                                                                                                                                     |
| MF \_ 包裝 \_ 物件                         | [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | 包裝的物件                                                                                                                                   |
| MF \_ 包裝 \_ 緩衝區 \_ 服務                |                                                                                                                                          | 在 Windows 8.1 和更新版本中支援。<br/>                                                                                                    |
| MF \_ 包裝 \_ 範例 \_ SERVIC                 |                                                                                                                                          | 在 Windows 8.1 和更新版本中支援。<br/>                                                                                                    |
| MF \_ WORKQUEUE \_ 服務                     | [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | 媒體工作階段                                                                                                                                     |
| MFNET \_ SAVEJOB \_ 服務                     | [**IMFSaveJob**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | 位元組資料流程                                                                                                                                      |
| MFNETSOURCE \_ 統計資料 \_ 服務            | **IPropertyStore**                                                                                                                       | 網路來源。 使用此服務來取得網路統計資料。 請參閱 [**MFNETSOURCE \_ STATISTICS 屬性**](mfnetsource-statistics-property.md)。 |
| MR \_ 音訊 \_ 原則 \_ 服務                  | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | 音訊轉譯器                                                                                                                                    |
| MR \_ 緩衝區 \_ 服務                         | **IDirect3DSurface9**                                                                                                                    | DirectX 介面緩衝區                                                                                                                           |
| MR \_ CAPTURE \_ 原則 \_ 磁片區 \_ 服務        | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | 音訊捕獲來源                                                                                                                              |
| MR \_ 原則 \_ 磁片區 \_ 服務                 | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | 音訊轉譯器                                                                                                                                    |
| MR \_ 串流處理 \_ 大量 \_ 服務                 | [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | 音訊轉譯器                                                                                                                                    |
| MR \_ 影片 \_ 加速 \_ 服務            | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)、 [ **IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | 增強的影片轉譯器 (EVR)                                                                                                                      |
| MR \_ 影片 \_ 加速 \_ 服務            | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | DirectShow EVR 篩選器上的輸入釘                                                                                                           |
| MR \_ 影片 \_ 加速 \_ 服務            | [**IMFVideoSampleAllocator 介面**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | EVR 資料流程接收。                                                                                                                                 |
| MR \_ 影片 \_ 混音器 \_ 服務                   | EVR 混音器所公開的各種介面。 請參閱 [使用影片混音器控制項](using-the-video-mixer-controls.md)。                   | EVR                                                                                                                                               |
| MR \_ 影片 \_ 轉譯 \_ 服務                  | EVR 展示者公開的各種介面。 請參閱 [使用影片顯示控制項](using-the-video-display-controls.md)。           | EVR                                                                                                                                               |



 

您必須使用 [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 從下表所列的物件取得此資料表中所列的介面。

在某些情況下，介面會由一個物件類別以服務的形式傳回，並由另一個物件類別透過 **QueryInterface** 傳回。 每個介面的參考頁面會指出何時使用 [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 以及何時使用 **QueryInterface**。

> [!Caution]  
> 物件可能會以透過 **QueryInterface** 和 [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)傳回服務介面的方式來執行。 不過，在需要 **GetService** 時使用 **QueryInterface** 可能會在稍後導致相容性問題。

 

[**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)函式是協助程式函數，可查詢物件的 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) ，然後呼叫物件的 [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)方法。

## <a name="examples"></a>範例

下列範例會查詢媒體會話中的 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) ，並取得 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面。


```C++
IMFGetService *pGetService = NULL;
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = pMediaSession->QueryInterface(
    IID_IMFGetService, 
    (void**)&pGetService);

if (SUCCEEDED(hr))
{
    hr = pGetService->GetService(
        MF_RATE_CONTROL_SERVICE, 
        IID_IMFRateControl,
        (void**)&pRateControl);
}
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_REELEASE(pGetService);
SAFE_RELEASE(pRateControl);
```



下列範例相當於前一個範例，但使用 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 函式。


```C++
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = MFGetService(
    pMediaSession, 
    MF_RATE_CONTROL_SERVICE, 
    IID_IMFRateControl, 
    (void**) &pRateCtl 
); 
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_RELEASE(pRateControl);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFGetService 介面**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
</dt> <dt>

[媒體基礎平臺 Api](media-foundation-platform-apis.md)
</dt> </dl>

 

 




