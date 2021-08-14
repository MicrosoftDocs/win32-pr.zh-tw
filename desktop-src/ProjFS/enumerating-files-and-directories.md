---
title: 列舉檔案和目錄
description: 描述 ProjFS 提供者如何參與目錄列舉。
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: 606b379e206cdbc64726e0ea97aed34e00f5253ecbffb7f8b7d42469b0cbb5fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792811"
---
# <a name="enumerating-files-and-directories"></a>列舉檔案和目錄

當提供者先建立虛擬化根時，本機系統上就會是空的。  也就是說，支援資料存放區中的所有專案都尚未快取到磁片。  開啟每個專案時，它會快取，但在專案開啟之前，它只存在於支援資料存放區中。

因為未開啟的專案沒有本機存在，所以一般目錄列舉不會向使用者顯示其存在。  因此，提供者必須將有關其支援資料存放區中專案的資訊傳回給 ProjFS，以參與目錄列舉。  ProjFS 會將來自提供者的資訊與本機檔案系統上的內容合併，以提供給使用者，以統一的目錄內容清單呈現給使用者。

## <a name="directory-enumeration-callbacks"></a>目錄列舉回呼

若要參與目錄列舉，提供者必須執行 **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**、 **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** 和 **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** 回呼。  列舉提供者之虛擬化根下的目錄時，ProjFS 會執行下列動作：

1. ProjFS 會呼叫提供者的 **PRJ_START_DIRECTORY_ENUMERATION_CB** 回呼，以啟動列舉會話。

    在處理此回呼的過程中，提供者應該準備執行列舉。  例如，它應該配置任何記憶體，它可能需要在其支援資料存放區中追蹤列舉的進度。

    ProjFS 會識別在回呼的 _callbackData_ 參數的 **FilePathName** 成員中列舉的目錄。  這會指定為相對於虛擬化根的路徑。  例如，如果虛擬化根位於 `C:\virtRoot` ，且要列舉的目錄是 `C:\virtRoot\dir1\dir2` ，則 **FilePathName** 成員會包含 `dir1\dir2` 。  提供者將準備在其支援資料存放區中列舉該路徑。  視提供者備份存放區的功能而定，在 **PRJ_START_DIRECTORY_ENUMERATION_CB** 回呼中執行備份存放區列舉可能是合理的。

    由於多個列舉可能會在相同的目錄中平行執行，因此每個列舉回呼都有一個 _enumerationId_ 引數，可讓提供者將回呼調用與單一列舉會話產生關聯。

    如果提供者從 **PRJ_START_DIRECTORY_ENUMERATION_CB** 回呼傳回 S_OK，它必須在 ProjFS 叫用具有相同 _enumerationId_ 值的 **PRJ_END_DIRECTORY_ENUMERATION_CB** 回呼之前，維持它所擁有的任何列舉會話資訊。  如果提供者從 **PRJ_START_DIRECTORY_ENUMERATION_CB** 傳回錯誤，則 ProjFS 將不會叫用該 _enumerationId_ 的 **PRJ_END_DIRECTORY_ENUMERATION_CB** 回呼。

