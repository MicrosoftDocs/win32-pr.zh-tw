---
description: 裝置事件
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: '裝置事件 (核心音訊 Api) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0513fc49ee5f3cb2bfe95ca2330cb79b74720923
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977002"
---
# <a name="device-events-core-audio-apis"></a>裝置事件 (核心音訊 Api) 

裝置事件會通知用戶端系統中 [音訊端點裝置](audio-endpoint-devices.md) 的狀態變更。 以下是裝置事件的範例：

-   使用者可以從裝置管理員或從 Windows 多媒體控制台 Mmsys.cpl，啟用或停用音訊端點裝置。
-   使用者將音訊介面卡新增至系統，或從系統移除音訊介面卡。
-   使用者將音訊端點裝置插入具有插座狀態偵測的音訊插孔，或從這類插孔移除音訊端點裝置。
-   使用者變更指派給裝置的 [裝置角色](device-roles.md) 。
-   [裝置的屬性](device-properties.md)值會變更。

新增或移除音訊介面卡會為所有連接至介面卡的音訊端點裝置產生裝置事件。 上述清單中的前四個專案是裝置狀態變更的範例。 如需有關音訊端點裝置之裝置狀態的詳細資訊，請參閱 [裝置 \_ 狀態 \_ XXX 常數](device-state-xxx-constants.md)。 如需有關插座是否存在偵測的詳細資訊，請參閱 [音訊端點裝置](audio-endpoint-devices.md)。

用戶端可以註冊，以在裝置事件發生時收到通知。 為了回應這些通知，用戶端可以動態地變更其使用特定裝置的方式，或選取不同的裝置以用於特定用途。

例如，如果應用程式是透過一組 USB 喇叭來播放音訊播放軌，而使用者與 USB 連接器中斷喇叭的連線，應用程式就會收到裝置事件通知。 回應事件時，如果應用程式偵測到一組桌上型喇叭已連線到系統主機板上的整合式音訊介面卡，應用程式可以繼續透過桌面喇叭播放音訊播放軌。 在此範例中，會自動從 USB 喇叭轉換至桌上型喇叭，而不需要使用者透過明確地重新導向應用程式介入。

若要註冊以接收裝置通知，用戶端會呼叫 [**IMMDeviceEnumerator：： RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) 方法。 當用戶端不再需要通知時，它會藉由呼叫 [**IMMDeviceEnumerator：： UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) 方法將其取消。 這兩種方法都採用名為 *pNotify* 的輸入參數，也就是 [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) 介面實例的指標。

**IMMNotificationClient** 介面是由用戶端所執行。 介面包含數個方法，每個方法都可做為特定類型裝置事件的回呼常式。 當音訊端點裝置中發生裝置事件時，MMDevice 模組會在每個用戶端的 **IMMNotificationClient** 介面中呼叫適當的方法，而該用戶端目前已註冊要接收裝置事件通知。 這些呼叫會將事件的描述傳遞給用戶端。 如需詳細資訊，請參閱 [**IMMNotificationClient 介面**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)。

註冊接收裝置事件通知的用戶端將會收到系統中所有音訊端點裝置所發生之所有類型裝置事件的通知。 如果用戶端只對特定事件種類或某些裝置感興趣，則其 **IMMNotificationClient** 執行中的方法應該會適當地篩選事件。

Windows SDK 提供的範例包含數個 [**IMMNotificationClient 介面**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)的實作為。 如需詳細資訊，請參閱 [使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)。

下列程式碼範例顯示 **IMMNotificationClient** 介面的可能實作為：


