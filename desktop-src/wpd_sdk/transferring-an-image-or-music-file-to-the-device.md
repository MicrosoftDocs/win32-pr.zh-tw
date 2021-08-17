---
description: 將影像或音樂檔案傳送至裝置
ms.assetid: bace274c-512a-46da-80a7-84734ee880b7
title: 將影像或音樂檔案傳送至裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cf16c4c95080b5479825bbc4a0f8dcfd131fdb603821edab0a2e9df4d03c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928058"
---
# <a name="transferring-an-image-or-music-file-to-the-device"></a>將影像或音樂檔案傳送至裝置

應用程式最常完成的作業之一，就是將內容傳輸至連接的裝置。

您可以使用下表所述的介面來完成內容傳輸。



| 介面                                                                | 描述                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | 提供內容特定方法的存取權。               |
| [**IPortableDeviceDataStream 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | 在將內容寫入至裝置時使用。                   |
| [**IPortableDeviceValues 介面**](iportabledevicevalues.md)         | 用來取出描述內容的屬性。         |
| IStream 介面                                                        | 用來簡化內容的讀取和寫入至裝置。 |



 

`TransferContentToDevice`範例應用程式的 ContentTransfer .cpp 模組中的函式會示範應用程式如何將內容從電腦傳送至連線的裝置。 在此特定範例中，傳輸的內容可以是包含影像、音樂或連絡人資訊的檔案。

函式所完成的第一項工作 `TransferContentToDevice` 是提示使用者輸入物件識別碼，以識別要傳送的物件。


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
WCHAR                               szFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IPortableDeviceDataStream>  pFinalObjectDataStream;
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IStream>                    pTempStream;  // Temporary IStream which we use to QI for IPortableDeviceDataStream

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the file will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



函式所完成的第二個工作 `TransferContentToDevice` 是藉由呼叫 [**IPortableDevice：： Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content)方法來建立 [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)物件。


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



函式所完成的下一個工作 `TransferContentToDevice` 是建立 **FileOpen** 對話方塊，使用者可以用它來指定要傳送之檔案的位置和名稱。


```C++
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = szFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(szFilePath);
    OpenFileNameInfo.lpstrFilter    = pszFileTypeFilter;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = pszDefaultFileExtension;

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was canceled.\n");
        hr = E_ABORT;
    }
}
```



`TransferContentToDevice`函數會將篩選字串 (`wszFileTypeFilter`) 傳遞至 GetOpenFileName 方法，以決定使用者可以選擇的檔案類型。 `DoMenu`如需範例所允許的三種不同篩選準則的範例，請參閱 WpdApiSample .cpp 模組中的函式。

在使用者識別要傳送至裝置的特定檔案之後，此函 `TransferContentToDevice` 式會將該檔案開啟為 IStream 物件，並抓取完成傳送所需的屬性。


```C++
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(szFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // Get the required properties needed to properly describe the data being
        // transferred to the device.
        hr = GetRequiredPropertiesForContentType(guidContentType,           // Content type of the data
                                                 szSelection,              // Parent to transfer the data under
                                                 szFilePath,               // Full file path to the data file
                                                 pFileStream,               // Open IStream that contains the data
                                                 &pFinalObjectProperties);  // Returned properties describing the data
        if (FAILED(hr))
        {
            printf("! Failed to get required properties needed to transfer a file to the device, hr = 0x%lx\n", hr);
        }
    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",szFilePath, hr);
    }
}
```



藉由呼叫協助程式函式來抓取所需的屬性 `GetRequiredPropertiesForContentType` ，該函數會在 IStream 物件上運作。 `GetRequiredPropertiesForContentType`Helper 函式會建立 [**IPortableDeviceValues**](iportabledevicevalues.md)物件、抓取下列清單中的屬性，並將其加入至這個物件。

-   父物件識別碼
-   資料流程大小（以位元組為單位）
-   內容檔名稱
-   內容名稱 (不含副檔名的檔案名) 
-   內容類型 (影像、音訊或連絡人) 
-   內容格式 (JFIF、WMA 或 vCard2) 

範例應用程式會使用抓取的屬性在裝置上建立新的內容。 這會以三個階段完成：

1.  應用程式會呼叫 [**IPortableDeviceContent：： CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) 方法，在裝置上建立新的 IStream 物件。
2.  應用程式會使用此物件從 WPD 驅動程式取得 [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) 物件。
3.  應用程式會使用新的 **IPortableDeviceDataStream** 物件，透過 StreamCopy helper 函式) 將內容寫入至裝置 (。 Helper 函式會將來源檔案中的資料寫入 [**IPortableDeviceContent：： CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)所傳回的資料流程。
4.  應用程式會在目的地資料流程上呼叫 Commit 方法，以完成作業。


```C++
// 4) Transfer for the content to the device
if (SUCCEEDED(hr))
{
    hr = pContent->CreateObjectWithPropertiesAndData(pFinalObjectProperties,    // Properties describing the object data
                                                     &pTempStream,              // Returned object data stream (to transfer the data to)
                                                     &cbOptimalTransferSize,    // Returned optimal buffer size to use during transfer
                                                     NULL);

    // Once we have a the IStream returned from CreateObjectWithPropertiesAndData,
    // QI for IPortableDeviceDataStream so we can use the additional methods
    // to get more information about the object (i.e. The newly created object
    // identifier on the device)
    if (SUCCEEDED(hr))
    {
        hr = pTempStream->QueryInterface(IID_PPV_ARGS(&pFinalObjectDataStream));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface for IPortableDeviceDataStream, hr = 0x%lx\n",hr);
        }
    }

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pFinalObjectDataStream, // Destination (The Object to transfer to)
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
        hr = pFinalObjectDataStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit object to device, hr = 0x%lx\n",hr);
        }
    }

    // Some clients may want to know the object identifier of the newly created
    // object.  This is done by calling GetObjectID() method on the
    // IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        PWSTR pszNewlyCreatedObject = NULL;
        hr = pFinalObjectDataStream->GetObjectID(&pszNewlyCreatedObject);
        if (SUCCEEDED(hr))
        {
            printf("The file '%ws' was transferred to the device.\nThe newly created object's ID is '%ws'\n",szFilePath ,pszNewlyCreatedObject);
        }

        if (FAILED(hr))
        {
            printf("! Failed to get the newly transferred object's identifier from the device, hr = 0x%lx\n",hr);
        }

        // Free the object identifier string returned from the GetObjectID() method.
        CoTaskMemFree(pszNewlyCreatedObject);
        pszNewlyCreatedObject = NULL;
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceDataStream 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



