---
description: 正在抓取支援的服務事件
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: 正在抓取支援的服務事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc1df4c8255a4dc2a1297ae99216437ac3b4c9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423468"
---
# <a name="retrieving-supported-service-events"></a>正在抓取支援的服務事件

WpdServicesApiSample 應用程式包含的程式碼會示範應用程式如何藉由呼叫下列介面上的方法，來取得指定連絡人服務所支援的事件。



| 介面                | 描述    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | 用來取出 **IPortableDeviceServiceCapabilities** 介面，以存取支援的事件。 |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | 提供支援的事件和事件屬性的存取權。                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | 包含支援的事件清單。                                                                |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | 包含指定事件的屬性。                                                            |



 

當使用者在命令列選擇選項 "4" 時，應用程式會叫用在 ServiceCapabilities .cpp 模組中找到的 **ListSupportedEvents** 方法。

請注意，在抓取事件清單之前，範例應用程式會在連線的裝置上開啟連絡人服務。

在 WPD 中，事件的名稱、選項和參數會加以描述。 事件名稱是容易編寫腳本的字串，例如 "MyCustomEvent"。 事件選項會指出指定的事件是否會廣播給所有用戶端，以及該事件是否支援自動播放。 事件參數屬性包括指定參數的 PROPERTYKEY 和 VARTYPE。

ServiceCapabilities .cpp 模組中的四個方法支援抓取指定連絡人服務的支援事件： **ListSupportedEvents**、 **DisplayEvent**、 **DisplayEventOptions** 和 **DisplayEventParameters**。 **ListSupportedEvents** 方法會抓取支援的事件計數和每個事件的 GUID 識別碼。 **DisplayEvent** 方法會顯示事件名稱或 GUID，然後呼叫 **DisplayEventOptions** 和 **DisplayEventParameters** 來顯示事件相關資料。

**ListSupportedEvents** 方法會叫用 [**IPortableDeviceService：：功能**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities)方法來取出 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)介面。 使用這個介面，它會藉由呼叫 [**IPortableDeviceServiceCapabilities：： GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) 方法來抓取支援的事件。 **GetSupportedEvents** 方法會抓取服務所支援之每個事件的 guid，並將這些 guid 複製到 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)物件中。

下列程式碼說明如何取出支援的服務事件。


```C++
// List all supported events on the service
void ListSupportedEvents(
    IPortableDeviceService* pService)
{
    HRESULT hr          = S_OK;
    DWORD   dwNumEvents = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pEvents;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all events supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedEvents(&pEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get supported events from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported events found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pEvents->GetCount(&dwNumEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Events Found on the service\n\n", dwNumEvents);

    // Loop through each event and display it
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
                    DisplayEvent(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



在 **ListSupportedEvents** 方法取得代表指定服務所支援之每個事件的 guid 之後，它會叫用 **DisplayEvent** 方法以抓取事件特定資料。 這類資料包括事件名稱、其選項 (廣播或自動播放) 、參數 Guid、參數類型等等。

**DisplayEvent** 方法會叫用 [**IPortableDeviceServiceCapabilities：： GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes)方法，以取得指定事件的屬性集合。 然後，它會呼叫 [**IPortableDeviceValues：： GetStringValue**](iportabledevicevalues-getstringvalue.md) 方法，並要求驅動程式傳回指定事件的使用者易記名稱。 接下來， **DisplayEvent** 會呼叫 [**IPortableDeviceValues：： GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) 以取得事件選項。 最後，DisplayEvent 會呼叫 [**IPortableDeviceValues：： GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) 以取得事件參數的清單。 它會將這些方法所傳回的資料傳遞給 **DisplayEventOptions** 和 **DisplayEventParameters** helper 函式，以轉譯指定事件的選項和參數資訊。

下列程式碼會使用 **DisplayEvent** 方法。


```C++
// Display basic information about an event
void DisplayEvent(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Event)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the event attributes which describe the event
    HRESULT hr = pCapabilities->GetEventAttributes(Event, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the event attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the event if it is available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_EVENT_ATTRIBUTE_NAME, &pszFormatName);
        if (SUCCEEDED(hr))
        {
            printf("%ws\n", pszFormatName);
        }
        else
        {
            printf("%ws\n", (PWSTR)CGuidToString(Event));
        }       

        // Display the event options
        hr = pAttributes->GetIPortableDeviceValuesValue(WPD_EVENT_ATTRIBUTE_OPTIONS, &pOptions);
        if (SUCCEEDED(hr))
        {
            DisplayEventOptions(pOptions);
        }
        else
        {
            printf("! Failed to get the event options, hr = 0x%lx\n", hr);
        }       

        // Display the event parameters
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_EVENT_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayEventParameters(pCapabilities, Event, pParameters);
        }
        else
        {
            printf("! Failed to get the event parameters, hr = 0x%lx\n", hr);
        }       
        
        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



**DisplayEventOptions** helper 函式會接收 [**IPortableDeviceValues**](iportabledevicevalues.md)物件，其中包含事件的選項資料。 然後，它會呼叫 [**IPortableDeviceValues：： GetBoolValue**](iportabledevicevalues-getboolvalue.md) 方法來取出選項資料。 它會使用此資料轉譯字串，指出是否支援廣播和自動播放選項。


```C++
// Display the basic event options.
void DisplayEventOptions(
    IPortableDeviceValues* pOptions)
{
    printf("\tEvent Options:\n");
    // Read the WPD_EVENT_OPTION_IS_BROADCAST_EVENT value to see if the event is
    // a broadcast event. If the read fails, assume FALSE
    BOOL  bIsBroadcastEvent = FALSE;
    pOptions->GetBoolValue(WPD_EVENT_OPTION_IS_BROADCAST_EVENT, &bIsBroadcastEvent);
    printf("\tWPD_EVENT_OPTION_IS_BROADCAST_EVENT = %ws\n",bIsBroadcastEvent ? L"TRUE" : L"FALSE");
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



