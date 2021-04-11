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
# <a name="handling-view-changes"></a><span data-ttu-id="64281-103">處理視圖變更</span><span class="sxs-lookup"><span data-stu-id="64281-103">Handling View Changes</span></span>

<span data-ttu-id="64281-104">當虛擬化根下的檔案和目錄開啟時，提供者會在磁片上建立預留位置，而在讀取檔案時，會以內容水合預留位置。</span><span class="sxs-lookup"><span data-stu-id="64281-104">As files and directories under the virtualization root are opened, the provider creates placeholders on disk, and as files are read the placeholders are hydrated with contents.</span></span>  <span data-ttu-id="64281-105">這些預留位置代表建立時備份存放區的狀態。</span><span class="sxs-lookup"><span data-stu-id="64281-105">These placeholders represent the state of the backing store at the time they were created.</span></span>  <span data-ttu-id="64281-106">這些快取的專案（結合提供者在列舉中所投射的專案）會構成用戶端的備份存放區「視圖」。</span><span class="sxs-lookup"><span data-stu-id="64281-106">These cached items, combined with the items projected by the provider in enumerations, constitute the client's "view" of the backing store.</span></span>  <span data-ttu-id="64281-107">有時，提供者可能會想要更新用戶端的觀點，不論是因為備份存放區中的變更，或是使用者用來變更其觀點的明確動作。</span><span class="sxs-lookup"><span data-stu-id="64281-107">From time to time the provider may wish to update the client's view, whether because of changes in the backing store, or because of explicit action taken by the user to change their view.</span></span>

> <span data-ttu-id="64281-108">如果提供者會主動更新視圖，則在備份存放區變更時，建議您最好不要讓 view 變更變得相當罕見。</span><span class="sxs-lookup"><span data-stu-id="64281-108">If the provider updates the view proactively, as the backing store changes, it is recommended that view changes be relatively infrequent.</span></span>  <span data-ttu-id="64281-109">這是因為對已開啟之專案的視圖變更，因此在磁片上建立了一個預留位置，需要更新或刪除磁片上的專案，以反映視圖變更。</span><span class="sxs-lookup"><span data-stu-id="64281-109">This is because a view change to an item that has been opened, and therefore had a placeholder created on disk, requires that the on-disk item be either updated or deleted to reflect the view change.</span></span>  <span data-ttu-id="64281-110">頻繁的更新可能會導致額外的磁片活動，可能會對系統效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="64281-110">Frequent updates may result in extra disk activity that can negatively impact system performance.</span></span>

## <a name="item-versioning"></a><span data-ttu-id="64281-111">專案版本設定</span><span class="sxs-lookup"><span data-stu-id="64281-111">Item Versioning</span></span>

<span data-ttu-id="64281-112">為了支援維護多個視圖，ProjFS 提供 **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** 結構。</span><span class="sxs-lookup"><span data-stu-id="64281-112">To support maintaining multiple views, ProjFS provides the **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.</span></span>  <span data-ttu-id="64281-113">提供者會在對 **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** 的呼叫中獨立使用這個結構，並將它內嵌在 **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** 和 **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** 結構中。</span><span class="sxs-lookup"><span data-stu-id="64281-113">A provider uses this struct standalone in calls to **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)**, and it is embedded in the **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** and **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** structs.</span></span>  <span data-ttu-id="64281-114">**PRJ_PLACEHOLDER_VERSION_INFO**。ContentID 欄位是提供者為檔案或目錄儲存最多128個位元組版本資訊的位置。</span><span class="sxs-lookup"><span data-stu-id="64281-114">The **PRJ_PLACEHOLDER_VERSION_INFO**.ContentID field is where the provider stores up to 128 bytes of version information for a file or directory.</span></span>  <span data-ttu-id="64281-115">然後，提供者可能會在內部將此值與識別特定視圖的某個值產生關聯。</span><span class="sxs-lookup"><span data-stu-id="64281-115">The provider may then internally associate this value to some value that identifies a particular view.</span></span>

<span data-ttu-id="64281-116">例如，虛擬化原始檔控制存放庫的提供者可能會選擇使用檔案內容的雜湊做為 ContentID，而且可能會使用時間戳來識別儲存機制在不同時間點的觀點。</span><span class="sxs-lookup"><span data-stu-id="64281-116">For example, a provider that virtualizes a source control repository might choose to use a hash of a file's contents to serve as the ContentID, and it might use timestamps to identify views of the repository at various points in time.</span></span>  <span data-ttu-id="64281-117">時間戳記可能是對存放庫執行認可的時間。</span><span class="sxs-lookup"><span data-stu-id="64281-117">The timestamps might be the times that commits to the repository were performed.</span></span>

