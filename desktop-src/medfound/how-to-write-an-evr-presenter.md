---
description: 本文說明如何撰寫增強型影片轉譯器的自訂展示者 (EVR) 。
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: 如何撰寫 EVR 展示者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94933d9eb53b0b03105edc7056ace4fe73238d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551245"
---
# <a name="how-to-write-an-evr-presenter"></a>如何撰寫 EVR 展示者

本文說明如何撰寫增強型影片轉譯器的自訂展示者 (EVR) 。 自訂的簡報者可以與 DirectShow 和媒體基礎搭配使用;這兩種技術的介面和物件模型都相同，雖然作業的確切順序可能不同。

本主題中的範例程式碼是從 Windows SDK 中提供的 [EVRPresenter 範例](evrpresenter-sample.md)來調整。

本主題包含下列幾節：

-   [先決條件](#prerequisites)
-   [展示者物件模型](#presenter-object-model)
    -   [EVR 內的資料流程](#data-flow-inside-the-evr)
    -   [展示者狀態](#presenter-states)
    -   [展示者介面](#presenter-interfaces)
    -   [執行 IMFVideoDeviceID](#implementing-imfvideodeviceid)
    -   [執行 IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient)
    -   [執行 IMFVideoPresenter](#implementing-imfvideopresenter)
    -   [執行 IMFClockStateSink](#implementing-imfclockstatesink)
    -   [執行 IMFRateSupport](#implementing-imfratesupport)
    -   [將事件傳送至 EVR](#sending-events-to-the-evr)
-   [協商格式](#negotiating-formats)
-   [管理 Direct3D 裝置](#managing-the-direct3d-device)
    -   [配置 Direct3D 表面](#allocating-direct3d-surfaces)
    -   [追蹤範例](#tracking-samples)
-   [處理輸出](#processing-output)
    -   [重新繪製框架](#repainting-frames)
    -   [排程範例](#scheduling-samples)
    -   [呈現範例](#presenting-samples)
    -   [來源和目的地矩形](#source-and-destination-rectangles)
    -   [資料流程結尾](#end-of-stream)
-   [畫面逐步執行](#frame-stepping)
    -   [執行框架逐步執行](#implementing-frame-stepping)
-   [在 EVR 上設定展示者](#setting-the-presenter-on-the-evr)
    -   [在 DirectShow 中設定展示者](#setting-the-presenter-in-directshow)
    -   [在媒體基礎中設定展示者](#setting-the-presenter-in-media-foundation)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

撰寫自訂的簡報者之前，您應該先熟悉下列技術：

-   增強型影片轉譯器。 請參閱 [增強型影片](enhanced-video-renderer.md)轉譯器。
-   Direct3D 圖形。 您不需要瞭解3D 圖形來撰寫簡報者，但您必須知道如何建立 Direct3D 裝置並管理 Direct3D 介面。 如果您不熟悉 Direct3D，請閱讀 DirectX 圖形 SDK 檔中的「Direct3D 裝置」和「Direct3D 資源」章節。
-   DirectShow 篩選圖形或媒體基礎管線，取決於您的應用程式將用來呈現影片的技術。
-   [媒體基礎轉換](media-foundation-transforms.md)。 EVR 混音器是媒體基礎的轉換，而展示者會直接在混音器上呼叫方法。
-   執行 COM 物件。 展示者是同進程的無線程 COM 物件。

## <a name="presenter-object-model"></a>展示者物件模型

本節包含展示者物件模型和介面的總覽。

### <a name="data-flow-inside-the-evr"></a>EVR 內的資料流程

EVR 會使用兩個外掛程式元件來呈現影片： *混音* 器和展示 *者*。 如有需要，混音器會混合影片串流並 deinterlaces 影片。 展示者會繪製 (*，或在* 繪製每個畫面時，將影片) 顯示和排程。 應用程式可以將其中一個物件取代為自訂的執行。

EVR 有一或多個輸入資料流程，且混音器有對應的輸入資料流程數目。 資料流程0一律是 *參考資料流*。 其他資料流程是 *子串流*，混音器 Alpha 會混合到參考資料流上。 參考資料流會決定合成影片的主畫面格速率。 針對每個參考框架，混音器會從每個子串流取得最新的畫面格，並將其混合到參考框架，然後輸出單一複合框架。 如果有需要，混音器也會執行從 YUV 到 RGB 的去交錯和色彩轉換。 無論輸入資料流程的數目或影片格式為何，EVR 一律會將混音器插入影片管線中。 下圖說明此程式。

![顯示指向混音器之參考資料流和子資料流程的圖表，指向顯示](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

展示者會執行下列工作：

-   設定混音器上的輸出格式。 開始串流之前，展示者會在混音器的輸出資料流程上設定媒體類型。 此媒體類型會定義複合映射的格式。
-   建立 Direct3D 裝置。
-   配置 Direct3D 表面。 混音器會將複合框架 blits 至這些表面。
-   取得混音器的輸出。
-   排定畫面格的顯示時間。 EVR 會提供簡報時鐘，而展示者會根據此時鐘來排程畫面格。
-   使用 Direct3D 顯示每個畫面格。
-   執行畫面格逐步執行和清除。

### <a name="presenter-states"></a>展示者狀態

在任何時間，展示者都處於下列其中一種狀態：

-   *已啟動*。 EVR 的簡報時鐘正在執行。 展示者會在呈現時安排影片畫面。
-   已 *暫停*。 簡報時鐘已暫止。 展示者不會顯示任何新的範例，但會維護其排程範例的佇列。 如果收到新的範例，則展示者會將它們新增至佇列。
-   *已停止*。 表示時鐘已停止。 展示者會捨棄已排程的任何範例。
-   *關機*。 展示者會釋放與串流相關的任何資源，例如 Direct3D 介面。 這是展示者的初始狀態，以及呈現者終結之前的最終狀態。

在本主題的範例程式碼中，展示者狀態是以列舉表示：


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



當展示者處於關閉狀態時，某些作業無效。 範例程式碼會藉由呼叫 helper 方法來檢查此狀態：


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a>展示者介面

需要展示者才能執行下列介面：



| 介面                                                                | 描述                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | 當 EVR 的時鐘變更狀態時，通知簡報者。 請參閱 [執行 IMFClockStateSink](#implementing-imfclockstatesink)。                                   |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | 提供方法，讓管線中的應用程式和其他元件從展示者取得介面。                                                       |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | 讓展示者從 EVR 或混音器取得介面。 請參閱 [執行 IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient)。 |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | 確保展示者和混音器使用相容的技術。 請參閱 [執行 IMFVideoDeviceID](#implementing-imfvideodeviceid)。                          |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | 處理來自 EVR 的訊息。 請參閱 [執行 IMFVideoPresenter](#implementing-imfvideopresenter)。                                                             |



 

以下是選用介面：



| 介面                                                | 描述                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | 讓展示者能夠使用受保護的媒體。 如果您的展示者是受信任的元件，其設計目的是要在受保護的媒體路徑中 (PMP) ，請執行這個介面。 |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | 報告展示者支援的播放率範圍。 請參閱 [執行 IMFRateSupport](#implementing-imfratesupport)。                                         |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | 將輸出影片畫面上的座標組應到輸入影片畫面上的座標。                                                                                       |
| [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | 報告效能資訊。 EVR 會使用此資訊來進行品質控制管理。 此介面記載于 DirectShow SDK 中。                        |



 

您也可以提供介面讓應用程式與展示者進行通訊。 標準展示者會針對此用途來實行 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 介面。 您可以執行這個介面或定義自己的介面。 應用程式會在 EVR 上呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，以從展示者取得介面。 當 **MR_VIDEO_RENDER_SERVICE** 服務 GUID 時，EVR 會將 **GetService** 要求傳遞給展示者。

### <a name="implementing-imfvideodeviceid"></a>執行 IMFVideoDeviceID

[**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)介面包含一個方法 [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)，它會傳回裝置 GUID。 裝置 GUID 可確保展示者和混音器使用相容的技術。 如果裝置 Guid 不符，EVR 將無法初始化。

標準混音器和展示者都使用 Direct3D 9，其裝置 GUID 等於 **IID_IDirect3DDevice9**。 如果您想要搭配使用您的自訂展示者與標準混音器，則必須 **IID_IDirect3DDevice9** 簡報者的裝置 GUID。 如果您取代這兩個元件，則可以定義新的裝置 GUID。 本文的其餘部分將假設展示者使用 Direct3D 9。 以下是 [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)的標準實作為：


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



即使在展示者關閉的情況下，方法應該會成功。

### <a name="implementing-imftopologyservicelookupclient"></a>執行 IMFTopologyServiceLookupClient

[**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)介面可讓展示者從 EVR 和混音器取得介面指標，如下所示：

1.  當 EVR 初始化展示者時，它會呼叫展示者的 [**IMFTopologyServiceLookupClient：： InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) 方法。 引數是指向 EVR 之 [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) 介面的指標。
2.  展示者會呼叫 [**IMFTopologyServiceLookup：： LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) ，以從 EVR 或混音器取得介面指標。

[**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice)方法類似于 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)方法。 這兩種方法都會將服務 GUID 和介面識別碼 (IID) 做為輸入，但 **LookupService** 會傳回介面指標的陣列，而 **GetService** 會傳回單一指標。 不過在實務上，您一律可以將陣列大小設定為1。 查詢的物件取決於服務 GUID：

-   如果 **MR_VIDEO_RENDER_SERVICE** 服務 GUID，則會查詢 EVR。
-   如果 **MR_VIDEO_MIXER_SERVICE** 服務 GUID，則會查詢混音器。

在 [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)的執行中，從 EVR 取得下列介面：



| EVR 介面                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | 提供方法讓展示者將訊息傳送至 EVR。 此介面定義于 DirectShow SDK 中，因此訊息會遵循 DirectShow 事件的模式，而不是媒體基礎事件。<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**IMFClock**](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | 表示 EVR 的時鐘。 展示者會使用此介面來排程簡報的範例。 EVR 可在沒有時鐘的情況下執行，因此可能無法使用此介面。 如果沒有，請忽略 [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice)中的錯誤碼。<br/> 時鐘也會實 [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) 介面。 在媒體基礎管線中，時鐘會實 [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) 介面。 它不會在 DirectShow 中執行這個介面。<br/> |



 

從混音器取得下列介面：



| 混音器介面                              | Description                                                |
|----------------------------------------------|------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | 讓展示者與混音器進行通訊。       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | 讓展示者可以驗證混音器的裝置 GUID。 |



 

下列程式碼會實行 [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) 方法：


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



當從 [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) 取得的介面指標不再有效時，EVR 會呼叫 [**IMFTopologyServiceLookupClient：： ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers)。 在這個方法內，釋出所有介面指標，並將展示者狀態設定為 [已關閉]：


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



由於各種原因，EVR 會呼叫 [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) ，包括：

-   中斷連接或重新連接 (DirectShow) 的 pin，或 (媒體基礎) 新增或移除串流接收器。
-   變更格式。
-   設定新的時鐘。
-   EVR 的最終關機。

在展示者的存留期內，EVR 可能會呼叫 [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) 和 [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) 數次。

### <a name="implementing-imfvideopresenter"></a>執行 IMFVideoPresenter

[**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)介面會繼承 [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)並新增兩個方法：



| 方法                                                               | 描述                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | 傳回復合影片框架的媒體類型。 |
| [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | 指示展示者執行各種動作。      |



 

[**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype)方法會傳回展示者的媒體類型。  (如需設定媒體類型的詳細資訊，請參閱 [協商格式](#negotiating-formats)。 ) 媒體類型會以 [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) 介面指標的形式傳回。 下列範例假設展示者將媒體類型儲存為 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 指標。 若要從媒體類型取得 **IMFVideoMediaType** 介面，請呼叫 **QueryInterface**：


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



[**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)方法是 EVR 與展示者通訊的主要機制。 已定義下列訊息。 本主題的其餘部分會提供執行每個訊息的詳細資料。



| 訊息                                | 描述                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVP_MESSAGE_INVALIDATEMEDIATYPE** | 混音器的輸出媒體類型無效。 展示者應該使用混音器來協商新的媒體類型。 請參閱 [協商格式](#negotiating-formats)。                                                                                         |
| **MFVP_MESSAGE_BEGINSTREAMING**      | 串流已開始。 此訊息不需要任何特定動作，但您可以使用它來配置資源。                                                                                                                                 |
| **MFVP_MESSAGE_ENDSTREAMING**        | 串流已經結束。 釋放您為了回應 **MFVP_MESSAGE_BEGINSTREAMING** 訊息所配置的任何資源。                                                                                                                        |
| **MFVP_MESSAGE_PROCESSINPUTNOTIFY**  | 混音器已收到新的輸入範例，而且可能會產生新的輸出框架。 展示者應該在混音器上呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。 請參閱 [處理輸出](#processing-output)。 |
| **MFVP_MESSAGE_ENDOFSTREAM**         | 簡報已經結束。 請參閱 [資料流程的結尾](#end-of-stream)。                                                                                                                                                                                   |
| **MFVP_MESSAGE_FLUSH**               | EVR 正在清除其轉譯管線中的資料。 展示者應該捨棄任何已排程進行簡報的影片畫面。                                                                                                         |
| **MFVP_MESSAGE_STEP**                | 要求展示者逐步執行 N 個畫面格。 展示者應該捨棄下一個 N-1 的框架，並顯示第 n 個框架。 查看 [框架逐步執行](#frame-stepping)。                                                                                |
| **MFVP_MESSAGE_CANCELSTEP**          | 取消框架逐步執行。                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a>執行 IMFClockStateSink

展示者必須在其 [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)的實 [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)介面中執行，以繼承 **IMFClockStateSink**。 EVR 會使用此介面，在 EVR 的時鐘變更狀態時通知演講者。 如需有關時鐘狀態的詳細資訊，請參閱 [呈現頻率](presentation-clock.md)。

以下是在此介面中執行方法的一些指導方針。 如果展示者已關閉，所有方法都應該會失敗。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></td>
<td><ol>
<li>將展示者狀態設定為 [已啟動]。</li>
<li>如果未<strong>PRESENTATION_CURRENT_POSITION</strong> <em>llClockStartOffset</em> ，請清除展示者的範例佇列。  (這相當於接收 <strong>MFVP_MESSAGE_FLUSH</strong> 訊息。 ) </li>
<li>如果先前的框架步驟要求仍在擱置中，請處理要求 (查看 <a href="#frame-stepping">畫面格逐步執行</a>) 。 否則，請嘗試處理混音器的輸出 (查看 <a href="#processing-output">處理輸出</a>。</li>
</ol></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></td>
<td><ol>
<li>將展示者狀態設定為 [已停止]。</li>
<li>清除展示者的範例佇列。</li>
<li>取消任何暫止的框架步驟操作。</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></td>
<td>將展示者狀態設定為 [已暫停]。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></td>
<td>視為與 <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> 相同，但不會排清範例的佇列。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></td>
<td><ol>
<li>如果速率從0變更為非零值，則取消框架逐步執行。</li>
<li>儲存新的時脈速率。 顯示樣本時，頻率會受到影響。 如需詳細資訊，請參閱 <a href="#scheduling-samples">排程範例</a>。</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a>執行 IMFRateSupport

若要支援1×速度以外的播放率，展示者必須執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 介面。 以下是在此介面中執行方法的一些指導方針。 在展示者關閉之後，所有方法都應該會失敗。 如需此介面的詳細資訊，請參閱 [速率控制](rate-control.md)。



|                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | 傳回零以指出沒有最小的播放速率。                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | 若為非 thinned 播放，播放速率不應超過監視器的重新整理頻率：*最大速率* 重新整理  =  *頻率* (Hz) /*影片畫面播放速率* (fps) 。 影片畫面播放速率是在展示者的媒體類型中指定。 <br/> 針對 thinned 播放，播放速率為未系結;傳回 **FLT_MAX** 的值。 在實務上，來源和解碼器將會是 thinned 播放期間的限制因素。 <br/> 針對反向播放，傳回最大速率的負數。<br/> |
| [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | 如果 *flRate* 的絕對值超過展示者的播放速率上限，則傳回 **MF_E_UNSUPPORTED_RATE** 。 計算 [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)所述的最大播放速率。                                                                                                                                                                                                                                                                                    |



 

下列範例顯示如何執行 [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) 方法：


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



先前的範例會呼叫 helper 方法 GetMaxRate，以計算最大的向前播放速率：

下列範例顯示如何執行 [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) 方法：


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a>將事件傳送至 EVR

展示者必須通知 EVR 各種事件。 若要這樣做，它會使用 EVR 的 [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) 介面，此介面會在 EVR 呼叫展示者的 [**IMFTopologyServiceLookupClient：： InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) 方法時取得。  (**IMediaEventSink** 介面最初是一個 directshow 介面，但用於 directshow EVR 和媒體基礎。 ) 下列程式碼示範如何將事件傳送到 EVR：


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



下表列出展示者所傳送的事件，以及事件參數。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>事件</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></td>
<td>展示者已完成 MFVP_MESSAGE_ENDOFSTREAM 訊息之後的所有畫面格轉譯。<br/>
<ul>
<li><em>Param1</em>： HRESULT，指出作業的狀態。</li>
<li><em>Param2</em>：未使用。</li>
</ul>
如需詳細資訊，請參閱 <a href="#end-of-stream">資料流程的結尾</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></td>
<td>Direct3D 裝置已變更。<br/>
<ul>
<li><em>Param1</em>：未使用。</li>
<li><em>Param2</em>：未使用。</li>
</ul>
如需詳細資訊，請參閱 <a href="#managing-the-direct3d-device">管理 Direct3D 裝置</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></td>
<td>發生錯誤，需要串流處理停止。<br/>
<ul>
<li><em>Param1</em>： <strong>HRESULT</strong> ，表示發生的錯誤。</li>
<li><em>Param2</em>：未使用。</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></td>
<td>指定展示者花在轉譯每個畫面格的時間量。 (選擇性。)<br/>
<ul>
<li><em>Param1</em>：常數 <strong>LONGLONG</strong> 值的指標，其中包含處理框架的時間長度（以 100-毫微秒為單位）。</li>
<li><em>Param2</em>：未使用。</li>
</ul>
如需詳細資訊，請參閱 <a href="#processing-output">處理輸出</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></td>
<td>在轉譯範例中指定目前的延隔時間。 如果此值為正數，則樣本會落後排程。 如果值為負數，則範例會提前排程。 (選擇性。)<br/>
<ul>
<li><em>Param1</em>：常數 <strong>LONGLONG</strong> 值的指標，其中包含延隔時間（100-毫微秒單位）。</li>
<li><em>Param2</em>：未使用。</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></td>
<td>如果播放率為零，則會在 <strong>EC_STEP_COMPLETE</strong> 後立即傳送。 此事件包含所顯示框架的時間戳記。<br/>
<ul>
<li><em>Param1</em>：時間戳記的較低32位。</li>
<li><em>Param2</em>：時間戳記的上方32位。</li>
</ul>
如需詳細資訊，請參閱 <a href="#frame-stepping">框架逐步執行</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></td>
<td>展示者已完成或取消框架步驟。<br/>
<ul>
<li><em>Param1</em>：未使用。</li>
<li><em>Param2</em>：未使用。</li>
</ul>
如需詳細資訊，請參閱 <a href="#frame-stepping">框架逐步執行</a>。<br/>
<blockquote>
[!Note]<br />
先前版本的檔所述的 <em>Param1</em> 不正確。 此參數不適用於此事件。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a>協商格式

每當展示者收到來自 EVR 的 **MFVP_MESSAGE_INVALIDATEMEDIATYPE** 訊息時，就必須在混音器上設定輸出格式，如下所示：

1.  在混音器上呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以取得可能的輸出類型。 此類型描述混音器可產生的格式，並提供圖形裝置的輸入資料流程和影片處理功能。
2.  檢查展示者是否可以使用此媒體類型作為轉譯格式。 以下是要檢查的一些事項，雖然您的執行可能有自己的需求：

    -   影片必須未壓縮。
    -   影片必須只有漸進式框架。 檢查 [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) 屬性是否等於 **MFVideoInterlace_Progressive**。
    -   格式必須與 Direct3D 裝置相容。

    如果類型無法接受，請返回步驟1，並取得混音器下一個建議的類型。

3.  建立新的媒體類型，它是原始類型的複製，然後變更下列屬性：

    -   將 [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) 屬性設定為等於您要配置之 Direct3D 介面的寬度和高度。
    -   將 [ [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) ] 屬性設定為 [ **FALSE**]。
    -   將 [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) 屬性設定為等於顯示 (通常是 1:1) 。
    -   將幾何光圈 ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) 屬性) 等於 Direct3D 介面內的矩形。 當混音器產生輸出框架時，它會 blits 來源影像至此矩形。 幾何光圈可以像表面一樣大，也可以是表面內的 subrectangle。 如需詳細資訊，請參閱 [來源和目的地矩形](#source-and-destination-rectangles)。

4.  若要測試混音器是否會接受修改過的輸出類型，請使用 **MFT_SET_TYPE_TEST_ONLY** 旗標來呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 。 如果混音器拒絕該類型，請返回步驟1，並取得下一個類型。
5.  配置 direct3d 表面的集區，如配置 [direct3d](#allocating-direct3d-surfaces)介面中所述。 混音器會在繪製合成的影片框架時使用這些表面。
6.  藉由呼叫 [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) （沒有旗標）來設定混音器上的輸出類型。 如果在步驟4中第一次呼叫 **SetOutputType** 成功，此方法應該會再次成功。

如果混音器的類型不足， [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法會傳回 **MF_E_NO_MORE_TYPES**。 如果展示器找不到適合混音器的輸出類型，就無法轉譯資料流程。 在該情況下，DirectShow 或媒體基礎可能會嘗試另一個串流格式。 因此，在找到有效的型別之前，展示者可能會在一個資料列中接收數 **MFVP_MESSAGE_INVALIDATEMEDIATYPE** 的訊息。

混音器會自動 letterboxes 影片，將圖元外觀比例納入 (等同于來源和目的地的) 。 為了獲得最佳結果，表面寬度和高度和幾何光圈應等於您希望影片顯示在顯示器上的實際大小。 下圖說明此程式。

![此圖顯示的複合 fram 會導致 direct3d 介面，此介面會導致視窗](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

下列程式碼顯示程式的大綱。 某些步驟會放在 helper 函式中，而其確切詳細資料將取決於您的展示者需求。


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



如需影片媒體類型的詳細資訊，請參閱 [影片媒體類型](video-media-types.md)。

## <a name="managing-the-direct3d-device"></a>管理 Direct3D 裝置

展示者會建立 Direct3D 裝置，並處理串流期間的任何裝置遺失。 展示者也裝載了 Direct3D 裝置管理員，可讓其他元件使用相同的裝置。 例如，混音器會使用 Direct3D 裝置來混合子串流、逐行和執行色彩調整。 您可以使用 Direct3D 裝置來進行影片加速解碼。  (如需影片加速的詳細資訊，請參閱 [DirectX Video 加速 2.0](directx-video-acceleration-2-0.md). ) 

若要設定 Direct3D 裝置，請執行下列步驟：

1.  藉由呼叫 **Direct3DCreate9** 或 **Direct3DCreate9Ex** 來建立 Direct3D 物件。
2.  藉由呼叫 **IDirect3D9：： CreateDevice** 或 **IDirect3D9Ex：： CreateDevice** 來建立裝置。
3.  藉由呼叫 [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9)來建立裝置管理員。
4.  藉由呼叫 [**IDirect3DDeviceManager9：： ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)，在裝置管理員上設定裝置。

如果另一個管線元件需要裝置管理員，它會在 EVR 上呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，並指定服務 GUID 的 **MR_VIDEO_ACCELERATION_SERVICE** 。 EVR 會將要求傳送給展示者。 物件取得 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 指標之後，就可以呼叫 [**IDirect3DDeviceManager9：： OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle)來取得裝置的控制碼。 當物件需要使用裝置時，它會將裝置控制碼傳遞給 [**IDirect3DDeviceManager9：： LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) 方法，以傳回 **IDirect3DDevice9** 指標。

建立裝置之後，如果簡報者終結裝置並建立新裝置，則展示者必須再次呼叫 [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) 。 **ResetDevice** 方法會使任何現有的裝置控制碼失效，而導致 [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice)傳回 **DXVA2_E_NEW_VIDEO_DEVICE**。 此錯誤碼會向其他物件發出信號，而這些物件應該會開啟新的裝置控制碼。 如需使用 [裝置管理員] 的詳細資訊，請參閱 [Direct3D 裝置管理員](direct3d-device-manager.md)。

展示者可以在視窗模式或全螢幕獨佔模式中建立裝置。 針對視窗型模式，您應該提供方法讓應用程式指定影片視窗。 標準展示者會針對此用途來實行 [**IMFVideoDisplayControl：： SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) 方法。 第一次建立展示者時，您必須建立裝置。 一般來說，您不會知道所有的裝置參數，例如視窗或背景緩衝區格式。 您可以建立暫存裝置，並在稍後將它取代&\# ; 只要記得在裝置管理員上呼叫 [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) 。

如果您建立新的裝置，或在現有裝置上呼叫 **IDirect3DDevice9：： Reset** 或 **IDirect3DDevice9Ex：： ResetEx** ，請將 [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) 事件傳送至 EVR。 此事件會通知 EVR 重新協商媒體類型。 EVR 會忽略這個事件的事件參數。

### <a name="allocating-direct3d-surfaces"></a>配置 Direct3D 表面

在展示者設定媒體類型之後，它就可以配置用來寫入影片畫面的 Direct3D 表面。 介面必須符合展示者的媒體類型：

-   介面格式必須符合媒體子類型。 例如，如果 **MFVideoFormat_RGB24** 子類型，則必須將介面格式 **D3DFMT_X8R8G8B8**。 如需子類型和 Direct3D 格式的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。
-   介面寬度和高度必須符合媒體類型的 [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) 屬性中所提供的尺寸。

配置介面的建議方式，取決於簡報者是否以視窗方式執行或全螢幕。

如果 Direct3D 裝置在視窗中，您可以建立數個交換鏈，每個都有一個返回緩衝區。 使用這種方法，您可以單獨呈現每個介面，因為呈現一個交換鏈不會干擾其他交換鏈。 混音器可以將資料寫入介面，而另一個表面則是針對簡報進行排程。

首先，決定要建立多少個交換鏈。 建議最少3個。 針對每個交換鏈，請執行下列動作：

1.  呼叫 **IDirect3DDevice9：： CreateAdditionalSwapChain** 來建立交換鏈。
2.  呼叫 **IDirect3DSwapChain9：： GetBackBuffer** ，以取得交換鏈的背景緩衝區介面指標。
3.  呼叫 [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) 並傳入介面指標。 此函式會傳回影片範例物件的指標。 影片範例物件會實 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面，而展示者會使用這個介面，在展示者呼叫混音器的 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法時，將表面傳遞給混音器。 如需影片範例物件的詳細資訊，請參閱 [影片範例](video-samples.md)。
4.  將 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 指標儲存在佇列中。 在處理期間，展示者會從這個佇列提取範例，如 [處理輸出](#processing-output)中所述。
5.  保留 **IDirect3DSwapChain9** 指標的參考，因此不會釋放交換鏈。

在全螢幕專屬模式中，裝置不能有一個以上的交換鏈。 當您建立全螢幕裝置時，會隱含地建立此交換鏈。 交換鏈可以有一個以上的背景緩衝區。 但是，如果您在相同的交換鏈中寫入至另一個背景緩衝區時顯示一個後置緩衝區，則沒有任何簡單的方法可協調這兩個作業。 這是因為 Direct3D 執行介面翻轉的方式。 當您呼叫存在時，圖形驅動程式會更新圖形記憶體中的介面指標。 如果您在呼叫時保留任何 **IDirect3DSurface9** 指標，則會在 **目前****的呼叫傳回** 之後，指向不同的緩衝區。

最簡單的選項是建立一個交換鏈的影片範例。 如果您選擇此選項，請遵循針對視窗型模式所提供的相同步驟。 唯一的差別在於範例佇列包含單一影片範例。 另一個選項是建立螢幕上的介面，然後將它們 array.blit 至背景緩衝區。 您所建立的表面必須支援 [**IDirectXVideoProcessor：： VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) 方法，混音器會使用此方法來複合輸出畫面格。

### <a name="tracking-samples"></a>追蹤範例

當展示者第一次配置影片範例時，它會將它們放在佇列中。 當展示者需要從混音器取得新的框架時，就會從此佇列中繪製。 在混音器輸出框架之後，展示者會將範例移至第二個佇列。 第二個佇列適用于等待排程的呈現時間的範例。

為了讓您更輕鬆地追蹤每個範例的狀態，影片範例物件會執行 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 介面。 您可以使用此介面，如下所示：

1.  在您的展示者中執行 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。
2.  在排程的佇列中放置範例之前，請查詢 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 介面的影片範例物件。

3.  以您的回呼介面指標呼叫 [**IMFTrackedSample：： SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) 。
4.  當範例準備好進行簡報時，請將它從排程的佇列中移除、呈現，然後釋放範例的所有參考。
5.  此範例會叫用回呼。 在此情況下，不會刪除範例物件，因為在叫用回呼之前，它本身會保存參考計數。 )  (
6.  在回呼中，將範例傳回到可用的佇列。

展示者不需要使用 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 來追蹤範例;您可以實行任何最適合您設計的技術。 **IMFTrackedSample** 的其中一個優點是，您可以將展示者的排程和轉譯功能移至 helper 物件中，而這些物件不需要任何特殊機制，就能在發行影片範例時回呼給展示者，因為範例物件提供了該機制。

下列程式碼顯示如何設定回呼：


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



在回呼中，呼叫非同步結果物件上的 [**IMFAsyncResult：： GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) 以取出範例的指標：


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock **_/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /_*_ End lock _*_/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a>處理輸出

只要混音器收到新的輸入範例，EVR 就會將 _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY** 訊息傳送給展示者。 此訊息表示混音器可能會有新的影片框架可供傳遞。 在回應中，展示者會在混音器上呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。 如果方法成功，則展示者會排定展示的範例。

若要從混音器取得輸出，請執行下列步驟：

1.  檢查時鐘狀態。 如果時鐘已暫停，除非這是第一個影片畫面，否則請忽略 **MFVP_MESSAGE_PROCESSINPUTNOTIFY** 的訊息。 如果時鐘正在執行，或這是第一個影片畫面，請繼續。
2.  從可用範例的佇列取得範例。 如果佇列是空的，則表示目前已排程所有配置的樣本進行呈現。 在這種情況下，請忽略目前的 **MFVP_MESSAGE_PROCESSINPUTNOTIFY** 訊息。 當下一個範例變成可用時，請重複此處所列的步驟。
3.   (選擇項。 ) 如果有可用的時鐘，請呼叫 [**IMFClock：： GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)取得目前的時鐘時間 (*T1*) 。
4.  在混音器上呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。 如果 **ProcessOutput** 成功，範例就會包含影片畫面。 如果方法失敗，請檢查傳回碼。 **ProcessOutput** 中的下列錯誤碼不是嚴重失敗：

    

    | 錯誤碼                              | 描述                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **MF_E_TRANSFORM_NEED_MORE_INPUT** | 混音器需要更多輸入，才能產生新的輸出框架。<br/> 如果您收到此錯誤碼，請檢查 EVR 是否已到達資料流程的結尾並據以回應，如 [資料流程結尾](#end-of-stream)所述。 否則，請忽略此 **MF_E_TRANSFORM_NEED_MORE_INPUT** 訊息。 當混音器取得更多輸入時，EVR 會傳送另一個。<br/> |
    | **MF_E_TRANSFORM_STREAM_CHANGE**    | 混音器的輸出類型已變成無效，可能是因為格式變更上游。<br/> 如果您收到此錯誤碼，請將展示者的媒體類型設為 **Null**。 EVR 會要求新的格式。<br/>                                                                                                                                                                         |
    | **MF_E_TRANSFORM_TYPE_NOT_SET**    | 混音器需要新的媒體類型。<br/> 如果您收到此錯誤碼，請重新協商混音器的輸出類型，如 [協商格式](#negotiating-formats)所述。<br/>                                                                                                                                                                                                        |

    

     

    如果 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 成功，請繼續。

5.   (選擇項。 ) 如果有可用的時鐘，請 (*T2*) 取得目前的時鐘時間。 混音器引進的延遲量是 (*T2*  -  *T1*) 。 將具有此值的 **EC_PROCESSING_LATENCY** 事件傳送至 EVR。 EVR 會使用此值來進行品質控制。 如果沒有可用的時鐘，就沒有理由傳送 **EC_PROCESSING_LATENCY** 事件。
6.   (選擇項。 ) 查詢範例以 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) ，並呼叫 [**IMFTrackedSample：： SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) ，如 [追蹤範例](#tracking-samples)中所述。
7.  排程簡報的範例。

在展示器取得混音器的任何輸出之前，這一系列的步驟都可以終止。 為確保不會卸載任何要求，您應該在發生下列情況時重複相同的步驟：

-   會呼叫展示者的 [**IMFClockStateSink：： OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) 或 **IMFClockStateSink：： OnClockStart** 方法。 這會處理混音器忽略輸入的情況，因為時鐘是在步驟 1)  (暫停。
-   叫用 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 回呼。 這會處理混音器收到輸入的情況，但 (步驟 2) 使用所有顯示者的影片範例。

接下來的幾個程式碼範例會更詳細地顯示這些步驟。 展示者會在 `ProcessInputNotify` 取得 **MFVP_MESSAGE_PROCESSINPUTNOTIFY** 訊息時，呼叫方法 (下列範例所示) 。


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



這個 `ProcessInputNotify` 方法會設定布林值旗標，以記錄混音器有新輸入的事實。 然後，它會呼叫 `ProcessOutputLoop` 方法，如下一個範例所示。 這個方法會嘗試從混音器提取盡可能多的樣本：


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



`ProcessOutput`下一個範例所示的方法會嘗試從混音器取得單一的影片畫面。 如果沒有可用的影片畫面，會傳回 `ProcessSample` S_FALSE 或錯誤碼，而這兩個程式碼都會中斷中的迴圈 `ProcessOutputLoop` 。 大部分的工作都是在方法中完成 `ProcessOutput` ：


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



關於此範例的一些備註：

-   *M_SamplePool* 變數會假設為包含可用影片範例佇列的集合物件。 如果佇列是空的，則物件的 `GetSample` 方法會傳回 **MF_E_SAMPLEALLOCATOR_EMPTY** 。
-   如果混音器的 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法傳回 MF_E_TRANSFORM_NEED_MORE_INPUT，則表示混音器無法產生任何輸出，因此展示者會清除 *m_fSampleNotify* 旗標。
-   `TrackSample`設定 [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)回呼的方法會顯示在「[追蹤範例](#tracking-samples)」一節中。

### <a name="repainting-frames"></a>重新繪製框架

有時候，顯示者可能需要重新繪製最新的影片畫面。 例如，標準展示者會在下列情況中重新繪製框架：

-   在視窗模式下，回應應用程式視窗所接收的 **WM_PAINT** 訊息。 請參閱 [**IMFVideoDisplayControl：： RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo)。
-   當應用程式呼叫 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)時，如果目的地矩形變更。

使用下列步驟來要求混音器重新建立最新的框架：

1.  從佇列取得影片範例。
2.  查詢 [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) 介面的範例。
3.  呼叫 [**IMFDesiredSample：： SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration)。 指定最新影片畫面的時間戳記。  (您將需要快取此值，並為每個畫面格進行更新。 ) 
4.  在混音器上呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。

重新繪製框架時，您可以忽略簡報時鐘並立即呈現畫面格。

### <a name="scheduling-samples"></a>排程範例

影片框架隨時都可以觸及 EVR。 展示者負責根據框架的時間戳記，以正確的時間呈現每個畫面格。 當展示者從混音器取得新的範例時，它會將範例放在已排程的佇列上。 在不同的執行緒上，展示者會持續從佇列的標頭取得第一個範例，並決定是否要：

-   顯示範例。
-   將範例保留在佇列中，因為它是早期的。
-   捨棄範例，因為它已延遲。 雖然您應該盡可能避免卸載畫面格，但您可能需要在展示者持續落後的情況下。

若要取得影片框架的時間戳記，請在影片範例上呼叫 [**IMFSample：： GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) 。 時間戳記相對於 EVR 的簡報時鐘。 若要取得目前的時鐘時間，請呼叫 [**IMFClock：： GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)。 如果 EVR 沒有呈現時鐘，或是範例沒有時間戳記，您可以在取得範例之後立即提出範例。

若要取得每個範例的持續時間，請呼叫 [**IMFSample：： GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration)。 如果範例沒有持續時間，您可以使用 [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) 函式來計算畫面播放速率的持續時間。

當您排程範例時，請記住下列事項：

-   如果播放速率比正常速度快或慢很多，則會以較快或較慢的速率執行時鐘。 這表示樣本上的時間戳記一律會提供相對於呈現時鐘的正確目標時間。 但是，如果您將簡報時間轉譯為一些其他的時鐘時間 (例如，高解析度效能計數器) ，您就必須根據頻率速度來調整時間。 如果頻率速度變更，EVR 會呼叫展示者的 [**IMFClockStateSink：： OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) 方法。
-   播放速率可以是反向播放的負數。 當播放速率為負數時，標記法會往後執行。 換句話說，在時間 *n* 前發生時間 *n* + 1。

下列範例會計算樣本的初期或晚期（相對於簡報時鐘）：


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



簡報時鐘通常是由系統時鐘或音訊轉譯器驅動。  (音訊轉譯器會從音效卡耗用音訊的速率衍生時間。 ) 一般情況下，簡報時鐘不會與監視器的重新整理頻率同步。

如果您的 Direct3D 展示參數指定表示間隔 **D3DPRESENT_INTERVAL_DEFAULT** 或 **D3DPRESENT_INTERVAL_ONE** ，則 **目前** 的作業會等待監視器的垂直回溯。 這是防止破壞的簡單方法，但會降低排程演算法的精確度。 相反地，如果呈現間隔是 **D3DPRESENT_INTERVAL_IMMEDIATE**，則 **目前** 的方法會立即執行，這會導致卸載，除非您的排程演算法精確地指出 **您只在** 垂直回溯期間內呼叫。

下列函數可協助您取得準確的計時資訊：

-   **IDirect3DDevice9：： GetRasterStatus** 會傳回有關點陣的資訊，包括目前的掃描行，以及點陣是否在垂直空白期間內。
-   **DwmGetCompositionTimingInfo** 會傳回桌面視窗管理員的計時資訊。 如果啟用桌面組合，這項資訊會很有用。

### <a name="presenting-samples"></a>呈現範例

本節假設您已針對每個介面建立個別的交換鏈，如配置 [Direct3D](#allocating-direct3d-surfaces)介面中所述。 若要呈現範例，請從影片範例取得交換鏈，如下所示：

1.  在影片範例上呼叫 [**IMFSample：： GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) ，以取得緩衝區。
2.  查詢緩衝區以取得 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。
3.  呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得 Direct3D 介面的 **IDirect3DSurface9** 介面。  (您可以藉由呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)，將此步驟和前一個步驟結合在一起。 ) 
4.  在介面上呼叫 **IDirect3DSurface9：： GetContainer** ，以取得交換鏈的指標。
5.  呼叫 **IDirect3DSwapChain9：:P** 在交換鏈上重新傳送。

下列程式碼顯示這些步驟：


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a>來源和目的地矩形

*來源矩形* 是要顯示的影片畫面部分。 它是相對於正規化座標系統所定義，在此系統中，整個影片框架都會佔用座標為 {0，0，1，1} 的矩形。 *目的地矩形* 是在繪製影片畫面的目的介面內的區域。 標準展示者可讓應用程式藉由呼叫 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)來設定這些矩形。

有幾個選項可套用來源和目的地矩形。 第一個選項是讓混音器適用：

-   使用 [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) 屬性設定來源矩形。 混音器會在 blits 影片至目的地介面時套用來源矩形。 混音器的預設來源矩形是整個框架。
-   將目的地矩形設定為混音器輸出類型中的幾何光圈。 如需詳細資訊，請參閱 [協商格式](#negotiating-formats)。

第二個選項是在 IDirect3DSwapChain9 時套用矩形 **：:P** ，方法是在 **目前** 的方法中指定 *pSourceRect* 和 *pDestRect* 參數。 您可以結合這些選項。 例如，您可以在混音器上設定來源矩形，但在 **目前** 的方法中套用目的地矩形。

如果應用程式變更目的地矩形或調整視窗大小，您可能需要配置新的表面。 如果是，您必須小心將此作業與排程執行緒同步處理。 在配置新的表面之前，先排清排程佇列並捨棄舊的範例。

### <a name="end-of-stream"></a>資料流程結尾

當 EVR 上的每個輸入資料流程都已結束時，EVR 會將 **MFVP_MESSAGE_ENDOFSTREAM** 訊息傳送給展示者。 但是，當您收到訊息時，可能會有一些要處理的影片畫面。 在您回應資料流程結束之前，您必須先清空混音器的所有輸出，並呈現所有其餘的畫面格。 顯示最後一個畫面格之後，將 **EC_COMPLETE** 事件傳送至 EVR。

下一個範例顯示在符合各種條件時傳送 **EC_COMPLETE** 事件的方法。 否則，它會傳回 S_OK 而不傳送事件：


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



這個方法會檢查下列狀態：

-   如果 *m_fSampleNotify* 變數為 **TRUE**，則表示混音器有一或多個尚未處理過的框架。  (需詳細資訊，請參閱 [處理輸出](#processing-output)) 。
-   *M_fEndStreaming* 變數是布林值旗標，其初始值 **為 FALSE**。 當 EVR 傳送 **MFVP_MESSAGE_ENDOFSTREAM** 訊息時，展示者會將旗標設定為 **TRUE** 。
-   只要有 `AreSamplesPending` 一或多個框架在已排程的佇列中等待，方法會假設為傳回 **TRUE** 。

在 [**IMFVideoPresenter：:P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) 方法中，將 *M_fEndStreaming* 設定為 **TRUE** ，並在 `CheckEndOfStream` EVR 傳送 **MFVP_MESSAGE_ENDOFSTREAM** 訊息時呼叫：


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



此外， `CheckEndOfStream` 如果混音器的 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法傳回 **MF_E_TRANSFORM_NEED_MORE_INPUT**，則呼叫。 此錯誤碼表示混音器沒有其他輸入範例 (請參閱 [處理輸出](#processing-output)) 。

## <a name="frame-stepping"></a>畫面逐步執行

EVR 的設計是為了支援在 DirectShow 中逐步執行，並在媒體基礎中進行清理。 框架逐步執行和清除在概念上類似。 在這兩種情況下，應用程式一次都會要求一個影片畫面。 在內部，展示者會使用相同的機制來執行這兩項功能。

DirectShow 中的框架逐步執行方式如下：

-   應用程式會呼叫 [**IVideoFrameStep：： Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step)。 *DwSteps* 參數中提供的步驟數目。 EVR 會將 **MFVP_MESSAGE_STEP** 訊息傳送給展示者，其中 (*ulParam*) 的訊息參數是步驟數目。
-   如果應用程式呼叫 [**IVideoFrameStep：： CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) 或變更圖形狀態 (執行中、已暫停或已停止) ，EVR 就會傳送 **MFVP_MESSAGE_CANCELSTEP** 訊息。

媒體基礎中的清除作業的運作方式如下：

-   應用程式會藉由呼叫 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)，將播放速率設定為零。
-   若要呈現新的框架，應用程式會以所需的位置呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 。 EVR 會傳送 *ulParam* 等於1的 **MFVP_MESSAGE_STEP** 訊息。
-   若要停止清除，應用程式會將播放速率設定為非零值。 EVR 會傳送 **MFVP_MESSAGE_CANCELSTEP** 訊息。

收到 **MFVP_MESSAGE_STEP** 訊息之後，展示者會等待目標框架到達。 如果步驟數目為 *N*，則展示者會捨棄下一個 (*n* -1) 範例，並提供 *N* 個範例。 當展示者完成框架步驟時，會將 [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) 事件傳送至 EVR，並將 *LParam1* 設定為 **FALSE**。 此外，如果播放率為零，則展示者會傳送 [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) 事件。 如果 EVR 在畫面格步驟作業仍處於暫止狀態時取消框架逐步執行，則展示者會傳送將 *lParam1* 設為 **TRUE** 的 **EC_STEP_COMPLETE** 事件。

應用程式可以執行多個步驟或清除多次，讓展示者在取得 **MFVP_MESSAGE_CANCELSTEP** 訊息之前，可能會收到多 **MFVP_MESSAGE_STEP** 的訊息。 此外，展示者也可以在時鐘開始之前或時鐘正在執行時，接收 **MFVP_MESSAGE_STEP** 訊息。

### <a name="implementing-frame-stepping"></a>執行框架逐步執行

本節說明用來執行框架逐步執行的演算法。 畫面逐步執行演算法使用下列變數：

-   *step_count*。 不帶正負號的整數，指定目前畫面執行作業中的步驟數目。
-   *step_queue*。 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)指標的佇列。
-   *step_state*。 在任何時候，展示者都可以是下列其中一種狀態，與畫面格逐步執行有關： 

    | 州         | 描述                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NOT_STEPPING | 不是畫面的逐步執行。                                                                                                                                                                                             |
    | 等候       | 展示者已收到 **MFVP_MESSAGE_STEP** 的訊息，但時鐘尚未啟動。                                                                                                                  |
    | PENDING       | 展示者已收到 **MFVP_MESSAGE_STEP** 的訊息，而且時鐘已開始，但展示者正在等候接收目標框架。                                                             |
    | 計畫     | 展示者已收到目標框架，並已將它排程為展示，但尚未呈現畫面格。                                                                                        |
    | 完成      | 展示者已顯示目標框架並傳送 [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) 事件，並且正在等候下一個 **MFVP_MESSAGE_STEP** 或 **MFVP_MESSAGE_CANCELSTEP** 訊息。 |

    

     

    這些狀態與展示 [者狀態](#presenter-states)中所列的展示者狀態無關。

下列程式是針對框架逐步執行演算法所定義：

PrepareFrameStep 程式

1.  遞增 *step_count*。
2.  將 *step_state* 設定為 [等待中]。
3.  如果時鐘正在執行，請呼叫 StartFrameStep。

StartFrameStep 程式

1.  如果 *step_state* 等於等候，請將 *STEP_STATE* 設定為擱置中。 針對 *step_queue* 中的每個範例，呼叫 DeliverFrameStepSample。
2.  如果 *step_state* 等於 NOT_STEPPING，請從 *step_queue* 中移除任何範例，並針對簡報進行排程。

CompleteFrameStep 程式

1.  將 *step_state* 設定為 [完成]。
2.  傳送具有 *lParam1*  =  **FALSE** 的 EC_STEP_COMPLETE 事件。
3.  如果頻率為零，請傳送 **EC_SCRUB_TIME** 事件與取樣時間。

DeliverFrameStepSample 程式

1.  如果頻率為零，且 *取樣時間*  +  *範例持續時間長度* 為零  <  **，請捨棄範例。 結束。
2.  如果 *step_state* 等於 [已排程] 或 [已完成]，請將範例新增至 *step_queue*。 結束。
3.  遞減 *step_count*。
4.  如果 *step_count* > 0，請捨棄範例。 結束。
5.  如果 *step_state* 等於等候，請將範例新增至 *step_queue*。 結束。
6.  排程簡報的範例。
7.  將 *step_state* 設定為 [已排程]。

CancelFrameStep 程式

1.  將 *step_state* 設定為 NOT_STEPPING
2.  將 *step_count* 重設為零。
3.  如果先前的 *step_state* 值為「等待中」、「擱置中」或「已排程」，則傳送具有 *lParam1*  =  **TRUE** 的 EC_STEP_COMPLETE。

呼叫這些程式，如下所示：



| 展示者訊息或方法                                                   | 程序           |
|-------------------------------------------------------------------------------|---------------------|
| **MFVP_MESSAGE_STEP** 訊息                                               | `PrepareFrameStep`  |
| **MFVP_MESSAGE_STEP** 訊息                                               | `CancelStep`        |
| [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) 回呼                         | `CompleteFrameStep` |
| [**IMFClockStateSink::OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

下列流程圖顯示畫面的逐步執行程式。

![顯示路徑的流程圖，其開頭為 mfvp \- message \- step and mfvp \- message \- processinputnotify and end at "state = complete"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a>在 EVR 上設定展示者

完成展示者後，下一個步驟是設定 EVR 來使用它。

### <a name="setting-the-presenter-in-directshow"></a>在 DirectShow 中設定展示者

在 DirectShow 應用程式中，在 EVR 上設定展示者，如下所示：

1.  藉由呼叫 **CoCreateInstance** 來建立 EVR 篩選。 **CLSID_ENHANCEDVIDEORENDERER** CLSID。
2.  將 EVR 新增至篩選圖形。
3.  建立您的展示者實例。 您的展示者可以透過 **IClassFactory** 支援標準 COM 物件建立，但這並不是必要的。
4.  查詢 [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) 介面的 EVR 篩選準則。
5.  呼叫 [**IMFVideoRenderer：： InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)。

### <a name="setting-the-presenter-in-media-foundation"></a>在媒體基礎中設定展示者

在媒體基礎中，您有數個選項，取決於您是建立 EVR 媒體接收器或 EVR 啟用物件。 如需啟用物件的詳細資訊，請參閱 [啟用物件](activation-objects.md)。

針對 EVR 媒體接收器，請執行下列動作：

1.  呼叫 [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) 來建立媒體接收器。
2.  建立您的展示者實例。
3.  查詢 EVR 媒體接收器中的 [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) 介面。
4.  呼叫 [**IMFVideoRenderer：： InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)。

針對 EVR 啟用物件，請執行下列動作：

1.  呼叫 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) 來建立啟用物件。
2.  在啟用物件上設定下列其中一個屬性： 

    | 屬性                                                                                                         | 描述                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_ACTI加值稅E**](mf-activate-custom-video-presenter-activate-attribute.md) | 展示者的啟用物件指標。<br/> 使用這個旗標時，您必須為您的展示者提供啟用物件。 啟用物件必須執行 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面。<br/> |
    | [**MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | 展示者的 CLSID。<br/> 使用這個旗標時，您的展示者必須支援透過 **IClassFactory** 建立標準 COM 物件。<br/>                                                                                         |

    

     

3.  （選擇性）在啟用物件上設定 [**MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> <dt>

[EVRPresenter 範例](evrpresenter-sample.md)
</dt> </dl>

 

 
