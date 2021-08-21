---
title: 提供檔案資料
description: 描述提供者如何提供預留位置資訊和檔案資料。
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 4f0da65095e908ec3211bb23be654ee9e0e2853c093bb36e8a92701c24106ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792392"
---
# <a name="providing-file-data"></a>提供檔案資料

當提供者先建立虛擬化根時，本機系統上就會是空的。 也就是說，支援資料存放區中的所有專案都尚未快取到磁片。 當專案開啟時，ProjFS 會向提供者要求資訊，以允許在本機檔案系統中建立這些專案的預留位置。  存取專案內容時，ProjFS 會向提供者要求這些內容。  結果是，從使用者的觀點來看，虛擬化的檔案和目錄看起來類似于一般檔案和目錄，而這些檔案和目錄已存在於本機檔案系統上。

## <a name="placeholder-creation"></a>建立預留位置

當應用程式嘗試開啟虛擬化檔案的控制碼時，ProjFS 會針對每個尚未存在於磁片上的路徑專案呼叫 **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** 回呼。  例如，如果應用程式嘗試開啟 `C:\virtRoot\dir1\dir2\file.txt` ，但 `C:\virtRoot\dir1` 磁片上只有路徑存在，則提供者會接收的回呼 `C:\virtRoot\dir1\dir2` ，然後針對 `C:\virtRoot\dir1\dir2\file.txt` 。

當 ProjFS 呼叫提供者的 **PRJ_GET_PLACEHOLDER_INFO_CB** 回呼時，提供者會執行下列動作：

1. 提供者會判斷要求的名稱是否存在於其備份存放區中。  在搜尋備份存放區時，提供者應該使用 **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** 做為比較常式，以判斷所要求的名稱是否存在於備份存放區中。  如果不是，提供者會從回呼傳回 HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) 。

1. 如果要求的名稱存在於備份存放區中，則提供者會以該專案的檔案系統中繼資料填入 [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) 結構，並呼叫 **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** 將資料傳送至 ProjFS。  ProjFS 會使用該資訊在本機檔案系統中為專案建立預留位置。

    > ProjFS 會使用任何 FILE_ATTRIBUTE 旗標的 **FileBasicInfo FileAttributes** PRJ_PLACEHOLDER_INFO 成員中的提供者集合，但 FILE_ATTRIBUTE_DIRECTORY 除外;它會根據所提供的 **FileBasicInfo IsDirectory** 成員值，為 **FileBasicInfo. FileAttributes** 成員中的 FILE_ATTRIBUTE_DIRECTORY 設定正確的值。

    > 如果支援存放區支援符號連結，則提供者必須使用 **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** 將預留位置資料傳送至 ProjFS。  **PrjWritePlaceholderInfo2** 支援額外的緩衝區輸入，可讓提供者指定預留位置是符號連結和其目標。  否則， **PrjWritePlaceholderInfo** 會如上面所述運作。  下列範例說明如何使用 **PrjWritePlaceholderInfo2** 來提供符號連結的支援。
    >
    > 請注意，Windows 10 2004 版才支援 **PrjWritePlaceholderInfo2** 。  提供者應該探查是否存在 **PrjWritePlaceholderInfo2**，例如使用 **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**。

