---
title: 將檔案傳送至裝置
description: 將檔案傳送至裝置
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Windows媒體裝置管理員，將檔案傳送至裝置
- 裝置管理員，將檔案傳送至裝置
- 程式設計指南，將檔案傳送至裝置
- 桌面應用程式，將檔案傳送至裝置
- 建立 Windows 媒體裝置管理員應用程式，將檔案傳送至裝置
- 將檔案寫入至裝置、將檔案傳送至裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974a47de872d03d42701ff6e95516a9ead59f1206729ae9ca70d6dd9e5f1260f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124138"
---
# <a name="sending-the-file-to-the-device"></a>將檔案傳送至裝置

如有必要，已轉碼檔案，且已設定所有包含格式的中繼資料之後，您的應用程式就可以將檔案傳送至裝置。 若要這樣做，您必須先針對裝置上的目標位置取得 **IWMDMStorageControl** 介面 (或更新版本) 。 **插入** 旗標會指定新的儲存區是否應為目標的同級或子系。 一旦取得目標之後，您就可以呼叫 [**IWMDMStorageControl：： Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)、 [**IWMDMStorageControl2：： Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)或 [**IWMDMStorageControl3：： Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) 來傳送檔案。 應用程式可以藉由執行 [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)來處理讀取檔案資料本身，也可以允許 **Insert** 方法自動讀取和傳送檔案，方法是不要提供指向應用程式所執行之 **IWMDMOperation** 的指標。

下列 c + + 程式碼示範如何呼叫 **Insert3** ，以將檔案寫入至裝置。 如果傳遞至 **Insert3** 的 *POperation* 指標為 **Null**，則會在一個步驟中傳送檔案;如果這個指標是有效的介面指標，Windows Media 裝置管理員將會呼叫您的回呼方法，以取得區塊中的資料。 如需如何執行 **IWMDMOperation** 的詳細資訊，請參閱 [手動處理檔案傳輸](handling-file-transfers-manually.md)。


```C++
// Set the flags for the operation
UINT flags = WMDM_MODE_BLOCK | // Synchronous call. 
    WMDM_STORAGECONTROL_INSERTINTO | // Insert it into the destination folder.
    WMDM_CONTENT_FILE | // We're inserting a file.
    WMDM_FILE_CREATE_OVERWRITE; // Overwrite existing files.
if (pOperation != NULL)
    flags |= WMDM_CONTENT_OPERATIONINTERFACE;

// Send the file and metadata.
hr = pStgCtl3->Insert3(
    flags,
    WMDM_FILE_ATTR_FOLDER, // The current storage is a folder.
    const_cast<WCHAR*>(pwszFileName), // Source file.
    L"My New File.wma",//NULL, // Destination file name.
    pOperation, // NULL to allow the SDK to read the file; 
                // non-NULL to present raw data bytes to the SDK.
    pProgress, // Interface to send simple progress notifications.
    pMetadata, // IWMDMMetaData interface previously created and filled.
    NULL, 
    &pNewStorage); // Out: handle to the new storage, if the method succeeds.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將檔案寫入至裝置**](writing-files-to-the-device.md)
</dt> </dl>

 

 




