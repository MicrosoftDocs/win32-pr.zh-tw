---
title: 處理視圖變更
description: 說明如何更新提供者備份存放區的用戶端視圖。
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 1d5a709752f92b7449d2ccc38f67c4417edf8d62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023595"
---
# <a name="handling-view-changes"></a>處理視圖變更

當虛擬化根下的檔案和目錄開啟時，提供者會在磁片上建立預留位置，而在讀取檔案時，會以內容水合預留位置。  這些預留位置代表建立時備份存放區的狀態。  這些快取的專案（結合提供者在列舉中所投射的專案）會構成用戶端的備份存放區「視圖」。  有時，提供者可能會想要更新用戶端的觀點，不論是因為備份存放區中的變更，或是使用者用來變更其觀點的明確動作。

> 如果提供者會主動更新視圖，則在備份存放區變更時，建議您最好不要讓 view 變更變得相當罕見。  這是因為對已開啟之專案的視圖變更，因此在磁片上建立了一個預留位置，需要更新或刪除磁片上的專案，以反映視圖變更。  頻繁的更新可能會導致額外的磁片活動，可能會對系統效能造成負面影響。

## <a name="item-versioning"></a>專案版本設定

為了支援維護多個視圖，ProjFS 提供 **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** 結構。  提供者會在對 **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** 的呼叫中獨立使用這個結構，並將它內嵌在 **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** 和 **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** 結構中。  **PRJ_PLACEHOLDER_VERSION_INFO**。ContentID 欄位是提供者為檔案或目錄儲存最多128個位元組版本資訊的位置。  然後，提供者可能會在內部將此值與識別特定視圖的某個值產生關聯。

例如，虛擬化原始檔控制存放庫的提供者可能會選擇使用檔案內容的雜湊做為 ContentID，而且可能會使用時間戳來識別儲存機制在不同時間點的觀點。  時間戳記可能是對存放庫執行認可的時間。

使用時間戳索引存放庫的範例，使用專案 ContentID 的一般流程可能是：

1. 用戶端會指定要顯示存放庫內容的時間戳記，藉以建立一個視圖。  這會透過提供者所執行的部分介面來完成，而不是透過 ProjFS API。  例如，提供者可能會有命令列工具，可用來告訴提供者要查看使用者的需求。
1. 當用戶端建立虛擬化檔案或目錄的控制碼時，提供者會使用來自備份存放區的檔案系統中繼資料，為其建立預留位置。  它所使用的一組特定中繼資料是由與所需視圖的時間戳記相關聯的 ContentID 值所識別。  當提供者呼叫 **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** 來寫入預留位置資訊時，它會在 _placeholderInfo_ 引數的 VersionInfo 成員中提供 ContentID。  接著，提供者應該記錄在此視圖中建立該檔案或目錄的預留位置。
1. 當用戶端從預留位置讀取時，會叫用提供者的 **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** 回呼。  _CallbackData_ 參數的 VersionInfo 成員會包含 ContentID 在建立檔案預留位置時指定于 **PrjWritePlaceholderInfo** 中的提供者。  提供者會使用該 ContentID 從其備份存放區取出檔案的正確內容。
1. 用戶端藉由指定新的時間戳記來要求視圖變更。  對於提供者在上一個視圖中建立的每個預留位置，如果新的視圖中有不同版本的檔案，提供者可能會將磁片上的預留位置取代為已更新的檔案，其 ContentID 會藉由呼叫 **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)** 與新的時間戳記相關聯。  此外，提供者也可以藉由呼叫 **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** 來刪除預留位置，以便將檔案的新觀點投射在列舉中。  如果檔案不存在於新的視圖中，則提供者必須藉由呼叫 **PrjDeleteFile** 來刪除它。

請注意，提供者必須確定當用戶端列舉目錄時，提供者會提供對應至用戶端視圖的內容。  例如，提供者可以使用 **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** 之 _CallbackData_ 參數的 VersionInfo 成員，並且 **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** 回呼來即時取出目錄內容。  或者，它也可以在建立視圖的過程中，在其備份存放區中建立該視圖的目錄結構，然後直接列舉該結構。

> 每當針對預留位置或部分檔案叫用提供者回呼時，在回呼的 _callbackData_ 參數的 VersionInfo 成員中，就會提供提供者在建立專案時所指定的版本資訊。

