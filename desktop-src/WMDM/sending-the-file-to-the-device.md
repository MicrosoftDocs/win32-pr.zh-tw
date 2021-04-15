---
title: 將檔案傳送至裝置
description: 將檔案傳送至裝置
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Windows Media 裝置管理員，將檔案傳送至裝置
- 裝置管理員，將檔案傳送至裝置
- 程式設計指南，將檔案傳送至裝置
- 桌面應用程式，將檔案傳送至裝置
- 建立 Windows Media 裝置管理員應用程式，將檔案傳送至裝置
- 將檔案寫入至裝置、將檔案傳送至裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65be0c18a6022538dc5573d936f63392234e9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507260"
---
# <a name="sending-the-file-to-the-device"></a><span data-ttu-id="e5991-109">將檔案傳送至裝置</span><span class="sxs-lookup"><span data-stu-id="e5991-109">Sending the File to the Device</span></span>

<span data-ttu-id="e5991-110">如有必要，已轉碼檔案，且已設定所有包含格式的中繼資料之後，您的應用程式就可以將檔案傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="e5991-110">After the file has been transcoded if necessary, and all metadata including the format has been set, your application can send the file to the device.</span></span> <span data-ttu-id="e5991-111">若要這樣做，您必須先針對裝置上的目標位置取得 **IWMDMStorageControl** 介面 (或更新版本) 。</span><span class="sxs-lookup"><span data-stu-id="e5991-111">In order to do so, you must first get an **IWMDMStorageControl** interface (or a later version) for a target location on the device.</span></span> <span data-ttu-id="e5991-112">**插入** 旗標會指定新的儲存區是否應為目標的同級或子系。</span><span class="sxs-lookup"><span data-stu-id="e5991-112">The **Insert** flags specify whether the new storage should be a sibling or child of the target.</span></span> <span data-ttu-id="e5991-113">一旦取得目標之後，您就可以呼叫 [**IWMDMStorageControl：： Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)、 [**IWMDMStorageControl2：： Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)或 [**IWMDMStorageControl3：： Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) 來傳送檔案。</span><span class="sxs-lookup"><span data-stu-id="e5991-113">Once you have gotten the target, you can call [**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2), or [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to transfer the file.</span></span> <span data-ttu-id="e5991-114">應用程式可以藉由執行 [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)來處理讀取檔案資料本身，也可以允許 **Insert** 方法自動讀取和傳送檔案，方法是不要提供指向應用程式所執行之 **IWMDMOperation** 的指標。</span><span class="sxs-lookup"><span data-stu-id="e5991-114">The application can handle reading the file data itself by implementing [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), or it can allow the **Insert** method to read and transfer the file automatically by not providing a pointer to an application-implemented **IWMDMOperation**.</span></span>

<span data-ttu-id="e5991-115">下列 c + + 程式碼示範如何呼叫 **Insert3** ，以將檔案寫入至裝置。</span><span class="sxs-lookup"><span data-stu-id="e5991-115">The following C++ code demonstrates calling **Insert3** to write a file to a device.</span></span> <span data-ttu-id="e5991-116">如果傳遞至 **Insert3** 的 *POperation* 指標為 **Null**，則會在一個步驟中傳送檔案;如果這個指標是有效的介面指標，Windows Media 裝置管理員會呼叫您的回呼方法，以取得區塊中的資料。</span><span class="sxs-lookup"><span data-stu-id="e5991-116">If the *pOperation* pointer passed to **Insert3** is **NULL**, the file will be sent in one step; if this pointer is a valid interface pointer, Windows Media Device Manager will call your callback method to get data in blocks.</span></span> <span data-ttu-id="e5991-117">如需如何執行 **IWMDMOperation** 的詳細資訊，請參閱 [手動處理檔案傳輸](handling-file-transfers-manually.md)。</span><span class="sxs-lookup"><span data-stu-id="e5991-117">For details on how to implement **IWMDMOperation**, see [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e5991-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5991-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5991-119">**將檔案寫入至裝置**</span><span class="sxs-lookup"><span data-stu-id="e5991-119">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