```C++
//-----------------------------------------------------------
// Example implementation of IMMNotificationClient interface.
// When the status of audio endpoint devices change, the
// MMDevice module calls these methods to notify the client.
//-----------------------------------------------------------

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class CMMNotificationClient : public IMMNotificationClient
{
    LONG _cRef;
    IMMDeviceEnumerator *_pEnumerator;

    // Private function to print device-friendly name
    HRESULT _PrintDeviceName(LPCWSTR  pwstrId);

public:
    CMMNotificationClient() :
        _cRef(1),
        _pEnumerator(NULL)
    {
    }

    ~CMMNotificationClient()
    {
        SAFE_RELEASE(_pEnumerator)
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IMMNotificationClient) == riid)
        {
            AddRef();
            *ppvInterface = (IMMNotificationClient*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback methods for device-event notifications.

    HRESULT STDMETHODCALLTYPE OnDefaultDeviceChanged(
                                EDataFlow flow, ERole role,
                                LPCWSTR pwstrDeviceId)
    {
        char  *pszFlow = "?????";
        char  *pszRole = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (flow)
        {
        case eRender:
            pszFlow = "eRender";
            break;
        case eCapture:
            pszFlow = "eCapture";
            break;
        }

        switch (role)
        {
        case eConsole:
            pszRole = "eConsole";
            break;
        case eMultimedia:
            pszRole = "eMultimedia";
            break;
        case eCommunications:
            pszRole = "eCommunications";
            break;
        }

        printf("  -->New default device: flow = %s, role = %s\n",
               pszFlow, pszRole);
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceAdded(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Added device\n");
        return S_OK;
    };

    HRESULT STDMETHODCALLTYPE OnDeviceRemoved(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Removed device\n");
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceStateChanged(
                                LPCWSTR pwstrDeviceId,
                                DWORD dwNewState)
    {
        char  *pszState = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (dwNewState)
        {
        case DEVICE_STATE_ACTIVE:
            pszState = "ACTIVE";
            break;
        case DEVICE_STATE_DISABLED:
            pszState = "DISABLED";
            break;
        case DEVICE_STATE_NOTPRESENT:
            pszState = "NOTPRESENT";
            break;
        case DEVICE_STATE_UNPLUGGED:
            pszState = "UNPLUGGED";
            break;
        }

        printf("  -->New device state is DEVICE_STATE_%s (0x%8.8x)\n",
               pszState, dwNewState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnPropertyValueChanged(
                                LPCWSTR pwstrDeviceId,
                                const PROPERTYKEY key)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Changed device property "
               "{%8.8x-%4.4x-%4.4x-%2.2x%2.2x-%2.2x%2.2x%2.2x%2.2x%2.2x%2.2x}#%d\n",
               key.fmtid.Data1, key.fmtid.Data2, key.fmtid.Data3,
               key.fmtid.Data4[0], key.fmtid.Data4[1],
               key.fmtid.Data4[2], key.fmtid.Data4[3],
               key.fmtid.Data4[4], key.fmtid.Data4[5],
               key.fmtid.Data4[6], key.fmtid.Data4[7],
               key.pid);
        return S_OK;
    }
};

// Given an endpoint ID string, print the friendly device name.
HRESULT CMMNotificationClient::_PrintDeviceName(LPCWSTR pwstrId)
{
    HRESULT hr = S_OK;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;
    PROPVARIANT varString;

    CoInitialize(NULL);
    PropVariantInit(&varString);

    if (_pEnumerator == NULL)
    {
        // Get enumerator for audio endpoint devices.
        hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                              NULL, CLSCTX_INPROC_SERVER,
                              __uuidof(IMMDeviceEnumerator),
                              (void**)&_pEnumerator);
    }
    if (hr == S_OK)
    {
        hr = _pEnumerator->GetDevice(pwstrId, &pDevice);
    }
    if (hr == S_OK)
    {
        hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    }
    if (hr == S_OK)
    {
        // Get the endpoint device's friendly-name property.
        hr = pProps->GetValue(PKEY_Device_FriendlyName, &varString);
    }
    printf("----------------------\nDevice name: \"%S\"\n"
           "  Endpoint ID string: \"%S\"\n",
           (hr == S_OK) ? varString.pwszVal : L"null device",
           (pwstrId != NULL) ? pwstrId : L"null ID");

    PropVariantClear(&varString);

    SAFE_RELEASE(pProps)
    SAFE_RELEASE(pDevice)
    CoUninitialize();
    return hr;
}
```



上述程式碼範例中的 CMMNotificationClient 類別是 **IMMNotificationClient** 介面的實作為。 由於 **IMMNotificationClient** 繼承自 **iunknown**，因此類別定義包含 **iunknown** 方法 **AddRef**、 **Release** 和 **QueryInterface** 的實作為。 類別定義中其餘的公用方法是 **IMMNotificationClient** 介面專用的。 方法如下：

-   **OnDefaultDeviceChanged**，當使用者變更音訊端點裝置的裝置角色時呼叫。
-   **OnDeviceAdded**，當使用者將音訊端點裝置新增至系統時呼叫。
-   **OnDeviceRemoved**，當使用者從系統移除音訊端點裝置時呼叫。
-   **OnDeviceStateChanged**，當音訊端點裝置的裝置狀態變更時呼叫。  (如需裝置狀態的詳細資訊，請參閱 [裝置 \_ 狀態 \_ XXX 常數](device-state-xxx-constants.md)。 ) 
-   **OnPropertyValueChanged**，當音訊端點裝置的屬性值變更時，就會呼叫它。

這些方法的每一個都採用輸入參數 *pwstrDeviceId*，也就是端點識別碼字串的指標。 字串可識別裝置事件發生所在的音訊端點裝置。

在上述程式碼範例中， \_ PrintDeviceName 是 CMMNotificationClient 類別中的私用方法，可列印裝置的易記名稱。 \_PrintDeviceName 會採用端點識別碼字串做為輸入參數。 它會將字串傳遞給 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) 方法。 **GetDevice** 會建立端點裝置物件來代表裝置，並提供 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面給該物件。 接下來， \_ PrintDeviceName 會呼叫 [**IMMDevice：： OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) 方法，以將 **IPropertyStore** 介面取出至裝置的屬性存放區。 最後， \_ PrintDeviceName 會呼叫 **IPropertyStore：： GetItem** 方法，以取得裝置的易記名稱屬性。 如需 **IPropertyStore** 的詳細資訊，請參閱 Windows SDK 檔。

除了裝置事件之外，用戶端可以註冊以接收音訊會話事件和端點磁片區事件的通知。 如需詳細資訊，請參閱 [**IAudioSessionEvents 介面**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 和 [**IAudioEndpointVolumeCallback 介面**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊端點裝置](audio-endpoint-devices.md)
</dt> </dl>

 

 



