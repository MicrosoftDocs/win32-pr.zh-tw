---
description: 正在抓取支援的服務事件
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: 正在抓取支援的服務事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f515b65b8ed062c346777224a64539f5229a704a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997919"
---
# <a name="retrieving-supported-service-events"></a><span data-ttu-id="410a6-103">正在抓取支援的服務事件</span><span class="sxs-lookup"><span data-stu-id="410a6-103">Retrieving Supported Service Events</span></span>

<span data-ttu-id="410a6-104">WpdServicesApiSample 應用程式包含的程式碼會示範應用程式如何藉由呼叫下列介面上的方法，來取得指定連絡人服務所支援的事件。</span><span class="sxs-lookup"><span data-stu-id="410a6-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the events supported by a given Contacts service by calling methods on the following interfaces.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="410a6-105">介面</span><span class="sxs-lookup"><span data-stu-id="410a6-105">Interface</span></span>                                                                            | <span data-ttu-id="410a6-106">描述</span><span class="sxs-lookup"><span data-stu-id="410a6-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="410a6-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="410a6-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="410a6-108">用來取出 **IPortableDeviceServiceCapabilities** 介面，以存取支援的事件。</span><span class="sxs-lookup"><span data-stu-id="410a6-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="410a6-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="410a6-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="410a6-110">提供支援的事件和事件屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="410a6-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="410a6-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="410a6-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="410a6-112">包含支援的事件清單。</span><span class="sxs-lookup"><span data-stu-id="410a6-112">Contains the list of supported events.</span></span>                                                                |
| [<span data-ttu-id="410a6-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="410a6-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="410a6-114">包含指定事件的屬性。</span><span class="sxs-lookup"><span data-stu-id="410a6-114">Contains the attributes for a given event.</span></span>                                                            |



 

<span data-ttu-id="410a6-115">當使用者在命令列選擇選項 "4" 時，應用程式會叫用在 ServiceCapabilities .cpp 模組中找到的 **ListSupportedEvents** 方法。</span><span class="sxs-lookup"><span data-stu-id="410a6-115">When the user chooses option "4" at the command line, the application invokes the **ListSupportedEvents** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="410a6-116">請注意，在抓取事件清單之前，範例應用程式會在連線的裝置上開啟連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="410a6-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="410a6-117">在 WPD 中，事件的名稱、選項和參數會加以描述。</span><span class="sxs-lookup"><span data-stu-id="410a6-117">In WPD, an event is described by its name, options, and parameters.</span></span> <span data-ttu-id="410a6-118">事件名稱是容易編寫腳本的字串，例如 "MyCustomEvent"。</span><span class="sxs-lookup"><span data-stu-id="410a6-118">The event name is a script-friendly string, for example, "MyCustomEvent".</span></span> <span data-ttu-id="410a6-119">事件選項會指出指定的事件是否會廣播給所有用戶端，以及該事件是否支援自動播放。</span><span class="sxs-lookup"><span data-stu-id="410a6-119">The event options indicate whether a given event is broadcast to all clients and whether that event supports autoplay.</span></span> <span data-ttu-id="410a6-120">事件參數屬性包括指定參數的 PROPERTYKEY 和 VARTYPE。</span><span class="sxs-lookup"><span data-stu-id="410a6-120">The event parameter attributes includes a given parameter's PROPERTYKEY and VARTYPE.</span></span>

<span data-ttu-id="410a6-121">ServiceCapabilities .cpp 模組中的四個方法支援抓取指定連絡人服務的支援事件： **ListSupportedEvents**、 **DisplayEvent**、 **DisplayEventOptions** 和 **DisplayEventParameters**。</span><span class="sxs-lookup"><span data-stu-id="410a6-121">Four methods in the ServiceCapabilities.cpp module support the retrieval of supported events for the given Contacts service: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions**, and **DisplayEventParameters**.</span></span> <span data-ttu-id="410a6-122">**ListSupportedEvents** 方法會抓取支援的事件計數和每個事件的 GUID 識別碼。</span><span class="sxs-lookup"><span data-stu-id="410a6-122">The **ListSupportedEvents** method retrieves a count of supported events and the GUID identifier for each event.</span></span> <span data-ttu-id="410a6-123">**DisplayEvent** 方法會顯示事件名稱或 GUID，然後呼叫 **DisplayEventOptions** 和 **DisplayEventParameters** 來顯示事件相關資料。</span><span class="sxs-lookup"><span data-stu-id="410a6-123">The **DisplayEvent** method displays the event name or GUID, and then calls **DisplayEventOptions** and **DisplayEventParameters** to display the event-related data.</span></span>

<span data-ttu-id="410a6-124">**ListSupportedEvents** 方法會叫用 [**IPortableDeviceService：：功能**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities)方法來取出 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)介面。</span><span class="sxs-lookup"><span data-stu-id="410a6-124">The **ListSupportedEvents** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="410a6-125">使用這個介面，它會藉由呼叫 [**IPortableDeviceServiceCapabilities：： GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) 方法來抓取支援的事件。</span><span class="sxs-lookup"><span data-stu-id="410a6-125">Using this interface, it retrieves the supported events by calling the [**IPortableDeviceServiceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="410a6-126">**GetSupportedEvents** 方法會抓取服務所支援之每個事件的 guid，並將這些 guid 複製到 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)物件中。</span><span class="sxs-lookup"><span data-stu-id="410a6-126">The **GetSupportedEvents** method retrieves the GUIDs for each event supported by the service and copies those GUIDs into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="410a6-127">下列程式碼說明如何取出支援的服務事件。</span><span class="sxs-lookup"><span data-stu-id="410a6-127">The following code illustrates retrieving supported service events.</span></span>


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