```C++
HRESULT
MyGetPlaceholderInfoCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
    )
{
    // MyGetItemInfo is a routine the provider might implement to get
    // information from its backing store for a given file path.  The first
    // parameter is an _In_ parameter that supplies the name to look for.
    // If the item exists the routine provides the file information in the
    // remaining parameters, all of which are annotated _Out_:
    // * 2nd parameter: the name as it appears in the backing store
    // * 3rd-9th parameters: basic file info
    // * 10th parameter: if the item is a symbolic link, a pointer to a 
    //   NULL-terminated string identifying the link's target
    //
    // Note that the routine returns the name that is in the backing
    // store.  This is because the input file path may not be in the same
    // case as what is in the backing store.  The provider should create
    // the placeholder with the name it has in the backing store.
    //
    // Note also that this example does not provide anything beyond basic
    // file information and a possible symbolic link target.
    HRESULT hr;
    WCHAR* backingStoreName = NULL;
    WCHAR* symlinkTarget = NULL;
    PRJ_PLACEHOLDER_INFO placeholderInfo = {};
    hr = MyGetItemInfo(callbackData->FilePathName,
                       &backingStoreName,
                       &placeholderInfo.FileBasicInfo.IsDirectory,
                       &placeholderInfo.FileBasicInfo.FileSize,
                       &placeholderInfo.FileBasicInfo.CreationTime,
                       &placeholderInfo.FileBasicInfo.LastAccessTime,
                       &placeholderInfo.FileBasicInfo.LastWriteTime,
                       &placeholderInfo.FileBasicInfo.ChangeTime,
                       &placeholderInfo.FileBasicInfo.FileAttributes,
                       &symlinkTarget);

    if (FAILED(hr))
    {
        // If callbackData->FilePathName doesn't exist in our backing store then
        // MyGetItemInfo should HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND).
        // If this is some other error, e.g. E_OUTOFMEMORY because MyGetItemInfo
        // couldn't allocate space for backingStoreName, we return that.
        return hr;
    }

    // If the file path is for a symbolic link, pass that in with the placeholder info.
    if (symlinkTarget != NULL)
    {
        PRJ_EXTENDED_INFO extraInfo = {};

        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
        extraInfo.Symlink.TargetName = symlinkTarget;

        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo2(callbackData->NamespaceVirtualizationContext,
                                      backingStoreName,
                                      &placeholderInfo,
                                      sizeof(placeholderInfo),
                                      &extraInfo);
    }
    else
    {
        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo(callbackData->NamespaceVirtualizationContext,
                                     backingStoreName,
                                     &placeholderInfo,
                                     sizeof(placeholderInfo));
    }

    free(backingStoreName);

    if (symlinkTarget != NULL)
    {
        free(symlinkTarget);
    }

    return hr;
}
```

## <a name="providing-file-contents"></a>提供檔案內容

當 ProjFS 需要確保虛擬檔案包含資料時，例如當應用程式嘗試從檔案讀取時，ProjFS 會呼叫該專案的 **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** 回呼，要求提供者提供檔案的內容。  此提供者會從其備份存放區抓取檔案的資料，並使用 **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** 將資料傳送至本機檔案系統。

> 當 ProjFS 呼叫此回呼時， _callbackData_ 參數的 **FilePathName** 成員會在其預留位置建立時提供檔案的名稱。  亦即，如果檔案在建立後已重新命名，則回呼會提供原始 (預先重新命名) 名稱，而非目前的 (後重新命名) 名稱。  如有必要，提供者可以使用 _callbackData_ 參數的 **VersionInfo** 成員來判斷所要求的檔案資料。
>
> 如需有關如何使用 PRJ_CALLBACK_DATA **VersionInfo** 成員的詳細資訊，請參閱 [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) 的檔和 [處理視圖變更](handling-view-changes.md) 主題。

提供者可將 **PRJ_GET_FILE_DATA_CB** 回呼中要求的資料範圍分割成多個 **PrjWriteFileData** 呼叫，每個呼叫都提供部分要求的範圍。  但是，提供者必須在完成回呼之前，提供整個要求的範圍。  例如，如果回呼要求 10 MB 的資料從 _byteOffset_ 0 （ _長度_ 為10485760），提供者可能會選擇提供10個 **PrjWriteFileData** 的資料，每個呼叫都傳送 1 MB。

提供者也可以自由提供超過所要求的範圍，最多可達檔案的長度。  提供者所提供的範圍必須涵蓋要求的範圍。  例如，如果回呼要求 _byteOffset_ 4096 的 1 MB 資料 _長度_ 為1052672，而檔案的總大小為 10 mb，則提供者可以選擇傳回 2 mb 的資料，從位移0開始。

### <a name="buffer-alignment-considerations"></a>緩衝區對齊考慮

ProjFS 會使用來自呼叫端的 [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) ，要求資料將資料寫入本機檔案系統。  但是，ProjFS 無法控制是否針對已緩衝或未緩衝處理的 i/o 開啟 FILE_OBJECT。  如果 FILE_OBJECT 是針對未緩衝的 i/o 開啟，檔案的讀取和寫入必須遵守特定的對齊需求。  提供者可以執行下列兩項作業，以符合這些對齊需求：

1. 使用 **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** 來配置要傳入 **PrjWriteFileData** 之 _緩衝區_ 參數的緩衝區。
1. 確定 **PrjWriteFileData** 的 _byteOffset_ 和 _length_ 參數是儲存體裝置對齊需求的整數倍數 (請注意，如果 _byteOffset_   +  _長度_ 等於檔) 的結尾，則長度參數不需要符合這項需求。  提供者可以使用 **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** 來取得儲存體裝置的對齊需求。

