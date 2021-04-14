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
# <a name="retrieving-the-events-supported-by-a-device"></a><span data-ttu-id="fbaec-103">正在抓取裝置支援的事件</span><span class="sxs-lookup"><span data-stu-id="fbaec-103">Retrieving the Events Supported by a Device</span></span>

<span data-ttu-id="fbaec-104">某些 WPD 驅動程式支援事件通知。</span><span class="sxs-lookup"><span data-stu-id="fbaec-104">Some WPD drivers support event notification.</span></span> <span data-ttu-id="fbaec-105">這表示應用程式可以向驅動程式註冊，以在發生特定動作時接收通知。</span><span class="sxs-lookup"><span data-stu-id="fbaec-105">This means that an application can register with the driver to receive a notification when a specific action occurs.</span></span> <span data-ttu-id="fbaec-106">例如，應用程式可以註冊，以在新增或移除物件時接收通知。</span><span class="sxs-lookup"><span data-stu-id="fbaec-106">For example, an application can register to receive a notification when an object is added or removed.</span></span>

<span data-ttu-id="fbaec-107">有10個預先定義的事件可讓應用程式進行監視。</span><span class="sxs-lookup"><span data-stu-id="fbaec-107">There are ten predefined events that an application can monitor.</span></span> <span data-ttu-id="fbaec-108">如下表中所述。</span><span class="sxs-lookup"><span data-stu-id="fbaec-108">They are described in the following table.</span></span>



| <span data-ttu-id="fbaec-109">事件</span><span class="sxs-lookup"><span data-stu-id="fbaec-109">Event</span></span>                       | <span data-ttu-id="fbaec-110">描述</span><span class="sxs-lookup"><span data-stu-id="fbaec-110">Description</span></span>                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbaec-111">裝置功能已更新</span><span class="sxs-lookup"><span data-stu-id="fbaec-111">Device capabilities updated</span></span> | <span data-ttu-id="fbaec-112">發生于裝置功能變更時。</span><span class="sxs-lookup"><span data-stu-id="fbaec-112">Occurs when the device capabilities have changed.</span></span>                                                                                      |
| <span data-ttu-id="fbaec-113">裝置已移除</span><span class="sxs-lookup"><span data-stu-id="fbaec-113">Device removed</span></span>              | <span data-ttu-id="fbaec-114">裝置插上時發生。</span><span class="sxs-lookup"><span data-stu-id="fbaec-114">Occurs when the device is unplugged.</span></span>                                                                                                   |
| <span data-ttu-id="fbaec-115">裝置重設</span><span class="sxs-lookup"><span data-stu-id="fbaec-115">Device reset</span></span>                | <span data-ttu-id="fbaec-116">當裝置已重設時發生。</span><span class="sxs-lookup"><span data-stu-id="fbaec-116">Occurs when the device has been reset.</span></span>                                                                                                 |
| <span data-ttu-id="fbaec-117">加入的物件</span><span class="sxs-lookup"><span data-stu-id="fbaec-117">Object added</span></span>                | <span data-ttu-id="fbaec-118">發生于裝置上的新物件變成可用後。</span><span class="sxs-lookup"><span data-stu-id="fbaec-118">Occurs after a new object becomes available on the device.</span></span>                                                                             |
| <span data-ttu-id="fbaec-119">物件已移除</span><span class="sxs-lookup"><span data-stu-id="fbaec-119">Object removed</span></span>              | <span data-ttu-id="fbaec-120">發生于從裝置移除物件之後。</span><span class="sxs-lookup"><span data-stu-id="fbaec-120">Occurs after an object has been removed from the device.</span></span>                                                                               |
| <span data-ttu-id="fbaec-121">要求的物件傳輸</span><span class="sxs-lookup"><span data-stu-id="fbaec-121">Object transfer requested</span></span>   | <span data-ttu-id="fbaec-122">表示已提出要求以傳送物件。</span><span class="sxs-lookup"><span data-stu-id="fbaec-122">Indicates that a request has been made to transfer an object.</span></span>                                                                          |
| <span data-ttu-id="fbaec-123">物件已更新</span><span class="sxs-lookup"><span data-stu-id="fbaec-123">Object updated</span></span>              | <span data-ttu-id="fbaec-124">在物件或其子系已更新後發生。</span><span class="sxs-lookup"><span data-stu-id="fbaec-124">Occurs after either an object or its children has been updated.</span></span> <span data-ttu-id="fbaec-125">接著， (連線的用戶端應該更新其指定物件的視圖。 ) </span><span class="sxs-lookup"><span data-stu-id="fbaec-125">(Connected clients should then update their view of the given object.)</span></span> |
| <span data-ttu-id="fbaec-126">正在進行儲存格式</span><span class="sxs-lookup"><span data-stu-id="fbaec-126">Storage format in progress</span></span>  | <span data-ttu-id="fbaec-127">當裝置存放裝置格式化時發生。</span><span class="sxs-lookup"><span data-stu-id="fbaec-127">Occurs when the device storage is being formatted.</span></span>                                                                                     |



 

