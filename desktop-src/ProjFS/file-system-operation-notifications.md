---
title: 檔案系統作業通知
description: 描述提供者如何接收檔案系統作業的通知。
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 9eae9bde6d56592f371dcd48c24fef96a9eecbdf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682484"
---
# <a name="file-system-operation-notifications"></a><span data-ttu-id="690d4-103">檔案系統作業通知</span><span class="sxs-lookup"><span data-stu-id="690d4-103">File System Operation Notifications</span></span>

<span data-ttu-id="690d4-104">除了處理列舉、傳回檔案中繼資料和檔案內容的必要回呼之外，提供者可以選擇性地在呼叫 **[PrjStartVirtualizing]()** 時註冊 **[PRJ_NOTIFICATION_CB]()** 回呼。</span><span class="sxs-lookup"><span data-stu-id="690d4-104">In addition to required callbacks for handling enumeration, returning file metadata, and file contents, a provider may optionally register a **[PRJ_NOTIFICATION_CB]()** callback in its call to **[PrjStartVirtualizing]()**.</span></span>  <span data-ttu-id="690d4-105">此回呼會接收在實例虛擬化根下的檔案和目錄上所執行檔案系統作業的通知。</span><span class="sxs-lookup"><span data-stu-id="690d4-105">This callback receives notifications of file system operations performed on files and directories beneath the instance's virtualization root.</span></span>  <span data-ttu-id="690d4-106">某些通知是「作業後」通知，告訴提供者作業剛剛完成。</span><span class="sxs-lookup"><span data-stu-id="690d4-106">Some of the notifications are "post-operation" notifications, which tell the provider that an operation has just completed.</span></span>  <span data-ttu-id="690d4-107">其他通知是「前置作業」通知，表示提供者會在作業發生之前收到通知。</span><span class="sxs-lookup"><span data-stu-id="690d4-107">The other notifications are "pre-operation" notifications, meaning that the provider is notified before the operation happens.</span></span>  <span data-ttu-id="690d4-108">在前置操作通知中，提供者可以從回呼傳回錯誤碼，以防止作業。</span><span class="sxs-lookup"><span data-stu-id="690d4-108">In a pre-operation notification the provider can veto the operation by returning an error code from the callback.</span></span>  <span data-ttu-id="690d4-109">這會導致作業失敗，並傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="690d4-109">This causes the operation to fail with the returned error code.</span></span>

## <a name="how-to-specify-notifications-to-receive"></a><span data-ttu-id="690d4-110">如何指定要接收的通知</span><span class="sxs-lookup"><span data-stu-id="690d4-110">How to Specify Notifications to Receive</span></span>