## <a name="updating-the-view"></a>更新視圖

以下範例函式說明當使用者指定新的時間戳記時，提供者可能會如何更新本機視圖。  此函式會針對使用者剛變更的視圖，取得提供者所建立的預留位置清單，並根據新視圖中的每個預留位置狀態來更新本機快取狀態。  為了清楚起見，此常式會忽略處理檔案系統的特定複雜性。  例如，在舊的視圖中，指定的目錄可能已存在，其中有些檔案或目錄，但在新的視圖中，目錄 (及其內容) 可能已不存在。  為了避免發生這種情況的錯誤，提供者應該以深度優先的方式更新虛擬根目錄底下的檔案和目錄的狀態。

```C++
typedef struct MY_ON_DISK_PLACEHOLDER MY_ON_DISK_PLACEHOLDER;

typedef struct MY_ON_DISK_PLACEHOLDER {
    MY_ON_DISK_PLACEHOLDER* Next;
    PWSTR RelativePath;
} MY_ON_DISK_PLACEHOLDER;

HRESULT
MyViewUpdater(
    _In_ PRJ_CALLBACK_DATA callbackData,
    _In_ time_t newViewTime
    )
{
    HRESULT hr = S_OK;

    // MyGetOnDiskPlaceholders is a routine the provider might implement to produce
    // a pointer to a list of the placeholders the provider has created in the view.
    MY_ON_DISK_PLACEHOLDER* placeholder = MyGetOnDiskPlaceholders();
    while (placeholder != NULL)
    {
        // MyGetProjectedFileInfo is a routine the provider might implement to
        // determine whether a given file exists in its backing store at a
        // particular timestamp.  If it does, the routine returns a pointer to
        // a PRJ_PLACEHOLDER_INFO struct populated with information about the
        // file.
        PRJ_PLACEHOLDER_INFO* newViewPlaceholderInfo = NULL;
        UINT32 newViewPlaceholderInfoSize = 0;

        newViewPlaceholderInfo = MyGetProjectedFileInfo(placeholder->RelativePath,
                                                 newViewTime,
                                                 &newViewPlaceholderInfoSize);
        if (newViewPlaceholderInfo == NULL)
        {
            // The file no longer exists in the new view.  We want to remove its
            // placeholder from the local cache.
            PRJ_UPDATE_FAILURE_CAUSES deleteFailureReason;
            hr = PrjDeleteFile(callbackData->NamespaceVirtualizationContext,
                               placeholder->RelativePath,
                               PRJ_UPDATE_ALLOW_DIRTY_METADATA
                               | PRJ_UPDATE_ALLOW_DIRTY_DATA
                               | PRJ_UPDATE_ALLOW_TOMBSTONE,
                               &deleteFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not delete [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", deleteFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error deleting [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyRemovePlaceholderData is a routine the provider might implement
            // to remove an item from its list of placeholders it has created in
            // the view.
            MyRemovePlaceholderData(placeholder);
        }
        else
        {
            // The file exists in the new view.  Its local cache state may need
            // to be updated, for example if its content is different in this view.
            // As an optimization, the provider may compare the file's ContentID
            // in the new view (stored in newViewPlaceholderInfo->ContentId) with
            // the ContentID it had in the old view.  If they are the same, calling
            // PrjUpdateFileIfNeeded would not be needed.
            PRJ_UPDATE_FAILURE_CAUSES updateFailureReason;
            hr = PrjUpdateFileIfNeeded(callbackData->NamespaceVirtualizationContext,
                                       placeholder->RelativePath,
                                       newViewPlaceholderInfo,
                                       newViewPlaceholderInfoSize,
                                       PRJ_UPDATE_ALLOW_DIRTY_METADATA
                                       | PRJ_UPDATE_ALLOW_DIRTY_DATA
                                       | PRJ_UPDATE_ALLOW_TOMBSTONE,
                                       &updateFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not update [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", updateFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error updating [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyUpdatePlaceholderData is a routine the provider might implement
            // to update information about a placeholder it has created in the view.
            MyUpdatePlaceholderData(placeholder, newViewPlaceholderInfo);
        }

        placeholder = placeholder->Next;
    }

    return hr;
}
```