<span data-ttu-id="64281-118">使用時間戳索引存放庫的範例，使用專案 ContentID 的一般流程可能是：</span><span class="sxs-lookup"><span data-stu-id="64281-118">Using the example of a timestamp-indexed repository, a typical flow for using an item's ContentID might be:</span></span>

1. <span data-ttu-id="64281-119">用戶端會指定要顯示存放庫內容的時間戳記，藉以建立一個視圖。</span><span class="sxs-lookup"><span data-stu-id="64281-119">The client establishes a view by specifying the timestamp at which to present the repository contents.</span></span>  <span data-ttu-id="64281-120">這會透過提供者所執行的部分介面來完成，而不是透過 ProjFS API。</span><span class="sxs-lookup"><span data-stu-id="64281-120">This would be done through some interface implemented by the provider, not via a ProjFS API.</span></span>  <span data-ttu-id="64281-121">例如，提供者可能會有命令列工具，可用來告訴提供者要查看使用者的需求。</span><span class="sxs-lookup"><span data-stu-id="64281-121">For example, the provider may have a command-line tool that could be used to tell the provider which view the user desires.</span></span>
1. <span data-ttu-id="64281-122">當用戶端建立虛擬化檔案或目錄的控制碼時，提供者會使用來自備份存放區的檔案系統中繼資料，為其建立預留位置。</span><span class="sxs-lookup"><span data-stu-id="64281-122">When the client creates a handle to a virtualized file or directory, the provider creates a placeholder for it, using file system metadata from the backing store.</span></span>  <span data-ttu-id="64281-123">它所使用的一組特定中繼資料是由與所需視圖的時間戳記相關聯的 ContentID 值所識別。</span><span class="sxs-lookup"><span data-stu-id="64281-123">The particular set of metadata it uses is identified by the ContentID value associated with the timestamp of the desired view.</span></span>  <span data-ttu-id="64281-124">當提供者呼叫 **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** 來寫入預留位置資訊時，它會在 _placeholderInfo_ 引數的 VersionInfo 成員中提供 ContentID。</span><span class="sxs-lookup"><span data-stu-id="64281-124">When the provider calls **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to write the placeholder information, it supplies the ContentID in the VersionInfo member of the _placeholderInfo_ argument.</span></span>  <span data-ttu-id="64281-125">接著，提供者應該記錄在此視圖中建立該檔案或目錄的預留位置。</span><span class="sxs-lookup"><span data-stu-id="64281-125">The provider should then record that a placeholder for that file or directory was created in this view.</span></span>
1. <span data-ttu-id="64281-126">當用戶端從預留位置讀取時，會叫用提供者的 **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** 回呼。</span><span class="sxs-lookup"><span data-stu-id="64281-126">When the client reads from a placeholder, the provider's **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback is invoked.</span></span>  <span data-ttu-id="64281-127">_CallbackData_ 參數的 VersionInfo 成員會包含 ContentID 在建立檔案預留位置時指定于 **PrjWritePlaceholderInfo** 中的提供者。</span><span class="sxs-lookup"><span data-stu-id="64281-127">The _callbackData_ parameter's VersionInfo member contains the ContentID the provider specified in **PrjWritePlaceholderInfo** when it created the file placeholder.</span></span>  <span data-ttu-id="64281-128">提供者會使用該 ContentID 從其備份存放區取出檔案的正確內容。</span><span class="sxs-lookup"><span data-stu-id="64281-128">The provider uses that ContentID to retrieve the correct contents of the file from its backing store.</span></span>
1. <span data-ttu-id="64281-129">用戶端藉由指定新的時間戳記來要求視圖變更。</span><span class="sxs-lookup"><span data-stu-id="64281-129">The client requests a view change by specifying a new timestamp.</span></span>  <span data-ttu-id="64281-130">對於提供者在上一個視圖中建立的每個預留位置，如果新的視圖中有不同版本的檔案，提供者可能會將磁片上的預留位置取代為已更新的檔案，其 ContentID 會藉由呼叫 **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)** 與新的時間戳記相關聯。</span><span class="sxs-lookup"><span data-stu-id="64281-130">For each placeholder the provider created in the previous view, if a different version of that file exists in the new view the provider may replace the placeholder on disk with an updated one whose ContentID is associated with the new timestamp by calling **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span></span>  <span data-ttu-id="64281-131">此外，提供者也可以藉由呼叫 **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** 來刪除預留位置，以便將檔案的新觀點投射在列舉中。</span><span class="sxs-lookup"><span data-stu-id="64281-131">Alternatively, the provider may delete the placeholder by calling **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** so that the new view of the file will be projected in enumerations.</span></span>  <span data-ttu-id="64281-132">如果檔案不存在於新的視圖中，則提供者必須藉由呼叫 **PrjDeleteFile** 來刪除它。</span><span class="sxs-lookup"><span data-stu-id="64281-132">If the file does not exist in the new view, the provider must delete it by calling **PrjDeleteFile**.</span></span>

