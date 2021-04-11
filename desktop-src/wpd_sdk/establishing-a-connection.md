---
description: 建立連線
ms.assetid: 16286da5-5979-413b-a4db-ca157b10a571
title: 建立連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ea922b3cd44430dc7c213a513c44fa8ef2ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027546"
---
# <a name="establishing-a-connection"></a>建立連線

一旦使用者選取裝置之後，ChooseDevice 函式就會呼叫 [**IPortableDevice：： Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) 方法，以建立應用程式與裝置之間的連接。 IPortableDevice：： Open 方法採用兩個引數：

-   以 null 結束的字串指標，指定裝置的隨插即用名稱。  (藉由呼叫 [**IPortableDeviceManager：： GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) 方法來抓取此字串。 ) 
-   [**IPortableDeviceValues 介面**](iportabledevicevalues.md)的指標，可指定應用程式的用戶端資訊。


```C++
// CoCreate the IPortableDevice interface and call Open() with
// the chosen PnPDeviceID string.
hr = CoCreateInstance(CLSID_PortableDeviceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(ppDevice));
if (SUCCEEDED(hr))
{
    hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the device for Read Write access, will open it for Read-only access instead\n");
            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);
            hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
            if (FAILED(hr))
            {
                printf("! Failed to Open the device, hr = 0x%lx\n",hr);
                // Release the IPortableDevice interface, because we cannot proceed
                // with an unopen device.
                (*ppDevice)->Release();
                *ppDevice = NULL;
            }
        }
        else
        {
            printf("! Failed to Open the device, hr = 0x%lx\n",hr);
            // Release the IPortableDevice interface, because we cannot proceed
            // with an unopen device.
            (*ppDevice)->Release();
            *ppDevice = NULL;
        }
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceFTM, hr = 0x%lx\n",hr);
}
```



針對 Windows 7， [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) 支援兩個適用于 **CoCreateInstance** 的 clsid。 **CLSID \_PortableDevice** 會傳回未匯總無限制執行緒封送處理器的 **IPortableDevice** 指標; **CLSID \_PortableDeviceFTM** 是新的 CLSID，會傳回匯總無限制執行緒封送處理器的 **IPortableDevice** 指標。 這兩個指標都支援相同的功能，否則為。

存留于單一執行緒單元中的應用程式應該使用 **CLSID \_ PortableDeviceFTM** ，因為這樣可避免介面指標封送處理的額外負荷。 **CLSID \_** 繼承應用程式仍支援 PortableDevice。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**選取裝置**](selecting-a-device.md)
</dt> </dl>

 

 



