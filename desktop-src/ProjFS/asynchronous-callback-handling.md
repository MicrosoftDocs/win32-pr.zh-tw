---
title: 非同步回呼完成
description: 描述提供者如何以非同步方式服務回呼。
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/12/2018
ms.topic: article
ms.openlocfilehash: 8ec23f5ea6e8ec55be2eaa2811d9dee8b1870edc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106996370"
---
# <a name="asynchronous-callback-handling"></a>非同步回呼處理

當用戶端與提供者虛擬化根底下的檔案和目錄互動時，這些互動通常會導致叫用提供者的回呼。  ProjFS 會叫用提供者回呼，方法是將訊息從核心模式傳送至 ProjFS 使用者模式程式庫，其中背景工作執行緒會接收訊息並呼叫適當的回呼。  回呼傳回後，背景工作執行緒會等待另一則訊息抵達核心模式。  如果所有背景工作執行緒都忙於執行提供者回呼程式碼，則會觸發回呼區塊的任何進一步用戶端 i/o，直到背景工作執行緒可供接收訊息並叫用相關的回呼為止。  當提供者啟動時，可以透過 **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** 的 _options_ 參數，指定其想要 ProjFS 建立給服務回呼的背景工作執行緒數目。  提供者可以非同步服務回呼，以改善訊息接收工作者執行緒的效率。

> 如果提供者未指定要 **PrjStartVirtualizing** 的 _options_ 參數，或針對 _options_ 參數的 ConcurrentThreadCount 成員指定0，ProjFS 將會使用系統中的邏輯處理器數目來作為 ConcurrentThreadCount 的值。
>
> 如果提供者未指定要 **PrjStartVirtualizing** 的 _options_ 參數，或針對 _options_ 參數的 PoolThreadCount 成員指定0，ProjFS 將會使用 ConcurrentThreadCount 值的兩倍作為 PoolThreadCount 的值。

提供者會透過從回呼傳回 HRESULT_FROM_WIN32 (ERROR_IO_PENDING) ，並在稍後使用 **[PrjCompleteCommand](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand)** 完成這些回呼，以非同步方式回呼。  以非同步方式處理回呼的提供者，也應藉由實 **[PRJ_CANCEL_COMMAND_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb)** 回呼來支援回呼取消。

當 ProjFS 呼叫提供者的回呼時，它會使用回呼的 _callbackData_ 參數的 CommandId 成員來識別回呼的特定調用。  如果提供者決定以非同步方式處理該回呼，它必須儲存 CommandId 成員的值，並從回呼傳回 HRESULT_FROM_WIN32 (ERROR_IO_PENDING) 。  一旦提供者完成回呼的處理，它就會呼叫 **PrjCompleteCommand**，並在 _commandId_ 參數中傳遞預存的識別碼。  這會告訴 ProjFS 已完成的回呼調用。

實 **PRJ_CANCEL_COMMAND_CB** 回呼的提供者必須追蹤尚未完成的回呼。  如果提供者收到此回呼，則表示會明確地取消導致叫用其中一個回呼的 i/o，或是因為它在終止時所發出的執行緒而被取消。 提供者應該盡可能地取消處理 CommandId 所識別的回呼調用。

> 雖然 ProjFS 只會在叫用取消回呼之後叫用指定 CommandId 的 **PRJ_CANCEL_COMMAND_CB** ，但是取消和原始調用可能會在多執行緒提供者中並存執行。  提供者必須能夠正常地處理這種情況。

下列範例是針對 [列舉檔案和目錄](enumerating-files-and-directories.md) 主題提供的範例版本，修改為說明非同步回呼處理。

