---
description: 正在抓取支援的服務格式
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: 正在抓取支援的服務格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed8021d8feefaaad3da7905e17e8c658dfb19e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996925"
---
# <a name="retrieving-supported-service-formats"></a><span data-ttu-id="5f724-103">正在抓取支援的服務格式</span><span class="sxs-lookup"><span data-stu-id="5f724-103">Retrieving Supported Service Formats</span></span>

<span data-ttu-id="5f724-104">WpdServicesApiSample 應用程式所包含的程式碼會示範應用程式如何藉由呼叫下表中的介面方法，來取得指定連絡人服務所支援的格式。</span><span class="sxs-lookup"><span data-stu-id="5f724-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the formats supported by a given Contacts service by calling methods of the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f724-105">介面</span><span class="sxs-lookup"><span data-stu-id="5f724-105">Interface</span></span>                                                                            | <span data-ttu-id="5f724-106">描述</span><span class="sxs-lookup"><span data-stu-id="5f724-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="5f724-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="5f724-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="5f724-108">用來取出 **IPortableDeviceServiceCapabilities** 介面，以存取支援的事件。</span><span class="sxs-lookup"><span data-stu-id="5f724-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="5f724-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5f724-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="5f724-110">提供支援的事件和事件屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="5f724-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="5f724-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="5f724-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="5f724-112">包含支援的格式清單。</span><span class="sxs-lookup"><span data-stu-id="5f724-112">Contains the list of supported formats.</span></span>                                                               |
| [<span data-ttu-id="5f724-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="5f724-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="5f724-114">包含給定格式的屬性。</span><span class="sxs-lookup"><span data-stu-id="5f724-114">Contains the attributes for a given format.</span></span>                                                           |



 

<span data-ttu-id="5f724-115">當使用者在命令列選擇選項 "3" 時，應用程式會叫用在 ServiceCapabilities .cpp 模組中找到的 **ListSupportedFormats** 方法。</span><span class="sxs-lookup"><span data-stu-id="5f724-115">When the user chooses option "3" at the command line, the application invokes the **ListSupportedFormats** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="5f724-116">請注意，在抓取事件清單之前，範例應用程式會在連線的裝置上開啟連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="5f724-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="5f724-117">在 WPD 中，格式是由指定名稱的屬性描述， (選擇性地) 指定格式的 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="5f724-117">In WPD, a format is described by attributes that specify the name and (optionally) the MIME type of a given format.</span></span> <span data-ttu-id="5f724-118">這些屬性是在 thePortableDevice 標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="5f724-118">These attributes are defined in thePortableDevice.h header file.</span></span> <span data-ttu-id="5f724-119">如需支援屬性的說明，請參閱 [屬性](attributes.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="5f724-119">For a description of supported attributes, refer to the [Attributes](attributes.md) topic.</span></span>

<span data-ttu-id="5f724-120">在範例應用程式的案例中，如果 WpdServiceSampleDriver 是唯一安裝的裝置，驅動程式會針對其 Contact service 傳回兩種支援的格式： "AbstractContactFormat" 和 "VCard2Format"。</span><span class="sxs-lookup"><span data-stu-id="5f724-120">In the case of the sample application, if the WpdServiceSampleDriver is the only installed device, the driver returns two supported formats for its Contact service: "AbstractContactFormat" and "VCard2Format".</span></span> <span data-ttu-id="5f724-121">這些格式對應于 **WPD \_ 物件格式的「 \_ \_ 抽象 \_ 連絡人** 」和「 **WPD \_ 物件格式」 \_ \_ VCARD2** 在 PortableDevice 中找到的屬性。</span><span class="sxs-lookup"><span data-stu-id="5f724-121">These formats correspond to the **WPD\_OBJECT\_FORMAT\_ABSTRACT\_CONTACT** and the **WPD\_OBJECT\_FORMAT\_VCARD2** attributes found in PortableDevice.h.</span></span>

<span data-ttu-id="5f724-122">ServiceCapabilities .cpp 模組中的兩個方法支援將連絡人服務的支援格式抓取： **ListSupportedFormats** 和 **DisplayFormat**。</span><span class="sxs-lookup"><span data-stu-id="5f724-122">Two methods in the ServiceCapabilities.cpp module support the retrieval of supported formats for the Contacts service: **ListSupportedFormats** and **DisplayFormat**.</span></span> <span data-ttu-id="5f724-123">前者會針對每個支援的格式抓取 GUID 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f724-123">The former retrieves the GUID identifier for each supported format.</span></span> <span data-ttu-id="5f724-124">後者會將此 GUID 轉換為使用者易記字串。</span><span class="sxs-lookup"><span data-stu-id="5f724-124">The latter converts this GUID into a user-friendly string.</span></span>

<span data-ttu-id="5f724-125">**ListSupportedFormats** 方法會叫用 [**IPortableDeviceService：：功能**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities)方法來取出 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)介面。</span><span class="sxs-lookup"><span data-stu-id="5f724-125">The **ListSupportedFormats** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="5f724-126">使用這個介面，它會藉由呼叫 [**IPortableDeviceServiceCapabilities：： GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) 方法來抓取支援的格式。</span><span class="sxs-lookup"><span data-stu-id="5f724-126">Using this interface, it retrieves the supported formats by calling the [**IPortableDeviceServiceCapabilities::GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) method.</span></span> <span data-ttu-id="5f724-127">**GetSupportedFormats** 方法會針對服務所支援的每種格式抓取 guid，並將該 guid 複製到 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)物件中。</span><span class="sxs-lookup"><span data-stu-id="5f724-127">The **GetSupportedFormats** method retrieves the GUID for each format supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="5f724-128">下列程式碼會使用 **ListSupportedFormats** 方法。</span><span class="sxs-lookup"><span data-stu-id="5f724-128">The following code uses the **ListSupportedFormats** method.</span></span>


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

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

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="5f724-129">在 **ListSupportedFormats** 方法為指定服務所支援的每種格式取得 GUID 之後，它會叫用 **DisplayFormat** 方法，以顯示每個格式的腳本易記名稱;例如，"VCard2"。</span><span class="sxs-lookup"><span data-stu-id="5f724-129">After the **ListSupportedFormats** method retrieves the GUID for each format supported by the given service, it invokes the **DisplayFormat** method to display the script friendly name for each format; for example, "VCard2".</span></span>

<span data-ttu-id="5f724-130">**DisplayFormat** 方法會叫用 [**IPortableDeviceServiceCapabilities：： GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes)方法，以取得指定之格式 GUID 的屬性集合。</span><span class="sxs-lookup"><span data-stu-id="5f724-130">The **DisplayFormat** method invokes the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method retrieve a collection of attributes for the given format GUID.</span></span> <span data-ttu-id="5f724-131">然後，它會呼叫 [**IPortableDeviceValues：： GetStringValue**](iportabledevicevalues-getstringvalue.md) 方法，並要求驅動程式針對指定的格式傳回腳本易記的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f724-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a script-friendly name for the given format.</span></span>

<span data-ttu-id="5f724-132">下列程式碼會使用 **DisplayFormat** 方法。</span><span class="sxs-lookup"><span data-stu-id="5f724-132">The following code uses the **DisplayFormat** method.</span></span>


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="5f724-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f724-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f724-134">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="5f724-134">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="5f724-135">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5f724-135">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="5f724-136">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="5f724-136">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="5f724-137">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="5f724-137">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



