---
description: Windows Vista 引進受保護的使用者模式音訊 (PUMA) 、受保護環境中的使用者模式音訊引擎 (PE) ，可提供更安全的音訊處理和轉譯環境。
ms.assetid: 27a50026-9e48-48b1-9249-7528a97333c9
title: '受保護的使用者模式音訊 (PUMA) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233dc82109feb66472e66e4235031696937d70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847515"
---
# <a name="protected-user-mode-audio-puma"></a><span data-ttu-id="a726f-103">受保護的使用者模式音訊 (PUMA) </span><span class="sxs-lookup"><span data-stu-id="a726f-103">Protected User Mode Audio (PUMA)</span></span>

<span data-ttu-id="a726f-104">Windows Vista 引進受保護的使用者模式音訊 (PUMA) 、受保護環境中的使用者模式音訊引擎 (PE) ，可提供更安全的音訊處理和轉譯環境。</span><span class="sxs-lookup"><span data-stu-id="a726f-104">Windows Vista introduced Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE) that provides a safer environment for audio processing and rendering.</span></span> <span data-ttu-id="a726f-105">它只允許啟用可接受的音訊輸出，並確保能可靠地停用輸出。</span><span class="sxs-lookup"><span data-stu-id="a726f-105">It allows only the acceptable audio outputs to be enabled and ensures that the outputs are disabled reliably.</span></span> <span data-ttu-id="a726f-106">如需 PUMA 的詳細資訊，請參閱 [內容保護和 Windows Vista 的輸出](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc)。</span><span class="sxs-lookup"><span data-stu-id="a726f-106">For more information about PUMA, see [Output Content Protection and Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).</span></span>

<span data-ttu-id="a726f-107">Windows 7 的 PUMA 已更新，可提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="a726f-107">PUMA has been updated for Windows 7 to provide the following features:</span></span>

