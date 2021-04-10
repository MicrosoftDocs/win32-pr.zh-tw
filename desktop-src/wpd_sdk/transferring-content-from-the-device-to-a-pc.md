---
description: 將內容從裝置傳輸到電腦
ms.assetid: 76069097-a513-42f7-bdcc-a65714e95f0a
title: 將內容從裝置傳輸到電腦
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de06861ba74b4b7883c8d96e25cebe3fbb64e21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194248"
---
# <a name="transferring-content-from-the-device-to-a-pc"></a><span data-ttu-id="64dc3-103">將內容從裝置傳輸到電腦</span><span class="sxs-lookup"><span data-stu-id="64dc3-103">Transferring Content from the Device to a PC</span></span>

<span data-ttu-id="64dc3-104">WPD 應用程式所完成的一項常見作業是將內容從已連線的裝置傳送到電腦。</span><span class="sxs-lookup"><span data-stu-id="64dc3-104">One common operation accomplished by a WPD application is the transfer of content from a connected device to the PC.</span></span>

<span data-ttu-id="64dc3-105">您可以使用下表所述的介面來完成內容傳輸。</span><span class="sxs-lookup"><span data-stu-id="64dc3-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="64dc3-106">介面</span><span class="sxs-lookup"><span data-stu-id="64dc3-106">Interface</span></span>                                                                | <span data-ttu-id="64dc3-107">描述</span><span class="sxs-lookup"><span data-stu-id="64dc3-107">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="64dc3-108">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="64dc3-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="64dc3-109">提供 **IPortableDeviceProperties** 介面的存取權。</span><span class="sxs-lookup"><span data-stu-id="64dc3-109">Provides access to the **IPortableDeviceProperties** interface.</span></span> |
| [<span data-ttu-id="64dc3-110">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="64dc3-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="64dc3-111">提供屬性特定方法的存取。</span><span class="sxs-lookup"><span data-stu-id="64dc3-111">Provides access to property-specific methods.</span></span>                   |
| [<span data-ttu-id="64dc3-112">**IPortableDeviceResources 介面**</span><span class="sxs-lookup"><span data-stu-id="64dc3-112">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)   | <span data-ttu-id="64dc3-113">用來儲存指定設定檔的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="64dc3-113">Used to store the property keys for the given profile.</span></span>          |
| <span data-ttu-id="64dc3-114">IStream 介面</span><span class="sxs-lookup"><span data-stu-id="64dc3-114">IStream Interface</span></span>                                                        | <span data-ttu-id="64dc3-115">用來讀取和寫入資料。</span><span class="sxs-lookup"><span data-stu-id="64dc3-115">Used to read and write the data.</span></span>                                |



 

<span data-ttu-id="64dc3-116">`TransferContentFromDevice`範例應用程式的 ContentTransfer .cpp 模組中的函式會示範應用程式如何將連絡人資訊從已連線的裝置傳送到電腦。</span><span class="sxs-lookup"><span data-stu-id="64dc3-116">The `TransferContentFromDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a connected device to a PC.</span></span>

<span data-ttu-id="64dc3-117">函式所完成的第一 `TransferContentFromDevice` 項工作是提示使用者在裝置上輸入父物件的物件識別碼， (將) 傳送內容。</span><span class="sxs-lookup"><span data-stu-id="64dc3-117">The first task accomplished by the `TransferContentFromDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                            hr                   = S_OK;
WCHAR                              szSelection[81]      = {0};
CComPtr<IPortableDeviceContent>    pContent;
CComPtr<IPortableDeviceResources>  pResources;
CComPtr<IPortableDeviceProperties> pProperties;
CComPtr<IStream>                   pObjectDataStream;
CComPtr<IStream>                   pFinalFileStream;
DWORD                              cbOptimalTransferSize = 0;
CAtlStringW                        strOriginalFileName;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Prompt user to enter an object identifier on the device to transfer.
printf("Enter the identifer of the object you wish to transfer.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="64dc3-118">下一步是抓取範例用來存取內容特定方法的 **IPortableDeviceContent** 物件。</span><span class="sxs-lookup"><span data-stu-id="64dc3-118">The next step is the retrieval of an **IPortableDeviceContent** object that the sample uses to access the content-specific methods.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="64dc3-119">下一步是抓取範例用來存取資源特定方法的 **IPortableDeviceResources** 物件。</span><span class="sxs-lookup"><span data-stu-id="64dc3-119">The next step is the retrieval of an **IPortableDeviceResources** object that the sample uses to access the resource-specific methods.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="64dc3-120">下一步是抓取 IStream 物件，此範例會使用此物件來讀取從裝置傳送的資料。</span><span class="sxs-lookup"><span data-stu-id="64dc3-120">The next step is the retrieval of an IStream object that the sample uses to read the data it is transferring from the device.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pResources->GetStream(szSelection,             // Identifier of the object we want to transfer
                               WPD_RESOURCE_DEFAULT,    // We are transferring the default resource (which is the entire object's data)
                               STGM_READ,               // Opening a stream in READ mode, because we are reading data from the device.
                               &cbOptimalTransferSize,  // Driver supplied optimal transfer size
                               &pObjectDataStream);
    if (FAILED(hr))
    {
        printf("! Failed to get IStream (representing object data on the device) from IPortableDeviceResources, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="64dc3-121">下一步是在裝置上抓取物件的檔案名。</span><span class="sxs-lookup"><span data-stu-id="64dc3-121">The next step is the retrieval of the object's file name on the device.</span></span> <span data-ttu-id="64dc3-122">這個字串是用來在電腦上建立對應的檔案名。</span><span class="sxs-lookup"><span data-stu-id="64dc3-122">This string is used to create the corresponding file name on the PC.</span></span> <span data-ttu-id="64dc3-123">如果物件沒有裝置上的檔案名，則物件的識別碼會轉換成字串，並用來建立目的地檔案名。</span><span class="sxs-lookup"><span data-stu-id="64dc3-123">If the object does not have a file name on the device, the object's identifier is converted to a string and used to create the destination file name.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (SUCCEEDED(hr))
    {
        hr = GetStringValue(pProperties,
                            szSelection,
                            WPD_OBJECT_ORIGINAL_FILE_NAME,
                            strOriginalFileName);
        if (FAILED(hr))
        {
            printf("! Failed to read WPD_OBJECT_ORIGINAL_FILE_NAME on object '%ws', hr = 0x%lx\n", szSelection, hr);
            strOriginalFileName.Format(L"%ws.data", szSelection);
            printf("* Creating a filename '%ws' as a default.\n", (PWSTR)strOriginalFileName.GetString());
            // Set the HRESULT to S_OK, so we can continue with our newly generated
            // temporary file name.
            hr = S_OK;
        }
    }
    else
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="64dc3-124">之後，此範例會建立目的地 IStream 物件。</span><span class="sxs-lookup"><span data-stu-id="64dc3-124">After this, the sample creates a destination IStream object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = SHCreateStreamOnFile(strOriginalFileName, STGM_CREATE|STGM_WRITE, &pFinalFileStream);
    if (FAILED(hr))
    {
        printf("! Failed to create a temporary file named (%ws) to transfer object (%ws), hr = 0x%lx\n",(PWSTR)strOriginalFileName.GetString(), szSelection, hr);
    }
}
```



<span data-ttu-id="64dc3-125">最後，來源 IStream 物件會複製到電腦上的目的地。</span><span class="sxs-lookup"><span data-stu-id="64dc3-125">Finally, the source IStream object is copied to the destination on the PC.</span></span>


```C++
if (SUCCEEDED(hr))
{
    DWORD cbTotalBytesWritten = 0;

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    hr = StreamCopy(pFinalFileStream,       // Destination (The Final File to transfer to)
                    pObjectDataStream,      // Source (The Object's data to transfer from)
                    cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                    &cbTotalBytesWritten);  // The total number of bytes transferred from device to the finished file
    if (FAILED(hr))
    {
        printf("! Failed to transfer object from device, hr = 0x%lx\n",hr);
    }
    else
    {
        printf("* Transferred object '%ws' to '%ws'.\n", szSelection, (PWSTR)strOriginalFileName.GetString());
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="64dc3-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="64dc3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64dc3-127">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="64dc3-127">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="64dc3-128">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="64dc3-128">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="64dc3-129">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="64dc3-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="64dc3-130">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="64dc3-130">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



