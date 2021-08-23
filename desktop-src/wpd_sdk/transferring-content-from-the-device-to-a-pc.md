---
description: 將內容從裝置傳輸到電腦
ms.assetid: 76069097-a513-42f7-bdcc-a65714e95f0a
title: 將內容從裝置傳輸到電腦
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a8695f8158040e75a4aae40f95386ed70af45df56a137dabc944ab6d1771e69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806518"
---
# <a name="transferring-content-from-the-device-to-a-pc"></a>將內容從裝置傳輸到電腦

WPD 應用程式所完成的一項常見作業是將內容從已連線的裝置傳送到電腦。

您可以使用下表所述的介面來完成內容傳輸。



| 介面                                                                | 描述                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | 提供 **IPortableDeviceProperties** 介面的存取權。 |
| [**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | 提供屬性特定方法的存取。                   |
| [**IPortableDeviceResources 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)   | 用來儲存指定設定檔的屬性索引鍵。          |
| IStream 介面                                                        | 用來讀取和寫入資料。                                |



 

`TransferContentFromDevice`範例應用程式的 ContentTransfer .cpp 模組中的函式會示範應用程式如何將連絡人資訊從已連線的裝置傳送到電腦。

函式所完成的第一 `TransferContentFromDevice` 項工作是提示使用者在裝置上輸入父物件的物件識別碼， (將) 傳送內容。


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



下一步是抓取範例用來存取內容特定方法的 **IPortableDeviceContent** 物件。


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



下一步是抓取範例用來存取資源特定方法的 **IPortableDeviceResources** 物件。


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



下一步是抓取 IStream 物件，此範例會使用此物件來讀取從裝置傳送的資料。


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



下一步是在裝置上抓取物件的檔案名。 這個字串是用來在電腦上建立對應的檔案名。 如果物件沒有裝置上的檔案名，則物件的識別碼會轉換成字串，並用來建立目的地檔案名。


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



之後，此範例會建立目的地 IStream 物件。


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



最後，來源 IStream 物件會複製到電腦上的目的地。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



