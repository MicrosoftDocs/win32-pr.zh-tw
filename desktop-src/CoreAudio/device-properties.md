---
description: 裝置內容
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: '裝置屬性 (核心音訊 Api) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970306"
---
# <a name="device-properties-core-audio-apis"></a>裝置屬性 (核心音訊 Api) 

在列舉 [音訊端點裝置](audio-endpoint-devices.md)的過程中，用戶端應用程式可以詢問端點物件的裝置屬性。 裝置屬性會在 MMDevice API 的 **IPropertyStore** 介面執行中公開。 針對端點物件的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面參考，用戶端可以藉由呼叫 [**IMMDevice：： OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) 方法，取得端點物件的屬性存放區的參考。

屬性存放區物件會公開 **IPropertyStore** 介面。 這個介面中的兩個主要方法是 **IPropertyStore：： GetValue**（可取得裝置屬性值）和 **IPropertyStore：： SetValue**（可設定裝置屬性值）。 如需 **IPropertyStore** 的詳細資訊，請參閱 Windows SDK 檔。

MMDevice API 的屬性存放區實作為不同于標準 shell 屬性存放區物件。 若要變更屬性值，用戶端應用程式必須呼叫 **IPropertyStore：： SetValue** 方法。 在此呼叫過程中，新的值會設定並寫入登錄中。 因此，應用程式不需要在 **SetValue** 呼叫之後呼叫 **IPropertyStore：： Commit** 方法。 只有當用戶端釋放介面指標時，才會關閉登錄的控制碼。

一般來說，協力廠商用戶端應用程式會呼叫 **GetValue** 方法，但不會呼叫 **SetValue** 方法。 端點管理員會設定端點的基本裝置屬性。 端點管理員是 Windows Vista 元件，負責偵測音訊端點裝置是否存在。

下列清單中的每個 PKEY \_ Xxx 屬性識別碼都是 **PROPERTYKEY** 的常數，定義于標頭檔 Functiondiscoverykeys \_ devpkey 中。 所有音訊端點裝置都有這三個裝置屬性。



| 屬性                                                                         | 描述                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | 端點裝置所連接之音訊介面卡的易記名稱 (例如「XYZ 音訊介面卡」 ) 。 **PROPVARIANT** 成員 **VT** 設定為 vt \_ LPWSTR，而成員 **pwszVal** 指向以 null 結尾的寬字元字串，其中包含易記名稱。 |
| [**PKEY \_ 裝置 \_ DeviceDesc**](pkey-device-devicedesc.md)                       | 端點裝置的裝置描述 (例如「喇叭」 ) 。 **PROPVARIANT** 成員 **VT** 設定為 vt \_ LPWSTR，而成員 **pwszVal** 指向以 null 終止的寬字元字串，其中包含裝置描述。                                       |
| [**PKEY \_ 裝置 \_ FriendlyName**](pkey-device-friendlyname.md)                   | 端點裝置的易記名稱 (例如「喇叭 (XYZ 音訊介面卡) 」 ) 。 **PROPVARIANT** 成員 **VT** 設定為 vt \_ LPWSTR，而成員 **pwszVal** 指向以 null 結尾的寬字元字串，其中包含易記名稱。                             |



 

某些音訊端點裝置可能會有未出現在上述清單中的其他屬性。 如需其他屬性的詳細資訊，請參閱 [音訊端點屬性](audio-endpoint-properties.md)。 如需 **PROPERTYKEY** 的詳細資訊，請參閱 Windows SDK 檔。

下列程式碼範例會列印系統中所有音訊呈現端點裝置的顯示名稱：


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



上述程式碼範例中的 FAILED 巨集定義在標頭檔 Winerror.h 中。

在上述程式碼範例中，PrintEndpointNames 函數中的 **for** 迴圈主體會呼叫 [**IMMDevice：： GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid)方法，以取得 **IMMDevice** 介面實例所代表之音訊端點裝置的 [端點識別碼字串](endpoint-id-strings.md)。 此字串可唯一識別與系統中所有其他音訊端點裝置相關的裝置。 用戶端可以藉由呼叫 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) 方法，使用端點識別碼字串來建立音訊端點裝置的實例，或在不同的進程中建立實例。 用戶端應將端點識別碼字串的內容視為不透明。 也就是說，用戶端不應該嘗試剖析字串的內容，以取得裝置的相關資訊。 原因是字串格式未定義，而且可能會從一個 MMDevice API 的執行變更為下一個。

上述程式碼範例中 PrintEndpointNames 函式所取得的易記裝置名稱和端點識別碼字串，與 DirectSound 在裝置列舉期間提供的易記裝置名稱和端點識別碼字串相同。 如需詳細資訊，請參閱 [舊版音訊應用程式的音訊事件](audio-events-for-legacy-audio-applications.md)。

在上述程式碼範例中，PrintEndpointNames 函式會呼叫 **CoCreateInstance** 函數，以建立系統中音訊端點裝置的列舉值。 除非呼叫程式之前呼叫 **CoInitialize** 或 **CoInitializeEx** 函式來初始化 COM 程式庫，否則 **CoCreateInstance** 呼叫會失敗。 如需有關 **CoCreateInstance**、 **CoInitialize** 和 **CoInitializeEx** 的詳細資訊，請參閱 Windows SDK 檔。

如需 **IMMDeviceEnumerator**、 **IMMDeviceCollection** 和 **IMMDevice** 介面的詳細資訊，請參閱 [MMDevice API](mmdevice-api.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊端點裝置](audio-endpoint-devices.md)
</dt> </dl>

 

 