<span data-ttu-id="fbaec-128">如需與這些事件相關聯的常數清單，請參閱「 [事件常數](event-constants.md) 」主題。</span><span class="sxs-lookup"><span data-stu-id="fbaec-128">For a list of the constants associated with these events, see the [Event Constants](event-constants.md) topic.</span></span>

<span data-ttu-id="fbaec-129">DeviceCapabilities .cpp 模組中的 ListSupportedEvents 函式會示範如何抓取指定裝置所支援的事件。</span><span class="sxs-lookup"><span data-stu-id="fbaec-129">The ListSupportedEvents function in the DeviceCapabilities.cpp module demonstrates the retrieval of events supported by a given device.</span></span>

<span data-ttu-id="fbaec-130">您的應用程式可以使用下表所述的介面，來取得裝置所支援之事件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fbaec-130">Your application can retrieve the identifiers for events supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="fbaec-131">介面</span><span class="sxs-lookup"><span data-stu-id="fbaec-131">Interface</span></span>                                                                                      | <span data-ttu-id="fbaec-132">描述</span><span class="sxs-lookup"><span data-stu-id="fbaec-132">Description</span></span>                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="fbaec-133">**IPortableDeviceCapabilities 介面**</span><span class="sxs-lookup"><span data-stu-id="fbaec-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="fbaec-134">提供支援事件抓取方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="fbaec-134">Provides access to the supported-event retrieval methods.</span></span> |
| [<span data-ttu-id="fbaec-135">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="fbaec-135">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="fbaec-136">用來列舉和儲存功能分類資料。</span><span class="sxs-lookup"><span data-stu-id="fbaec-136">Used to enumerate and store functional-category data.</span></span>     |



 

<span data-ttu-id="fbaec-137">範例應用程式所完成的第一項工作是抓取 [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) 物件，此物件是用來取得指定裝置所支援的事件。</span><span class="sxs-lookup"><span data-stu-id="fbaec-137">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the events supported by the given device.</span></span>


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



<span data-ttu-id="fbaec-138">藉由呼叫 [**IPortableDeviceCapabilities：： GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) 方法，即可取出支援的事件。</span><span class="sxs-lookup"><span data-stu-id="fbaec-138">The supported events are retrieved by calling the [**IPortableDeviceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="fbaec-139">這個方法會抓取指定裝置的事件識別碼集合，並將它們儲存在 pEvents 引數所指向的 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件中。</span><span class="sxs-lookup"><span data-stu-id="fbaec-139">This method retrieves a collection of event identifiers for the given device and stores them in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object pointed to by the pEvents argument.</span></span>


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



<span data-ttu-id="fbaec-140">下一步是取得支援事件的計數，讓應用程式可以逐一查看 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件，並取得每個的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fbaec-140">The next step is to retrieve the count of supported events so that the application can iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object and retrieve the identifier for each.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fbaec-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="fbaec-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbaec-142">**事件常數**</span><span class="sxs-lookup"><span data-stu-id="fbaec-142">**Event Constants**</span></span>](event-constants.md)
</dt> <dt>

[<span data-ttu-id="fbaec-143">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="fbaec-143">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="fbaec-144">**IPortableDeviceCapabilities 介面**</span><span class="sxs-lookup"><span data-stu-id="fbaec-144">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="fbaec-145">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="fbaec-145">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="fbaec-146">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="fbaec-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



