---
description: 正在抓取裝置支援的內容類型
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: 正在抓取裝置支援的內容類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e1b37160065be3130fca687f5f3277d9108a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983801"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a><span data-ttu-id="7afc7-103">正在抓取裝置支援的內容類型</span><span class="sxs-lookup"><span data-stu-id="7afc7-103">Retrieving the Content Types Supported by a Device</span></span>

<span data-ttu-id="7afc7-104">如「取得 [裝置所支援的功能分類](retrieving-the-functional-categories-supported-by-a-device.md) 」主題所述，Windows 可攜式裝置可支援一或多個功能類別。</span><span class="sxs-lookup"><span data-stu-id="7afc7-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="7afc7-105">任何指定的功能類別都可支援一或多個內容類型。</span><span class="sxs-lookup"><span data-stu-id="7afc7-105">Any given functional category may support one or more content types.</span></span> <span data-ttu-id="7afc7-106">例如，儲存體類別目錄可能支援資料夾、音訊和影像的內容類型。</span><span class="sxs-lookup"><span data-stu-id="7afc7-106">For example, the storage category may support content types of folder, audio, and image.</span></span>

<span data-ttu-id="7afc7-107">如需 WPD 所支援內容類型的描述，請參閱 [**WPD \_ 內容類型 \_ 的 \_ 所有**](wpd-content-type-all.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7afc7-107">For a description of the content types supported by WPD, see the [**WPD\_CONTENT\_TYPE\_ALL**](wpd-content-type-all.md) topic.</span></span>

<span data-ttu-id="7afc7-108">DeviceCapabilities .cpp 模組中的 ListSupportedContentTypes 函式會示範如何抓取所選裝置所支援之功能類別目錄的內容類型。</span><span class="sxs-lookup"><span data-stu-id="7afc7-108">The ListSupportedContentTypes function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="7afc7-109">您的應用程式可以使用下表所述的介面，來取得裝置所支援的功能類別。</span><span class="sxs-lookup"><span data-stu-id="7afc7-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="7afc7-110">介面</span><span class="sxs-lookup"><span data-stu-id="7afc7-110">Interface</span></span>                                                                                      | <span data-ttu-id="7afc7-111">描述</span><span class="sxs-lookup"><span data-stu-id="7afc7-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="7afc7-112">**IPortableDeviceCapabilities 介面**</span><span class="sxs-lookup"><span data-stu-id="7afc7-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="7afc7-113">提供功能類別抓取方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="7afc7-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="7afc7-114">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="7afc7-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="7afc7-115">用來列舉和儲存功能分類資料。</span><span class="sxs-lookup"><span data-stu-id="7afc7-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="7afc7-116">在 ListSupportedContentTypes 函式中找到的程式碼與在 ListFunctionalCategories 函數中找到的程式碼幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="7afc7-116">The code found in the ListSupportedContentTypes function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="7afc7-117"> (查看裝置主題所支援的「正在抓取」 [功能類別目錄](retrieving-the-functional-categories-supported-by-a-device.md) 。 ) 其中一個差異是呼叫 [**IPortableDeviceCapabilities：： GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) 方法，該方法會出現在可逐一查看功能類別的迴圈中。</span><span class="sxs-lookup"><span data-stu-id="7afc7-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) method, which appears within the loop that iterates through the functional categories.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7afc7-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="7afc7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7afc7-119">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="7afc7-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="7afc7-120">**IPortableDeviceCapabilities 介面**</span><span class="sxs-lookup"><span data-stu-id="7afc7-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="7afc7-121">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="7afc7-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="7afc7-122">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="7afc7-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