<span data-ttu-id="690d4-111">如果提供者在啟動虛擬化實例時提供了 **PRJ_NOTIFICATION_CB** 的執行，則也應該指定要接收的通知。</span><span class="sxs-lookup"><span data-stu-id="690d4-111">If the provider supplies an implementation of **PRJ_NOTIFICATION_CB** when it starts a virtualization instance, it should also specify which notifications it wishes to receive.</span></span>  <span data-ttu-id="690d4-112">提供者可註冊的通知會定義在 [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="690d4-112">The notifications for which the provider can register are defined in the [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) enum.</span></span>

<span data-ttu-id="690d4-113">當提供者指定要接收的通知時，它會使用一或多個 [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) 結構的陣列來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="690d4-113">When the provider specifies the notifications it wishes to receive, it does so using an array of one or more [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) structures.</span></span>  <span data-ttu-id="690d4-114">這些會定義「通知對應」。</span><span class="sxs-lookup"><span data-stu-id="690d4-114">These define "notification mappings".</span></span>  <span data-ttu-id="690d4-115">通知對應是目錄（稱為「通知根目錄」）與一組通知（以位遮罩表示）之間的配對，ProjFS 應該傳送該目錄及其下階。</span><span class="sxs-lookup"><span data-stu-id="690d4-115">A notification mapping is a pairing between a directory, referred to as a "notification root", and a set of notifications, expressed as a bit mask, which ProjFS should send for that directory and its descendants.</span></span>  <span data-ttu-id="690d4-116">也可以建立單一檔案的通知對應。</span><span class="sxs-lookup"><span data-stu-id="690d4-116">A notification mapping can also be established for a single file.</span></span>  <span data-ttu-id="690d4-117">在通知對應中指定的檔案或目錄，在提供者呼叫 **PrjStartVirtualizing** 時不一定要存在，而提供者可以指定任何路徑，而且對應會在建立時套用。</span><span class="sxs-lookup"><span data-stu-id="690d4-117">A file or directory specified in a notification mapping does not have to exist already at the time the provider calls **PrjStartVirtualizing**, the provider can specify any path and the mapping will apply to it if it is ever created.</span></span>

<span data-ttu-id="690d4-118">如果提供者指定多個通知對應，而有些則是其他的子系，則必須以遞減的深度指定對應。</span><span class="sxs-lookup"><span data-stu-id="690d4-118">If the provider specifies multiple notification mappings, and some are descendants of others, the mappings must be specified in descending depth.</span></span>  <span data-ttu-id="690d4-119">較深層級的通知對應會覆寫其子系的較高層級。</span><span class="sxs-lookup"><span data-stu-id="690d4-119">Notification mappings at deeper levels override higher-level ones for their descendants.</span></span>

<span data-ttu-id="690d4-120">如果提供者未指定一組通知對應，ProjFS 會預設為將它 PRJ_NOTIFY_FILE_OPENED、PRJ_NOTIFY_NEW_FILE_CREATED 和 PRJ_NOTIFY_FILE_OVERWRITTEN 傳送給虛擬化根下的所有檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="690d4-120">If the provider does not specify a set of notification mappings, ProjFS will default to sending it PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED, and PRJ_NOTIFY_FILE_OVERWRITTEN for all files and directories beneath the virtualization root.</span></span>

<span data-ttu-id="690d4-121">下列程式碼片段說明如何在啟動虛擬化實例時註冊一組通知。</span><span class="sxs-lookup"><span data-stu-id="690d4-121">The following code snippet illustrates how to register a set of notifications when starting a virtualization instance.</span></span>

```C++
PRJ_CALLBACKS callbackTable;

// Supply required callbacks.
callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
callbackTable.GetFileDataCallback = MyGetFileDataCallback;

// The rest of the callbacks are optional.  We want notifications, so specify
// our notification callback.
callbackTable.QueryFileNameCallback = nullptr;
callbackTable.NotificationCallback = MyNotificationCallback;
callbackTable.CancelCommandCallback = nullptr;

// Assume the provider has created a new virtualization root at C:\VirtRoot and
// initialized it with this layout:
//
//     C:\VirtRoot
//     +--- baz
//     \--- foo
//          +--- subdir1
//          \--- subdir2
//
// The provider wants these notifications:
// * Notification of new file/directory creates for all locations within the
//   virtualization root that are not subject to one of the following more
//   specific notification mappings.
// * Notification of new file/directory creates, file opens, post-renames, and
//   pre- and post-deletes for C:\VirtRoot\foo
// * No notifications for C:\VirtRoot\foo\subdir1
PRJ_STARTVIRTUALIZING_OPTIONS startOpts = {};
PRJ_VIRTUALIZATION_MAPPING notificationMappings[3];

// Configure default notifications - notify of new files for most of the tree.
notificationMappings[0].NotificationRoot = L"";
notificationMappings[0].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED;

// Override default notifications - notify of new files, opened files, and file
// deletes for C:\VirtRoot\foo and its descendants.
notificationMappings[1].NotificationRoot = L"foo";
notificationMappings[1].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED |
                                              PRJ_NOTIFY_FILE_OPENED |
                                              PRJ_NOTIFY_PRE_DELETE |
                                              PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED |
                                              PRJ_NOTIFY_FILE_RENAMED;

// Override all notifications for C:\VirtRoot\foo\subdir1 and its descendants.
notificationMappings[2].NotificationRoot = L"foo\\subdir1";
notificationMappings[2].NotificationBitMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;

startOpts.NotificationMappings = notificationMappings;
startOpts.NotificationMappingsCount = ARRAYSIZE(notificationMapping);

// Start the instance and provide our notification mappings.
HRESULT hr;
PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
hr = PrjStartVirtualizing(rootName,
                          &callbackTable,
                          nullptr,
                          &startOpts,
                          &instanceHandle);
if (FAILED(hr))
{
    wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
    return;
}
```

## <a name="receiving-notifications"></a><span data-ttu-id="690d4-122">接收告知</span><span class="sxs-lookup"><span data-stu-id="690d4-122">Receiving Notifications</span></span>

<span data-ttu-id="690d4-123">ProjFS 藉由呼叫提供者的 **PRJ_NOTIFICATION_CB** 回呼來傳送檔案系統作業的通知。</span><span class="sxs-lookup"><span data-stu-id="690d4-123">ProjFS sends notifications of file system operations by calling the provider's **PRJ_NOTIFICATION_CB** callback.</span></span>  <span data-ttu-id="690d4-124">它會針對提供者所註冊的每個作業執行此動作。</span><span class="sxs-lookup"><span data-stu-id="690d4-124">It does this for each operation the provider has registered for.</span></span>  <span data-ttu-id="690d4-125">如果在上述範例中，已註冊 PRJ_NOTIFY_NEW_FILE_CREATED 的提供者 |PRJ_NOTIFY_FILE_OPENED |PRJ_NOTIFY_PRE_DELETE |PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED |PRJ_NOTIFY_FILE_RENAMED，而應用程式在通知根目錄中建立了新的檔案，則 ProjFS 會使用新檔案的路徑名稱和設定為 PRJ_NOTIFICATION_NEW_FILE_CREATED 的 _通知_ 參數，呼叫 **PRJ_NOTIFICATION_CB** 回呼。</span><span class="sxs-lookup"><span data-stu-id="690d4-125">If, as in the above example, the provider registered for PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, and an application created a new file in the notification root, ProjFS would call the **PRJ_NOTIFICATION_CB** callback with the new file's path name and the _notification_ parameter set to PRJ_NOTIFICATION_NEW_FILE_CREATED.</span></span>

<span data-ttu-id="690d4-126">ProjFS 會在相關聯的檔案系統作業發生之前，傳送下列清單中的通知。</span><span class="sxs-lookup"><span data-stu-id="690d4-126">ProjFS sends the notifications in the following list before the associated file system operation takes place.</span></span>  <span data-ttu-id="690d4-127">如果提供者從 **PRJ_NOTIFICATION_CB** 回呼傳回失敗碼，檔案系統作業將會失敗，並傳回提供者所指定的失敗碼。</span><span class="sxs-lookup"><span data-stu-id="690d4-127">If the provider returns a failure code from the **PRJ_NOTIFICATION_CB** callback, the file system operation will fail and return the failure code the provider specified.</span></span>

* <span data-ttu-id="690d4-128">PRJ_NOTIFICATION_PRE_DELETE-即將刪除此檔案。</span><span class="sxs-lookup"><span data-stu-id="690d4-128">PRJ_NOTIFICATION_PRE_DELETE - The file is about to be deleted.</span></span>
* <span data-ttu-id="690d4-129">PRJ_NOTIFICATION_PRE_RENAME-即將重新命名檔案。</span><span class="sxs-lookup"><span data-stu-id="690d4-129">PRJ_NOTIFICATION_PRE_RENAME - The file is about to be renamed.</span></span>
* <span data-ttu-id="690d4-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK-即將為檔案建立硬式連結。</span><span class="sxs-lookup"><span data-stu-id="690d4-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK - A hard link is about to be created for the file.</span></span>
* <span data-ttu-id="690d4-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL-即將將檔案從預留位置擴充至完整檔案，這表示可能會修改其內容。</span><span class="sxs-lookup"><span data-stu-id="690d4-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL - A file is about to be expanded from a placeholder to a full file, which indicates its contents are likely to be modified.</span></span>

<span data-ttu-id="690d4-132">ProjFS 會在相關聯的檔案系統作業完成之後，傳送下列清單中的通知。</span><span class="sxs-lookup"><span data-stu-id="690d4-132">ProjFS sends the notifications in the following list after the associated file system operation has completed.</span></span>

* <span data-ttu-id="690d4-133">PRJ_NOTIFICATION_FILE_OPENED-已開啟現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="690d4-133">PRJ_NOTIFICATION_FILE_OPENED - An existing file has been opened.</span></span>
  * <span data-ttu-id="690d4-134">雖然此通知是在檔案開啟之後傳送的，但提供者可能會傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="690d4-134">Even though this notification is sent after the file has been opened, the provider can return a failure code.</span></span>  <span data-ttu-id="690d4-135">在回應中，ProjFS 會取消開啟，並將失敗傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="690d4-135">In response, ProjFS will cancel the open and return the failure to the caller.</span></span>
* <span data-ttu-id="690d4-136">PRJ_NOTIFICATION_NEW_FILE_CREATED-已建立新的檔案。</span><span class="sxs-lookup"><span data-stu-id="690d4-136">PRJ_NOTIFICATION_NEW_FILE_CREATED - A new file has been created.</span></span>
* <span data-ttu-id="690d4-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN-已覆寫現有的檔案，例如藉由使用 **CREATE_ALWAYS** _dwCreationDisposition_ 旗標來呼叫 [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) 。</span><span class="sxs-lookup"><span data-stu-id="690d4-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN - An existing file has been overwritten, for example by calling [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) with the **CREATE_ALWAYS** _dwCreationDisposition_ flag.</span></span>
* <span data-ttu-id="690d4-138">PRJ_NOTIFICATION_FILE_RENAMED-已重新命名檔案。</span><span class="sxs-lookup"><span data-stu-id="690d4-138">PRJ_NOTIFICATION_FILE_RENAMED - A file has been renamed.</span></span>
* <span data-ttu-id="690d4-139">PRJ_NOTIFICATION_HARDLINK_CREATED-已建立檔案的 [硬式連結](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) 。</span><span class="sxs-lookup"><span data-stu-id="690d4-139">PRJ_NOTIFICATION_HARDLINK_CREATED - A [hard link](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) has been created for a file.</span></span>
* <span data-ttu-id="690d4-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION-檔案控制代碼已關閉，且檔案的內容未經過修改，也不會刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="690d4-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION - A file handle has been closed, and the file's content was not modified, nor was the file deleted.</span></span>
* <span data-ttu-id="690d4-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED-檔案控制代碼已關閉，且檔案的內容已修改。</span><span class="sxs-lookup"><span data-stu-id="690d4-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED - A file handle has been closed, and the file's content has been modified.</span></span>
* <span data-ttu-id="690d4-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED-檔案控制代碼已關閉，並在關閉控制碼的過程中刪除該檔案。</span><span class="sxs-lookup"><span data-stu-id="690d4-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED - A file handle has been closed, and the file was deleted as part of closing the handle.</span></span>

<span data-ttu-id="690d4-143">如需每個通知的詳細資訊，請參閱 **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)** 的檔。</span><span class="sxs-lookup"><span data-stu-id="690d4-143">For more details on each notification refer to the documentation for **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span></span>