<span data-ttu-id="410a6-128">在 **ListSupportedEvents** 方法取得代表指定服務所支援之每個事件的 guid 之後，它會叫用 **DisplayEvent** 方法以抓取事件特定資料。</span><span class="sxs-lookup"><span data-stu-id="410a6-128">After the **ListSupportedEvents** method retrieves the GUIDs representing each event supported by the given service, it invokes the **DisplayEvent** method to retrieve event-specific data.</span></span> <span data-ttu-id="410a6-129">這類資料包括事件名稱、其選項 (廣播或自動播放) 、參數 Guid、參數類型等等。</span><span class="sxs-lookup"><span data-stu-id="410a6-129">This data includes the event name, its options (broadcast or autoplay), parameter GUIDs, parameter types, and so on.</span></span>

<span data-ttu-id="410a6-130">**DisplayEvent** 方法會叫用 [**IPortableDeviceServiceCapabilities：： GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes)方法，以取得指定事件的屬性集合。</span><span class="sxs-lookup"><span data-stu-id="410a6-130">The **DisplayEvent** method invokes the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method to retrieve a collection of attributes for the given event.</span></span> <span data-ttu-id="410a6-131">然後，它會呼叫 [**IPortableDeviceValues：： GetStringValue**](iportabledevicevalues-getstringvalue.md) 方法，並要求驅動程式傳回指定事件的使用者易記名稱。</span><span class="sxs-lookup"><span data-stu-id="410a6-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a user-friendly name for the given event.</span></span> <span data-ttu-id="410a6-132">接下來， **DisplayEvent** 會呼叫 [**IPortableDeviceValues：： GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) 以取得事件選項。</span><span class="sxs-lookup"><span data-stu-id="410a6-132">Next, **DisplayEvent** calls the [**IPortableDeviceValues::GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) to retrieve the event options.</span></span> <span data-ttu-id="410a6-133">最後，DisplayEvent 會呼叫 [**IPortableDeviceValues：： GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) 以取得事件參數的清單。</span><span class="sxs-lookup"><span data-stu-id="410a6-133">Finally, DisplayEvent calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the list of event parameters.</span></span> <span data-ttu-id="410a6-134">它會將這些方法所傳回的資料傳遞給 **DisplayEventOptions** 和 **DisplayEventParameters** helper 函式，以轉譯指定事件的選項和參數資訊。</span><span class="sxs-lookup"><span data-stu-id="410a6-134">It passes the data returned by these methods to the **DisplayEventOptions** and the **DisplayEventParameters** helper functions, which render the options and parameter information for the given event.</span></span>

<span data-ttu-id="410a6-135">下列程式碼會使用 **DisplayEvent** 方法。</span><span class="sxs-lookup"><span data-stu-id="410a6-135">The following code uses the **DisplayEvent** method.</span></span>


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



<span data-ttu-id="410a6-136">**DisplayEventOptions** helper 函式會接收 [**IPortableDeviceValues**](iportabledevicevalues.md)物件，其中包含事件的選項資料。</span><span class="sxs-lookup"><span data-stu-id="410a6-136">The **DisplayEventOptions** helper function receives an [**IPortableDeviceValues**](iportabledevicevalues.md) object which contains the event's option data.</span></span> <span data-ttu-id="410a6-137">然後，它會呼叫 [**IPortableDeviceValues：： GetBoolValue**](iportabledevicevalues-getboolvalue.md) 方法來取出選項資料。</span><span class="sxs-lookup"><span data-stu-id="410a6-137">It then calls the [**IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md) method to retrieve the options data.</span></span> <span data-ttu-id="410a6-138">它會使用此資料轉譯字串，指出是否支援廣播和自動播放選項。</span><span class="sxs-lookup"><span data-stu-id="410a6-138">Using this data, it renders a string indicating whether the broadcast and autoplay options are supported.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="410a6-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="410a6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="410a6-140">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="410a6-140">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="410a6-141">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="410a6-141">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="410a6-142">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="410a6-142">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="410a6-143">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="410a6-143">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="410a6-144">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="410a6-144">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



