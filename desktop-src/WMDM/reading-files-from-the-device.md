---
title: 從裝置讀取檔案
description: 從裝置讀取檔案
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows媒體裝置管理員，從裝置讀取檔案
- 裝置管理員，從裝置讀取檔案
- 程式設計指南，從裝置讀取檔案
- 桌面應用程式，從裝置讀取檔案
- 建立 Windows 媒體裝置管理員應用程式、從裝置讀取檔案
- 從裝置讀取檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4352be59a335461f46bfc722146e4c51d31f72c1559e9ad8631e80cb6752c241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903998"
---
# <a name="reading-files-from-the-device"></a>從裝置讀取檔案

當您找到想要從裝置複製的檔案時，您就可以在單一呼叫中將檔案從裝置複製到電腦，或使用回呼將檔案位元組直接讀取至您的應用程式，如此就可以在適當的情況下處理或儲存資料。

下列步驟顯示在單一呼叫中從裝置複製檔案的基本方式：

1.  取得裝置上檔案的控制碼。 您可以藉由呼叫 [**IWMDMDevice3：： FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage)，使用遞迴檔案搜尋或（如果您知道儲存體的持續性識別碼）來取得控制碼。 無論是哪一種情況，您都需要物件的 [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) 介面。
2.  判斷儲存體是否為檔案或資料夾。 只有檔案可以從裝置複製。 呼叫 [**IWMDMStorage：： GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) 來取得儲存體屬性，以指出儲存體是否為檔案或資料夾。
3.  針對 [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)查詢 **IWMDMStorage** ，並呼叫 [**IWMDMStorageControl：： read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)以從裝置讀取檔案，並將其儲存至指定的位置。

如果您想要從裝置依區塊讀取檔案區塊，則必須執行 [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) 回呼介面。 將此介面傳遞至 **IWMDMStorageControl：： Read** 呼叫，Windows Media 裝置管理員會依序將檔案資料區區塊轉送至您的回呼。 下列步驟說明如何依區塊讀取裝置檔案區塊：

1.  取得儲存體的 **IWMDMStorage** 介面，並判斷它是否為檔案（如先前所述）。
2.  準備任何檔案控制代碼或其他必要的控制碼，以保存接收的資料。
3.  查詢儲存體的 **IWMDMStorageControl** 介面
4.  呼叫 **IWMDMStorageControl：： read** 以開始讀取作業，並傳入您所執行的 **IWMDMOperation** 介面。
5.  Windows媒體裝置管理員將依區塊將資料區區塊轉送至您的裝置，如[手動處理檔案傳輸](handling-file-transfers-manually.md)中所述。

下列 c + + 範例函數會從裝置讀取儲存物件。 函數會接受選擇性的 **IWMDMOperation** 介面指標;如果已提交，函式將會明確建立檔案，並在其 **IWMDMOperation：： TransferObjectData**; 的執行時，處理將資料寫入檔案的程式。如果沒有，則會讀取檔案，並儲存至 *pwszDestName* 所指定的目的地。


```C++
HANDLE m_File = NULL;

HRESULT myFileRead(IWMDMStorage pStorage, LPWSTR pwszDestName, IWMDMOperation* pOperation)
{
    HRESULT hr = S_OK;
    if ((pStorage == NULL) || (pwszDestName == NULL)) 
    {
        return E_INVALIDPARAM;
    }

    // Check that the storage is readable.
    DWORD attributes = 0;
    UINT flags = 0;
    hr = pStorage->GetAttributes(&attributes, NULL); 
    if (FAILED(hr))
    {
        return hr;
    }

    // Check that content is readable.
    if ((attributes & WMDM_FILE_ATTR_CANREAD) == 0)
    {
        return E_FAIL;
    }
    // Check that it is not abstract (such as an abstract playlist).
    else if (attributes & WMDM_STORAGE_ATTR_VIRTUAL)
    {
        return E_FAIL;
    }

    // Set some flag values for the read operation.
    flags |= WMDM_MODE_BLOCK;
    if (attributes & WMDM_FILE_ATTR_FOLDER)
    {
        flags |= WMDM_CONTENT_FOLDER;
    }
    if (attributes & WMDM_FILE_ATTR_FILE)
    {
        flags |= WMDM_CONTENT_FILE;
    }

    // Get the IWMDMStorageControl interface.
    CComQIPtr<IWMDMStorageControl> pStgControl(pStorage);
    
    // Extra steps if we want to read the file ourselves using IWMDMOperation3.
    if (pOperation != NULL)
    {
        // Create a new file and get the handle. m_File is a global variable
        // that we will use in IWMDMOperation::TransferObjectData.
        // This can also be done when IWMDMOperation::BeginRead is called.
        m_File = CreateFile(
            pwszDestName,   // Destination file name.
            GENERIC_WRITE,  // Write and append writes
            NULL,           // File can't be shared while using, and must be closed.
            NULL,           // Handle can't be inherited.
            CREATE_ALWAYS,  // Overwrite existing files.
            FILE_ATTRIBUTE_NORMAL, // No special attributes.
            NULL            // No template file supplied.
           );
        if (m_File == INVALID_HANDLE_VALUE) return E_FAIL;
        // Modify the Read() method flag. WMDM_CONTENT_FILE and WMDM_CONTENT_FOLDER 
        // are not valid flags when pOperation != NULL.
        flags |= WMDM_CONTENT_OPERATIONINTERFACE;
    }

    // Read the file.
    hr = pStgControl->Read(
             flags,        // Synchronous call specified.
             pwszDestName, // Ignored if pOperation is not NULL.
             NULL,         // No progress callback sent.
             pOperation);  // IWMDMOperation interface, if provided.
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows 媒體裝置管理員應用程式**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