ProjFS 會將其保留給提供者，以計算適當的對齊方式。  這是因為在處理 **PRJ_GET_FILE_DATA_CB** 回呼時，提供者可能會選擇在多個 **PrjWriteFileData** 呼叫之間傳回要求的資料，每個呼叫都會在完成回呼之前傳回要求的總數據部分。

> 如果提供者要使用 **PrjWriteFileData** 的單一呼叫來寫入整個檔案，也就是從 _byteOffset_ = 0 到 _length_ = 檔案的大小，或傳回 **PRJ_GET_FILE_DATA_CB** 回呼中要求的確切範圍，則提供者不需要執行任何對齊計算。  不過，它仍然必須使用 **PrjAllocateAlignedBuffer** ，以確保 _緩衝區_ 符合存放裝置的對齊需求。

如需有關緩衝處理與未緩衝 i/o 的詳細資訊，請參閱檔案 [緩衝](/windows/desktop/FileIO/file-buffering) 處理主題。

```C++
//  BlockAlignTruncate(): Aligns P on the previous V boundary (V must be != 0).
#define BlockAlignTruncate(P,V) ((P) & (0-((UINT64)(V))))

// This sample illustrates both returning the entire requested range in a
// single call to PrjWriteFileData(), and splitting it up into smaller 
// units.  Note that the provider must return all the requested data before
// completing the PRJ_GET_FILE_DATA_CB callback with S_OK.
HRESULT
MyGetFileDataCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ UINT64 byteOffset,
    _In_ UINT32 length
    )
{
    HRESULT hr;

    // For the purposes of this sample our provider has a 1 MB limit to how
    // much data it can return at once (perhaps its backing store imposes such
    // a limit).
    UINT64 writeStartOffset;
    UINT32 writeLength;
    if (length <= 1024*1024)
    {
        // The range requested in the callback is less than 1MB, so we can return
        // the data in a single call, without doing any alignment calculations.
        writeStartOffset = byteOffset;
        writeLength = length;
    }
    else
    {
        // The range requested is more than 1MB.  Retrieve the device alignment
        // and calculate a transfer size that conforms to the device alignment and
        // is <= 1MB.
        PRJ_VIRTUALIZATION_INSTANCE_INFO instanceInfo;
        UINT32 infoSize = sizeof(instanceInfo);
        hr = PrjGetVirtualizationInstanceInfo(callbackData->NamespaceVirtualizationContext,
                                              &infoSize,
                                              &instanceInfo);

        if (FAILED(hr))
        {
            return hr;
        }

        // The first transfer will start at the beginning of the requested range,
        // which is guaranteed to have the correct alignment.
        writeStartOffset = byteOffset;

        // Ensure our transfer size is aligned to the device alignment, and is
        // no larger than 1 MB (note this assumes the device alignment is less
        // than 1 MB).
        UINT64 writeEndOffset = BlockAlignTruncate(writeStartOffset + 1024*1024,
                                                   instanceInfo->WriteAlignment);
        assert(writeEndOffset > 0);
        assert(writeEndOffset > writeStartOffset);

        writeLength = writeEndOffset - writeStartOffset;
    }

    // Allocate a buffer that adheres to the needed memory alignment.
    void* writeBuffer = NULL;
    writeBuffer = PrjAllocateAlignedBuffer(callbackData->NamespaceVirtualizationContext,
                                           writeLength);

    if (writeBuffer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    do
    {
        // MyGetFileDataFromStore is a routine the provider might implement to copy
        // data for the specified file from the provider's backing store to a
        // buffer.  The routine finds the file located at callbackData->FilePathName
        // and copies writeLength bytes of its data, starting at writeStartOffset,
        // to the buffer pointed to by writeBuffer.
        hr = MyGetFileDataFromStore(callbackData->FilePathName,
                                    writeStartOffset,
                                    writeLength,
                                    writeBuffer);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // Write the data to the file in the local file system.
        hr = PrjWriteFileData(callbackData->NamespaceVirtualizationContext,
                              callbackData->DataStreamId,
                              writeBuffer,
                              writeStartOffset,
                              writeLength);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // The length parameter to the callback is guaranteed to be either
        // correctly aligned or to result in a write to the end of the file.
        length -= writeLength;
        if (length < writeLength)
        {
            writeLength = length;
        }
    }
    while (writeLength > 0);

    PrjFreeAlignedBuffer(writeBuffer);
    return hr;
}
```