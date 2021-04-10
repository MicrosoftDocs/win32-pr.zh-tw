---
description: 將 Properties-Only 物件傳輸至裝置
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: 將 Properties-Only 物件傳輸至裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20f9bcfecd46ea3047310ea5b946a366b35b9c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694275"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a><span data-ttu-id="d3553-103">將 Properties-Only 物件傳輸至裝置</span><span class="sxs-lookup"><span data-stu-id="d3553-103">Transferring a Properties-Only Object to the Device</span></span>

<span data-ttu-id="d3553-104">雖然上一個主題中的範例示範了如何在包含屬性和資料的裝置上建立內容，但本主題的重點在於建立僅限屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="d3553-104">While the example in the previous topic demonstrated the creation of content on a device consisting of both properties and data, this topic focuses on the creation of a properties-only object.</span></span>

<span data-ttu-id="d3553-105">使用下表所述的介面來完成僅限屬性的傳輸。</span><span class="sxs-lookup"><span data-stu-id="d3553-105">Property-only transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="d3553-106">介面</span><span class="sxs-lookup"><span data-stu-id="d3553-106">Interface</span></span>                                                          | <span data-ttu-id="d3553-107">描述</span><span class="sxs-lookup"><span data-stu-id="d3553-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="d3553-108">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="d3553-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | <span data-ttu-id="d3553-109">提供內容特定方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="d3553-109">Provides access to the content-specific methods.</span></span>       |
| [<span data-ttu-id="d3553-110">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="d3553-110">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)   | <span data-ttu-id="d3553-111">用來取出描述內容的屬性。</span><span class="sxs-lookup"><span data-stu-id="d3553-111">Used to retrieve properties that describe the content.</span></span> |



 

<span data-ttu-id="d3553-112">`TransferContactToDevice`範例應用程式的 ContentTransfer .cpp 模組中的函式會示範應用程式如何將連絡人資訊從電腦傳送至連線的裝置。</span><span class="sxs-lookup"><span data-stu-id="d3553-112">The `TransferContactToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a PC to a connected device.</span></span> <span data-ttu-id="d3553-113">在此特定範例中，傳輸的連絡人名稱是硬式編碼的 "John Kane"，而傳輸的連絡人電話號碼一律為 "425-555-0123"。</span><span class="sxs-lookup"><span data-stu-id="d3553-113">In this particular sample, the transferred contact name is a hard-coded "John Kane" and the transferred contact phone number is always "425-555-0123".</span></span>

<span data-ttu-id="d3553-114">函式所完成的第一 `TransferContactToDevice` 項工作是提示使用者在裝置上輸入父物件的物件識別碼， (將) 傳送內容。</span><span class="sxs-lookup"><span data-stu-id="d3553-114">The first task accomplished by the `TransferContactToDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the contact will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="d3553-115">下一步是取得 contact 屬性的抓取，當範例將新的連絡人寫入裝置時，將會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="d3553-115">The next step is the retrieval of contact properties, which will be used when the sample writes the new contact to the device.</span></span> <span data-ttu-id="d3553-116">連絡人屬性的抓取是由 `GetRequiredPropertiesForPropertiesOnlyContact` helper 函數所執行。</span><span class="sxs-lookup"><span data-stu-id="d3553-116">The retrieval of contact properties is performed by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function.</span></span>


```C++
// 2) Get the properties that describe the object being created on the device

if (SUCCEEDED(hr))
{
    hr = GetRequiredPropertiesForPropertiesOnlyContact(szSelection,              // Parent to transfer the data under
                                                       &pFinalObjectProperties);  // Returned properties describing the data
    if (FAILED(hr))
    {
        printf("! Failed to get required properties needed to transfer an image file to the device, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="d3553-117">此函數會將下列資料寫入 **IPortableDeviceValues** 物件。</span><span class="sxs-lookup"><span data-stu-id="d3553-117">This function writes the following data to an **IPortableDeviceValues** object.</span></span>

-   <span data-ttu-id="d3553-118">裝置上連絡人父系的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3553-118">The object identifier for the contact's parent on the device.</span></span> <span data-ttu-id="d3553-119"> (這是裝置將用來儲存物件的目的地。 ) </span><span class="sxs-lookup"><span data-stu-id="d3553-119">(This is the destination where the device will store the object.)</span></span>
-   <span data-ttu-id="d3553-120">連絡人)  (的物件類型。</span><span class="sxs-lookup"><span data-stu-id="d3553-120">The object type (a contact).</span></span>
-   <span data-ttu-id="d3553-121">連絡人名稱 (「John Kane」 ) 的硬式編碼字串。</span><span class="sxs-lookup"><span data-stu-id="d3553-121">The contact name (a hard coded string of "John Kane").</span></span>
-   <span data-ttu-id="d3553-122">連絡人電話號碼 (「425-555-0123」 ) 的硬式編碼字串。</span><span class="sxs-lookup"><span data-stu-id="d3553-122">The contact phone number (a hard-coded string of "425-555-0123").</span></span>

<span data-ttu-id="d3553-123">最後一個步驟會使用 helper 函式) 所設定的屬性，在裝置上建立僅限屬性的物件 (`GetRequiredPropertiesForPropertiesOnlyContact` 。</span><span class="sxs-lookup"><span data-stu-id="d3553-123">The final step creates the properties-only object on the device (using the properties set by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function).</span></span> <span data-ttu-id="d3553-124">這是藉由呼叫 **IPortableDeviceContent：： CreateObjectWithPropertiesOnly** 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="d3553-124">This is accomplished by calling the **IPortableDeviceContent::CreateObjectWithPropertiesOnly** method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    PWSTR pszNewlyCreatedObject = NULL;
    hr = pContent->CreateObjectWithPropertiesOnly(pFinalObjectProperties,    // Properties describing the object data
                                                  &pszNewlyCreatedObject);
    if (SUCCEEDED(hr))
    {
        printf("The contact was transferred to the device.\nThe newly created object's ID is '%ws'\n",pszNewlyCreatedObject);
    }

    if (FAILED(hr))
    {
        printf("! Failed to transfer contact object to the device, hr = 0x%lx\n",hr);
    }

    // Free the object identifier string returned from CreateObjectWithPropertiesOnly
    CoTaskMemFree(pszNewlyCreatedObject);
    pszNewlyCreatedObject = NULL;
}
```



## <a name="related-topics"></a><span data-ttu-id="d3553-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3553-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3553-126">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="d3553-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="d3553-127">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="d3553-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="d3553-128">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="d3553-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d3553-129">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="d3553-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



