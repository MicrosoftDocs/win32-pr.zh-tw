---
description: DirectShow 應用程式的裝置角色
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: DirectShow 應用程式的裝置角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df8b43ddd56870b65fc9ec1e3bb600e8e6b79528
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104467965"
---
# <a name="device-roles-for-directshow-applications"></a><span data-ttu-id="c163a-103">DirectShow 應用程式的裝置角色</span><span class="sxs-lookup"><span data-stu-id="c163a-103">Device Roles for DirectShow Applications</span></span>

> [!Note]  
> <span data-ttu-id="c163a-104">[MMDEVICE API](mmdevice-api.md)支援裝置角色。</span><span class="sxs-lookup"><span data-stu-id="c163a-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="c163a-105">不過，Windows Vista 中的使用者介面並不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="c163a-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="c163a-106">裝置角色的使用者介面支援可能會在未來的 Windows 版本中執行。</span><span class="sxs-lookup"><span data-stu-id="c163a-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="c163a-107">如需詳細資訊，請參閱 [Windows Vista 中的裝置角色](device-roles-in-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="c163a-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="c163a-108">DirectShow API 未提供方法讓應用程式選取指派給特定[裝置角色](device-roles.md)的[音訊端點裝置](audio-endpoint-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="c163a-108">The DirectShow API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that is assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="c163a-109">不過，在 Windows Vista 中，核心音訊 Api 可以與 DirectShow 應用程式搭配使用，以根據裝置角色啟用裝置選取。</span><span class="sxs-lookup"><span data-stu-id="c163a-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectShow application to enable device selection based on device role.</span></span> <span data-ttu-id="c163a-110">透過核心音訊 Api 的協助，應用程式可以：</span><span class="sxs-lookup"><span data-stu-id="c163a-110">With the help of the core audio APIs, the application can:</span></span>

-   <span data-ttu-id="c163a-111">識別使用者已指派給特定裝置角色的音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="c163a-111">Identify the audio endpoint device that the user has assigned to a particular device role.</span></span>
-   <span data-ttu-id="c163a-112">使用封裝音訊端點裝置的 [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) 介面建立 DirectShow 音訊轉譯篩選器。</span><span class="sxs-lookup"><span data-stu-id="c163a-112">Create a DirectShow audio rendering filter with an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface that encapsulates the audio endpoint device.</span></span>
-   <span data-ttu-id="c163a-113">建立包含篩選準則的 DirectShow 圖形。</span><span class="sxs-lookup"><span data-stu-id="c163a-113">Build a DirectShow graph that incorporates the filter.</span></span>

<span data-ttu-id="c163a-114">如需有關 DirectShow 和 [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter)的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="c163a-114">For more information about DirectShow and [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), see the Windows SDK documentation.</span></span>

<span data-ttu-id="c163a-115">下列程式碼範例示範如何建立 DirectShow 音訊轉譯篩選器，以封裝指派給特定裝置角色的轉譯端點裝置：</span><span class="sxs-lookup"><span data-stu-id="c163a-115">The following code example shows how to create a DirectShow audio rendering filter that encapsulates the rendering endpoint device that is assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// Create a DirectShow audio rendering filter that
// encapsulates the audio endpoint device that is currently
// assigned to the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

// This application's audio session GUID
const GUID guidAudioSessionId = {
    0xb13ff52e, 0xa5cf, 0x4fca,
    {0x9f, 0xc3, 0x42, 0x26, 0x5b, 0x0b, 0x14, 0xfb}
};

HRESULT CreateAudioRenderer(ERole role, IBaseFilter** ppAudioRenderer)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    if (ppAudioRenderer == NULL)
    {
        return E_POINTER;
    }

    // Activate the IBaseFilter interface on the
    // audio renderer with the specified role.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator,
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    DIRECTX_AUDIO_ACTIVATION_PARAMS  daap;
    daap.cbDirectXAudioActivationParams = sizeof(daap);
    daap.guidAudioSession = guidAudioSessionId;
    daap.dwAudioStreamFlags = AUDCLNT_STREAMFLAGS_CROSSPROCESS;

    PROPVARIANT  var;
    PropVariantInit(&var);

    var.vt = VT_BLOB;
    var.blob.cbSize = sizeof(daap);
    var.blob.pBlobData = (BYTE*)&daap;

    hr = pDevice->Activate(__uuidof(IBaseFilter),
                           CLSCTX_ALL, &var,
                           (void**)ppAudioRenderer);
    EXIT_ON_ERROR(hr)

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    return hr;
}
```



<span data-ttu-id="c163a-116">在上述程式碼範例中，CreateAudioRenderer 函式會接受裝置角色 (eConsole、eMultimedia 或 eCommunications) 做為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="c163a-116">In the preceding code example, the CreateAudioRenderer function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="c163a-117">第二個參數是函式用來寫入 [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) 介面實例位址的指標。</span><span class="sxs-lookup"><span data-stu-id="c163a-117">The second parameter is a pointer through which the function writes the address of an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface instance.</span></span> <span data-ttu-id="c163a-118">此外，此範例會示範如何使用 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法，將 **IBaseFilter** 實例中的音訊串流指派給跨進程音訊會話，並使用 **guidAudioSessionId** 常數) 指定的應用程式特定會話 GUID (。</span><span class="sxs-lookup"><span data-stu-id="c163a-118">In addition, the example shows how to use the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to assign the audio stream in the **IBaseFilter** instance to a cross-process audio session with an application-specific session GUID (specified by the **guidAudioSessionId** constant).</span></span> <span data-ttu-id="c163a-119">**啟動** 呼叫中的第三個參數指向包含會話 GUID 和跨進程旗標的結構。</span><span class="sxs-lookup"><span data-stu-id="c163a-119">The third parameter in the **Activate** call points to a structure that contains the session GUID and cross-process flag.</span></span> <span data-ttu-id="c163a-120">如果使用者執行應用程式的多個實例，則來自所有實例的音訊串流會使用相同的會話 GUID，因此屬於相同的會話。</span><span class="sxs-lookup"><span data-stu-id="c163a-120">If the user runs multiple instances of the application, then the audio streams from all the instances use the same session GUID and thus belong to the same session.</span></span>

<span data-ttu-id="c163a-121">或者，呼叫端可以指定 **Null** 做為 [**啟動**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 呼叫中的第三個參數，將資料流程指派為預設會話，以做為具有會話 guid 值 guid Null 的進程特定會話 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c163a-121">Alternatively, the caller can specify **NULL** as the third parameter in the [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) call to assign the stream to the default session as the process-specific session with session GUID value GUID\_NULL.</span></span> <span data-ttu-id="c163a-122">如需詳細資訊，請參閱 **IMMDevice：： Activate**。</span><span class="sxs-lookup"><span data-stu-id="c163a-122">For more information, see **IMMDevice::Activate**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c163a-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="c163a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c163a-124">與舊版音訊 Api 的互通性</span><span class="sxs-lookup"><span data-stu-id="c163a-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
