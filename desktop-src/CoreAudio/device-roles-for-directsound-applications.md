---
description: DirectSound 應用程式的裝置角色
ms.assetid: 7d82d67f-aad8-4e5b-ac65-87d75774e613
title: DirectSound 應用程式的裝置角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3829817f8b00c7288aceb8d0b6d418d5793ae580
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936052"
---
# <a name="device-roles-for-directsound-applications"></a><span data-ttu-id="3937a-103">DirectSound 應用程式的裝置角色</span><span class="sxs-lookup"><span data-stu-id="3937a-103">Device Roles for DirectSound Applications</span></span>

> [!Note]  
> <span data-ttu-id="3937a-104">[MMDEVICE API](mmdevice-api.md)支援裝置角色。</span><span class="sxs-lookup"><span data-stu-id="3937a-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="3937a-105">不過，Windows Vista 中的使用者介面並不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="3937a-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="3937a-106">裝置角色的使用者介面支援可能會在未來的 Windows 版本中執行。</span><span class="sxs-lookup"><span data-stu-id="3937a-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="3937a-107">如需詳細資訊，請參閱 [Windows Vista 中的裝置角色](device-roles-in-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="3937a-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="3937a-108">DirectSound API 不提供應用程式選取使用者指派給特定[裝置角色](device-roles.md)之[音訊端點裝置](audio-endpoint-devices.md)的方法。</span><span class="sxs-lookup"><span data-stu-id="3937a-108">The DirectSound API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="3937a-109">不過，在 Windows Vista 中，核心音訊 Api 可以搭配 DirectSound 應用程式使用，以根據裝置角色啟用裝置選取。</span><span class="sxs-lookup"><span data-stu-id="3937a-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectSound application to enable device selection based on device role.</span></span> <span data-ttu-id="3937a-110">透過核心音訊 Api 的協助，應用程式可以識別指派給特定角色的音訊端點裝置、取得端點裝置的 DirectSound 裝置 GUID，以及呼叫 **DirectSoundCreate** 或 **DirectSoundCaptureCreate** 函式來建立封裝端點裝置的 **IDirectSound** 或 **IDirectSoundCapture** 介面實例。</span><span class="sxs-lookup"><span data-stu-id="3937a-110">With the help of the core audio APIs, the application can identify the audio endpoint device that is assigned to a particular role, get the DirectSound device GUID for the endpoint device, and call the **DirectSoundCreate** or **DirectSoundCaptureCreate** function to create an **IDirectSound** or **IDirectSoundCapture** interface instance that encapsulates the endpoint device.</span></span> <span data-ttu-id="3937a-111">如需 DirectSound 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="3937a-111">For more information about DirectSound, see the Windows SDK documentation.</span></span>

