---
title: 列舉 Windows 媒體裝置管理員裝置
description: 瞭解如何使用列舉介面 Windows 媒體裝置管理員來列舉偵測到的裝置。
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Windows媒體裝置管理員，列舉裝置
- 裝置管理員，列舉裝置
- 程式設計指南，列舉裝置
- 桌面應用程式，列舉裝置
- 建立 Windows 媒體裝置管理員應用程式，列舉裝置
- 列舉裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0009e2206bf7c97839d890d00c08a8e1806196efee9af95db72336b95d8b2cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584656"
---
# <a name="enumerating-windows-media-device-manager-devices"></a>列舉 Windows 媒體裝置管理員裝置

驗證應用程式之後，您可以開始列舉 Windows 媒體裝置管理員偵測到的裝置。 列舉是藉由使用 [**IWMDeviceManager2：： EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2)或 [**IWMDeviceManager：： EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices)所取得的列舉介面 [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)來完成。 如果支援，則使用 **EnumDevices2** 方法，因為較早的版本只會傳回裝置上的舊版介面，而新的版本則會傳回舊版和新的介面。

取得列舉值之前，您應該決定要使用的列舉視圖。 有些裝置會將每個存放裝置公開為不同的裝置。 例如，裝置上的兩個快閃記憶卡會列舉為不同的裝置。 您可以指定將裝置上的所有存放裝置都列舉成單一裝置。 您只能在應用程式中設定此喜好設定一次。如果您想要變更它，則必須關閉並重新啟動應用程式。 不過，請注意，舊版裝置有時候會忽略將個別裝置存放裝置列舉為單一裝置的要求，並繼續個別列舉它們。

下列步驟顯示如何列舉連線的裝置：

1.  使用 [**IWMDeviceManager3：： SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference)設定裝置列舉喜好設定。 如果未呼叫這個方法，則預設方法會將儲存體顯示為個別的裝置。 若要判斷個別的「裝置」是否實際上是在相同的裝置上進行存放裝置，請呼叫 [**IWMDMDevice2：： GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname);來自相同裝置的儲存體將會傳回相同的值，但最後一個 "$" 符號之後的最後一個數位除外。
2.  查詢 [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) 或 [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)，然後呼叫 [**IWMDeviceManager2：： EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) 來取得裝置列舉值介面 [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)。  (如果支援的話，請使用 **EnumDevices2**，這樣會更有效率，因為較舊的版本可能不會傳回 MTP 裝置) 。
3.  呼叫 [**IWMDMEnumDevices：： Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) 方法，一次取出一或多個裝置。 繼續呼叫這個方法，直到該方法傳回 \_ FALSE 或錯誤訊息為止。 如果一次只抓取一個裝置，您不需要配置陣列來保存裝置。

由於使用者可以在您的應用程式執行時，從電腦附加或移除裝置，因此最好是執行裝置連線或移除的通知。 這是藉由執行 [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) 介面並註冊它來完成。 如需有關這個的詳細資訊，請參閱 [啟用通知](enabling-notifications.md)。

下列 c + + 程式碼會列舉裝置，並要求每個裝置的相關資訊。


```C++
HRESULT CWMDMController::EnumDevices()
{
    HRESULT hr = S_OK;

    // Change behavior to show devices as one object, not each storage as a device.
    // This can be called only once for each instance of this application.
    CComQIPtr<IWMDeviceManager3>pDevMgr3(m_IWMDMDeviceMgr);
    hr = pDevMgr3->SetDeviceEnumPreference(DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES);
    
    // Get number of attached devices.
    DWORD iDevices = 0;
    hr = m_IWMDMDeviceMgr->GetDeviceCount(&iDevices);
    if (hr == S_OK)
    {
        // TODO: Display count of devices.
    }

    //
    // Get a device enumerator to enumerate devices.
    //
    CComPtr<IWMDeviceManager2> pDevMgr2;
    hr = m_IWMDMDeviceMgr->QueryInterface (__uuidof(IWMDeviceManager2), (void**) &pDevMgr2);
    if (hr == S_OK)
    {
        // TODO: Display message indicating that application obtained IWMDeviceManager2.
    }
    else
    {
        // TODO: Display message indicating that we couldn't 
        // get IWMDeviceManager2 in EnumDevices.
        return hr;
    }
   CComPtr<IWMDMEnumDevice> pEnumDevice;
   hr = pDevMgr2->EnumDevices2(&pEnumDevice);
    if (hr != S_OK)
    {
        // TODO: Display messaging indicating that an error occurred 
        // in calling EnumDevices2.
        return hr;
    }

    // Length of all the strings we'll send in. 
    const UINT MAX_CHARS = 100;

    // Iterate through devices.
    while(TRUE)
    {
        // Get a device handle.
        IWMDMDevice *pIWMDMDevice;
        ULONG ulFetched = 0;
        hr = pEnumDevice->Next(1, &pIWMDMDevice, &ulFetched);
        if ((hr != S_OK) || (ulFetched != 1))
        {
            break;
        }
        
        // Get a display icon for the device.
        ULONG deviceIcon = 0;
        hr = pIWMDMDevice->GetDeviceIcon(&deviceIcon);

        // Print the device manufacturer.
        WCHAR manufacturer[MAX_CHARS];
        hr = pIWMDMDevice->GetManufacturer((LPWSTR)&manufacturer, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display manufacturer name.
        }

        // Get the device name.
        WCHAR name[MAX_CHARS];
        hr = pIWMDMDevice->GetName((LPWSTR)&name, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display name.
        }

        // TODO: Get other device information if wanted.

        // Obtain an IWMDMDevice2 interface and call some methods.
        CComQIPtr<IWMDMDevice2> pIWMDMDevice2(pIWMDMDevice);
        if (pIWMDMDevice2 != NULL)
        {
            // Get the canonical name.
            WCHAR canonicalName[MAX_CHARS];
            hr = pIWMDMDevice2->GetCanonicalName(canonicalName, MAX_CHARS);
            if (hr == S_OK)
            {
                // TODO: Display canonical name.
            }
        }

        // Obtain an IWMDMDevice3 interface and call some methods.
        CComQIPtr<IWMDMDevice3>pIWMDMDevice3(pIWMDMDevice);
        if (pIWMDMDevice3 != NULL)
        {
            // Find out what protocol is being used.
            PROPVARIANT val;
            PropVariantInit(&val);
            hr = pIWMDMDevice3->GetProperty(g_wszWMDMDeviceProtocol, &val);

            if (hr == S_OK)
            {
                if (*val.puuid == WMDM_DEVICE_PROTOCOL_RAPI)
                {
                    // TODO: Display message indicating device is a RAPI device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MTP)
                {
                    / /TODO: Display message indicating device is an MTP device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MSC)
                {
                    // TODO: Display message indicating device is an MSC device.
                }
                else
                {
                    // TODO: Display message indicating that the 
                    // application encountered an unknown protocol.
                }
                PropVariantClear(&val);
            }
        }

        // Examine the device capabilities. You could use some of these
        // to enable or disable the application's UI elements.
        CComQIPtr<IWMDMDeviceControl> pDeviceControl(pIWMDMDevice);
        if (pDeviceControl != NULL)
        {
            DWORD caps = 0;
            hr = pDeviceControl->GetCapabilities(&caps);
            if (caps & WMDM_DEVICECAP_CANPLAY)
            {
                // TODO: Display message indicating that the media 
                // device can play MP3 audio.
            }
            // TODO: Test for other capabilities here.
        }
    } // Get the next device.
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows 媒體裝置管理員應用程式**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




