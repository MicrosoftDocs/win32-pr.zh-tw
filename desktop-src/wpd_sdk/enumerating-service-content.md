---
description: 列舉服務內容
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: 列舉服務內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b701bdab867e96bc9658e2624ea18aa65dfc33
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424248"
---
# <a name="enumerating-service-content"></a><span data-ttu-id="adab5-103">列舉服務內容</span><span class="sxs-lookup"><span data-stu-id="adab5-103">Enumerating Service Content</span></span>

<span data-ttu-id="adab5-104">當您的應用程式開啟服務之後，就可以開始執行與服務相關的作業。</span><span class="sxs-lookup"><span data-stu-id="adab5-104">After your application opens a service, it can begin performing service-related operations.</span></span> <span data-ttu-id="adab5-105">在 WpdServicesApiSample 應用程式的案例中，其中一項作業是指定連絡人服務的內容列舉。</span><span class="sxs-lookup"><span data-stu-id="adab5-105">In the case of the WpdServicesApiSample application, one of these operations is the enumeration of content for a given Contacts service.</span></span> <span data-ttu-id="adab5-106">下表說明所使用的介面。</span><span class="sxs-lookup"><span data-stu-id="adab5-106">The following table describes the interfaces used.</span></span>



| <span data-ttu-id="adab5-107">介面</span><span class="sxs-lookup"><span data-stu-id="adab5-107">Interface</span></span>                                                            | <span data-ttu-id="adab5-108">描述</span><span class="sxs-lookup"><span data-stu-id="adab5-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="adab5-109">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="adab5-109">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="adab5-110">用來取出 IPortableDeviceContent2 介面，以存取服務的內容。</span><span class="sxs-lookup"><span data-stu-id="adab5-110">Used to retrieve the IPortableDeviceContent2 interface to access content on the service.</span></span>         |
| [<span data-ttu-id="adab5-111">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="adab5-111">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="adab5-112">用來取出 IEnumPortableDeviceObjectIDs 介面，以列舉服務上的物件。</span><span class="sxs-lookup"><span data-stu-id="adab5-112">Used to retrieve the IEnumPortableDeviceObjectIDs interface to enumerate objects on the service.</span></span> |
| [<span data-ttu-id="adab5-113">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="adab5-113">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | <span data-ttu-id="adab5-114">用來列舉服務上的物件。</span><span class="sxs-lookup"><span data-stu-id="adab5-114">Used to enumerate objects on the service.</span></span>                                                        |



 

<span data-ttu-id="adab5-115">內容列舉程式碼可在 ContentEnumeration .cpp 模組中找到。</span><span class="sxs-lookup"><span data-stu-id="adab5-115">The content enumeration code is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="adab5-116">此程式碼位於 **EnumerateAllContent** 和 **RecursiveEnumerate** 方法中。</span><span class="sxs-lookup"><span data-stu-id="adab5-116">This code resides in the **EnumerateAllContent** and the **RecursiveEnumerate** methods.</span></span> <span data-ttu-id="adab5-117">先前的方法會呼叫後者。</span><span class="sxs-lookup"><span data-stu-id="adab5-117">The former method calls the latter.</span></span>

<span data-ttu-id="adab5-118">**EnumerateContent** 方法會採用 [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)物件的指標作為其一個參數。</span><span class="sxs-lookup"><span data-stu-id="adab5-118">The **EnumerateContent** method takes a pointer to an [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) object as its one parameter.</span></span> <span data-ttu-id="adab5-119">這個物件會對應到應用程式在呼叫 [**IPortableDeviceService：： Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) 方法時先前開啟的服務。</span><span class="sxs-lookup"><span data-stu-id="adab5-119">This object corresponds to a service that the application opened earlier when it called the [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) method.</span></span>

<span data-ttu-id="adab5-120">**EnumerateContent** 方法會建立 [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)物件，並將此物件傳遞給 [**IPortableDeviceService：： Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content)方法。</span><span class="sxs-lookup"><span data-stu-id="adab5-120">The **EnumerateContent** method creates an [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) object and passes this object to the [**IPortableDeviceService::Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) method.</span></span> <span data-ttu-id="adab5-121">接著，這個方法會在服務的根層級抓取內容，然後以遞迴方式開始抓取在根目錄底下找到的內容。</span><span class="sxs-lookup"><span data-stu-id="adab5-121">This method, in turn, retrieves the content at the root level of the service, and then recursively begins to retrieve content found beneath the root.</span></span>

<span data-ttu-id="adab5-122">下列程式碼會對應至 **EnumerateContent** 方法。</span><span class="sxs-lookup"><span data-stu-id="adab5-122">The following code corresponds to the **EnumerateContent** method.</span></span>


```C++
// Enumerate all content on the service starting with the
// "DEVICE" object
void EnumerateAllContent(
    IPortableDeviceService* pService)
{
    HRESULT                          hr = S_OK;
    CComPtr<IPortableDeviceContent2> pContent;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    hr = pService->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="adab5-123">下列程式碼會對應至 **RecursiveEnumerate** 方法。</span><span class="sxs-lookup"><span data-stu-id="adab5-123">The following code corresponds to the **RecursiveEnumerate** method.</span></span> <span data-ttu-id="adab5-124">RecursiveEnumerate 方法會具現化所提供父物件的 **IEnumPortableDeviceObjectIDs** 介面，然後呼叫 **IEnumPortableDeviceObjectIDs：： Next**，以抓取立即子物件的批次。</span><span class="sxs-lookup"><span data-stu-id="adab5-124">The RecursiveEnumerate method instantiates an **IEnumPortableDeviceObjectIDs** interface for the supplied parent object, and calls **IEnumPortableDeviceObjectIDs::Next**, retrieving a batch of immediate child objects.</span></span> <span data-ttu-id="adab5-125">針對每個子物件，會再次呼叫 RecursiveEnumerate，以傳回其子物件的子物件等等。</span><span class="sxs-lookup"><span data-stu-id="adab5-125">For each child object, RecursiveEnumerate is called again to return its descendent child objects, and so on.</span></span>


```C++
// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                   pszObjectID,
    IPortableDeviceContent2* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent2, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="adab5-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="adab5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adab5-127">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="adab5-127">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="adab5-128">**IPortableDeviceContent2 介面**</span><span class="sxs-lookup"><span data-stu-id="adab5-128">**IPortableDeviceContent2 Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="adab5-129">**IPortableDeviceService 介面**</span><span class="sxs-lookup"><span data-stu-id="adab5-129">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="adab5-130">開啟服務</span><span class="sxs-lookup"><span data-stu-id="adab5-130">Opening a Service</span></span>](opening-a-service.md)
</dt> <dt>

[<span data-ttu-id="adab5-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="adab5-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