<span data-ttu-id="3937a-112">下列程式碼範例示範如何取得目前指派給特定裝置角色之轉譯或捕獲裝置的 DirectSound 裝置 GUID：</span><span class="sxs-lookup"><span data-stu-id="3937a-112">The following code example shows how to obtain the DirectSound device GUID for the rendering or capture device that is currently assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// Get the DirectSound or DirectSoundCapture device GUID for
// an audio endpoint device. If flow = eRender, the function
// gets the DirectSound device GUID for the rendering device
// with the specified device role. If flow = eCapture, the
// function gets the DirectSoundCapture device GUID for the
// capture device with the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetDirectSoundGuid(EDataFlow flow, ERole role, GUID* pDevGuid)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    if (pDevGuid == NULL)
    {
        return E_POINTER;
    }

    // Get a device enumerator for the audio endpoint
    // devices in the system.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the endpoint device with the specified dataflow
    // direction (eRender or eCapture) and device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    EXIT_ON_ERROR(hr)

    // Get the DirectSound or DirectSoundCapture device GUID
    // (in WCHAR string format) for the endpoint device.
    hr = pProps->GetValue(PKEY_AudioEndpoint_GUID, &var);
    EXIT_ON_ERROR(hr)

    // Convert the WCHAR string to a GUID structure.
    hr = CLSIDFromString(var.pwszVal, pDevGuid);
    EXIT_ON_ERROR(hr)

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    SAFE_RELEASE(pProps);
    return hr;
}
```



<span data-ttu-id="3937a-113">在上述的程式碼範例中，GetDirectSoundGuid 函式會接受 (eRender 或 eCapture) 的資料流程方向，以及 (eConsole、eMultimedia 或 eCommunications) 做為輸入參數的裝置角色。</span><span class="sxs-lookup"><span data-stu-id="3937a-113">In the preceding code example, the GetDirectSoundGuid function accepts a data-flow direction (eRender or eCapture) and a device role (eConsole, eMultimedia, or eCommunications) as input parameters.</span></span> <span data-ttu-id="3937a-114">第三個參數是函式所用的指標，函式會將應用程式可提供的裝置 GUID 做為 **DirectSoundCreate** 或 **DirectSoundCaptureCreate** 函數的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="3937a-114">The third parameter is a pointer through which the function writes a device GUID that the application can supply as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span>

<span data-ttu-id="3937a-115">上述程式碼範例會藉由下列方式取得 DirectSound 裝置 GUID：</span><span class="sxs-lookup"><span data-stu-id="3937a-115">The preceding code example obtains the DirectSound device GUID by:</span></span>

-   <span data-ttu-id="3937a-116">建立 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面實例，代表具有指定之資料流程程方向和裝置角色的音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="3937a-116">Creating an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface instance that represents the audio endpoint device that has the specified data-flow direction and device role.</span></span>
-   <span data-ttu-id="3937a-117">開啟音訊端點裝置的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="3937a-117">Opening the property store of the audio endpoint device.</span></span>
-   <span data-ttu-id="3937a-118">從屬性存放區取得 [**PKEY \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="3937a-118">Getting the [**PKEY\_AudioEndpoint\_GUID**](pkey-audioendpoint-guid.md) property from the property store.</span></span> <span data-ttu-id="3937a-119">屬性值是音訊端點裝置之 DirectSound 裝置 GUID 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="3937a-119">The property value is a string representation of the DirectSound device GUID for the audio endpoint device.</span></span>
-   <span data-ttu-id="3937a-120">呼叫 [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) 函式，將裝置 GUID 的字串表示轉換成 GUID 結構。</span><span class="sxs-lookup"><span data-stu-id="3937a-120">Calling the [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) function to convert the string representation of the device GUID to a GUID structure.</span></span> <span data-ttu-id="3937a-121">如需 **CLSIDFromString** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="3937a-121">For more information about **CLSIDFromString**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="3937a-122">從 GetDirectSoundGuid 函式取得裝置 GUID 之後，應用程式可以使用此 GUID 來呼叫 **DirectSoundCreate** 或 **DirectSoundCaptureCreate** ，以建立封裝音訊端點裝置的 DirectSound 轉譯或捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="3937a-122">After obtaining a device GUID from the GetDirectSoundGuid function, the application can call **DirectSoundCreate** or **DirectSoundCaptureCreate** with this GUID to create the DirectSound rendering or capture device that encapsulates the audio endpoint device.</span></span> <span data-ttu-id="3937a-123">當 DirectSound 以這種方式建立裝置時，它一律會將裝置的音訊串流指派給預設的會話，也就是由會話 GUID 值 GUID Null 所識別的進程特定音訊會話 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3937a-123">When DirectSound creates a device in this way, it always assigns the device's audio stream to the default session—the process-specific audio session that is identified by the session GUID value GUID\_NULL.</span></span>

<span data-ttu-id="3937a-124">如果應用程式需要 DirectSound 將串流指派給跨進程音訊會話，或指派給具有非 **Null** 會話 GUID 的會話，則應該呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法來建立 **IDirectSound** 或 **IDirectSoundCapture** 物件，而不是使用上述程式碼範例中所示的技巧。</span><span class="sxs-lookup"><span data-stu-id="3937a-124">If the application requires DirectSound to assign the stream to a cross-process audio session or to a session with a non-**NULL** session GUID, it should call the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to create an **IDirectSound** or **IDirectSoundCapture** object instead of using the technique shown in the preceding code example.</span></span> <span data-ttu-id="3937a-125">如需示範如何使用 **Activate** 方法來指定串流的跨進程音訊會話或非 **Null** 會話 GUID 的程式碼範例，請參閱 [DirectShow 應用程式的裝置角色](device-roles-for-directshow-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="3937a-125">For a code example that shows how to use the **Activate** method to specify a cross-process audio session or a non-**NULL** session GUID for a stream, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="3937a-126">該章節中的程式碼範例會示範如何建立 DirectShow 篩選器，但若要進行輕微修改，可以調整程式碼以建立 DirectSound 裝置。</span><span class="sxs-lookup"><span data-stu-id="3937a-126">The code example in that section shows how to create a DirectShow filter, but, with minor modifications, the code can be adapted to create a DirectSound device.</span></span>

<span data-ttu-id="3937a-127">上述程式碼範例中的 GetDirectSoundGuid 函式會呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數，以建立系統中音訊端點裝置的列舉值。</span><span class="sxs-lookup"><span data-stu-id="3937a-127">The GetDirectSoundGuid function in the preceding code example calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="3937a-128">除非呼叫程式之前呼叫 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 函式來初始化 COM 程式庫，否則 **CoCreateInstance** 呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="3937a-128">Unless the calling program previously called either the [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="3937a-129">如需有關 **CoCreateInstance**、 **CoInitialize** 和 **CoInitializeEx** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="3937a-129">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3937a-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="3937a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3937a-131">與舊版音訊 Api 的互通性</span><span class="sxs-lookup"><span data-stu-id="3937a-131">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
