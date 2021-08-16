---
description: 正在抓取裝置支援的功能分類
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: 正在抓取裝置支援的功能分類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410788616cc20563b914a293afcd8e2bbbd87099f738ae21463d2092c620597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842690"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a>正在抓取裝置支援的功能分類

Windows可攜式裝置可支援一或多個功能類別。 下表將說明這些類別。



| 類別                    | 描述                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| 音訊捕獲               | 裝置可以用來錄製音訊。                                              |
| 轉譯資訊       | 裝置會提供描述其能夠轉譯之媒體檔案的資料。 |
| 短訊息服務 (SMS)  | 裝置支援文字訊息。                                                  |
| 靜止影像捕捉         | 裝置可以用來捕捉仍是映射。                                      |
| 儲存體                     | 裝置可以用來儲存檔案。                                               |



 

DeviceCapabilities .cpp 模組中的 ListFunctionalCategories 函式會示範如何抓取所選裝置的功能分類。

您的應用程式可以使用下表所述的介面，來取得裝置所支援的功能類別。



| 介面                                                                                      | 描述                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**IPortableDeviceCapabilities 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | 提供功能類別抓取方法的存取權。 |
| [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) | 用來列舉和儲存功能分類資料。         |



 

範例應用程式所完成的第一項工作是抓取 [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) 物件，此物件是用來在選取的裝置上取得功能類別目錄。


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
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



抓取的分類會儲存在 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件中。

下一步是列舉和顯示支援的類別。 範例應用程式完成的第一個步驟是取得支援類別的計數。 然後，它會使用此計數來逐一查看包含支援之類別的 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件。


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
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

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
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

 

 



