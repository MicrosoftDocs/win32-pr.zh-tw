---
description: DXVA 影片處理會封裝圖形硬體的功能，專門用來處理未壓縮的影片影像。 影片處理服務包含去交錯和影片混合。
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: DXVA 影片處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e38da7505e8ec877c332aaeb06f884c49a9ca590b239c603d4664bbf97131c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879679"
---
# <a name="dxva-video-processing"></a>DXVA 影片處理

DXVA 影片處理會封裝圖形硬體的功能，專門用來處理未壓縮的影片影像。 影片處理服務包含去交錯和影片混合。

本主題包含下列幾節：

-   [概觀](#overview)
-   [建立視頻處理裝置](#creating-a-video-processing-device)
    -   [取得 IDirectXVideoProcessorService 指標](#get-the-idirectxvideoprocessorservice-pointer)
    -   [列舉影片處理裝置](#enumerate-the-video-processing-devices)
    -   [列舉 Render-Target 格式](#enumerate-render-target-formats)
    -   [查詢裝置功能](#query-the-device-capabilities)
    -   [建立裝置](#create-the-device)
-   [影片流程 Array.blit](#video-process-blit)
    -   [Array.blit 參數](#blit-parameters)
    -   [輸入範例](#input-samples)
-   [影像組合](#image-composition)
    -   [範例1：上下黑邊縮](#example-1-letterboxing)
    -   [範例2：延展子串流映射](#example-2-stretching-substream-images)
    -   [範例3：不相符的資料流程高度](#example-3-mismatched-stream-heights)
    -   [範例4：目標矩形小於目的介面](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [範例5：來源矩形](#example-5-source-rectangles)
    -   [範例6：交集的目的地矩形](#example-6-intersecting-destination-rectangles)
    -   [範例7：延展和裁剪影片](#example-7-stretching-and-cropping-video)
-   [輸入範例順序](#input-sample-order)
    -   [範例 1](#example-1-letterboxing)
    -   [範例 2](#example-2-stretching-substream-images)
    -   [範例 3](#example-3-mismatched-stream-heights)
    -   [範例 4](#example-4-target-rectangle-smaller-than-destination-surface)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

圖形硬體可以使用圖形處理器 (GPU) 來處理未壓縮的影片影像。 *影片處理* 裝置是封裝這些功能的軟體元件。 應用程式可以使用影片處理裝置來執行下列功能：

-   去交錯和反向電視
-   將影片子串流混合到主要影片影像
-   色彩調整 (ProcAmp) 和影像篩選
-   影像縮放比例
-   色彩空間轉換
-   Alpha 混色

下圖顯示影片處理管線中的階段。 此圖表並非用來顯示實際的實作為。 例如，圖形驅動程式可能會將數個階段合併成單一作業。 所有這些作業都可以在視頻處理裝置的單一呼叫中執行。 驅動程式可能不支援此處顯示的一些階段，例如雜訊和詳細資料篩選。

![此圖顯示 dxva 影片處理的階段。](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

影片處理管線的輸入一律包含 *主要* 影片串流，其中包含主要影像資料。 主要影片串流決定輸出影片的畫面播放速率。 輸出影片的每個畫面格都會相對於主要影片串流的輸入資料進行計算。 主要資料流程中的圖元一律是不透明的，不含每圖元的 Alpha 資料。 主要影片串流可以是漸進式或交錯式。

（選擇性）影片處理管線最多可接收15個影片子串流。 子資料流程包含輔助的影像資料，例如隱藏式輔助字幕或 DVD subpictures。 這些影像會顯示在主要影片串流上，通常不會自行顯示。 子資料流程圖片可以包含每圖元的 Alpha 資料，而且一律是漸進式的框架。 影片處理裝置 Alpha-使用主要影片串流中的目前 deinterlaced 框架來混合子資料流程影像。

在本主題的其餘部分，將會使用「詞彙 *圖片* 」將輸入資料用於視頻處理裝置。 圖片可能由漸進式框架、單一欄位或兩個交錯欄位所組成。 輸出一律為 deinterlaced 的框架。

視頻驅動程式可以執行一個以上的影片處理裝置，以提供不同的影片處理功能組合。 裝置是由 GUID 所識別。 下列是預先定義的 Guid：

-   **DXVA2 \_VideoProcBobDevice**。 此裝置會執行 bob 去交錯。
-   **DXVA2 \_VideoProcProgressiveDevice**。 如果影片只包含漸進式框架，而沒有交錯框架，則會使用此裝置。  (部分影片內容包含漸進和交錯框架的混合。 漸進式裝置無法用於這種「混合」的影片內容，因為交錯框架需要去交錯步驟。 ) 

每個支援 DXVA 視頻處理的圖形驅動程式都必須至少執行這兩個裝置。 圖形驅動程式也可以提供其他裝置，這些裝置是由驅動程式特定的 Guid 所識別。 例如，驅動程式可能會執行專屬的去交錯演算法，產生比 bob 去交錯更優質的輸出。 某些去交錯演算法可能需要來自主要資料流程的向前或向後參考圖片。 如果是，呼叫端必須以正確的順序將這些圖片提供給驅動程式，如本節稍後所述。

也提供參考軟體裝置。 軟體裝置已針對品質而非速度優化，而且可能不適合即時影片處理。 參考軟體裝置使用 GUID 值 DXVA2 \_ VideoProcSoftwareDevice。

## <a name="creating-a-video-processing-device"></a>建立視頻處理裝置

使用 DXVA 影片處理之前，應用程式必須建立影片處理裝置。 以下是步驟的簡短概述，本節的其餘部分將更詳細地說明這些步驟：

1.  取得 [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) 介面的指標。
2.  建立主要影片串流的影片格式描述。 您可以使用此描述來取得支援影片格式的影片處理裝置清單。 裝置是由 GUID 所識別。
3.  針對特定裝置，取得裝置所支援的轉譯目標格式清單。 格式會以 **D3DFORMAT** 值清單的形式傳回。 如果您打算混合子串流，也可以取得一份支援的子串流格式清單。
4.  查詢每個裝置的功能。
5.  建立影片處理裝置。

有時您可以省略這些步驟的其中一部分。 例如，您可以嘗試使用慣用的格式來建立影片處理裝置，並查看是否成功，而不是取得轉譯目標格式的清單。 常見的格式，例如 D3DFMT \_ X8R8G8B8 可能會成功。

本節的其餘部分將詳細說明這些步驟。

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a>取得 IDirectXVideoProcessorService 指標

[**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)介面是從 Direct3D 裝置取得的。 有兩種方式可以取得這個介面的指標：

-   從 Direct3D 裝置。
-   從 [Direct3D 裝置管理員](direct3d-device-manager.md)。

如果您有 Direct3D 裝置的指標，您可以藉由呼叫 [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice)函數來取得 [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)指標。 傳入裝置 **IDirect3DDevice9** 介面的指標，並針對 *Riid* 參數指定 **IID \_ IDirectXVideoProcessorService** ，如下列程式碼所示：


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



在某些情況下，一個物件會建立 Direct3D 裝置，然後透過 [Direct3D 裝置管理員](direct3d-device-manager.md)與其他物件共用它。 在此情況下，您可以在裝置管理員上呼叫 [**IDirect3DDeviceManager9：： GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) 來取得 [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) 指標，如下列程式碼所示：


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a>列舉影片處理裝置

若要取得影片處理裝置的清單，請使用主要影片串流的格式填入 [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) 結構，並將此結構傳遞至 [**IDirectXVideoProcessorService：： GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) 方法。 方法會傳回 Guid 的陣列，每個可搭配此影片格式使用的影片處理裝置都有一個。

請考慮使用 YUY2 格式轉譯影片資料流程的應用程式，並使用709定義的 YUV 色彩，畫面播放速率為每秒29.97 個畫面格。 假設影片內容完全由漸進式框架組成。 下列程式碼片段顯示如何填入格式描述，並取得裝置 Guid：


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



此範例的程式碼取自 [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) SDK 範例。

此範例中的 *pGuids* 陣列是由 [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) 方法配置，因此應用程式必須藉由呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放陣列。 您可以使用這個方法所傳回的任何裝置 Guid 來執行其餘步驟。

### <a name="enumerate-render-target-formats"></a>列舉 Render-Target 格式

若要取得裝置支援的轉譯目標格式清單，請將裝置 GUID 和 [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) 結構傳遞至 [**IDirectXVideoProcessorService：： GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) 方法，如下列程式碼所示：


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



方法會傳回 **D3DFORMAT** 值的陣列。 在此範例中，輸入類型是 YUY2，一般格式清單可能是 D3DFMT \_ X8R8G8B8 (32 位 RGB) 和 D3DMFT \_ YUY2 (輸入格式) 。 不過，確切的清單將取決於驅動程式。

子串流的可用格式清單會根據轉譯目標格式和輸入格式而有所不同。 若要取得子串流格式的清單，請將裝置 GUID、格式結構和轉譯目標格式傳遞給 [**IDirectXVideoProcessorService：： GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) 方法，如下列程式碼所示：


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



這個方法會傳回另一個 **D3DFORMAT** 值陣列。 一般的子串流格式為 AYUV 和 AI44。

### <a name="query-the-device-capabilities"></a>查詢裝置功能

若要取得特定裝置的功能，請將裝置 GUID、格式結構和轉譯目標格式傳遞給 [**IDirectXVideoProcessorService：： GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) 方法。 方法會以裝置功能填入 [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) 結構結構。


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a>建立裝置

若要建立影片處理裝置，請呼叫 [**IDirectXVideoProcessorService：： CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor)。 此方法的輸入是裝置 GUID、格式描述、轉譯目標格式，以及您打算混合的子串流數目上限。 方法會傳回 [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) 介面的指標，該介面表示影片處理裝置。


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a>影片流程 Array.blit

主要的影片處理作業是 *影片處理 array.blit*。  (*array.blit* 是將兩個或多個點陣圖組合成單一點陣圖的任何作業。 影片處理 array.blit 會結合輸入圖片以建立輸出框架。 ) 若要執行影片處理 array.blit，請呼叫 [**IDirectXVideoProcessor：： VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)。 這個方法會將一組影片範例傳遞給影片處理裝置。 在回應中，影片處理裝置會處理輸入圖片並產生一個輸出畫面格。 處理可能包括去交錯、色彩空間轉換和子流混合。 輸出會寫入至呼叫端所提供的目的介面。

[**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)方法會採用下列參數：

-   *pRT* 會指向 **IDirect3DSurface9** 轉譯目標介面，以接收已處理的影片畫面。
-   *pBltParams* 會指向指定 array.blit 參數的 [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) 結構。
-   *pSamples* 是 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) 結構陣列的位址。 這些結構包含 array.blit 的輸入範例。
-   *NumSamples* 會提供 *pSamples* 陣列的大小。
-   *保留* 的參數是保留的，而且應該設定為 **Null**。

在 *pSamples* 陣列中，呼叫端必須提供下列輸入範例：

-   主要影片資料流程中目前的圖片。
-   向前及向後參考圖片（如果去交錯演算法有需要）。
-   零或多個子串流圖片，最多可達15子串流。

驅動程式預期此陣列是以特定順序排列，如 [輸入範例順序](#input-sample-order)中所述。

### <a name="blit-parameters"></a>Array.blit 參數

[**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams)結構包含 array.blit 的一般參數。 最重要的參數會儲存在下列結構的成員中：

-   **TargetFrame** 是輸出框架的呈現時間。 針對漸進式內容，這次必須等於主要影片資料流程中目前框架的開始時間。 這段時間是在該輸入範例的 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **Start** 成員中指定。

    針對交錯式內容，有兩個交錯欄位的框架會產生兩個 deinterlaced 輸出畫面格。 在第一個輸出框架上，表示時間必須等於主要影片資料流程中目前圖片的開始時間，就像漸進式內容一樣。 在第二個輸出框架上，開始時間必須等於主要影片資料流程中目前圖片的開始時間，以及資料流程中下一張圖片的開始時間。 例如，如果輸入影片是每秒25個畫面格 (每秒50個欄位) ，則輸出畫面將會有下表中顯示的時間戳記。 時間戳記會以100毫微秒的單位顯示。

    

    | 輸入圖片 | **TargetFrame** (1)  | **TargetFrame** (2)  |
    |---------------|---------------------|---------------------|
    | 0             | 0                   | 200000              |
    | 400000        | 0                   | 600000              |
    | 800000        | 800000              | 1000000             |
    | 1200000       | 1200000             | 1400000             |

    

     

    如果交錯的內容是由單一欄位而非交錯欄位所組成，則輸出時間一律會符合輸入時間，如同漸進式內容一樣。

-   **TargetRect** 會定義目的介面內的矩形區域。 Array.blit 會將輸出寫入此區域。 具體來說， **TargetRect** 內的每個圖元都會修改，而且不會修改 **TargetRect** 以外的任何圖元。 目標矩形會定義所有輸入影片資料流程的周框。 在該矩形內放置個別資料流程是透過 [**IDirectXVideoProcessor：： VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)的 *pSamples* 參數來控制。
-   **BackgroundColor** 會提供背景的色彩，而不會顯示任何影片影像。 例如，當 16 x 9 的影片影像顯示在 4 x 3 區域內時 (上下黑邊縮) ，letterboxed 區域會以背景色彩顯示。 背景色彩只適用于 (**TargetRect**) 的目標矩形內。 **TargetRect** 之外的任何圖元都不會修改。
-   **DestFormat** 描述輸出影片的色彩空間，例如，是否使用 Itu-t-R BT. 709 或 BT. 601 color。 這項資訊會影響影像的顯示方式。 如需詳細資訊，請參閱 [擴充色彩資訊](extended-color-information.md)。

其他參數則會在 [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) 結構的參考頁面上說明。

### <a name="input-samples"></a>輸入範例

[**IDirectXVideoProcessor：： VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)的 *pSamples* 參數會指向 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的陣列。 其中每個結構都包含一個輸入範例的相關資訊，以及包含範例的 Direct3D 介面指標。 每個範例都是下列其中一項：

-   主要資料流程中目前的圖片。
-   主要資料流程的向前或向後參考圖片，用於去交錯。
-   子流圖片。

範例必須出現在陣列中的確切順序，稍後會在 [ [輸入範例順序](#input-sample-order)] 區段中描述。

雖然大部分的影片應用程式最多隻需要一個子串流，但可以提供最多15個子流圖片。 每次呼叫 [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)時，子串流的數目可能會變更。 子流圖片的表示方式是將 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **SampleFormat** 成員設定為等於 DXVA2 \_ SampleSubStream。 針對主要影片串流，此成員描述輸入影片的交錯。 如需詳細資訊，請參閱 [**DXVA2 \_ SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) 列舉。

針對主要影片資料流程， [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **開頭** 和 **結尾** 成員會提供輸入範例的開始和結束時間。 針對子資料流程圖片，將這些值設定為零，因為呈現時間一律會從主要資料流程計算。 應用程式會負責追蹤每個子串流圖片應該呈現的時間，並在適當的時間將其提交至 [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) 。

兩個矩形會定義每個串流的來源影片位置：

-   [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **>srcrect** 成員會指定 *來源矩形*，也就是要出現在複合輸出框架中的來源圖片矩形區域。 若要裁剪圖片，請將此值設定為小於框架大小的值。 否則，請將它設定為等於框架大小。
-   相同結構的 **>dstrect** 成員會指定 *目的地矩形*，也就是顯示影片框架的目的介面矩形區域。

驅動程式會 blits 從來源矩形到目的矩形的圖元。 這兩個矩形可以有不同的大小或外觀比例;驅動程式會視需要調整映射。 此外，每個輸入資料流程都可以使用不同的縮放比例。 事實上，您可能需要進行調整，才能在輸出框架中產生正確的外觀比例。 驅動程式不會將來源的圖元外觀比例納入考慮，因此，如果來源影像使用非正方形圖元，則應用程式會由應用程式計算正確的目的地矩形。

慣用的子流格式為 AYUV 和 AI44。 後者是具有16色的 palletized 格式。 在 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **Pal** 成員中指定了調色板專案。  (如果您的來源影片格式原本是以媒體基礎媒體類型表示，則會將調色板專案儲存在 [**MF \_ MT \_**](mf-mt-palette-attribute.md) 選擇區屬性中。 ) 非 palletized 格式，請將此陣列清除為零。

## <a name="image-composition"></a>影像組合

每個 array.blit 作業都是由下列三個矩形所定義：

-   *目標* 矩形 (**TargetRect**) 會定義要顯示輸出的目的介面內的區域。 輸出影像會裁剪到這個矩形。
-   每個資料流程 (**>dstrect**) 的 *目的地* 矩形會定義輸入資料流程出現在複合影像中的位置。
-   每個資料流程 (**>srcrect**) 的 *來源* 矩形會定義要顯示的來源影像部分。

目標和目的地矩形會指定為相對於目的地介面。 會指定相對於來源影像的來源矩形。 所有矩形都會以圖元為單位來指定。

![顯示來源、目的地和目標矩形的圖表](images/dxva-vp-rects.gif)

影片處理裝置 Alpha 會使用下列任何一種 Alpha 資料來源來混合輸入圖片：

-   來自子串流的每圖元 Alpha 資料。
-   每個影片資料流程的平面 Alpha 值，指定于 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **PlanarAlpha** 成員中。
-   複合影像的平面 Alpha 值，在 [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams)結構的 **Alpha** 成員中指定。 這個值是用來 blend 整個合成影像與背景色彩。

本節提供一系列示範影片處理裝置如何建立輸出影像的範例。

### <a name="example-1-letterboxing"></a>範例1：上下黑邊縮

此範例示範如何將目的矩形設定為小於目標矩形，以黑邊來源影像。 此範例中的主要影片串流是720×480影像，而且應以16:9 外觀比例顯示。 目的地介面為640×480圖元 (4:3 外觀比例) 。 若要達到正確的外觀比例，目的地矩形必須是640×360。 為了簡單起見，此範例不包含子流。 下圖顯示來源和目的地矩形。

![顯示上下黑邊縮的圖表。](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

上圖顯示下列矩形：

-   目標矩形： {0，0，640，480}
-   主要影片：

    -   來源矩形： {0，0，720，480}
    -   目的地矩形： {0，60，640，420}

驅動程式會將影片進行逐行轉換，將 deinterlaced 框架壓縮成640×360，然後將框架 array.blit 到目的地矩形中。 目標矩形大於目的矩形，因此驅動程式會使用背景色彩來填滿框架上方和下方的水準列。 背景色彩是在 [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) 結構中指定的。

### <a name="example-2-stretching-substream-images"></a>範例2：延展子串流映射

子串流圖片可延伸至主要的影片圖片之外。 例如，在 DVD video 中，主要影片串流在子資料流程為16:9 時可能會有4:3 的外觀比例。 在此範例中，兩個影片串流都有相同的來源維度 (720 × 480) ，但子資料流程的設計是以16:9 的外觀比例顯示。 為了達到此長寬比，子串流影像會水準伸展。 來源和目的地矩形如下圖所示。

![顯示子流影像延展的圖表。](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

上圖顯示下列矩形：

-   目標矩形： {0，0，854，480}
-   主要影片：

    -   來源矩形： {0，0，720，480}
    -   目的地矩形： {0，107，474，480}

-   子串流
    -   來源矩形： {0，0，720，480}
    -   目的地矩形： {0，0，854，480}

這些值會保留影像高度，並以水準方式調整影像的大小。 在兩張影像顯示的區域中，它們都是以 Alpha 混合。 子串流圖片 exends 超過 primay 影片，而子串流則是使用背景色彩來混合使用 Alpha。 此 Alpha 混合帳戶會在圖表右手邊改變色彩。

### <a name="example-3-mismatched-stream-heights"></a>範例3：不相符的資料流程高度

在上述範例中，子資料流程和主要資料流程的高度相同。 資料流程也可以有不相符的高度，如這個範例所示。 目標矩形內不會顯示任何影片的區域會使用背景色彩來繪製（在此範例中為黑色）。 來源和目的地矩形如下圖所示。

![顯示不相符之資料流程高度的圖表](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

上圖顯示下列矩形：

-   目標矩形： {0，0，150，85}
-   主要影片：
    -   來源矩形： {0，0，150，50}
    -   目的地矩形： {0，17，150，67}
-   子串流
    -   來源矩形： {0，0，100，85}
    -   目的地矩形： {25，0，125，85}

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a>範例4：目標矩形小於目的介面

這個範例會顯示目標矩形小於目的表面的案例。

![顯示目的地矩形 array.blit 的圖表。](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

上圖顯示下列矩形：

-   目的地介面： {0，0，300，200}
-   目標矩形： {0，0，150，85}
-   主要影片：
    -   來源矩形： {0，0，150，50}
    -   目的地矩形： {0，17，150，67}
-   子串流
    -   來源矩形： {0，0，100，85}
    -   目的地矩形： {25，0，125，85}

目標矩形外的圖元不會被修改，因此背景色彩只會出現在目標矩形內。 點狀區域表示不受 array.blit 影響的目的表面部分。

### <a name="example-5-source-rectangles"></a>範例5：來源矩形

如果您指定的來源矩形小於來源圖片，驅動程式就只會 array.blit 該部分的圖片。 在此範例中，來源矩形會指定主要影片資料流程的右下象限，以及圖表) 中的雜湊標記所表示之子資料流程 (的左下象限。 目的地矩形的大小與來源矩形相同，因此不會伸展影片。 來源和目的地矩形如下圖所示。

![顯示兩個來源矩形 array.blit 的圖表。](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

上圖顯示下列矩形：

-   目標矩形： {0，0，720，576}
-   主要影片：
    -   來源介面大小： {0，0，720，480}
    -   來源矩形： {360、240、720、480}
    -   目的地矩形： {0，0，360，240}
-   子串流
    -   來源介面大小： {0，0，640，576}
    -   來源矩形： {0，288，320，576}
    -   目的地矩形： {400，0，720，288}

### <a name="example-6-intersecting-destination-rectangles"></a>範例6：交集的目的地矩形

這個範例與上一個範例類似，但目的矩形交集。 表面尺寸與上一個範例相同，但來源和目的地矩形則不是。 同樣地，影片會裁剪但不會伸展。 來源和目的地矩形如下圖所示。

![顯示交集目的矩形的圖表。](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

上圖顯示下列矩形：

-   目標矩形： {0，0，720，576}
-   主要影片：
    -   來源介面大小： {0，0，720，480}
    -   來源矩形： {260、92、720、480}
    -   目的地矩形： {0，0，460，388}
-   子串流
    -   來源介面大小： {0，0，640，576}
    -   來源矩形： {0，0，460，388}
    -   目的地矩形： {260、188、720、576}

### <a name="example-7-stretching-and-cropping-video"></a>範例7：延展和裁剪影片

在此範例中，影片會伸展並裁剪。 每個串流的180×120區域都會延展，以涵蓋目的地矩形中的360×240區域。

![顯示延展和裁剪的圖表。](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

上圖顯示下列矩形：

-   目標矩形： {0，0，720，480}
-   主要影片：
    -   來源介面大小： {0，0，360，240}
    -   來源矩形： {180、120、360、240}
    -   目的地矩形： {0，0，360，240}
-   子串流
    -   來源介面大小： {0，0，360，240}
    -   來源矩形： {0，0，180，120}
    -   目的地矩形： {360、240、720、480}

## <a name="input-sample-order"></a>輸入範例順序

[**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)方法的 *pSamples* 參數是輸入範例陣列的指標。 主要影片串流中的範例會先出現，後面接著以 Z 順序顯示的子資料流程圖片。 範例必須依照下列順序放入陣列中：

-   主要影片串流的範例會先出現在陣列中的時態順序中。 根據 [交錯] 模式，驅動程式可能需要主要影片串流中的一或多個參考範例。 [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps)結構的 **NumForwardRefSamples** 和 **NumBackwardRefSamples** 成員會指定所需的向前和向後參考樣本數。 呼叫端必須提供這些參考範例，即使影片內容是漸進式的，也不需要去交錯。  (當漸進式框架提供給去交錯裝置時（例如，當來源同時包含交錯和漸進式框架的混合時），就會發生這種情況。 ) 
-   在主要影片串流的範例之後，陣列最多可包含15個子資料流程範例（以 Z 順序排列），從下到上。 子串流一律是漸進式的，不需要參考圖片。

在任何時間，主要影片串流都可以在交錯和漸進式內容之間切換，而子串流數目也可以變更。

[**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **SampleFormat. SampleFormat** 成員表示圖片的類型。 針對子流圖片，將此值設定為 DXVA2 \_ SampleSubStream。 針對漸進式圖片，此值為 DXVA2 \_ SampleProgressiveFrame。 若為交錯圖片，此值取決於欄位配置。

如果驅動程式需要向前及向後參考範例，則在影片順序開始時，可能無法使用完整的樣本數。 在此情況下，請在 *pSamples* 陣列中包含這些專案的專案，但將遺漏的範例標示為具有類型 DXVA2 \_ SampleUnknown。

[**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **開頭** 和 **結尾** 成員會提供每個範例的時態位置。 這些值只會用於主要影片串流中的樣本。 若為子串流圖片，請將這兩個成員設定為零。

下列範例可能有助於澄清這些需求。

### <a name="example-1"></a>範例 1

最簡單的情況是在沒有子串流時，而且去交錯演算法不需要參考範例 (**NumForwardRefSamples** 和 **NumBackwardRefSamples** 都是零) 。 Bob 去交錯是這類演算法的範例。 在此情況下， *pSamples* 陣列應包含單一輸入介面，如下表所示。



| 索引           | 介面類別型        | 時態性位置 |
|-----------------|---------------------|-------------------|
| *pSamples* \[0\] | 交錯圖片。 | *T*               |



 

時間值 *T* 會假設為目前影片框架的開始時間。

### <a name="example-2"></a>範例 2

在此範例中，應用程式會混用兩個子串流與主要串流。 去交錯演算法不需要參考範例。 下表顯示如何在 *pSamples* 陣列中排列這些範例。



| 索引           | 介面類別型       | 時態性位置 | Z 順序 |
|-----------------|--------------------|-------------------|---------|
| *pSamples* \[0\] | 交錯圖片 | *T*               | 0       |
| *pSamples* \[單\] | 子串流          | 0                 | 1       |
| *pSamples* \[二級\] | 子串流          | 0                 | 2       |



 

### <a name="example-3"></a>範例 3

現在假設去交錯演算法需要一個反向參考範例和一個向前參考範例。 此外，還提供兩個子流圖片，總共五個表面。 下表顯示正確的順序。



| 索引           | 介面類別型                   | 時態性位置 | Z 順序        |
|-----------------|--------------------------------|-------------------|----------------|
| *pSamples* \[0\] | 交錯式圖片 (參考)  | *T* −1            | 不適用 |
| *pSamples* \[單\] | 交錯圖片             | *T*               | 0              |
| *pSamples* \[二級\] | 交錯式圖片 (參考)  | *T* + 1            | 不適用 |
| *pSamples* \[3\] | 子串流                      | 0                 | 1              |
| *pSamples* \[億\] | 子串流                      | 0                 | 2              |



 

時間 *T* −1是目前畫面格之前的框架開始時間，而 *T* + 1 是下列框架的開始時間。

如果影片資料流程切換至漸進式內容（使用相同的去交錯模式），應用程式必須提供相同的樣本數，如下表所示。



| 索引           | 介面類別型                    | 時態性位置 | Z 順序        |
|-----------------|---------------------------------|-------------------|----------------|
| *pSamples* \[0\] | 漸進式圖片 (參考)  | *T* −1            | 不適用 |
| *pSamples* \[單\] | 漸進式圖片             | *T*               | 0              |
| *pSamples* \[二級\] | 漸進式圖片 (參考)  | *T* + 1            | 不適用 |
| *pSamples* \[3\] | 子串流                       | 0                 | 1              |
| *pSamples* \[億\] | 子串流                       | 0                 | 2              |



 

### <a name="example-4"></a>範例 4

在影片順序開始時，向前和向後參考範例可能無法使用。 發生這種情況時，遺漏範例的專案會包含在 *pSamples* 陣列中，其範例類型為 DXVA2 \_ SampleUnknown。

假設去交錯模式需要一個向前和一個反向參考範例，則前三個對 [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) 的呼叫會有下列三個數據表中所顯示的輸入序列。



| 索引           | 介面類別型                   | 時態性位置 |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[0\] | Unknown                        | 0                 |
| *pSamples* \[單\] | Unknown                        | 0                 |
| *pSamples* \[二級\] | 交錯式圖片 (參考)  | *T* + 1            |



 



| 索引           | 介面類別型                   | 時態性位置 |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[0\] | Unknown                        | 0                 |
| *pSamples* \[單\] | 交錯圖片             | *T*               |
| *pSamples* \[二級\] | 交錯式圖片 (參考)  | *T* + 1            |



 



| 索引           | 介面類別型                   | 時態性位置 |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[0\] | 交錯圖片             | *T* −1            |
| *pSamples* \[單\] | 交錯圖片             | *T*               |
| *pSamples* \[二級\] | 交錯式圖片 (參考)  | *T* + 1            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX Video 加速2。0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA2 \_ VideoProc 範例](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
