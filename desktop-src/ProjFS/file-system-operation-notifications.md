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
# <a name="file-system-operation-notifications"></a>檔案系統作業通知

除了處理列舉、傳回檔案中繼資料和檔案內容的必要回呼之外，提供者可以選擇性地在呼叫 **[PrjStartVirtualizing]()** 時註冊 **[PRJ_NOTIFICATION_CB]()** 回呼。  此回呼會接收在實例虛擬化根下的檔案和目錄上所執行檔案系統作業的通知。  某些通知是「作業後」通知，告訴提供者作業剛剛完成。  其他通知是「前置作業」通知，表示提供者會在作業發生之前收到通知。  在前置操作通知中，提供者可以從回呼傳回錯誤碼，以防止作業。  這會導致作業失敗，並傳回錯誤碼。

## <a name="how-to-specify-notifications-to-receive"></a>如何指定要接收的通知

如果提供者在啟動虛擬化實例時提供了 **PRJ_NOTIFICATION_CB** 的執行，則也應該指定要接收的通知。  提供者可註冊的通知會定義在 [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) 列舉中。

當提供者指定要接收的通知時，它會使用一或多個 [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) 結構的陣列來執行此動作。  這些會定義「通知對應」。  通知對應是目錄（稱為「通知根目錄」）與一組通知（以位遮罩表示）之間的配對，ProjFS 應該傳送該目錄及其下階。  也可以建立單一檔案的通知對應。  在通知對應中指定的檔案或目錄，在提供者呼叫 **PrjStartVirtualizing** 時不一定要存在，而提供者可以指定任何路徑，而且對應會在建立時套用。

如果提供者指定多個通知對應，而有些則是其他的子系，則必須以遞減的深度指定對應。  較深層級的通知對應會覆寫其子系的較高層級。

如果提供者未指定一組通知對應，ProjFS 會預設為將它 PRJ_NOTIFY_FILE_OPENED、PRJ_NOTIFY_NEW_FILE_CREATED 和 PRJ_NOTIFY_FILE_OVERWRITTEN 傳送給虛擬化根下的所有檔案和目錄。

下列程式碼片段說明如何在啟動虛擬化實例時註冊一組通知。

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

## <a name="receiving-notifications"></a>接收告知

ProjFS 藉由呼叫提供者的 **PRJ_NOTIFICATION_CB** 回呼來傳送檔案系統作業的通知。  它會針對提供者所註冊的每個作業執行此動作。  如果在上述範例中，已註冊 PRJ_NOTIFY_NEW_FILE_CREATED 的提供者 |PRJ_NOTIFY_FILE_OPENED |PRJ_NOTIFY_PRE_DELETE |PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED |PRJ_NOTIFY_FILE_RENAMED，而應用程式在通知根目錄中建立了新的檔案，則 ProjFS 會使用新檔案的路徑名稱和設定為 PRJ_NOTIFICATION_NEW_FILE_CREATED 的 _通知_ 參數，呼叫 **PRJ_NOTIFICATION_CB** 回呼。

ProjFS 會在相關聯的檔案系統作業發生之前，傳送下列清單中的通知。  如果提供者從 **PRJ_NOTIFICATION_CB** 回呼傳回失敗碼，檔案系統作業將會失敗，並傳回提供者所指定的失敗碼。

* PRJ_NOTIFICATION_PRE_DELETE-即將刪除此檔案。
* PRJ_NOTIFICATION_PRE_RENAME-即將重新命名檔案。
* PRJ_NOTIFICATION_PRE_SET_HARDLINK-即將為檔案建立硬式連結。
* PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL-即將將檔案從預留位置擴充至完整檔案，這表示可能會修改其內容。

ProjFS 會在相關聯的檔案系統作業完成之後，傳送下列清單中的通知。

* PRJ_NOTIFICATION_FILE_OPENED-已開啟現有的檔案。
  * 雖然此通知是在檔案開啟之後傳送的，但提供者可能會傳回失敗碼。  在回應中，ProjFS 會取消開啟，並將失敗傳回給呼叫者。
* PRJ_NOTIFICATION_NEW_FILE_CREATED-已建立新的檔案。
* PRJ_NOTIFICATION_FILE_OVERWRITTEN-已覆寫現有的檔案，例如藉由使用 **CREATE_ALWAYS** _dwCreationDisposition_ 旗標來呼叫 [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) 。
* PRJ_NOTIFICATION_FILE_RENAMED-已重新命名檔案。
* PRJ_NOTIFICATION_HARDLINK_CREATED-已建立檔案的 [硬式連結](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) 。
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION-檔案控制代碼已關閉，且檔案的內容未經過修改，也不會刪除檔案。
* PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED-檔案控制代碼已關閉，且檔案的內容已修改。
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED-檔案控制代碼已關閉，並在關閉控制碼的過程中刪除該檔案。

如需每個通知的詳細資訊，請參閱 **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)** 的檔。

**PRJ_NOTIFICATION_CB** 回呼的 _notificationParameters_ 參數會指定特定通知的額外參數。  如果提供者收到 PRJ_NOTIFICATION_FILE_OPENED、PRJ_NOTIFICATION_NEW_FILE_CREATED 或 PRJ_NOTIFICATION_FILE_OVERWRITTEN，或 PRJ_NOTIFICATION_FILE_RENAMED 通知，提供者可以為檔案指定要接收的一組新通知。 如需詳細資訊，請參閱 **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)** 的檔。

下列範例會示範提供者如何處理在上述程式碼片段中註冊的通知的簡單範例。

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