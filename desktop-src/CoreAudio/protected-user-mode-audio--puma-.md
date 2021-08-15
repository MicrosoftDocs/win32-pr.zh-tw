---
description: WindowsVista 引進了受保護的使用者模式音訊 (PUMA) ，受保護環境中的使用者模式音訊引擎 (PE) ，可為音訊處理和轉譯提供更安全的環境。
ms.assetid: 27a50026-9e48-48b1-9249-7528a97333c9
title: '受保護的使用者模式音訊 (PUMA) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f119094440297c90ae67c46d5a6b39b1ba6e2e9931b43b4bdda17393d0273dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077452"
---
# <a name="protected-user-mode-audio-puma"></a>受保護的使用者模式音訊 (PUMA) 

WindowsVista 引進了受保護的使用者模式音訊 (PUMA) ，受保護環境中的使用者模式音訊引擎 (PE) ，可為音訊處理和轉譯提供更安全的環境。 它只允許啟用可接受的音訊輸出，並確保能可靠地停用輸出。 如需 PUMA 的詳細資訊，請參閱[內容保護和 Windows Vista 的輸出](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc)。

PUMA 已更新為 Windows 7，以提供下列功能：

-   在) 的多媒體介面 High-Definition HDMI (端點上，設定序號複製管理系統 (SCMS) 位於 S/PDIF 端點和高頻寬數位內容保護 (HDCP) 位。
-   在受保護的環境以外啟用 SCMS 和 HDMI 保護控制項， (PE) 。

## <a name="drm-protection-in-audio-drivers"></a>音訊驅動程式中的 DRM 保護

數位 Rights Management (DRM) 讓您能夠在安全的容器中封裝媒體資料，並將使用規則附加至內容。 例如，內容提供者可能會使用 **禁止複製** 或 **數位輸出停** 用來停用直接數位複製或從電腦系統傳輸。

某些 Microsoft 產品中的音訊堆疊藉由實行管理音訊內容播放的使用規則，支援 DRM。 若要播放受保護的內容，基礎音訊驅動程式必須是 *信任的驅動程式*;也就是說，驅動程式必須是 DRMLevel 1300 的標誌認證。 如需開發受信任驅動程式的相關資訊，您可以使用 Windows 2000 驅動程式開發工具組中定義的介面 ( 「DDK」 ) 或更新版本。 使用 DDK 開發的驅動程式將會針對 DRM 執行必要的介面。 如需詳細資訊，請參閱 [數位 Rights Management](/windows-hardware/drivers/audio/digital-rights-management)。

若要轉譯受保護的內容，信任的驅動程式必須檢查是否已在流經音訊堆疊的內容上設定 **禁止複製** 和 **數位輸出停** 用，並據以回應設定。

### <a name="copy-protection-rule"></a>禁止複製規則

**禁止複製** 表示系統不允許直接數位複製。 對 WHQL 測試合約的展示 B 已更新，以反映在內容上設定 **禁止複製** 時，驅動程式的新期望和需求。 針對 Windows 7，內建的 HD 音訊類別驅動程式符合最新的需求。

除了確保不允許內容傳遞至另一個元件，或儲存在 DRM 系統未驗證的任何非靜態儲存媒體上，音訊驅動程式會在設定 **禁止複製** 時執行下列工作：

-   驅動程式可讓您在 HDMI 端點上進行 HDCP。
-   針對 S/PDIF 介面，驅動程式會驗證 L、Cp 和分類程式代碼位的組合是否表示「永遠不復制」的 SCMS 狀態，如 IEC 60958 中所定義。
-   L 位設定為0，而類別代碼會設定為「數位信號 Mixer」。

受信任音訊驅動程式所使用的 **DRMRIGHTS** 結構，指定指派給 KS 音訊 pin 或埠類別驅動程式資料流程物件的 DRM 內容許可權。 **CopyProtect** 成員會指出是否已在音訊內容上設定 **禁止複製**。

針對 Windows 7，使用 **CopyProtect** 會更嚴格。 驅動程式可確保在音訊介面上設定保護控制項，並針對 HDMI 輸出設定 HDCP，並將 [狀態] 設定為 [永遠不復制]，以設定 S/PDIF 輸出的 SCMS。

### <a name="digital-output-disable-rule"></a>數位輸出停用規則

**數位輸出停** 用表示不允許從系統傳送內容。 在 Windows 7 中，內建的 HD 音訊類別驅動程式會藉由啟用在 HDMI 端點上的 HDCP 來回應此設定。 這類似于驅動程式對 **禁止複製** 設定的回應。

## <a name="enabling-content-protection-mechanisms-outside-of-a-protected-environment"></a>啟用受保護環境以外的內容保護機制

PUMA 位於受保護環境 (PE) 中的個別進程。 在 Windows Vista 中，若要使用 PUMA 所提供的音訊內容保護控制項，媒體應用程式必須在 PE 中。 因為只有媒體基礎 Api 可以與 PE 互動，所以內容保護控制項僅限於使用媒體基礎 Api 來串流音訊內容的應用程式。

在 Windows 7 中，任何應用程式都可以存取 PUMA 輸出信任授權單位 (OTA) 所提供的內容保護控制項，不論它們是在 PE 中或使用媒體基礎 api 來播放音訊。

## <a name="implementation-instructions"></a>實作指示

音訊應用程式需要執行下列步驟，才能控制音訊端點上的 SCMS 或 HDCP 內容保護。 支援的音訊 api 為 DirectShow、DirectSound 和 WASAPI。

此範例程式碼會使用下列介面。

-   [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)
-   [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
-   [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput)
-   [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)

媒體應用程式必須執行下列工作。

1.  設定開發環境。
    -   參考所需的介面，包括下列程式碼中所示的標頭。
        ```cpp
        #include <MMdeviceapi.h>        // Device endpoint definitions
        #include <Mfidl.h>              // OTA interface definitions
        ```

        

    -   連結至 Mfuuid，以使用 OTA 介面。
    -   停用內核偵錯工具和驅動程式驗證程式，以避免任何驗證檢查錯誤。
2.  列舉系統中的所有端點，並從端點集合中選取目標端點，如下列程式碼所示。 如需列舉裝置的詳細資訊，請參閱 [列舉音訊裝置](/previous-versions//ms678716(v=vs.85))。
    ```cpp
    BOOL IsDigitalEndpoint(IMMDevice *pDevice)
    {
       PROPVARIANT         var;
       IPropertyStore      *pProperties = NULL;
       EndpointFormFactor  formfactor;
       BOOL                bResult = FALSE;
       HRESULT             hr = S_OK;
       PropVariantInit(&var);
       // Open endpoint properties
       hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
       IF_FAILED_JUMP(hr, Exit);

       // get form factor 
       hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
       IF_FAILED_JUMP(hr, Exit);
       formfactor = (EndpointFormFactor)var.uiVal;
       // DigitalAudioDisplayDevice is defined same as HDMI formfactor
       if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
       {
           bResult = TRUE;
       }

    Exit:
       PropVariantClear(&var);
       SAFE_RELEASE(pProperties);
       return bResult;
    }
    ```

    

    ```cpp
    /******************************************************************
    *                                                                 *
    *  GetDevice:  Selects an endpoint that meets the requirements.   *
    *                                                                 *
    *  ppDevice: Receives a pointer to an IMMDevice interface of      *
    *            the device's endpoint object                         *                                             *                                            *
    *                                                                 *
    ******************************************************************/
    HRESULT GetDevice(IMMDevice** ppDevice)
    {
       IMMDeviceEnumerator    *pEnumerator = NULL;
       IMMDevice              *pDevice = NULL;
       IMMDeviceCollection    *pEndpoints = NULL;
       UINT                    cEndpoints = 0;

       const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
       const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

       // Get enumerator for audio endpoint devices
       hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, 
           NULL,
           CLSCTX_ALL, 
           IID_IMMDeviceEnumerator,
           (void**)&pEnumerator));


       EXIT_ON_ERROR(hr)

       // Enumerate all active endpoints,
       hr = pEnumerator->EnumAudioEndpoints (
           eRender,
           DEVICE_STATE_ACTIVE,
           &pEndpoints);
       EXIT_ON_ERROR(hr)

       hr = pEndpoints->GetCount(&cEndpoints);
       EXIT_ON_ERROR(hr)

       for (UINT i = 0; i < cEndpoints; i++)
       {
           hr = pEndpoints->Item(i, &pDevice);
           IF_FAILED_JUMP(hr, Exit);
           {
               // Select the endpoint that meets the requirements.
               // For example, SPDIF analog output or HDMI
               if (IsDigitalEndpoint(pDevice))
               {
                   *(ppDevice) = pDevice;
                   (*ppDevice)->AddRef();
                   break;
               }
           }
           SAFE_RELEASE(pDevice);
       }
    Exit:
       if (FAILED(hr))
       {
           // Notify error.
           // Not Shown.
       }
       SAFE_RELEASE(pEndpoints);
       SAFE_RELEASE(pEnumerator);
    }
    ```

    

3.  使用列舉程式所傳回之端點的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 指標，來啟用所需的音訊串流 API 並準備進行串流。 不同的音訊 Api 需要稍微不同的準備工作。
    -   針對 DShow 音訊應用程式：
        1.  藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)並指定 IID \_ IBaseFilter 作為介面識別碼，建立 DirectShow COM 物件。
            ```cpp
            IUnknown *pDShowFilter = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IBaseFilter,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDShowFilter));
            ```

            

        2.  使用裝置啟動的這個 COM 物件來建立 DirectShow 的篩選圖形。 如需此程式的詳細資訊，請參閱 DirectShow SDK 檔中的 < 建立篩選 Graph」。
    -   針對 DSound 音訊應用程式：
        1.  藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 並指定 IID \_ IDirectSound8 作為介面識別碼，來建立 DSound COM 物件。
            ```cpp
            IDirectSound8  *pDSSound8;
            ...
            hr = pDevice->Activate (
                              IID_IDirectSound8,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDSSound8));
            ```

            

        2.  使用上面建立的 DSound 物件，以針對串流進行程式 DSound。 如需此程式的詳細資訊，請參閱 MSDN 上的 [DirectSound](/previous-versions//bb219818(v=vs.85)) 。
    -   針對 WASAPI：
        1.  藉由 [](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)呼叫 [**IMMDevice：： ACTI加值稅E**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)並指定 IID \_ IAudioClient 作為介面識別碼，來建立 IAudioClient COM 物件。
            ```cpp
            IAudioClient *pIAudioClient = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IAudioClient,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pIAudioClient));
            ```

            

        2.  開啟音訊串流。
            ```cpp
            hr = pIAudioClient->Initialize(...);
            ```

            
4.  開始音訊串流。
5.  設定資料流程的保護原則。
    1.  針對 WASAPI 用戶端，請呼叫 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) ，並指定 IID IMFTrustedOutput 作為介面識別碼，以取得資料流程的輸出信任授權單位的 [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput)介面參考 (OTA) 物件 \_ 。
        ```cpp
        IMFTrustedOutput*       pTrustedOutput = NULL;
        hr = pIAudioClient>GetService(
                       __uuidof(IMFTrustedOutput),
                       (void**)& pTrustedOutput);
        ```

        

    2.  藉由呼叫 [**IMFTrustedOutput：： GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount)來取得可用 OTA 物件的計數。
        ```cpp
        hr = pTrustedOutput->GetOutputTrustAuthorityCount(&m_dwCountOTA);
        ```

        

    3.  列舉 OTA 集合，並取得支援 action PEACTION PLAY 之 OTA 物件的參考 \_ 。 所有 OTAs 都會公開 [**IMFOutputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) 介面。
        ```cpp
        hr = pMFTrustedOutput->GetOutputTrustAuthorityByIndex(I, &pMFOutputTrustAuthority);
        hr = pMFOutputTrustAuthority->GetAction(&action) 
        ```

        

    4.  使用 [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) 介面設定資料流程上的保護原則。

        ```cpp
        hr = pTrustedOutput ->SetPolicy(&pPolicy, nPolicy, &pbTicket, &cbTicket);
        ```

        

        > [!Note]
        > 如果您使用 EVR， [**SetPolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) 會引發 [MEPolicySet](../medfound/mepolicyset.md) 事件，並傳回 MF \_ S \_ 等候 \_ \_ 原則 \_ 設定，以表示 OTA 將會以非同步方式強制執行原則。 不過，在此範例程式碼中，應用程式是直接 WASAPI 用戶端，從音訊用戶端取出 OTA 物件 (步驟 5 a) 。 不同于 EVR，音訊用戶端和其他 WASAPI 物件不會執行媒體事件產生器。 如果沒有媒體事件產生器， **IMFTrustedOutput：： SetPolicy** 不會傳回 MF \_ \_ 等候 \_ \_ 原則 \_ 集。
        >
        > 音訊原則設定必須在音訊串流開始之後設定，否則 [**IMFTrustedOutput：： GetOutputTrustAuthorityByIndex**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) 會失敗。 此外，若要支援這項功能，基礎音訊驅動程式必須是 *信任的驅動程式*。

         

        在範例程式碼中， *pPolicy* 是用戶端所執行之原則物件的 [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) 介面指標。 如需詳細資訊，請參閱 [媒體基礎 SDK](../medfound/microsoft-media-foundation-sdk.md) 檔。

        在 [**IMFOutputPolicy：： GenerateRequiredSchemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) 方法的執行中，必須產生 OTA 必須強制執行的輸出保護系統 (架構) 的集合。 每個架構都是由 GUID 所識別，並包含保護系統的設定資料。 請確定集合中的保護系統限制為使用受信任的音訊驅動程式。 這項限制是由 GUID、 **MFPROTECTION \_ TRUSTEDAUDIODRIVERS**、DISABLE 或 CONSTRICTAUDIO 所識別。 如果 \_ 使用 MFPROTECTION TRUSTEDAUDIODRIVERS，則此架構的設定資料為 DWORD。 如需有關架構和相關設定資料的詳細資訊，請參閱受保護的環境 SDK 檔。

        用戶端也必須提供架構定義，方法是執行 [**IMFOutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) 介面。 [**IMFOutputSchema：： GetSchemaType**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) 會將 **MFPROTECTION \_ TRUSTEDAUDIODRIVERS** 抓取為架構 GUID。 [**IMFOutputSchema：： GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) 會傳回架構設定資料的指標。

6.  繼續音訊串流。
7.  在停止串流之前，請確定保護原則是明確的。

    釋放上述的相關原則介面參考。

    發行呼叫會清除先前設定的原則設定。

    > [!Note]  
    > 每次重新開機串流時，都必須在資料流程上再次設定保護原則。 步驟 5-d 中會說明此程式。

    ```cpp
    pMFOutputTrustAuthority->Release()
    pMFTrustedOutput->Release()
    ```
  

下列程式碼範例顯示原則和架構物件的範例執行。


```cpp
//OTADsoundSample.cpp
#include <stdio.h>
#include <tchar.h>
#include <initguid.h>
#include <windows.h>
#include <mmreg.h>
#include <dsound.h>

#include <mfidl.h>
#include <Mmdeviceapi.h>
#include <AVEndpointKeys.h>
#include "OTADSoundSample.h"

#define STATIC_KSDATAFORMAT_SUBTYPE_AC3\
    DEFINE_WAVEFORMATEX_GUID(WAVE_FORMAT_DOLBY_AC3_SPDIF)
DEFINE_GUIDSTRUCT("00000092-0000-0010-8000-00aa00389b71", KSDATAFORMAT_SUBTYPE_AC3);
#define KSDATAFORMAT_SUBTYPE_AC3 DEFINE_GUIDNAMED(KSDATAFORMAT_SUBTYPE_AC3)


HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy);
HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy);


const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

BOOL IsDigitalEndpoint(IMMDevice *pDevice)
{
    PROPVARIANT         var;
    IPropertyStore      *pProperties = NULL;
    EndpointFormFactor  formfactor;
    BOOL                bResult = FALSE;
    HRESULT             hr = S_OK;
    PropVariantInit(&var);

    // Open endpoint properties
    hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
    IF_FAILED_JUMP(hr, Exit);

    // get form factor 
    hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
    IF_FAILED_JUMP(hr, Exit);

    formfactor = (EndpointFormFactor)var.uiVal;
    if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
    {
        bResult = TRUE;
    }

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pProperties);

    return bResult;
}


HRESULT GetDigitalAudioEndpoint(IMMDevice** ppDevice)
{
    IMMDeviceEnumerator    *pEnumerator = NULL;
    IMMDevice              *pDevice = NULL;
    IMMDeviceCollection    *pEndpoints = NULL;
    UINT                    cEndpoints = 0;
    HRESULT hr = S_OK;

    *ppDevice = NULL;
    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator, NULL,
                          CLSCTX_ALL, IID_IMMDeviceEnumerator,
                          (void**)&pEnumerator);
    IF_FAILED_JUMP(hr, Exit);

    // Enumerate all active render endpoints, 
    hr = pEnumerator->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    hr = pEndpoints->GetCount(&cEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    for (UINT i = 0; i < cEndpoints; i++)
    {
        hr = pEndpoints->Item(i, &pDevice);
        IF_FAILED_JUMP(hr, Exit);
        // Select the endpoint that meets the requirements.
        // For example, SPDIF analog output or HDMI
        // Not Shown.
        if (IsDigitalEndpoint(pDevice))
        {
            *ppDevice = pDevice;
            (*ppDevice)->AddRef();
            break;
        }
        SAFE_RELEASE(pDevice);
    }
Exit:
    if (FAILED(hr))
    {
        // Notify error.
        // Not Shown.
    }
    SAFE_RELEASE(pEndpoints);
    SAFE_RELEASE(pEnumerator);
    return hr; 
}


//-------------------------------------------------------------------
int __cdecl wmain(int argc, char* argv[])
{
    IMMDevice *pEndpoint=NULL;
    HRESULT hr = S_OK;

    // DSound related variables
    IDirectSound8*          DSSound8 = NULL; 
    IDirectSoundBuffer*     DSBuffer = NULL; 
    DSBUFFERDESC            DSBufferDesc;
    WAVEFORMATEXTENSIBLE    wfext;
    WORD nChannels = 2;
    DWORD nSamplesPerSec = 48000;
    WORD wBitsPerSample = 16;

    // OTA related variables
    IMFTrustedOutput *pMFTrustedOutput=NULL;
    IMFOutputPolicy *pMFOutputPolicy=NULL;
    IMFOutputTrustAuthority *pMFOutputTrustAuthority=NULL;
    DWORD dwConfigData=0;

    // Initialize COM
    hr = CoInitialize(NULL);
    IF_FAILED_JUMP(hr, Exit);

    printf("OTA test app for DSound\n");

    hr = GetDigitalAudioEndpoint(&pEndpoint);
    IF_FAILED_JUMP(hr, Exit);

    if (pEndpoint)
    {
        printf("Found digital audio endpoint.\n");
    }
    //
    // Active DSound interface
    //
    hr = pEndpoint->Activate(IID_IDirectSound8, CLSCTX_INPROC_SERVER, NULL, reinterpret_cast<void **>(&DSSound8));
    IF_FAILED_JUMP(hr, Exit);

    nChannels = 2;
    nSamplesPerSec = 48000;
    wBitsPerSample = 16;

    ZeroMemory(&wfext, sizeof(wfext));
    wfext.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
    wfext.Format.nChannels = nChannels;
    wfext.Format.nSamplesPerSec = nSamplesPerSec;
    wfext.Format.wBitsPerSample = wBitsPerSample;
    wfext.Format.nBlockAlign = (nChannels * wBitsPerSample) / 8;
    wfext.Format.nAvgBytesPerSec = nSamplesPerSec * ((nChannels * wBitsPerSample) / 8);
    wfext.Format.cbSize = 22;
    wfext.Samples.wValidBitsPerSample = wBitsPerSample;
    wfext.dwChannelMask = 0x3;
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_PCM;
#if 1 
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_AC3;
#endif

    ZeroMemory(&DSBufferDesc, sizeof(DSBufferDesc));
    DSBufferDesc.dwSize = sizeof(DSBufferDesc);
    DSBufferDesc.dwFlags = DSBCAPS_GLOBALFOCUS | DSBCAPS_LOCSOFTWARE | DSBCAPS_GETCURRENTPOSITION2;
    DSBufferDesc.lpwfxFormat = (WAVEFORMATEX *)&wfext;
    DSBufferDesc.dwBufferBytes = wfext.Format.nAvgBytesPerSec / 100;

    HWND hwnd = GetForegroundWindow();
    hr = DSSound8->SetCooperativeLevel(hwnd, DSSCL_PRIORITY);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSSound8->CreateSoundBuffer(&DSBufferDesc, &DSBuffer, NULL);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    printf("Will set the following audio policy:\n");
    printf("Test Certificate Enable: %s\n", TRUE ? "True" : "False");
    printf("Copy OK: %s\n", FALSE ? "True" : "False");
    printf("Digital Output Disable: %s\n", FALSE ? "True" : "False");
    printf("DRM Level: %u\n", 1300);

    // Set policy when the stream is in RUN state
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    //
    // Perform all the necessary streaming operations here.
    //

    // stop audio streaming
    DSBuffer->Stop();

    // In order for the stream to restart successfully 
    // Need to release the following OutputTrust* interface to release audio endpoint
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // After above release operations, the following Play() will succeed without without device-in-use error message 0x8889000A
    DSBuffer->SetCurrentPosition(0);
    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    // Need to reset the new audio protection state because previous settings were gone with the ClearOTAPolicy call.
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    // Clean up setting before leaving your streaming app.
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    DSBuffer->SetCurrentPosition(0);

Exit:
    SAFE_RELEASE(DSBuffer);
    SAFE_RELEASE(DSSound8);

    SAFE_RELEASE(pEndpoint);

    CoUninitialize();

    return 0;
}
```




```cpp
//OTADSoundSample.h
// Macro defines
#define IF_FAILED_JUMP(_hresult, label)                         \
    if(FAILED(_hresult))                                        \
    {                                                           \
        goto label;                                             \
    }

#define SAFE_RELEASE(p) \
    if (NULL != p) { \
        (p)->Release(); \
        (p) = NULL; \
    }

#define IF_TRUE_ACTION_JUMP(condition, action, label)           \
    if(condition)                                               \
    {                                                           \
        action;                                                 \
        goto label;                                             \
    }
```




```cpp
// outputpolicy.h

class CTrustedAudioDriversOutputPolicy : public CMFAttributesImpl<IMFOutputPolicy> 
{
friend
    HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy);
private:
    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginator;
    IMFOutputSchema *m_pOutputSchema;
    
    CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr);
    ~CTrustedAudioDriversOutputPolicy();

public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(/* [in] */ REFIID riid,/* [out] */ LPVOID *ppvObject);
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();
    
    // IMFOutputPolicy methods
    HRESULT STDMETHODCALLTYPE
        GenerateRequiredSchemas( 
            /* [in] */ DWORD dwAttributes,
            /* [in] */ GUID guidOutputSubType,
            /* [in] */ GUID *rgGuidProtectionSchemasSupported,
            /* [in] */ DWORD cProtectionSchemasSupported,
            /* [annotation][out] */ 
            __out  IMFCollection **ppRequiredProtectionSchemas);

    HRESULT STDMETHODCALLTYPE GetOriginatorID(/* [annotation][out] */ __out  GUID *pguidOriginatorID);

    HRESULT STDMETHODCALLTYPE GetMinimumGRLVersion(/* [annotation][out] */ __out  DWORD *pdwMinimumGRLVersion);
}; // CTrustedAudioDriversOutputPolicy

class CTrustedAudioDriversOutputSchema : public CMFAttributesImpl<IMFOutputSchema> 
{

friend
    HRESULT CreateTrustedAudioDriversOutputSchema(
        DWORD dwConfigData,
        GUID guidOriginatorID,
        IMFOutputSchema **ppMFOutputSchema
    );

private:
    CTrustedAudioDriversOutputSchema(DWORD dwConfigData, GUID guidOriginatorID);
    ~CTrustedAudioDriversOutputSchema();

    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginatorID;
    
public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(
       /* [in] */ REFIID riid,
       /* [out] */ LPVOID *ppvObject
    );
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();

    // IMFOutputSchema methods
    HRESULT STDMETHODCALLTYPE GetConfigurationData(__out DWORD *pdwVal);
    HRESULT STDMETHODCALLTYPE GetOriginatorID(__out GUID *pguidOriginatorID);
    HRESULT STDMETHODCALLTYPE GetSchemaType(__out GUID *pguidSchemaType);

}; // CTrustedAudioDriversOutputSchema
```




```cpp
// outputpolicy.cpp

#include <windows.h>
#include <tchar.h>
#include <mfidl.h>
#include <atlstr.h>
#include <attributesbase.h>
#include "OTADSoundSample.h"

#include <Mmdeviceapi.h>
#include "OutputPolicy.h"

#define RETURN_INTERFACE(T, iid, ppOut) \
    if (IsEqualIID(__uuidof(T), (iid))) { \
        this->AddRef(); \
        *(ppOut) = static_cast<T *>(this); \
        return S_OK; \
    } else {} (void)0

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputPolicy
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputPolicy::CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr)
: m_cRefCount(1), m_dwConfigData(dwConfigData), m_pOutputSchema(NULL)
{
    hr = CoCreateGuid(&m_guidOriginator);
    IF_FAILED_JUMP(hr, Exit);

    hr = CreateTrustedAudioDriversOutputSchema(dwConfigData, m_guidOriginator, &m_pOutputSchema);
    IF_FAILED_JUMP(hr, Exit);

Exit:
    if (FAILED(hr))
    {
        printf("CreateTrustedAudioDriversOutputSchema failed: hr = 0x%08x", hr);
    }
    return;
}

// destructor
CTrustedAudioDriversOutputPolicy::~CTrustedAudioDriversOutputPolicy()
{
    if (NULL != m_pOutputSchema) 
    {
        m_pOutputSchema->Release();
    }
}


// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE
    CTrustedAudioDriversOutputPolicy::QueryInterface(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject)
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);

    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputPolicy, riid, ppvObject);    

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}

// IMFOutputPolicy::GenerateRequiredSchemas
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GenerateRequiredSchemas
( 
        /* [in] */ DWORD dwAttributes,
        /* [in] */ GUID guidOutputSubType,
        /* [in] */ GUID *rgGuidProtectionSchemasSupported,
        /* [in] */ DWORD cProtectionSchemasSupported,
        /* [annotation][out] */ 
        __out  IMFCollection **ppRequiredProtectionSchemas
)
{
    HRESULT hr = S_OK;
    bool bTrustedAudioDriversSupported = false;
    // if we've made it this far then the Output Trust Authority supports Trusted Audio Drivers
    // create a collection and put our output policy in it
    // then give that collection to the caller
    CComPtr<IMFCollection> pMFCollection;

    // sanity checks
    IF_TRUE_ACTION_JUMP((NULL == ppRequiredProtectionSchemas), hr = E_POINTER, Exit); 
    *ppRequiredProtectionSchemas = NULL;

    IF_TRUE_ACTION_JUMP((NULL == rgGuidProtectionSchemasSupported) && (0 != cProtectionSchemasSupported), 
                    hr = E_POINTER, Exit); 

    // log all the supported protection schemas
    for (DWORD i = 0; i < cProtectionSchemasSupported; i++) 
    {
        if (IsEqualIID(MFPROTECTION_TRUSTEDAUDIODRIVERS, rgGuidProtectionSchemasSupported[i])) 
        {
            bTrustedAudioDriversSupported = true;
        }
    }

    if (!bTrustedAudioDriversSupported) 
    {
        return HRESULT_FROM_WIN32(ERROR_RANGE_NOT_FOUND);
    }


    // create the collection
    hr = MFCreateCollection(&pMFCollection);
    if (FAILED(hr)) 
    {
        return hr;
    }

    // add our output policy to the collection
    hr = pMFCollection->AddElement(m_pOutputSchema);
    if (FAILED(hr)) 
    {
        return hr;
    }
Exit:
    // give the collection to the caller
    return pMFCollection.CopyTo(ppRequiredProtectionSchemas); // increments refcount
}// GenerateRequiredSchemas

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetOriginatorID(__out  GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) 
    {
        return E_POINTER;
    }
    *pguidOriginatorID = m_guidOriginator;
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetMinimumGRLVersion(__out  DWORD *pdwMinimumGRLVersion) 
{
    if (NULL == pdwMinimumGRLVersion) 
    {
        return E_POINTER;
    }
    *pdwMinimumGRLVersion = 0;
    return S_OK;
}

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputSchema
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputSchema::CTrustedAudioDriversOutputSchema
(    
    DWORD dwConfigData, 
    GUID guidOriginatorID
)
: m_cRefCount(1)
, m_dwConfigData(dwConfigData)
, m_guidOriginatorID(guidOriginatorID)
{}

// destructor
CTrustedAudioDriversOutputSchema::~CTrustedAudioDriversOutputSchema() {}

// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::QueryInterface
(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject
) 
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);
    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputSchema, riid, ppvObject);

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}
// IMFOutputSchema::GetConfigurationData
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetConfigurationData(__out DWORD *pdwVal) 
{
    if (NULL == pdwVal) { return E_POINTER; }
    *pdwVal = m_dwConfigData;
    return S_OK;
}

// IMFOutputSchema::GetOriginatorID
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetOriginatorID(__out GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) { return E_POINTER; }
    *pguidOriginatorID = m_guidOriginatorID;
    return S_OK;
}
// IMFOutputSchema::GetSchemaType
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetSchemaType(__out GUID *pguidSchemaType) 
{
    if (NULL == pguidSchemaType) { return E_POINTER; }
    *pguidSchemaType = MFPROTECTION_TRUSTEDAUDIODRIVERS;
    return S_OK;
}

//---------------------------------------------------------------------------------------------------
//
// Other subroutine declarations
//
//---------------------------------------------------------------------------------------------------
HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy) 
{
    if (NULL == ppMFOutputPolicy) 
    {
        return E_POINTER;
    }

    *ppMFOutputPolicy = NULL;

    HRESULT hr = S_OK;
    CTrustedAudioDriversOutputPolicy *pPolicy = new CTrustedAudioDriversOutputPolicy(dwConfigData, hr);
    if (NULL == pPolicy) 
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr)) 
    {
        delete pPolicy;
        return hr;
    }
    *ppMFOutputPolicy = static_cast<IMFOutputPolicy *>(pPolicy);
    return S_OK;
}// CreateTrustedAudioDriversOutputPolicy

HRESULT CreateTrustedAudioDriversOutputSchema
(
    DWORD dwConfigData,
    GUID guidOriginatorID,
    IMFOutputSchema **ppMFOutputSchema) 
{
    if (NULL == ppMFOutputSchema) 
    {
        return E_POINTER;
    }

    *ppMFOutputSchema = NULL;

    CTrustedAudioDriversOutputSchema *pSchema =
        new CTrustedAudioDriversOutputSchema(dwConfigData, guidOriginatorID);

    if (NULL == pSchema) 
    {
        return E_OUTOFMEMORY;
    }

    *ppMFOutputSchema = static_cast<IMFOutputSchema *>(pSchema);

    return S_OK;
}// CreateTrustedAudioDriversOutputSchema



HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy)
{
    HRESULT hr = S_OK;

    DWORD dwCountOfOTAs = 0;
    bool bRet = false;

    hr = CreateTrustedAudioDriversOutputPolicy(_dwConfigData, _ppMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // activate IMFTrustedOutput
    hr = _pMMDevice->Activate(__uuidof(IMFTrustedOutput), CLSCTX_ALL, NULL,
                             (void**)_ppMFTrustedOutput);
    IF_FAILED_JUMP(hr, Exit);

    // get count of Output Trust Authorities on this trusted output
    hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityCount(&dwCountOfOTAs);
    IF_FAILED_JUMP(hr, Exit);

    // sanity check - fail on endpoints with no output trust authorities
    IF_TRUE_ACTION_JUMP((0 == dwCountOfOTAs), hr = E_NOTFOUND, Exit);

    printf("dwCountOfOTAs = %d\n", dwCountOfOTAs);

     
    // loop over each output trust authority on the endpoint
    for (DWORD i = 0; i < dwCountOfOTAs; i++) 
    {
        // get the output trust authority
        hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityByIndex(i, ppMFOutputTrustAuthority);
        IF_FAILED_JUMP(hr, Exit);


        // log the purpose of the output trust authority
        MFPOLICYMANAGER_ACTION action;
        hr = (*ppMFOutputTrustAuthority)->GetAction(&action);
        if (FAILED(hr)) 
        {
            return hr;
        }

        printf(" It's %s.", (PEACTION_PLAY==action) ? "PEACTION_PLAY" :
                            (PEACTION_COPY==action) ? "PEACTION_COPY" :
                            "Others");
 
        // only PEACTION_PLAY Output Trust Authorities are relevant
        if (PEACTION_PLAY != action) 
        {
            printf("Skipping as the OTA action is not PEACTION_PLAY");
            SAFE_RELEASE(*ppMFOutputTrustAuthority);
            continue;
        }

        BYTE *pbTicket = NULL;
        DWORD cbTicket = 0;
        // audio ota does not support ticket, leaving it NULL is ok.
        hr = (*ppMFOutputTrustAuthority)->SetPolicy(_ppMFOutputPolicy, 1, &pbTicket, &cbTicket);
        IF_FAILED_JUMP(hr, Exit);
        printf("SetPolicy succeeded.\n");

        bRet = true;
        break;

    }// for each output trust authority

Exit:
    if (bRet)
    {
        hr = S_OK;
    }
    if (FAILED(hr))
    {
        printf("failure code is 0x%0x\n", hr);
        SAFE_RELEASE(*ppMFOutputTrustAuthority);
        SAFE_RELEASE(*_ppMFTrustedOutput);
        if (*_ppMFOutputPolicy)
        {
            delete (*_ppMFOutputPolicy);
        }
    }

    return hr;
}


HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy)
{
    SAFE_RELEASE(_pMFOutputTrustAuthority);
    SAFE_RELEASE(_pMFTrustedOutput);
    if (_pMFOutputPolicy)
    {
        delete _pMFOutputPolicy;
    }
    return S_OK;
}
```




```cpp
//OTADSoundSample.rc
#include "windows.h"

/////////////////////////////////////////////////////////////////////////////
// Version
#include <ntverp.h>

#define VER_FILETYPE                VFT_DLL
#define VER_FILESUBTYPE             VFT2_UNKNOWN
#define VER_FILEDESCRIPTION_STR     "Default Device Heuristic Dumper"
#define VER_INTERNALNAME_STR        "DefaultDeviceDump.exe"
#define VER_ORIGINALFILENAME_STR    "DefaultDeviceDump.exe"

#include "common.ver"
```




```cpp
Sources file:

TARGETNAME=OTADSoundSample
TARGETTYPE=PROGRAM
TARGET_DESTINATION=retail
UMTYPE=console
UMENTRY=wmain
UMBASE=0x1000000
#_NT_TARGET_VERSION=$(_NT_TARGET_VERSION_VISTA)
MSC_WARNING_LEVEL=$(MSC_WARNING_LEVEL) /WX
USE_ATL=1
ATL_VER=70
USE_NATIVE_EH=1
USE_MSVCRT=1
C_DEFINES=-DUNICODE -D_UNICODE
INCLUDES=$(INCLUDES);  

SOURCES=OTADSoundSample.cpp \
        OTADSoundSample.rc \
        outputpolicy.cpp\

TARGETLIBS=\
       $(SDK_LIB_PATH)\advapi32.lib         \
       $(SDK_LIB_PATH)\kernel32.lib         \
       $(SDK_LIB_PATH)\User32.lib           \
       $(SDK_LIB_PATH)\shlwapi.lib          \
       $(SDK_LIB_PATH)\ole32.lib            \
       $(SDK_LIB_PATH)\oleaut32.lib         \
       $(SDK_LIB_PATH)\rpcrt4.lib           \
       $(SDK_LIB_PATH)\strmiids.lib         \
       $(SDK_LIB_PATH)\uuid.lib             \
       $(SDK_LIB_PATH)\SetupAPI.lib         \
       $(SDK_LIB_PATH)\mfplat.lib \
```



## <a name="related-topics"></a>相關主題

[程式設計指南](programming-guide.md)

[使用者模式音訊元件](user-mode-audio-components.md)
