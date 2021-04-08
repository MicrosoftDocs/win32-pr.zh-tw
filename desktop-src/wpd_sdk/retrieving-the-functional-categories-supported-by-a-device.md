---
description: 正在抓取裝置支援的功能分類
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: 正在抓取裝置支援的功能分類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514c6255fa089dc235b5edd8a25b5ef581aee84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850627"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a><span data-ttu-id="a0ab7-103">正在抓取裝置支援的功能分類</span><span class="sxs-lookup"><span data-stu-id="a0ab7-103">Retrieving the Functional Categories Supported by a Device</span></span>

<span data-ttu-id="a0ab7-104">Windows 可攜式裝置可支援一或多個功能類別。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-104">Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="a0ab7-105">下表將說明這些類別。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-105">These categories are described in the following table.</span></span>



| <span data-ttu-id="a0ab7-106">類別</span><span class="sxs-lookup"><span data-stu-id="a0ab7-106">Category</span></span>                    | <span data-ttu-id="a0ab7-107">描述</span><span class="sxs-lookup"><span data-stu-id="a0ab7-107">Description</span></span>                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ab7-108">音訊捕獲</span><span class="sxs-lookup"><span data-stu-id="a0ab7-108">Audio capture</span></span>               | <span data-ttu-id="a0ab7-109">裝置可以用來錄製音訊。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-109">The device can be used to record audio.</span></span>                                              |
| <span data-ttu-id="a0ab7-110">轉譯資訊</span><span class="sxs-lookup"><span data-stu-id="a0ab7-110">Rendering information</span></span>       | <span data-ttu-id="a0ab7-111">裝置會提供描述其能夠轉譯之媒體檔案的資料。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-111">The device provides data describing the media files that it is capable of rendering.</span></span> |
| <span data-ttu-id="a0ab7-112">短訊息服務 (SMS) </span><span class="sxs-lookup"><span data-stu-id="a0ab7-112">Short message service (SMS)</span></span> | <span data-ttu-id="a0ab7-113">裝置支援文字訊息。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-113">The device supports text messaging.</span></span>                                                  |
| <span data-ttu-id="a0ab7-114">靜止影像捕捉</span><span class="sxs-lookup"><span data-stu-id="a0ab7-114">Still image capture</span></span>         | <span data-ttu-id="a0ab7-115">裝置可以用來捕捉仍是映射。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-115">The device can be used to capture still images.</span></span>                                      |
| <span data-ttu-id="a0ab7-116">儲存體</span><span class="sxs-lookup"><span data-stu-id="a0ab7-116">Storage</span></span>                     | <span data-ttu-id="a0ab7-117">裝置可以用來儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-117">The device can be used to store files.</span></span>                                               |



 

<span data-ttu-id="a0ab7-118">DeviceCapabilities .cpp 模組中的 ListFunctionalCategories 函式會示範如何抓取所選裝置的功能分類。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-118">The ListFunctionalCategories function in the DeviceCapabilities.cpp module demonstrates the retrieval of functional categories for a selected device.</span></span>

<span data-ttu-id="a0ab7-119">您的應用程式可以使用下表所述的介面，來取得裝置所支援的功能類別。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-119">Your application can retrieve the functional categories supported by a device by using the interfaces described in the following table.</span></span>



| <span data-ttu-id="a0ab7-120">介面</span><span class="sxs-lookup"><span data-stu-id="a0ab7-120">Interface</span></span>                                                                                      | <span data-ttu-id="a0ab7-121">描述</span><span class="sxs-lookup"><span data-stu-id="a0ab7-121">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="a0ab7-122">**IPortableDeviceCapabilities 介面**</span><span class="sxs-lookup"><span data-stu-id="a0ab7-122">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="a0ab7-123">提供功能類別抓取方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-123">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="a0ab7-124">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="a0ab7-124">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="a0ab7-125">用來列舉和儲存功能分類資料。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-125">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="a0ab7-126">範例應用程式所完成的第一項工作是抓取 [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) 物件，此物件是用來在選取的裝置上取得功能類別目錄。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-126">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the functional categories on the selected device.</span></span>


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



<span data-ttu-id="a0ab7-127">抓取的分類會儲存在 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件中。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-127">The retrieved categories are stored in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="a0ab7-128">下一步是列舉和顯示支援的類別。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-128">The next step is the enumeration and display of the supported categories.</span></span> <span data-ttu-id="a0ab7-129">範例應用程式完成的第一個步驟是取得支援類別的計數。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-129">The first step that the sample application accomplishes is to retrieve the count of supported categories.</span></span> <span data-ttu-id="a0ab7-130">然後，它會使用此計數來逐一查看包含支援之類別的 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a0ab7-130">It then uses this count to iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that contains the supported categories.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a0ab7-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0ab7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0ab7-132">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="a0ab7-132">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="a0ab7-133">**IPortableDeviceCapabilities 介面**</span><span class="sxs-lookup"><span data-stu-id="a0ab7-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="a0ab7-134">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="a0ab7-134">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="a0ab7-135">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="a0ab7-135">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



