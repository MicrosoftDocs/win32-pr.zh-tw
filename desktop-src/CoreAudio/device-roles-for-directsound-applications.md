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
# <a name="device-roles-for-directsound-applications"></a>DirectSound 應用程式的裝置角色

> [!Note]  
> [MMDEVICE API](mmdevice-api.md)支援裝置角色。 不過，Windows Vista 中的使用者介面並不支援這項功能。 裝置角色的使用者介面支援可能會在未來的 Windows 版本中執行。 如需詳細資訊，請參閱 [Windows Vista 中的裝置角色](device-roles-in-windows-vista.md)。

 

DirectSound API 不提供應用程式選取使用者指派給特定[裝置角色](device-roles.md)之[音訊端點裝置](audio-endpoint-devices.md)的方法。 不過，在 Windows Vista 中，核心音訊 Api 可以搭配 DirectSound 應用程式使用，以根據裝置角色啟用裝置選取。 透過核心音訊 Api 的協助，應用程式可以識別指派給特定角色的音訊端點裝置、取得端點裝置的 DirectSound 裝置 GUID，以及呼叫 **DirectSoundCreate** 或 **DirectSoundCaptureCreate** 函式來建立封裝端點裝置的 **IDirectSound** 或 **IDirectSoundCapture** 介面實例。 如需 DirectSound 的詳細資訊，請參閱 Windows SDK 檔。

下列程式碼範例示範如何取得目前指派給特定裝置角色之轉譯或捕獲裝置的 DirectSound 裝置 GUID：


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



在上述的程式碼範例中，GetDirectSoundGuid 函式會接受 (eRender 或 eCapture) 的資料流程方向，以及 (eConsole、eMultimedia 或 eCommunications) 做為輸入參數的裝置角色。 第三個參數是函式所用的指標，函式會將應用程式可提供的裝置 GUID 做為 **DirectSoundCreate** 或 **DirectSoundCaptureCreate** 函數的輸入參數。

上述程式碼範例會藉由下列方式取得 DirectSound 裝置 GUID：

-   建立 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面實例，代表具有指定之資料流程程方向和裝置角色的音訊端點裝置。
-   開啟音訊端點裝置的屬性存放區。
-   從屬性存放區取得 [**PKEY \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md) 屬性。 屬性值是音訊端點裝置之 DirectSound 裝置 GUID 的字串表示。
-   呼叫 [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) 函式，將裝置 GUID 的字串表示轉換成 GUID 結構。 如需 **CLSIDFromString** 的詳細資訊，請參閱 Windows SDK 檔。

從 GetDirectSoundGuid 函式取得裝置 GUID 之後，應用程式可以使用此 GUID 來呼叫 **DirectSoundCreate** 或 **DirectSoundCaptureCreate** ，以建立封裝音訊端點裝置的 DirectSound 轉譯或捕獲裝置。 當 DirectSound 以這種方式建立裝置時，它一律會將裝置的音訊串流指派給預設的會話，也就是由會話 GUID 值 GUID Null 所識別的進程特定音訊會話 \_ 。

如果應用程式需要 DirectSound 將串流指派給跨進程音訊會話，或指派給具有非 **Null** 會話 GUID 的會話，則應該呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法來建立 **IDirectSound** 或 **IDirectSoundCapture** 物件，而不是使用上述程式碼範例中所示的技巧。 如需示範如何使用 **Activate** 方法來指定串流的跨進程音訊會話或非 **Null** 會話 GUID 的程式碼範例，請參閱 [DirectShow 應用程式的裝置角色](device-roles-for-directshow-applications.md)。 該章節中的程式碼範例會示範如何建立 DirectShow 篩選器，但若要進行輕微修改，可以調整程式碼以建立 DirectSound 裝置。

上述程式碼範例中的 GetDirectSoundGuid 函式會呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數，以建立系統中音訊端點裝置的列舉值。 除非呼叫程式之前呼叫 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 函式來初始化 COM 程式庫，否則 **CoCreateInstance** 呼叫會失敗。 如需有關 **CoCreateInstance**、 **CoInitialize** 和 **CoInitializeEx** 的詳細資訊，請參閱 Windows SDK 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[與舊版音訊 Api 的互通性](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