1. ProjFS 會呼叫提供者的 **PRJ_GET_DIRECTORY_ENUMERATION_CB** 回呼一或多次，以從提供者取得目錄內容。

    為了回應此回呼，提供者會從其支援資料存放區傳回已排序的專案清單。

    回呼可能會在其 _searchExpression_ 參數中提供搜尋運算式，讓提供者用來界定列舉的結果範圍。  如果 _searchExpression_ 為 Null，則提供者會傳回所列舉之目錄中的所有專案。  如果非 Null，則提供者可以使用 **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** 來判斷運算式中是否有萬用字元。  如果有，則提供者會使用 **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** 來判斷目錄中的專案是否符合搜尋運算式。

    提供者應該在此回呼的第一個調用上，捕捉 _searchExpression_ 的值。  除非在回呼的 _callbackData_ 參數的 [**旗標**] 欄位中設定 PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN，否則它會在相同列舉會話中任何後續的回呼調用中使用捕捉到的值。  在這種情況下，應該重新捕獲 _searchExpression_ 的值。

    如果其備份存放區中沒有相符專案，則提供者會直接從回呼傳回 S_OK。  否則，提供者會將其備份存放區中的每個相符專案格式化為 **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** 結構，然後使用 **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** 來填滿回呼的 _dirEntryBufferHandle_ 參數所提供的緩衝區。  提供者會持續新增專案，直到其全部加入，或直到 **PrjFillDirEntryBuffer** 傳回 HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) 為止。  然後，提供者會從回呼傳回 S_OK。  請注意，提供者必須以正確的排序次序將專案加入至 _dirEntryBufferHandle_ 緩衝區。  提供者應該使用 **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** 來判斷正確的排序次序。

    > 提供者必須提供 **PRJ_FILE_BASIC_INFO** 之 **IsDirectory** 成員的值。  如果 **IsDirectory** 為 FALSE，則提供者也必須提供 **FileSize** 成員的值。
    >
    > 如果提供者未提供 **CreationTime**、 **LastAccessTime**、 **LastWriteTime** 和 **ChangeTime** 成員的值，ProjFS 將會使用目前的系統時間。
    >
    > ProjFS 會使用任何 FILE_ATTRIBUTE 旗標 **FileAttributes** 成員中的提供者集合，但 FILE_ATTRIBUTE_DIRECTORY 除外;它會根據所提供的 **IsDirectory** 成員值，設定 **FileAttributes** 成員中 FILE_ATTRIBUTE_DIRECTORY 的正確值。

    如果 **PrjFillDirEntryBuffer** 在提供者用完要加入的專案之前，傳回 HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) ，則提供者必須在收到錯誤時追蹤嘗試加入的專案。  下次 ProjFS 呼叫相同列舉會話的 **PRJ_GET_DIRECTORY_ENUMERATION_CB** 回呼時，提供者必須繼續將專案加入至 _dirEntryBufferHandle_ 緩衝區，並將其新增至其嘗試加入的專案。

    > 如果支援存放區支援符號連結，則提供者必須使用 **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** 來填滿回呼的 _dirEntryBufferHandle_ 參數所提供的緩衝區。  **PrjFillDirEntryBuffer2** 支援額外的緩衝區輸入，可讓提供者指定列舉專案是符號連結和其目標。  否則， **PrjFillDirEntryBuffer** 會如上面所述運作。  下列範例會使用 **PrjFillDirEntryBuffer2** 來說明符號連結的支援。
    >
    > 請注意，Windows 10 2004 版才支援 **PrjFillDirEntryBuffer2** 。  提供者應該探查是否存在 **PrjFillDirEntryBuffer2**，例如使用 **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**。

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
    } MY_ENUM_ENTRY;

    typedef struct MY_ENUM_SESSION {
        GUID EnumerationId;
        PWSTR SearchExpression;
        USHORT SearchExpressionMaxLen;
        BOOLEAN SearchExpressionCaptured;
        MY_ENUM_ENTRY* EnumHead;
        MY_ENUM_ENTRY* LastEnumEntry;
        BOOLEAN EnumCompleted;
    } MY_ENUM_SESSION;

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            // Ensure that if the caller is requesting a restart we reset our
            // bookmark of how far we got in the enumeration.
            session->LastEnumEntry = NULL;

            // In case we're restarting ensure we don't think we're done.
            session->EnumCompleted = FALSE;

            // We need to start considering items from the beginning of the list
            // retrieved from the backing store.
            enumHead = session->EnumHead;
        }
        else
        {
            // We are resuming an existing enumeration session.  Note that
            // session->LastEnumEntry may be NULL.  That is okay; it means
            // we got all the entries the last time this callback was invoked.
            // Returning S_OK without adding any new entries to the
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
            enumHead = session->LastEnumEntry;
        }

        if (enumHead == NULL)
        {
            // There are no items to return.  Remember that we've returned everything
            // we can.
            session->EnumCompleted = TRUE;
        }
        else
        {
            MY_ENUM_ENTRY* thisEntry = enumHead;
            while (thisEntry != NULL)
            {
                // We'll insert the entry into the return buffer if it matches
                // the search expression captured for this enumeration session.
                if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
                {
                    PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                    fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                    fileBasicInfo.FileSize = thisEntry->FileSize;

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. ProjFS 會呼叫提供者的 **PRJ_END_DIRECTORY_ENUMERATION_CB** 回呼，以結束列舉會話。

    提供者應該執行任何必須執行的清除作業，以結束列舉會話，例如將配置的記憶體解除配置為處理 **PRJ_START_DIRECTORY_ENUMERATION_CB** 的一部分。
