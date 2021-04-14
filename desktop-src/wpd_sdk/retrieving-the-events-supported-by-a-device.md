---
description: 正在抓取裝置支援的事件
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: 正在抓取裝置支援的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514161"
---
# <a name="retrieving-the-events-supported-by-a-device"></a>正在抓取裝置支援的事件

某些 WPD 驅動程式支援事件通知。 這表示應用程式可以向驅動程式註冊，以在發生特定動作時接收通知。 例如，應用程式可以註冊，以在新增或移除物件時接收通知。

有10個預先定義的事件可讓應用程式進行監視。 如下表中所述。



| 事件                       | 描述                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| 裝置功能已更新 | 發生于裝置功能變更時。                                                                                      |
| 裝置已移除              | 裝置插上時發生。                                                                                                   |
| 裝置重設                | 當裝置已重設時發生。                                                                                                 |
| 加入的物件                | 發生于裝置上的新物件變成可用後。                                                                             |
| 物件已移除              | 發生于從裝置移除物件之後。                                                                               |
| 要求的物件傳輸   | 表示已提出要求以傳送物件。                                                                          |
| 物件已更新              | 在物件或其子系已更新後發生。 接著， (連線的用戶端應該更新其指定物件的視圖。 )  |
| 正在進行儲存格式  | 當裝置存放裝置格式化時發生。                                                                                     |



 

如需與這些事件相關聯的常數清單，請參閱「 [事件常數](event-constants.md) 」主題。

DeviceCapabilities .cpp 模組中的 ListSupportedEvents 函式會示範如何抓取指定裝置所支援的事件。

您的應用程式可以使用下表所述的介面，來取得裝置所支援之事件的識別碼。



| 介面                                                                                      | 描述                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [**IPortableDeviceCapabilities 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | 提供支援事件抓取方法的存取權。 |
| [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) | 用來列舉和儲存功能分類資料。     |



 

範例應用程式所完成的第一項工作是抓取 [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) 物件，此物件是用來取得指定裝置所支援的事件。


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



藉由呼叫 [**IPortableDeviceCapabilities：： GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) 方法，即可取出支援的事件。 這個方法會抓取指定裝置的事件識別碼集合，並將它們儲存在 pEvents 引數所指向的 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件中。


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



下一步是取得支援事件的計數，讓應用程式可以逐一查看 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件，並取得每個的識別碼。


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pEvents->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have an event.  It is assumed that
            // events are returned as VT_CLSID VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**事件常數**](event-constants.md)
</dt> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



