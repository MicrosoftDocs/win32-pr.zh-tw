---
description: 將資源新增至物件
ms.assetid: 81476f50-5ea0-4e02-9e38-2b1dfcc32c4f
title: 將資源新增至物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869b5cdcf172c4b8f27f7081bfce8e6f05073789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319611"
---
# <a name="adding-a-resource-to-an-object"></a><span data-ttu-id="90d21-103">將資源新增至物件</span><span class="sxs-lookup"><span data-stu-id="90d21-103">Adding a Resource to an Object</span></span>

<span data-ttu-id="90d21-104">除了將物件傳送至裝置之外，也可以將資源新增至物件。</span><span class="sxs-lookup"><span data-stu-id="90d21-104">In addition to transferring objects to a device, it's also possible to add resources to objects.</span></span> <span data-ttu-id="90d21-105">例如，應用程式可以將相片新增至指定連絡人的現有資訊。</span><span class="sxs-lookup"><span data-stu-id="90d21-105">For example, an application could add a photo to existing information for a given contact.</span></span>

<span data-ttu-id="90d21-106">使用下表所述的介面來新增資源。</span><span class="sxs-lookup"><span data-stu-id="90d21-106">Resources are added using the interfaces described in the following table.</span></span>



| <span data-ttu-id="90d21-107">介面</span><span class="sxs-lookup"><span data-stu-id="90d21-107">Interface</span></span>                                                              | <span data-ttu-id="90d21-108">描述</span><span class="sxs-lookup"><span data-stu-id="90d21-108">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="90d21-109">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="90d21-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)     | <span data-ttu-id="90d21-110">提供內容特定方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="90d21-110">Provides access to the content-specific methods.</span></span>                  |
| [<span data-ttu-id="90d21-111">**IPortableDeviceResources 介面**</span><span class="sxs-lookup"><span data-stu-id="90d21-111">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) | <span data-ttu-id="90d21-112">在將資源屬性和資料寫入至裝置時使用。</span><span class="sxs-lookup"><span data-stu-id="90d21-112">Used when writing the resource properties and data to the device.</span></span> |
| [<span data-ttu-id="90d21-113">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="90d21-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)       | <span data-ttu-id="90d21-114">用來寫入描述資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="90d21-114">Used to write properties that describe the resource.</span></span>              |
| <span data-ttu-id="90d21-115">IStream 介面</span><span class="sxs-lookup"><span data-stu-id="90d21-115">IStream Interface</span></span>                                                      | <span data-ttu-id="90d21-116">用來簡化將資源寫入裝置的工作。</span><span class="sxs-lookup"><span data-stu-id="90d21-116">Used to simplify writing the resource to the device.</span></span>              |



 

<span data-ttu-id="90d21-117">範例應用程式 ContentTransfer .cpp 模組中的 CreateContactPhotoResourceOnDevice 函式會示範應用程式如何將相片資源新增至 contact 物件。</span><span class="sxs-lookup"><span data-stu-id="90d21-117">The CreateContactPhotoResourceOnDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application could add a photo resource to a contact object.</span></span> <span data-ttu-id="90d21-118">此函式會提示使用者輸入要新增相片資源的裝置上連絡人的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="90d21-118">This function prompts the user for the object identifier of the contact on the device, to which the photo resource will be added.</span></span> <span data-ttu-id="90d21-119">然後，它會顯示 [FileOpen] 對話方塊，讓使用者可以選取要加入的影像。</span><span class="sxs-lookup"><span data-stu-id="90d21-119">Then it displays a FileOpen dialog box so that the user can select the image to be added.</span></span> <span data-ttu-id="90d21-120">收集這項資料之後，應用程式就會將資源寫入裝置。</span><span class="sxs-lookup"><span data-stu-id="90d21-120">Once this data is collected, the application writes the resource to the device.</span></span>

<span data-ttu-id="90d21-121">CreateContactPhotoResourceOnDevice 函式所完成的第一項工作是提示使用者輸入要新增相片之連絡人的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="90d21-121">The first task accomplished by the CreateContactPhotoResourceOnDevice function is to prompt the user to enter an object identifier for the contact to which the photo will be added.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
printf("Enter the identifer of the object to which we will add an Audio annotation.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting resource creation\n");
}do
```



<span data-ttu-id="90d21-122">下一步是要抓取 [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) 物件，而此物件會接著用來取得 [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) 物件。</span><span class="sxs-lookup"><span data-stu-id="90d21-122">The next step is the retrieval of an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which in turn is used to obtain an [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) object.</span></span> <span data-ttu-id="90d21-123"> (應用程式會使用這個第二個物件來建立和寫入新的資源。 ) </span><span class="sxs-lookup"><span data-stu-id="90d21-123">(The application uses this latter object to create and write the new resource.)</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}





if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="90d21-124">之後，此範例會顯示 [ **FileOpen** ] 對話方塊，讓使用者指定包含要加入連絡人資訊之相片的影像檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="90d21-124">After this, the sample displays the **FileOpen** dialog box, which allows the user to specify the name of the image file that contains the photo they want to add to the contact information.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = wszFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(wszFilePath);
    OpenFileNameInfo.lpstrFilter    = L"JPEG (*.JPG)\0*.JPG\0JPEG (*.JPEG)\0*.JPEG\0JPG (*.JPE)\0*.JPE\0JPG (*.JFIF)\0*.JFIF\0\0";;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = L"JPG";

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was cancelled.\n");
        hr = E_ABORT;
    }
}
```



