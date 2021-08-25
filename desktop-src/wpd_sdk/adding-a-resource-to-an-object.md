---
description: 將資源新增至物件
ms.assetid: 81476f50-5ea0-4e02-9e38-2b1dfcc32c4f
title: 將資源新增至物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f95cd4b11182a8cc6bc3d249f2065744ba0f6d8efe1be204e47ad321429a88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930238"
---
# <a name="adding-a-resource-to-an-object"></a>將資源新增至物件

除了將物件傳送至裝置之外，也可以將資源新增至物件。 例如，應用程式可以將相片新增至指定連絡人的現有資訊。

使用下表所述的介面來新增資源。



| 介面                                                              | 描述                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)     | 提供內容特定方法的存取權。                  |
| [**IPortableDeviceResources 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) | 在將資源屬性和資料寫入至裝置時使用。 |
| [**IPortableDeviceValues 介面**](iportabledevicevalues.md)       | 用來寫入描述資源的屬性。              |
| IStream 介面                                                      | 用來簡化將資源寫入裝置的工作。              |



 

範例應用程式 ContentTransfer .cpp 模組中的 CreateContactPhotoResourceOnDevice 函式會示範應用程式如何將相片資源新增至 contact 物件。 此函式會提示使用者輸入要新增相片資源的裝置上連絡人的物件識別碼。 然後，它會顯示 [FileOpen] 對話方塊，讓使用者可以選取要加入的影像。 收集這項資料之後，應用程式就會將資源寫入裝置。

CreateContactPhotoResourceOnDevice 函式所完成的第一項工作是提示使用者輸入要新增相片之連絡人的物件識別碼。


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



下一步是要抓取 [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) 物件，而此物件會接著用來取得 [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) 物件。  (應用程式會使用這個第二個物件來建立和寫入新的資源。 ) 


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



之後，此範例會顯示 [ **FileOpen** ] 對話方塊，讓使用者指定包含要加入連絡人資訊之相片的影像檔案名稱。


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



一旦範例有 [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) 物件和影像檔案的名稱，它就會執行下列動作，以準備實際將資料傳輸到裝置。

1.  它會在選取的檔案上開啟 IStream 物件以進行讀取作業。
2.  它會建立 [**IPortableDeviceValues**](iportabledevicevalues.md) 物件，其中會包含影像大小和格式等資訊。


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



針對寫入作業準備 IStream 和 [**IPortableDeviceValues**](iportabledevicevalues.md) 物件之後，此範例會將影像傳送至裝置。 此範例會以三個步驟完成傳送，如下所示：

1.  它會藉由呼叫 [**IPortableDeviceResources：： CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) 方法，在裝置上建立資源。
2.  它會呼叫 StreamCopy helper 函式，以將來來源資料流複製到目的地資料流程。
3.  它會藉由呼叫 IPortableDeviceDataStream：： Commit 方法，通知設備磁碟機傳送已完成。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceResources 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)
</dt> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