<span data-ttu-id="690d4-144">**PRJ_NOTIFICATION_CB** 回呼的 _notificationParameters_ 參數會指定特定通知的額外參數。</span><span class="sxs-lookup"><span data-stu-id="690d4-144">The **PRJ_NOTIFICATION_CB** callback's _notificationParameters_ parameter specifies extra parameters for certain notifications.</span></span>  <span data-ttu-id="690d4-145">如果提供者收到 PRJ_NOTIFICATION_FILE_OPENED、PRJ_NOTIFICATION_NEW_FILE_CREATED 或 PRJ_NOTIFICATION_FILE_OVERWRITTEN，或 PRJ_NOTIFICATION_FILE_RENAMED 通知，提供者可以為檔案指定要接收的一組新通知。</span><span class="sxs-lookup"><span data-stu-id="690d4-145">If a provider receives a PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, or PRJ_NOTIFICATION_FILE_OVERWRITTEN, or PRJ_NOTIFICATION_FILE_RENAMED notification, the provider can specify a new set of notifications to receive for the file.</span></span> <span data-ttu-id="690d4-146">如需詳細資訊，請參閱 **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)** 的檔。</span><span class="sxs-lookup"><span data-stu-id="690d4-146">For further details, refer to the documentation for **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span></span>

<span data-ttu-id="690d4-147">下列範例會示範提供者如何處理在上述程式碼片段中註冊的通知的簡單範例。</span><span class="sxs-lookup"><span data-stu-id="690d4-147">The following sample shows simple examples of how a provider might process the notifications it registered for in the code snippet above.</span></span>

