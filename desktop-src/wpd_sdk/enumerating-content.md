---
description: 列舉內容
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: 列舉內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973048"
---
# <a name="enumerating-content"></a>列舉內容

裝置上的內容 (內容是否為資料夾、電話簿、影片或靜止影像) 在 WPD API 中稱為物件。 這些物件是由物件識別碼參考，並由屬性描述。 您可以藉由呼叫 [**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)中的方法、 [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)和 [**IEnumPortableDeviceObjectIDs 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)來列舉裝置上的物件。

範例應用程式示範在 ContentEnumeration .cpp 模組中找到的 EnumerateAllContent 函式中的內容列舉。 接著，此函式會呼叫 RecursiveEnumerate 函式，此函式會逐步解說在所選裝置上找到的物件階層，並傳回每個物件的物件識別碼。

如所述，RecursiveEnumerate 函式會針對在裝置上找到的每個物件，取得物件識別碼。 物件識別碼是字串值。 當您的應用程式抓取此識別碼之後，就可以取得更具描述性的物件資訊 (例如物件的名稱、物件的父系的識別碼等等) 。 這項描述性資訊稱為物件屬性 (或中繼資料) 。 您的應用程式可以藉由呼叫 [**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)的成員來取得這些屬性。

EnumerateAllContent 函式一開始會先取出 [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)的指標。 它會藉由呼叫 [**IPortableDevice：： Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) 方法來抓取這個指標。


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



一旦它抓取 IPortableDeviceContent 介面的指標，EnumerateAllContent 函式就會呼叫 RecursiveEnumerate 函式，該函式會引導在指定裝置上找到的物件階層，並傳回每個物件的物件識別碼。

RecursiveEnumerate 函式一開始會先取出 [**IEnumPortableDeviceObjectIDs 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)的指標。 此介面會公開應用程式用來流覽在指定裝置上找到的物件清單的方法。

在此範例中，RecursiveEnumerate 函式會呼叫 [**IEnumPortableDeviceObjectIDs：： Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) 方法以遍歷物件清單。

[**IEnumPortableDeviceObjects：： Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next)方法的每個呼叫都會要求10個識別碼的批次。  (這個值是由 NUM 物件指定 \_ \_ ，以 \_ 要求以第一個引數提供的常數。 ) 


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
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
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
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

[**IEnumPortableDeviceObjectIDs 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



