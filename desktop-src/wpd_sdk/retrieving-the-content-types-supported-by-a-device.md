---
description: 正在抓取裝置支援的內容類型
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: 正在抓取裝置支援的內容類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f85366374ec28ed44664a3b86edbee1e046e1a5ee4e331dbe041398bdc48a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083462"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a>正在抓取裝置支援的內容類型

如「取得[裝置所支援的功能分類](retrieving-the-functional-categories-supported-by-a-device.md)」主題所述，Windows 可攜式裝置可支援一或多個功能類別。 任何指定的功能類別都可支援一或多個內容類型。 例如，儲存體類別目錄可能支援資料夾、音訊和影像的內容類型。

如需 WPD 所支援內容類型的描述，請參閱 [**WPD \_ 內容類型 \_ 的 \_ 所有**](wpd-content-type-all.md) 主題。

DeviceCapabilities .cpp 模組中的 ListSupportedContentTypes 函式會示範如何抓取所選裝置所支援之功能類別目錄的內容類型。

您的應用程式可以使用下表所述的介面，來取得裝置所支援的功能類別。



| 介面                                                                                      | 描述                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**IPortableDeviceCapabilities 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | 提供功能類別抓取方法的存取權。 |
| [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) | 用來列舉和儲存功能分類資料。         |



 

在 ListSupportedContentTypes 函式中找到的程式碼與在 ListFunctionalCategories 函數中找到的程式碼幾乎完全相同。  (查看裝置主題所支援的「正在抓取」 [功能類別目錄](retrieving-the-functional-categories-supported-by-a-device.md) 。 ) 其中一個差異是呼叫 [**IPortableDeviceCapabilities：： GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) 方法，該方法會出現在可逐一查看功能類別的迴圈中。


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

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

// Loop through each functional category and display its name and supported content types.
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

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
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

 

 