<span data-ttu-id="90d21-125">一旦範例有 [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) 物件和影像檔案的名稱，它就會執行下列動作，以準備實際將資料傳輸到裝置。</span><span class="sxs-lookup"><span data-stu-id="90d21-125">Once the sample has an [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) object and the name of the image file, it does the following in preparation for actually transferring data to the device.</span></span>

1.  <span data-ttu-id="90d21-126">它會在選取的檔案上開啟 IStream 物件以進行讀取作業。</span><span class="sxs-lookup"><span data-stu-id="90d21-126">It opens an IStream object on the selected file for read operations.</span></span>
2.  <span data-ttu-id="90d21-127">它會建立 [**IPortableDeviceValues**](iportabledevicevalues.md) 物件，其中會包含影像大小和格式等資訊。</span><span class="sxs-lookup"><span data-stu-id="90d21-127">It creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, which will contain information such as the image size and format.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(wszFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // CoCreate the IPortableDeviceValues to hold the resource attributes
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pResourceAttributes);
        if (SUCCEEDED(hr))
        {
            // Fill in the necessary information regarding this resource

            // Set the WPD_OBJECT_ID.  This informs the driver which object this request is intended for.
            hr = pResourceAttributes->SetStringValue(WPD_OBJECT_ID, wszSelection);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID when creating a resource, hr = 0x%lx\n",hr);
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetKeyValue(WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY, WPD_RESOURCE_CONTACT_PHOTO);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE by requesting the total size of the
            // data stream.
            if (SUCCEEDED(hr))
            {
                STATSTG statstg = {0};
                hr = pFileStream->Stat(&statstg, STATFLAG_NONAME);
                if (SUCCEEDED(hr))
                {
                    hr = pResourceAttributes->SetUnsignedLargeIntegerValue(WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, statstg.cbSize.QuadPart);
                    if (FAILED(hr))
                    {
                        printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to get file's total size, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF because we are
            // creating a contact photo resource with JPG image data.
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetGuidValue(WPD_RESOURCE_ATTRIBUTE_FORMAT, WPD_OBJECT_FORMAT_JFIF);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF, hr = 0x%lx\n",hr);
                }
            }
        }

    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",wszFilePath, hr);
    }
}
```



<span data-ttu-id="90d21-128">針對寫入作業準備 IStream 和 [**IPortableDeviceValues**](iportabledevicevalues.md) 物件之後，此範例會將影像傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="90d21-128">After preparing the IStream and [**IPortableDeviceValues**](iportabledevicevalues.md) objects for the write operation, the sample transfers the image to the device.</span></span> <span data-ttu-id="90d21-129">此範例會以三個步驟完成傳送，如下所示：</span><span class="sxs-lookup"><span data-stu-id="90d21-129">The sample completes the transfer in three steps, as follows:</span></span>

1.  <span data-ttu-id="90d21-130">它會藉由呼叫 [**IPortableDeviceResources：： CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) 方法，在裝置上建立資源。</span><span class="sxs-lookup"><span data-stu-id="90d21-130">It creates the resource on the device by calling the [**IPortableDeviceResources::CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) method.</span></span>
2.  <span data-ttu-id="90d21-131">它會呼叫 StreamCopy helper 函式，以將來來源資料流複製到目的地資料流程。</span><span class="sxs-lookup"><span data-stu-id="90d21-131">It calls a StreamCopy helper function to copy the source stream to the destination stream.</span></span>
3.  <span data-ttu-id="90d21-132">它會藉由呼叫 IPortableDeviceDataStream：： Commit 方法，通知設備磁碟機傳送已完成。</span><span class="sxs-lookup"><span data-stu-id="90d21-132">It informs the device driver that the transfer is complete by calling the IPortableDeviceDataStream::Commit method.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pResources->CreateResource(pResourceAttributes,    // Properties describing this resource
                                    &pResourceStream,       // Returned resource data stream (to transfer the data to)
                                    &cbOptimalTransferSize, // Returned optimal buffer size to use during transfer
                                    NULL);


    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pResourceStream,        // Destination (The resource to transfer to)
                        pFileStream,            // Source (The File data to transfer from)
                        cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                        &cbTotalBytesWritten);  // The total number of bytes transferred from file to the device
        if (FAILED(hr))
        {
            printf("! Failed to transfer object to device, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to get IStream (representing destination object data on the device) from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // After transferring content to the device, the client is responsible for letting the
    // driver know that the transfer is complete by calling the Commit() method
    // on the IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        hr = pResourceStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit resource to device, hr = 0x%lx\n",hr);
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="90d21-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="90d21-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90d21-134">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="90d21-134">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="90d21-135">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="90d21-135">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="90d21-136">**IPortableDeviceResources 介面**</span><span class="sxs-lookup"><span data-stu-id="90d21-136">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)
</dt> <dt>

[<span data-ttu-id="90d21-137">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="90d21-137">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="90d21-138">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="90d21-138">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