```C++
typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

typedef struct MY_ENUM_ENTRY {
    MY_ENUM_ENTRY* Next;
    PWSTR Name;
    BOOLEAN IsDirectory;
    INT64 FileSize;
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

typedef struct MY_ENUM_PARAMS {
    GUID EnumerationId;
    PRJ_DIR_ENTRY_BUFFER_HANDLE DirEntryBufferHandle;
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT NamespaceVirtualizationContext;
    INT32 CommandId;
    PRJ_CALLBACK_DATA_FLAGS Flags;
    WCHAR SearchExpression[1];
} MY_ENUM_PARAMS;

// Prototype for the enumeration worker routine.  In this example this is a
// ThreadProc.  See https://msdn.microsoft.com/library/windows/desktop/ms686736.aspx
DWORD WINAPI MyGetEnumCallbackWorker(_In_ LPVOID parameter);

#define ROLLBACK_NONE           0
#define ROLLBACK_PARAM_ALLOC    1
#define ROLLBACK_TRACK_ENUM     2

HRESULT
MyGetEnumCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ const GUID* enumerationId,
    _In_opt_z_ PCWSTR searchExpression,
    _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
    )
{
    UINT rollback = ROLLBACK_NONE;

    // This example creates a thread to run the enumeration in.  The provider
    // can access callbackData only while the callback is running, so we copy
    // out the fields that the worker thread will need.
    MY_ENUM_PARAMS* enumParams = NULL;
    size_t bufSize = sizeof(MY_ENUM_PARAMS);

    // Allocate enough space for the parameter buffer and the search expression
    // string plus a terminating NULL character.
    if (searchExpression != NULL)
    {
        bufSize += (wcslen(searchExpression) + 1) * sizeof(WCHAR);
    }
    else
    {
        // We'll store "*" as the search expression in this case.
        bufSize += 2 * sizeof(WCHAR);
    }

    enumParams = (MY_ENUM_PARAMS*) calloc(1, bufSize);

    if (enumParams == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // enumParams allocated.
    rollback = ROLLBACK_PARAM_ALLOC;

    // Copy the search expression into our parameter buffer.
    if (searchExpression != NULL)
    {
        wcsncpy_s(enumParams->SearchExpression,
                  wcslen(searchExpression),
                  searchExpression,
                  wcslen(searchExpression));
    }
    else
    {
        wcsncpy_s(enumParams->SearchExpression, 1, "*", 1);
    }

    // Copy the other parameters into our parameter buffer.
    enumParams->EnumerationId = enumerationId;
    enumParams->DirEntryBufferHandle = dirEntryBufferHandle;
    enumParams->NamespaceVirtualizationContext = callbackData->NamespaceVirtualizationContext
    enumParams->CommandId = callbackData->CommandId;
    enumParams->Flags = callbackData->Flags;

    // MyTrackEnumForCancellation is a routine the provider might implement to
    // track active enumeration callbacks in case they are cancelled.  It stores
    // the CommandId for the callback in some structure.
    hr = MyTrackEnumForCancellation(callbackData->CommandId);

    if (FAILED(hr))
    {
        goto RollbackOnError;
    }

    // Enum callback tracked.
    rollback = ROLLBACK_TRACK_ENUM;

    // Create the worker thread.
    HANDLE workerThread = NULL;
    workerThread = CreateThread(NULL,
                                0,
                                MyGetEnumCallbackWorker,
                                enumParams,
                                0
                                NULL);

    // We'll treat failure to create the thread as a low-resources error.
    if (workerThread == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // Return pending to signal that we'll complete the enumeration later.
    return HRESULT_FROM_WIN32(ERROR_IO_PENDING);

RollbackOnError:

    // Clean up manually.  Note the fall-through structure of the switch, and that
    // we clean up in reverse order.
    switch(rollback)
    {
    case ROLLBACK_TRACK_ENUM:
        // MyUntrackEnumForCancellation removes the CommandId for the callback
        // from the structure that MyTrackEnumForCancellation put it in.
        MyUntrackEnumForCancellation(callbackData->CommandId);

    case ROLLBACK_PARAM_ALLOC:
        free(enumParams);

    default:
        break;
    }

    return hr;
}

DWORD
WINAPI
MyGetEnumCallbackWorker(
    _In_ LPVOID parameter
)
{
    HRESULT hr = S_OK;
    MY_ENUM_PARAMS* enumParams = (MY_ENUM_PARAMS*) parameter;

    // MyCheckEnumForCancellation is a routine the provider might implement to
    // check whether a pended enumeration callback has been cancelled.  Even
    // though the enumeration has been cancelled, ProjFS will still call the
    // provider's end-enumeration callback.  This allows general cleanup, such
    // as tearing down the enumeration session, to always happen in that callback.
    if (MyCheckEnumForCancellation(enumParams->CommandId))
    {
        // The operation has been cancelled.  Clean up and get out.
        free(enumParams);
        return 0;
    }

    // MyGetEnumSession is a routine the provider might implement to find
    // information about the enumeration session that it first stored
    // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
    //
    // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
    // already retrieved a list of the items in the backing store located at
    // callbackData->FilePathName, sorted them using PrjFileNameCompare()
    // to determine collation order, and stored the list in session->EnumHead.
    MY_ENUM_SESSION* session = NULL;
    session = MyGetEnumSession(enumParams->EnumerationId);

    if (session == NULL)
    {
        hr = HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        goto CompleteCallback;
    }

    if (!session->SearchExpressionCaptured ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        if (wcsncpy_s(session->SearchExpression,
                      session->SearchExpressionMaxLen,
                      enumParams->SearchExpression,
                      wcslen(enumParams->SearchExpression)))
        {
            // Failed to copy the search expression; perhaps the provider
            // could try reallocating session->SearchExpression.
        }

        session->SearchExpressionCaptured = TRUE;
    }

    MY_ENUM_ENTRY* enumHead = NULL;

    // We have to start the enumeration from the beginning if we aren't
    // continuing an existing session or if the caller is requesting a restart.
    if (((session->LastEnumEntry == NULL) &&
         !session->EnumCompleted) ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
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
        // enumParams->DirEntryBufferHandle buffer signals ProjFS that the
        // enumeration has returned everything it can.
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

                // Format the entry for return to ProjFS.
                if (S_OK != PrjFillDirEntryBuffer(thisEntry->Name,
                                                  &fileBasicInfo,
                                                  enumParams->DirEntryBufferHandle))
                {
                    // We couldn't add this entry to the buffer; remember where we left
                    // off for the next time we're called for this enumeration session.
                    session->LastEnumEntry = thisEntry;
                    hr = S_OK;

                    goto CompleteCallback;
                }
            }

            thisEntry = thisEntry->Next;
        }

        // We reached the end of the list of entries; remember that we've returned
        // everything we can.
        session->EnumCompleted = TRUE;
    }

CompleteCallback:

    // Signal ProjFS that we've completed this callback.  Since this is an enumeration
    // we use the extendedParameters parameter to PrjCompleteCommand.
    PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS extendedParams = {};
    extendedParams.CommandType = PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION;
    extendedParams.enumeration.DirEntryBufferHandle = enumParams->DirEntryBufferHandle;

    PrjCompleteCommand(enumParams->NamespaceVirtualizationContext,
                       enumParams->CommandId,
                       hr,
                       &extendedParams);

    MyUntrackEnumForCancellation(enumParams->CommandId);

    free(enumParams);

    // ThreadProc returns 0 on successful completion.
    return 0;
}
```

以下是使用上述範例程式碼的簡短範例 PRJ_CANCEL_COMMAND_CB。

```C++
void
MyCancelCommandCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
)
{
    // MyMarkEnumForCancellation is a routine the provider might implement to
    // mark a pended enumeration callback as cancelled.  If the given CommandId
    // is not found, it is not an error.  It may not yet have been tracked or
    // it may already have completed and been untracked.
    MyMarkEnumForCancellation(callbackData->CommandId);
}
```