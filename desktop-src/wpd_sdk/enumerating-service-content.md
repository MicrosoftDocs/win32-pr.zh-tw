---
description: 列舉服務內容
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: 列舉服務內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adb949fdec9a0001583b1481ccd50ada1ef1df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191283"
---
# <a name="enumerating-service-content"></a>列舉服務內容

當您的應用程式開啟服務之後，就可以開始執行與服務相關的作業。 在 WpdServicesApiSample 應用程式的案例中，其中一項作業是指定連絡人服務的內容列舉。 下表說明所使用的介面。



|                                                                      |                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 介面                                                            | 描述                                                                                      |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | 用來取出 IPortableDeviceContent2 介面，以存取服務的內容。         |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | 用來取出 IEnumPortableDeviceObjectIDs 介面，以列舉服務上的物件。 |
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | 用來列舉服務上的物件。                                                        |



 

內容列舉程式碼可在 ContentEnumeration .cpp 模組中找到。 此程式碼位於 **EnumerateAllContent** 和 **RecursiveEnumerate** 方法中。 先前的方法會呼叫後者。

**EnumerateContent** 方法會採用 [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)物件的指標作為其一個參數。 這個物件會對應到應用程式在呼叫 [**IPortableDeviceService：： Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) 方法時先前開啟的服務。

**EnumerateContent** 方法會建立 [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)物件，並將此物件傳遞給 [**IPortableDeviceService：： Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content)方法。 接著，這個方法會在服務的根層級抓取內容，然後以遞迴方式開始抓取在根目錄底下找到的內容。

下列程式碼會對應至 **EnumerateContent** 方法。


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



下列程式碼會對應至 **RecursiveEnumerate** 方法。 RecursiveEnumerate 方法會具現化所提供父物件的 **IEnumPortableDeviceObjectIDs** 介面，然後呼叫 **IEnumPortableDeviceObjectIDs：： Next**，以抓取立即子物件的批次。 針對每個子物件，會再次呼叫 RecursiveEnumerate，以傳回其子物件的子物件等等。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**IPortableDeviceContent2 介面**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceService 介面**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[開啟服務](opening-a-service.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