<span data-ttu-id="64281-133">請注意，提供者必須確定當用戶端列舉目錄時，提供者會提供對應至用戶端視圖的內容。</span><span class="sxs-lookup"><span data-stu-id="64281-133">Note that the provider must ensure that when the client enumerates a directory, the provider will supply the contents that correspond to the client's view.</span></span>  <span data-ttu-id="64281-134">例如，提供者可以使用 **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** 之 _CallbackData_ 參數的 VersionInfo 成員，並且 **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** 回呼來即時取出目錄內容。</span><span class="sxs-lookup"><span data-stu-id="64281-134">For example, the provider could use the VersionInfo member of the _callbackData_ parameter of the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** and **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** callbacks to retrieve directory contents on the fly.</span></span>  <span data-ttu-id="64281-135">或者，它也可以在建立視圖的過程中，在其備份存放區中建立該視圖的目錄結構，然後直接列舉該結構。</span><span class="sxs-lookup"><span data-stu-id="64281-135">Alternatively it could build a directory structure for that view in its backing store as part of establishing the view, and then simply enumerate that structure.</span></span>

> <span data-ttu-id="64281-136">每當針對預留位置或部分檔案叫用提供者回呼時，在回呼的 _callbackData_ 參數的 VersionInfo 成員中，就會提供提供者在建立專案時所指定的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="64281-136">Whenever a provider callback is invoked for a placeholder or partial file, the version information the provider specified when creating the item is provided in the VersionInfo member of the callback's _callbackData_ parameter.</span></span>

## <a name="updating-the-view"></a><span data-ttu-id="64281-137">更新視圖</span><span class="sxs-lookup"><span data-stu-id="64281-137">Updating the View</span></span>

<span data-ttu-id="64281-138">以下範例函式說明當使用者指定新的時間戳記時，提供者可能會如何更新本機視圖。</span><span class="sxs-lookup"><span data-stu-id="64281-138">Below is a sample function illustrating how a provider might update the local view when the user specifies a new timestamp.</span></span>  <span data-ttu-id="64281-139">此函式會針對使用者剛變更的視圖，取得提供者所建立的預留位置清單，並根據新視圖中的每個預留位置狀態來更新本機快取狀態。</span><span class="sxs-lookup"><span data-stu-id="64281-139">The function retrieves a list of the placeholders the provider created for the view the user has just changed from, and updates the local cache state based on each placeholder's state in the new view.</span></span>  <span data-ttu-id="64281-140">為了清楚起見，此常式會忽略處理檔案系統的特定複雜性。</span><span class="sxs-lookup"><span data-stu-id="64281-140">For clarity, this routine omits certain complexities of dealing with the file system.</span></span>  <span data-ttu-id="64281-141">例如，在舊的視圖中，指定的目錄可能已存在，其中有些檔案或目錄，但在新的視圖中，目錄 (及其內容) 可能已不存在。</span><span class="sxs-lookup"><span data-stu-id="64281-141">For example, in the old view a given directory may have existed with some files or directories in it, but in the new view that directory (and its contents) may no longer exist.</span></span>  <span data-ttu-id="64281-142">為了避免發生這種情況的錯誤，提供者應該以深度優先的方式更新虛擬根目錄底下的檔案和目錄的狀態。</span><span class="sxs-lookup"><span data-stu-id="64281-142">To avoid encountering errors in such a situation the provider should update the state of the file and directories beneath the virtualization root in a depth-first fashion.</span></span>

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