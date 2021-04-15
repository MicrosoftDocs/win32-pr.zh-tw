---
description: 本主題說明如何在 DirectShow 解碼器篩選器中支援 (DXVA) 2.0 的 DirectX 影片加速。
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: 支援 DirectShow 中的 DXVA 2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848435"
---
# <a name="supporting-dxva-20-in-directshow"></a>支援 DirectShow 中的 DXVA 2。0

本主題說明如何在 DirectShow 解碼器篩選器中支援 (DXVA) 2.0 的 DirectX 影片加速。 具體而言，它會描述解碼器與影片轉譯器之間的通訊。 本主題不會說明如何執行 DXVA 解碼。

-   [先決條件](#prerequisites)
-   [遷移注意事項](#migration-notes)
-   [尋找解碼器設定](#finding-a-decoder-configuration)
-   [通知影片轉譯器](#notifying-the-video-renderer)
-   [配置未壓縮的緩衝區](#allocating-uncompressed-buffers)
-   [解碼](#decoding)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

本主題假設您已熟悉撰寫 DirectShow 篩選。 如需詳細資訊，請參閱 DirectShow SDK 檔中的 [撰寫 Directshow 篩選器](../directshow/writing-directshow-filters.md) 主題。 本主題中的程式碼範例假設已使用下列類別定義衍生自 [**CTransformFilter**](../directshow/ctransformfilter.md) 類別的解碼器篩選準則：


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



在本主題的其餘部分，「 *解碼* 」一詞指的是「解碼」篩選器，它會接收壓縮的影片並輸出未壓縮的影片。 「 *解碼* 」一詞是指由圖形驅動程式所執行的硬體視頻加速器。

以下是「解碼」篩選準則必須執行以支援 DXVA 2.0 的基本步驟：

1.  協商媒體類型。
2.  尋找 DXVA 的解碼器設定。
3.  使用 DXVA 解碼通知影片轉譯器。
4.  提供可配置 Direct3D 表面的自訂配置器。

本主題的其餘部分將更詳細地描述這些步驟。

## <a name="migration-notes"></a>遷移注意事項

如果您要從 DXVA 1.0 進行遷移，您應該注意這兩個版本之間的一些重大差異：

-   DXVA 2.0 不會使用 [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) 和 [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) 介面，因為此解碼器可以直接透過 [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) 介面存取 DXVA 2.0 api。
-   在媒體類型協商期間，解碼器不會使用影片加速 GUID 做為子類型。 相反地，子類型只是未壓縮的影片格式 (例如 NV12) ，如同軟體解碼一樣。
-   設定加速器的程式已變更。 在 DXVA 1.0 中，使用 **DXVA \_ ConfigPictureDecode** 結構來 **執行** 的解碼器呼叫會設定 accerlator。 在 DXVA 2.0 中，此解碼器會使用 [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 介面，如下一節中所述。
-   此解碼會配置未壓縮的緩衝區。 影片轉譯器不再配置它們。
-   除了呼叫 [**IAMVideoAccelerator：:D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) 來顯示已解碼的框架，解碼器也會藉由呼叫 [**IMemInputPin：： Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive)將框架傳遞到轉譯器，如同軟體解碼一樣。
-   當資料緩衝區可以安全地進行更新時，此解碼器不再負責檢查。 因此，DXVA 2.0 沒有任何相當於 [**IAMVideoAccelerator：： QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus)的方法。
-   子圖片混色是由影片轉譯器使用 DXVA 2.0 video 處理器 Api 來完成。 提供 subpictures (的解碼器例如，DVD 解碼器) 應該會在個別的輸出 pin 上傳送子圖片的資料。

針對解碼作業，DXVA 2.0 使用與 DXVA 1.0 相同的資料結構。

增強型影片轉譯器 (EVR) 篩選器支援 DXVA 2.0。 影片混合轉譯器篩選 (VMR-7 和 VMR-9) 僅支援 DXVA 1.0。

## <a name="finding-a-decoder-configuration"></a>尋找解碼器設定

在解碼器協商輸出媒體類型之後，它必須找到 DXVA 解碼器裝置的相容設定。 您可以在輸出釘選的 [**CBaseOutputPin：： CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) 方法內執行這個步驟。 此步驟可確保在使用 DXVA 認可之前，圖形驅動程式支援該解碼器所需的功能。

若要尋找適用于解碼器裝置的設定，請執行下列動作：

1.  查詢轉譯器的輸入圖釘以取得 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。
2.  呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標。 服務 GUID 是 MR \_ 影片 \_ 加速 \_ 服務。
3.  呼叫 [**IDirect3DDeviceManager9：： OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) 來取得轉譯器之 Direct3D 裝置的控制碼。
4.  呼叫 [**IDirect3DDeviceManager9：： GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) ，並傳入裝置控制碼。 這個方法會傳回 [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 介面的指標。
5.  呼叫 [**IDirectXVideoDecoderService：： GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids)。 這個方法會傳回一組解碼裝置 Guid。
6.  在解碼 Guid 陣列中迴圈，以找出該解碼篩選器所支援的專案。 例如，針對 MPEG-2 解碼器，您會尋找 **DXVA2 \_ ModeMPEG2 \_ MOCOMP**、 **DXVA2 \_ ModeMPEG2 \_ IDCT** 或 **DXVA2 \_ ModeMPEG2 \_ VLD**。

7.  當您找到候選的解碼器裝置 GUID 時，請將 GUID 傳遞給 [**IDirectXVideoDecoderService：： GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) 方法。 這個方法會傳回呈現目標格式的陣列，並指定為 **D3DFORMAT** 值。
8.  逐一查看轉譯目標格式，並尋找符合您輸出格式的專案。 一般而言，解碼器裝置支援單一轉譯目標格式。 您應使用此子類型連接到轉譯器的轉譯器。 在第一次呼叫 [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md)時，此解碼器可以判斷轉譯目標格式，然後將此格式傳回為慣用的輸出類型。

9.  呼叫 [**IDirectXVideoDecoderService：： GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations)。 傳入相同的解碼器裝置 GUID，以及描述建議格式的 [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) 結構。 方法會傳回 [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) 結構的陣列。 每個結構都描述一個可能的解碼器裝置設定。

10. 假設先前的步驟成功，請儲存 Direct3D 裝置控制碼、解碼器裝置 GUID 和設定結構。 篩選器會使用此資訊來建立解碼器裝置。

下列程式碼顯示如何尋找解碼器設定。


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



因為此範例為泛型，所以某些邏輯已放在必須由該解碼器實作為的 helper 函式中。 下列程式碼顯示這些函數的宣告：


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a>通知影片轉譯器

如果此解碼器找到解碼器設定，下一步就是通知影片轉譯器，該解碼器將會使用硬體加速。 您可以在 [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) 方法中執行此步驟。 在選取配置器之前，必須先執行此步驟，因為它會影響配置器的選取方式。

1.  查詢轉譯器的輸入圖釘以取得 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。
2.  呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得 [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) 介面的指標。 服務 GUID 是 **MR \_ 影片 \_ 加速 \_ 服務**。
3.  在迴圈中呼叫 [**IDirectXVideoMemoryConfiguration：： GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) ，將 *dwTypeIndex* 變數從零遞增。 當方法傳回 *pdwType* 參數中的 **DXVA2 \_ SurfaceType \_ DecoderRenderTarget** 值時停止。 此步驟可確保影片轉譯器支援硬體加速解碼。 EVR 篩選器的這個步驟一律會成功。
4.  如果上一個步驟成功，請呼叫 [**IDirectXVideoMemoryConfiguration：： SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) ，其值為 DXVA2 \_ SurfaceType \_ DecoderRenderTarget。 使用此值呼叫 **SetSurfaceType** ，會將影片轉譯器放入 DXVA 模式。 當影片轉譯器處於此模式時，該解碼器必須提供它自己的配置器。

下列程式碼說明如何通知影片轉譯器。


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



如果此解碼器找到有效的設定並成功通知影片轉譯器，則該解碼器可以使用 DXVA 進行解碼。 此解碼器必須針對其輸出圖釘來執行自訂配置器，如下一節所述。

## <a name="allocating-uncompressed-buffers"></a>配置未壓縮的緩衝區

在 DXVA 2.0 中，此解碼器負責配置 Direct3D 介面，以作為未壓縮的視訊緩衝區。 因此，此解碼器必須執行將建立介面的自訂配置器。 此配置器所提供的媒體範例會保存 Direct3D 介面的指標。 EVR 會藉由呼叫媒體範例上的 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，來抓取介面的指標。 服務識別碼是 **MR \_ 緩衝區 \_ 服務**。

若要提供自訂配置器，請執行下列步驟：

1.  定義媒體範例的類別。 這個類別可以衍生自 [**CMediaSample**](../directshow/cmediasample.md) 類別。 在這個類別中，執行下列動作：
    -   將指標儲存至 Direct3D 介面。
    -   執行 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。 在 [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 方法中，如果服務 GUID 是 **MR \_ 緩衝區 \_ 服務**，請查詢 Direct3D 介面以取得所要求的介面。 否則， **GetService** 可以傳回 **MF \_ E \_ 不受支援的 \_ 服務**。
    -   覆寫 [**CMediaSample：： GetPointer**](../directshow/cmediasample-getpointer.md) 方法，以傳回 E \_ >notimpl。
2.  定義配置器的類別。 配置器可以衍生自 [**CBaseAllocator**](../directshow/cbaseallocator.md) 類別。 在這個類別中，執行下列動作。
    -   覆寫 [**CBaseAllocator：：分配**](../directshow/cbaseallocator-alloc.md) 方法。 在這個方法中，呼叫 [**IDirectXVideoAccelerationService：： CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) 以建立表面。  ([**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 介面從 [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)繼承這個方法。 ) 
    -   覆寫 [**CBaseAllocator：： Free**](../directshow/cbaseallocator-free.md) 方法以釋放表面。
3.  在篩選的輸出釘選中，覆寫 [**CBaseOutputPin：： InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) 方法。 在這個方法內，建立自訂配置器的實例。
4.  在篩選準則中，執行 [**CTransformFilter：:D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) 方法。 *>pproperties* 參數會指出 EVR 需要的表面數目。 將您的解碼所需的介面數目加到這個值，並在配置器上呼叫 [**IMemAllocator：： SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) 。

下列程式碼示範如何執行 media 範例類別：


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



下列程式碼顯示如何在配置器上執行 [**配置方法。**](../directshow/cbaseallocator-alloc.md)


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



以下是 [**免費**](../directshow/cbaseallocator-free.md) 方法的程式碼：


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



如需有關如何執行自訂配置器的詳細資訊，請參閱 DirectShow SDK 檔中 [提供自訂](../directshow/providing-a-custom-allocator.md) 配置器的主題。

## <a name="decoding"></a>解碼

若要建立解碼器裝置，請呼叫 [**IDirectXVideoDecoderService：： CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder)。 方法會傳回解碼裝置之 [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) 介面的指標。

在每個畫面上，呼叫 [**IDirect3DDeviceManager9：： TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) 來測試裝置控制碼。 如果裝置已變更，此方法會傳回 DXVA2 \_ E \_ NEW \_ VIDEO \_ 裝置。 如果發生這種情況，請執行下列動作：

1.  藉由呼叫 [**IDirect3DDeviceManager9：： CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle)來關閉裝置控制碼。
2.  釋放 [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 和 [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) 指標。
3.  開啟新的裝置控制碼。
4.  如 [尋找解碼器](#finding-a-decoder-configuration)設定一節所述，協商新的解碼器設定。
5.  建立新的解碼器裝置。

假設裝置控制碼有效，則解碼程式的運作方式如下：

1.  呼叫 [**IDirectXVideoDecoder：： BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)。
2.  執行下列一或多次：
    1.  呼叫 [**IDirectXVideoDecoder：： GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) 來取得 DXVA 的解碼器緩衝區。
    2.  填滿緩衝區。
    3.  呼叫 [**IDirectXVideoDecoder：： ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer)。
3.  呼叫 [**IDirectXVideoDecoder：： Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) 以執行框架上的解碼作業。

DXVA 2.0 使用與 DXVA 1.0 相同的資料結構來進行解碼作業。 針對 DXVA 設定檔的原創組 (261、.H 和 MPEG-2) ，這些資料結構會在 [DXVA 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)中說明。

在每對 [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [**執行**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute)呼叫中，您可以多次呼叫 [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) ，但每種類型的 DXVA 緩衝區都只會呼叫一次。 如果您使用相同的緩衝區類型呼叫它兩次，則會覆寫資料。

呼叫 [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute)之後，呼叫 [**IMemInputPin：： Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) 將框架傳遞給影片轉譯器，如同軟體解碼一樣。 **Receive** 方法是非同步;在傳回之後，可以繼續對下一個框架進行解碼。 當緩衝區正在使用中時，顯示驅動程式會防止任何解碼命令覆寫緩衝區。 除非轉譯器已釋放範例，否則，此解碼器不應重複使用介面將另一個框架解碼。 當轉譯器釋放範例時，配置器會將範例放回其可用範例的集區。 若要取得下一個可用的範例，請呼叫 [**CBaseOutputPin：： GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md)，它接著會呼叫 [**IMemAllocator：： GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer)。 如需詳細資訊，請參閱 DirectShow 檔中有關 [directshow 之資料流程](../directshow/overview-of-data-flow-in-directshow.md) 的主題總覽。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX Video 加速2。0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
