---
description: 正在抓取裝置的功能物件識別碼
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: 正在抓取裝置的功能物件識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a753324e24a6b78625a78b4128380288b6672f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997814"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a>正在抓取裝置的功能物件識別碼

如「取得 [裝置所支援的功能分類](retrieving-the-functional-categories-supported-by-a-device.md) 」主題所述，Windows 可攜式裝置可支援一或多個功能類別。 任何指定的功能類別都可支援一個或多個功能物件。 例如，儲存體類別目錄可能支援三個功能儲存物件，每個物件都是由唯一識別碼字串來識別。 然後，第一個儲存物件可以透過字串 "Storage1" 來識別，並以字串 ">storage2" 來識別，而第三個儲存物件則是以字串 "Storage3" 來識別。

DeviceCapabilities .cpp 模組中的 ListFunctionalObjects 函式會示範如何抓取所選裝置所支援之功能類別目錄的內容類型。

您的應用程式可以使用下表所述的介面，來取得裝置所支援的功能類別。



| 介面                                                                                      | 描述                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**IPortableDeviceCapabilities 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | 提供功能類別抓取方法的存取權。 |
| [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) | 用來列舉和儲存功能分類資料。         |



 

在 ListFunctionalObjects 函式中找到的程式碼與在 ListFunctionalCategories 函數中找到的程式碼幾乎完全相同。  (查看裝置主題所支援的「正在抓取」 [功能類別目錄](retrieving-the-functional-categories-supported-by-a-device.md) 。 ) 其中一個差異是呼叫 [**IPortableDeviceCapabilities：： GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) 方法，該方法會出現在可逐一查看功能類別的迴圈中。


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

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

// Get all functional categories supported by the device.
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.
            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