```C++
#include <windows.h>

HRESULT
MyNotificationCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ BOOLEAN isDirectory,
    _In_ PRJ_NOTIFICATION notification,
    _In_opt_z_ PCWSTR destinationFileName,
    _Inout_ PRJ_NOTIFICATION_PARAMETERS* operationParameters
    )
{
    HRESULT hr = S_OK;

    switch (notification)
    {
    case PRJ_NOTIFY_NEW_FILE_CREATED:

        wprintf(L"A new %ls was created at [%ls].\n",
                isDirectory ? L"directory" : L"file",
                callbackData->FilePathName);

        // Let's stop getting notifications inside newly-created directories.
        if (isDirectory)
        {
            operationParameters->PostCreate.NotificationMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;
        }
        break;

    case PRJ_NOTIFY_FILE_OPENED:

        wprintf(L"Handle opened to %ls [%ls].\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_PRE_DELETE:

        wprintf(L"Attempt to delete %ls [%ls]: ",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);

        // MyAllowDelete is a routine the provider might implement to decide
        // whether to allow a given file/directory to be deleted.
        if (!MyAllowDelete(callbackData->FilePathName, isDirectory))
        {
            wprintf(L"DENIED\n");
            hr = HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED);
        }
        else
        {
            wprintf(L"ALLOWED\n");
        }
        break;

    case PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED:

        wprintf(L"The %ls [%ls] was deleted.\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_FILE_RENAMED:

        if (wcslen(callbackData->FilePathName) == 0)
        {
            // If callbackData->FilePathName is an empty string, then the item
            // that was renamed was originally in a location not under the
            // virtualization root.
            wprintf(L"A %ls was renamed into the virtualization root,\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its new location is [%ls].\n",
                    destinationFileName);
        }
        else if (wcslen(destinationFileName) == 0)
        {
            // If destinationFileName is an empty string, then the item that was
            // renamed is now in a location not under the virtualization root.
            wprintf(L"A %ls was renamed out of the virtualization root.\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its original location was [%ls].\n",
                    callbackData->FilePathName);
        }
        else
        {
            // If both names are specified, both the new and old names are under
            // the virtualization root (it is never the case that nether name is
            // specified).
            wprintf(L"A %ls [%ls] was renamed.\n",
                    isDirectory ? L"directory": L"file",
                    callbackData->FilePathName);
            wprintf(L"Its new name is [%ls].\n", destinationFileName);
        }
        break;

    default:
        wprintf(L"Unrecognized notification: 0x%08x");
    }

    // Note that this may be a failure code from MyAllowDelete().
    return hr;
}
```