-   <span data-ttu-id="a726f-108">在) 的多媒體介面 High-Definition HDMI (端點上，設定序號複製管理系統 (SCMS) 位於 S/PDIF 端點和高頻寬數位內容保護 (HDCP) 位。</span><span class="sxs-lookup"><span data-stu-id="a726f-108">Setting Serial Copying Management System (SCMS) bits on S/PDIF endpoints and High-bandwidth Digital Content Protection (HDCP) bits on High-Definition Multimedia Interface (HDMI) endpoints.</span></span>
-   <span data-ttu-id="a726f-109">在受保護的環境以外啟用 SCMS 和 HDMI 保護控制項， (PE) 。</span><span class="sxs-lookup"><span data-stu-id="a726f-109">Enabling SCMS and HDMI protection controls outside of a Protected Environment (PE).</span></span>

## <a name="drm-protection-in-audio-drivers"></a><span data-ttu-id="a726f-110">音訊驅動程式中的 DRM 保護</span><span class="sxs-lookup"><span data-stu-id="a726f-110">DRM Protection in Audio Drivers</span></span>

<span data-ttu-id="a726f-111">數位 Rights Management (DRM) 讓您能夠在安全的容器中封裝媒體資料，並將使用規則附加至內容。</span><span class="sxs-lookup"><span data-stu-id="a726f-111">Digital Rights Management (DRM) provides the ability to package media data in a secure container and attach usage rules to the content.</span></span> <span data-ttu-id="a726f-112">例如，內容提供者可能會使用 **禁止複製** 或 **數位輸出停** 用來停用直接數位複製或從電腦系統傳輸。</span><span class="sxs-lookup"><span data-stu-id="a726f-112">For example, the content provider might use **Copy Protection** or **Digital Output Disable** to disable direct digital copies or transmission out of the PC system.</span></span>

<span data-ttu-id="a726f-113">某些 Microsoft 產品中的音訊堆疊藉由實行管理音訊內容播放的使用規則，支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="a726f-113">The audio stack in certain Microsoft products supports DRM by implementing the usage rules that govern playback of the audio content.</span></span> <span data-ttu-id="a726f-114">若要播放受保護的內容，基礎音訊驅動程式必須是 *信任的驅動程式*;也就是說，驅動程式必須是 DRMLevel 1300 的標誌認證。</span><span class="sxs-lookup"><span data-stu-id="a726f-114">To play the protected content, the underlying audio driver must be a *trusted driver*; that is, the driver must be logo-certified for DRMLevel 1300.</span></span> <span data-ttu-id="a726f-115">如需開發受信任驅動程式的相關資訊，您可以使用 Windows 2000 驅動程式開發工具組中定義的介面 ( 「DDK」 ) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a726f-115">For information about developing trusted drivers, you can use interfaces that are defined in the Windows 2000 Driver Development Kit ("DDK") or later.</span></span> <span data-ttu-id="a726f-116">使用 DDK 開發的驅動程式將會針對 DRM 執行必要的介面。</span><span class="sxs-lookup"><span data-stu-id="a726f-116">Drivers developed with the DDK will implement the necessary interfaces to DRM.</span></span> <span data-ttu-id="a726f-117">如需詳細資訊，請參閱 [數位 Rights Management](/windows-hardware/drivers/audio/digital-rights-management)。</span><span class="sxs-lookup"><span data-stu-id="a726f-117">For more information, see [Digital Rights Management](/windows-hardware/drivers/audio/digital-rights-management).</span></span>

<span data-ttu-id="a726f-118">若要轉譯受保護的內容，信任的驅動程式必須檢查是否已在流經音訊堆疊的內容上設定 **禁止複製** 和 **數位輸出停** 用，並據以回應設定。</span><span class="sxs-lookup"><span data-stu-id="a726f-118">To render the protected content, the trusted driver must check whether **Copy Protection** and **Digital Output Disable** are set on the content flowing through the audio stack, and respond to the settings accordingly.</span></span>

### <a name="copy-protection-rule"></a><span data-ttu-id="a726f-119">禁止複製規則</span><span class="sxs-lookup"><span data-stu-id="a726f-119">Copy Protection Rule</span></span>

<span data-ttu-id="a726f-120">**禁止複製** 表示系統不允許直接數位複製。</span><span class="sxs-lookup"><span data-stu-id="a726f-120">**Copy Protection** indicates that direct digital copies are not allowed on the system.</span></span> <span data-ttu-id="a726f-121">對 WHQL 測試合約的展示 B 已更新，以反映在內容上設定 **禁止複製** 時，驅動程式的新期望和需求。</span><span class="sxs-lookup"><span data-stu-id="a726f-121">Exhibit B to the WHQL Testing Agreement has been updated to reflect the new expectations and requirements of a driver when **Copy Protection** is set on the content.</span></span> <span data-ttu-id="a726f-122">在 Windows 7 中，內建的 HD 音訊類別驅動程式符合最新的需求。</span><span class="sxs-lookup"><span data-stu-id="a726f-122">For Windows 7, the built-in HD audio class driver complies with the latest requirements.</span></span>

<span data-ttu-id="a726f-123">除了確保不允許內容傳遞至另一個元件，或儲存在 DRM 系統未驗證的任何非靜態儲存媒體上，音訊驅動程式會在設定 **禁止複製** 時執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="a726f-123">In addition to ensuring that content is not allowed to pass to another component or be stored on any nonvolatile storage medium that is not authenticated by the DRM system, the audio driver performs the following tasks when **Copy Protection** is set:</span></span>

-   <span data-ttu-id="a726f-124">驅動程式可讓您在 HDMI 端點上進行 HDCP。</span><span class="sxs-lookup"><span data-stu-id="a726f-124">The driver enables HDCP on HDMI endpoints.</span></span>
-   <span data-ttu-id="a726f-125">針對 S/PDIF 介面，驅動程式會驗證 L、Cp 和分類程式代碼位的組合是否表示「永遠不復制」的 SCMS 狀態，如 IEC 60958 中所定義。</span><span class="sxs-lookup"><span data-stu-id="a726f-125">For S/PDIF interfaces, the driver validates that the combination of L, Cp and Category Code bits indicates an SCMS state of "Copy Never", as defined in IEC 60958.</span></span>
-   <span data-ttu-id="a726f-126">L 位設定為0，而類別代碼會設定為「數位信號混音器」。</span><span class="sxs-lookup"><span data-stu-id="a726f-126">The L bit is set to 0 and the Category Code is set to "Digital Signal Mixer".</span></span>

<span data-ttu-id="a726f-127">受信任音訊驅動程式所使用的 **DRMRIGHTS** 結構，指定指派給 KS 音訊 pin 或埠類別驅動程式資料流程物件的 DRM 內容許可權。</span><span class="sxs-lookup"><span data-stu-id="a726f-127">The **DRMRIGHTS** structure, used by trusted audio drivers, specifies the DRM content rights assigned to a KS audio pin or to a port-class driver's stream object.</span></span> <span data-ttu-id="a726f-128">**CopyProtect** 成員會指出是否已在音訊內容上設定 **禁止複製**。</span><span class="sxs-lookup"><span data-stu-id="a726f-128">The **CopyProtect** member indicates whether **Copy Protection** is set on the audio content.</span></span>

<span data-ttu-id="a726f-129">針對 Windows 7，使用 **CopyProtect** 會更嚴格。</span><span class="sxs-lookup"><span data-stu-id="a726f-129">For Windows 7, the use of **CopyProtect** is stricter.</span></span> <span data-ttu-id="a726f-130">驅動程式可確保在音訊介面上設定保護控制項，並針對 HDMI 輸出設定 HDCP，並將 [狀態] 設定為 [永遠不復制]，以設定 S/PDIF 輸出的 SCMS。</span><span class="sxs-lookup"><span data-stu-id="a726f-130">The driver ensures that the protection controls are set on the audio interfaces, HDCP is set for HDMI output, and SCMS is set for S/PDIF output by setting the state to "Copy Never".</span></span>

### <a name="digital-output-disable-rule"></a><span data-ttu-id="a726f-131">數位輸出停用規則</span><span class="sxs-lookup"><span data-stu-id="a726f-131">Digital Output Disable Rule</span></span>

<span data-ttu-id="a726f-132">**數位輸出停** 用表示不允許從系統傳送內容。</span><span class="sxs-lookup"><span data-stu-id="a726f-132">**Digital Output Disable** indicates that the content is not allowed to be transmitted out of the system.</span></span> <span data-ttu-id="a726f-133">在 Windows 7 中，內建的 HD 音訊類別驅動程式會藉由啟用在 HDMI 端點上的 HDCP 來回應此設定。</span><span class="sxs-lookup"><span data-stu-id="a726f-133">In Windows 7, the built-in HD audio class driver responds to this setting by enabling HDCP on HDMI endpoints.</span></span> <span data-ttu-id="a726f-134">這類似于驅動程式對 **禁止複製** 設定的回應。</span><span class="sxs-lookup"><span data-stu-id="a726f-134">This is similar to the driver's response to the **Copy Protection** setting.</span></span>

## <a name="enabling-content-protection-mechanisms-outside-of-a-protected-environment"></a><span data-ttu-id="a726f-135">啟用受保護環境以外的內容保護機制</span><span class="sxs-lookup"><span data-stu-id="a726f-135">Enabling Content-Protection Mechanisms Outside of a Protected Environment</span></span>

<span data-ttu-id="a726f-136">PUMA 位於受保護環境 (PE) 中的個別進程。</span><span class="sxs-lookup"><span data-stu-id="a726f-136">PUMA resides in a separate process in the Protected Environment (PE).</span></span> <span data-ttu-id="a726f-137">在 Windows Vista 中，若要使用 PUMA 所提供的音訊內容保護控制項，媒體應用程式必須在 PE 中。</span><span class="sxs-lookup"><span data-stu-id="a726f-137">In Windows Vista, to use the audio content protection controls offered by PUMA, a media application must be in a PE.</span></span> <span data-ttu-id="a726f-138">因為只有媒體基礎 Api 可以與 PE 互動，所以內容保護控制項僅限於使用媒體基礎 Api 來串流音訊內容的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a726f-138">Because only Media Foundation APIs can interact with a PE, the content protection controls are limited to applications using Media Foundation APIs to stream audio content.</span></span>

<span data-ttu-id="a726f-139">在 Windows 7 中，任何應用程式都可以存取 PUMA 輸出信任授權單位 (OTA) 所提供的內容保護控制項，不論它們是在 PE 中或使用媒體基礎 Api 來播放音訊。</span><span class="sxs-lookup"><span data-stu-id="a726f-139">In Windows 7, any application can access the content protection controls provided by the PUMA Output Trust Authority (OTA), regardless of whether they are in a PE or using Media Foundation APIs for audio playback.</span></span>

## <a name="implementation-instructions"></a><span data-ttu-id="a726f-140">實作指示</span><span class="sxs-lookup"><span data-stu-id="a726f-140">Implementation Instructions</span></span>

<span data-ttu-id="a726f-141">音訊應用程式需要執行下列步驟，才能控制音訊端點上的 SCMS 或 HDCP 內容保護。</span><span class="sxs-lookup"><span data-stu-id="a726f-141">The following steps are required for an audio application to control SCMS or HDCP content protection on an audio endpoint.</span></span> <span data-ttu-id="a726f-142">支援的音訊 Api 包括 DirectShow、DirectSound 和 WASAPI。</span><span class="sxs-lookup"><span data-stu-id="a726f-142">Supported Audio APIs are DirectShow, DirectSound, and WASAPI.</span></span>

<span data-ttu-id="a726f-143">此範例程式碼會使用下列介面。</span><span class="sxs-lookup"><span data-stu-id="a726f-143">This example code uses the following interfaces.</span></span>

-   [<span data-ttu-id="a726f-144">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="a726f-144">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="a726f-145">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="a726f-145">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="a726f-146">**IAudioClient**</span><span class="sxs-lookup"><span data-stu-id="a726f-146">**IAudioClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)
-   [<span data-ttu-id="a726f-147">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="a726f-147">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
-   [<span data-ttu-id="a726f-148">**IMFTrustedOutput**</span><span class="sxs-lookup"><span data-stu-id="a726f-148">**IMFTrustedOutput**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput)
-   [<span data-ttu-id="a726f-149">**IMFOutputPolicy**</span><span class="sxs-lookup"><span data-stu-id="a726f-149">**IMFOutputPolicy**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)

<span data-ttu-id="a726f-150">媒體應用程式必須執行下列工作。</span><span class="sxs-lookup"><span data-stu-id="a726f-150">The media application must perform the following tasks.</span></span>

1.  <span data-ttu-id="a726f-151">設定開發環境。</span><span class="sxs-lookup"><span data-stu-id="a726f-151">Set up the development environment.</span></span>
    -   <span data-ttu-id="a726f-152">參考所需的介面，包括下列程式碼中所示的標頭。</span><span class="sxs-lookup"><span data-stu-id="a726f-152">Reference the required interfaces, include the headers shown in the following code.</span></span>
        ```cpp
        #include <MMdeviceapi.h>        // Device endpoint definitions
        #include <Mfidl.h>              // OTA interface definitions
        ```

        

    -   <span data-ttu-id="a726f-153">連結至 Mfuuid，以使用 OTA 介面。</span><span class="sxs-lookup"><span data-stu-id="a726f-153">Link to the Mfuuid.lib to use the OTA interfaces.</span></span>
    -   <span data-ttu-id="a726f-154">停用內核偵錯工具和驅動程式驗證程式，以避免任何驗證檢查錯誤。</span><span class="sxs-lookup"><span data-stu-id="a726f-154">Disable the kernel debugger and driver verifier to avoid any authentication checking errors.</span></span>
2.  <span data-ttu-id="a726f-155">列舉系統中的所有端點，並從端點集合中選取目標端點，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="a726f-155">Enumerate all endpoints in the system and select the target endpoint from the endpoint collection, as shown in the following code.</span></span> <span data-ttu-id="a726f-156">如需列舉裝置的詳細資訊，請參閱 [列舉音訊裝置](/previous-versions//ms678716(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a726f-156">For more information about enumerating devices, see [Enumerating Audio Devices](/previous-versions//ms678716(v=vs.85)).</span></span>
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

    

3.  <span data-ttu-id="a726f-157">使用列舉程式所傳回之端點的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 指標，來啟用所需的音訊串流 API 並準備進行串流。</span><span class="sxs-lookup"><span data-stu-id="a726f-157">Use the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) pointer to the endpoint returned by the enumeration process to activate the desired audio streaming API and prepare for streaming.</span></span> <span data-ttu-id="a726f-158">不同的音訊 Api 需要稍微不同的準備工作。</span><span class="sxs-lookup"><span data-stu-id="a726f-158">Different audio APIs require slightly different preparation.</span></span>
    -   <span data-ttu-id="a726f-159">針對 DShow 音訊應用程式：</span><span class="sxs-lookup"><span data-stu-id="a726f-159">For DShow audio applications:</span></span>
        1.  <span data-ttu-id="a726f-160">藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 並指定 IID \_ IBaseFilter 作為介面識別碼，以建立 DirectShow COM 物件。</span><span class="sxs-lookup"><span data-stu-id="a726f-160">Create a DirectShow COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IBaseFilter as the interface identifier.</span></span>
            ```cpp
            IUnknown *pDShowFilter = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IBaseFilter,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDShowFilter));
            ```

            

        2.  <span data-ttu-id="a726f-161">使用由裝置啟用的這個 COM 物件來建立 DirectShow 篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="a726f-161">Build a DirectShow filter graph with this COM object activated by the device.</span></span> <span data-ttu-id="a726f-162">如需此程式的詳細資訊，請參閱 DirectShow SDK 檔中的「建立篩選圖形」。</span><span class="sxs-lookup"><span data-stu-id="a726f-162">For more information about this process, see "Building the Filter Graph" in DirectShow SDK documentation.</span></span>
    -   <span data-ttu-id="a726f-163">針對 DSound 音訊應用程式：</span><span class="sxs-lookup"><span data-stu-id="a726f-163">For DSound audio applications:</span></span>
        1.  <span data-ttu-id="a726f-164">藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 並指定 IID \_ IDirectSound8 作為介面識別碼，來建立 DSound COM 物件。</span><span class="sxs-lookup"><span data-stu-id="a726f-164">Create a DSound COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IDirectSound8 as the interface identifier.</span></span>
            ```cpp
            IDirectSound8  *pDSSound8;
            ...
            hr = pDevice->Activate (
                              IID_IDirectSound8,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDSSound8));
            ```

            

        2.  <span data-ttu-id="a726f-165">使用上面建立的 DSound 物件，以針對串流進行程式 DSound。</span><span class="sxs-lookup"><span data-stu-id="a726f-165">Use DSound object created above to program DSound for steaming.</span></span> <span data-ttu-id="a726f-166">如需此程式的詳細資訊，請參閱 MSDN 上的 [DirectSound](/previous-versions//bb219818(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="a726f-166">For more information about this process, see [DirectSound](/previous-versions//bb219818(v=vs.85)) on MSDN.</span></span>
    -   <span data-ttu-id="a726f-167">針對 WASAPI：</span><span class="sxs-lookup"><span data-stu-id="a726f-167">For WASAPI:</span></span>
        1.  <span data-ttu-id="a726f-168">藉由 [](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)呼叫 [**IMMDevice：： ACTI加值稅E**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)並指定 IID \_ IAudioClient 作為介面識別碼，來建立 IAudioClient COM 物件。</span><span class="sxs-lookup"><span data-stu-id="a726f-168">Create an [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IAudioClient as the interface identifier.</span></span>
            ```cpp
            IAudioClient *pIAudioClient = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IAudioClient,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pIAudioClient));
            ```

            

        2.  <span data-ttu-id="a726f-169">開啟音訊串流。</span><span class="sxs-lookup"><span data-stu-id="a726f-169">Open the audio stream.</span></span>
            ```cpp
            hr = pIAudioClient->Initialize(...);
            ```

            
4.  <span data-ttu-id="a726f-170">開始音訊串流。</span><span class="sxs-lookup"><span data-stu-id="a726f-170">Start audio streaming.</span></span>
5.  <span data-ttu-id="a726f-171">設定資料流程的保護原則。</span><span class="sxs-lookup"><span data-stu-id="a726f-171">Set the protection policy on the stream.</span></span>
    1.  <span data-ttu-id="a726f-172">針對 WASAPI 用戶端，請呼叫 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) ，並指定 IID IMFTrustedOutput 作為介面識別碼，以取得資料流程的輸出信任授權單位的 [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput)介面參考 (OTA) 物件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a726f-172">For WASAPI clients, get a reference to the [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) interface of the output trust authority (OTA) object for the stream by calling [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) and specifying IID\_IMFTrustedOutput as the interface identifier.</span></span>
        ```cpp
        IMFTrustedOutput*       pTrustedOutput = NULL;
        hr = pIAudioClient>GetService(
                       __uuidof(IMFTrustedOutput),
                       (void**)& pTrustedOutput);
        ```

        

    2.  <span data-ttu-id="a726f-173">藉由呼叫 [**IMFTrustedOutput：： GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount)來取得可用 OTA 物件的計數。</span><span class="sxs-lookup"><span data-stu-id="a726f-173">Get a count of the available OTA objects by calling [**IMFTrustedOutput::GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount).</span></span>
        ```cpp
        hr = pTrustedOutput->GetOutputTrustAuthorityCount(&m_dwCountOTA);
        ```

        

    3.  <span data-ttu-id="a726f-174">列舉 OTA 集合，並取得支援 action PEACTION PLAY 之 OTA 物件的參考 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a726f-174">Enumerate the OTA collection and get a reference to the OTA object that supports the action PEACTION\_PLAY.</span></span> <span data-ttu-id="a726f-175">所有 OTAs 都會公開 [**IMFOutputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) 介面。</span><span class="sxs-lookup"><span data-stu-id="a726f-175">All OTAs expose the [**IMFOutputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) interface.</span></span>
        ```cpp
        hr = pMFTrustedOutput->GetOutputTrustAuthorityByIndex(I, &pMFOutputTrustAuthority);
        hr = pMFOutputTrustAuthority->GetAction(&action) 
        ```

        

    4.  <span data-ttu-id="a726f-176">使用 [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) 介面設定資料流程上的保護原則。</span><span class="sxs-lookup"><span data-stu-id="a726f-176">Use the [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) interface to set the protection policy on the stream.</span></span>

        ```cpp
        hr = pTrustedOutput ->SetPolicy(&pPolicy, nPolicy, &pbTicket, &cbTicket);
        ```

        

        > [!Note]
        > <span data-ttu-id="a726f-177">如果您使用 EVR， [**SetPolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) 會引發 [MEPolicySet](../medfound/mepolicyset.md) 事件，並傳回 MF \_ S \_ 等候 \_ \_ 原則 \_ 設定，以表示 OTA 將會以非同步方式強制執行原則。</span><span class="sxs-lookup"><span data-stu-id="a726f-177">If you are using the EVR, [**SetPolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) raises the [MEPolicySet](../medfound/mepolicyset.md) event and returns MF\_S\_WAIT\_FOR\_POLICY\_SET to indicate that the OTA will enforce the policy asynchronously.</span></span> <span data-ttu-id="a726f-178">不過，在此範例程式碼中，應用程式是直接 WASAPI 用戶端，從音訊用戶端取出 OTA 物件 (步驟 5 a) 。</span><span class="sxs-lookup"><span data-stu-id="a726f-178">However, in this example code, the application is a direct WASAPI client that retrieved the OTA object from the audio client (Step 5 a).</span></span> <span data-ttu-id="a726f-179">不同于 EVR，音訊用戶端和其他 WASAPI 物件不會執行媒體事件產生器。</span><span class="sxs-lookup"><span data-stu-id="a726f-179">Unlike the EVR, an audio client and other WASAPI objects do not implement media event generators.</span></span> <span data-ttu-id="a726f-180">如果沒有媒體事件產生器， **IMFTrustedOutput：： SetPolicy** 不會傳回 MF \_ \_ 等候 \_ \_ 原則 \_ 集。</span><span class="sxs-lookup"><span data-stu-id="a726f-180">Without media event generators, **IMFTrustedOutput::SetPolicy** does not return MF\_S\_WAIT\_FOR\_POLICY\_SET.</span></span>
        >
        > <span data-ttu-id="a726f-181">音訊原則設定必須在音訊串流開始之後設定，否則 [**IMFTrustedOutput：： GetOutputTrustAuthorityByIndex**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) 會失敗。</span><span class="sxs-lookup"><span data-stu-id="a726f-181">The audio policy settings must be set after audio streaming starts, otherwise [**IMFTrustedOutput::GetOutputTrustAuthorityByIndex**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) fails.</span></span> <span data-ttu-id="a726f-182">此外，若要支援這項功能，基礎音訊驅動程式必須是 *信任的驅動程式*。</span><span class="sxs-lookup"><span data-stu-id="a726f-182">Also, to support this feature, the underlying audio driver must be a *trusted driver*.</span></span>

         

        <span data-ttu-id="a726f-183">在範例程式碼中， *pPolicy* 是用戶端所執行之原則物件的 [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="a726f-183">In the example code, *pPolicy* is a pointer to the [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) interface of a client-implemented policy object.</span></span> <span data-ttu-id="a726f-184">如需詳細資訊，請參閱 [媒體基礎 SDK](../medfound/microsoft-media-foundation-sdk.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="a726f-184">For information, see [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) documentation.</span></span>

        <span data-ttu-id="a726f-185">在 [**IMFOutputPolicy：： GenerateRequiredSchemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) 方法的執行中，必須產生 OTA 必須強制執行的輸出保護系統 (架構) 的集合。</span><span class="sxs-lookup"><span data-stu-id="a726f-185">In the implementation of the [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) method, a collection of the output protection systems (schemas) must be generated that the OTA must enforce.</span></span> <span data-ttu-id="a726f-186">每個架構都是由 GUID 所識別，並包含保護系統的設定資料。</span><span class="sxs-lookup"><span data-stu-id="a726f-186">Each schema is identified by a GUID and contains configuration data for the protection system.</span></span> <span data-ttu-id="a726f-187">請確定集合中的保護系統限制為使用受信任的音訊驅動程式。</span><span class="sxs-lookup"><span data-stu-id="a726f-187">Make sure that the protection systems in the collection are restricted to using trusted audio drivers.</span></span> <span data-ttu-id="a726f-188">這項限制是由 GUID、 **MFPROTECTION \_ TRUSTEDAUDIODRIVERS**、DISABLE 或 CONSTRICTAUDIO 所識別。</span><span class="sxs-lookup"><span data-stu-id="a726f-188">This restriction is identified by the GUID, **MFPROTECTION\_TRUSTEDAUDIODRIVERS**,DISABLE, or CONSTRICTAUDIO.</span></span> <span data-ttu-id="a726f-189">如果 \_ 使用 MFPROTECTION TRUSTEDAUDIODRIVERS，則此架構的設定資料為 DWORD。</span><span class="sxs-lookup"><span data-stu-id="a726f-189">If MFPROTECTION\_TRUSTEDAUDIODRIVERS is used, the configuration data for this schema is a DWORD.</span></span> <span data-ttu-id="a726f-190">如需有關架構和相關設定資料的詳細資訊，請參閱受保護的環境 SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="a726f-190">For more information about the schemas and the related configuration data, see Protected Environment SDK documentation.</span></span>

        <span data-ttu-id="a726f-191">用戶端也必須提供架構定義，方法是執行 [**IMFOutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) 介面。</span><span class="sxs-lookup"><span data-stu-id="a726f-191">The client must also provide the schema definition, by implementing the [**IMFOutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) interface.</span></span> <span data-ttu-id="a726f-192">[**IMFOutputSchema：： GetSchemaType**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) 會將 **MFPROTECTION \_ TRUSTEDAUDIODRIVERS** 抓取為架構 GUID。</span><span class="sxs-lookup"><span data-stu-id="a726f-192">[**IMFOutputSchema::GetSchemaType**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) retrieves **MFPROTECTION\_TRUSTEDAUDIODRIVERS** as the schema GUID.</span></span> <span data-ttu-id="a726f-193">[**IMFOutputSchema：： GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) 會傳回架構設定資料的指標。</span><span class="sxs-lookup"><span data-stu-id="a726f-193">[**IMFOutputSchema::GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) returns a pointer to the schema's configuration data.</span></span>

6.  <span data-ttu-id="a726f-194">繼續音訊串流。</span><span class="sxs-lookup"><span data-stu-id="a726f-194">Continue audio streaming.</span></span>
7.  <span data-ttu-id="a726f-195">在停止串流之前，請確定保護原則是明確的。</span><span class="sxs-lookup"><span data-stu-id="a726f-195">Make sure the protection policy is clear before stopping streaming.</span></span>

    <span data-ttu-id="a726f-196">釋放上述的相關原則介面參考。</span><span class="sxs-lookup"><span data-stu-id="a726f-196">Release the related policy interface references above.</span></span>

    <span data-ttu-id="a726f-197">發行呼叫會清除先前設定的原則設定。</span><span class="sxs-lookup"><span data-stu-id="a726f-197">The release calls clear the previously set policy settings.</span></span>

    > [!Note]  
    > <span data-ttu-id="a726f-198">每次重新開機串流時，都必須在資料流程上再次設定保護原則。</span><span class="sxs-lookup"><span data-stu-id="a726f-198">Every time a stream is restarted, the protection policy must be set again on the stream.</span></span> <span data-ttu-id="a726f-199">步驟 5-d 中會說明此程式。</span><span class="sxs-lookup"><span data-stu-id="a726f-199">The procedure is described in step 5-d.</span></span>

    ```cpp
    pMFOutputTrustAuthority->Release()
    pMFTrustedOutput->Release()
    ```
  

<span data-ttu-id="a726f-200">下列程式碼範例顯示原則和架構物件的範例執行。</span><span class="sxs-lookup"><span data-stu-id="a726f-200">The following code examples show a sample implementation of the policy and schema objects.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a726f-201">相關主題</span><span class="sxs-lookup"><span data-stu-id="a726f-201">Related topics</span></span>

[<span data-ttu-id="a726f-202">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="a726f-202">Programming Guide</span></span>](programming-guide.md)

[<span data-ttu-id="a726f-203">使用者模式音訊元件</span><span class="sxs-lookup"><span data-stu-id="a726f-203">User-Mode Audio Components</span></span>](user-mode-audio-components.md)
