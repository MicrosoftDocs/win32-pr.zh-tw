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
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a><span data-ttu-id="2fb49-103">正在抓取裝置的功能物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2fb49-103">Retrieving the Functional Object Identifiers for a Device</span></span>

<span data-ttu-id="2fb49-104">如「取得 [裝置所支援的功能分類](retrieving-the-functional-categories-supported-by-a-device.md) 」主題所述，Windows 可攜式裝置可支援一或多個功能類別。</span><span class="sxs-lookup"><span data-stu-id="2fb49-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="2fb49-105">任何指定的功能類別都可支援一個或多個功能物件。</span><span class="sxs-lookup"><span data-stu-id="2fb49-105">Any given functional category may support one or more functional objects.</span></span> <span data-ttu-id="2fb49-106">例如，儲存體類別目錄可能支援三個功能儲存物件，每個物件都是由唯一識別碼字串來識別。</span><span class="sxs-lookup"><span data-stu-id="2fb49-106">For example, the storage category may support three functional storage objects, each of which is identified by a unique identifier string.</span></span> <span data-ttu-id="2fb49-107">然後，第一個儲存物件可以透過字串 "Storage1" 來識別，並以字串 ">storage2" 來識別，而第三個儲存物件則是以字串 "Storage3" 來識別。</span><span class="sxs-lookup"><span data-stu-id="2fb49-107">The first storage object may then be identified by the string "Storage1", the second by the string "Storage2", and the third by the string "Storage3".</span></span>

<span data-ttu-id="2fb49-108">DeviceCapabilities .cpp 模組中的 ListFunctionalObjects 函式會示範如何抓取所選裝置所支援之功能類別目錄的內容類型。</span><span class="sxs-lookup"><span data-stu-id="2fb49-108">The ListFunctionalObjects function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="2fb49-109">您的應用程式可以使用下表所述的介面，來取得裝置所支援的功能類別。</span><span class="sxs-lookup"><span data-stu-id="2fb49-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="2fb49-110">介面</span><span class="sxs-lookup"><span data-stu-id="2fb49-110">Interface</span></span>                                                                                      | <span data-ttu-id="2fb49-111">描述</span><span class="sxs-lookup"><span data-stu-id="2fb49-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="2fb49-112">**IPortableDeviceCapabilities 介面**</span><span class="sxs-lookup"><span data-stu-id="2fb49-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="2fb49-113">提供功能類別抓取方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="2fb49-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="2fb49-114">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="2fb49-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="2fb49-115">用來列舉和儲存功能分類資料。</span><span class="sxs-lookup"><span data-stu-id="2fb49-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="2fb49-116">在 ListFunctionalObjects 函式中找到的程式碼與在 ListFunctionalCategories 函數中找到的程式碼幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="2fb49-116">The code found in the ListFunctionalObjects function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="2fb49-117"> (查看裝置主題所支援的「正在抓取」 [功能類別目錄](retrieving-the-functional-categories-supported-by-a-device.md) 。 ) 其中一個差異是呼叫 [**IPortableDeviceCapabilities：： GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) 方法，該方法會出現在可逐一查看功能類別的迴圈中。</span><span class="sxs-lookup"><span data-stu-id="2fb49-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method, which appears within the loop that iterates through the functional categories.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2fb49-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="2fb49-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fb49-119">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="2fb49-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="2fb49-120">**IPortableDeviceCapabilities 介面**</span><span class="sxs-lookup"><span data-stu-id="2fb49-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="2fb49-121">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="2fb49-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="2fb49-122">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="2fb49-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



