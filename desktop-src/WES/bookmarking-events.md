---
title: 將事件加上書簽
description: 書簽會識別通道或記錄檔中的事件。
ms.assetid: e7eeafc3-deb9-4cdc-9763-f784db7333be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64d7fb4aef883a51084420c5a2d78e4f0ff25dac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106999799"
---
# <a name="bookmarking-events"></a>將事件加上書簽

書簽會識別通道或記錄檔中的事件。 當您查詢或訂閱事件時，您可以使用書簽來開始從該書簽事件中讀取事件。 您通常會在結果集中建立最後一個事件的書簽， (假設您已經列舉結果集) 中的所有事件。

下列程式描述如何從事件建立書簽。

**從事件建立書簽**

1.  呼叫 [**EvtCreateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) 函數以建立書簽。 傳遞 **Null** 做為引數。
2.  呼叫 [**EvtUpdateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtupdatebookmark) 函式，以更新含有事件的書簽。 將控制碼傳遞給事件做為引數。
3.  呼叫 [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) 函數，以建立代表書簽的 XML 字串。 傳遞 EvtRenderBookmark 作為轉譯旗標。
4.  保存 XML 字串以供稍後使用 (例如，您可以將 XML 字串保存在檔案或登錄) 中。

下列程式描述如何使用先前程式中保存的 XML 書簽字串來建立書簽。

**使用 XML 書簽字串建立書簽**

1.  取得代表您先前保存之書簽的 XML 字串。
2.  呼叫 [**EvtCreateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) 函數以建立書簽。 傳遞引數的 XML 字串。

下列程式描述如何在查詢中使用書簽。

**若要在查詢中使用書簽**

1.  呼叫 [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) 函數，以取得符合查詢的事件。
2.  呼叫 [**EvtSeek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek) 函式以搜尋有書簽的事件。 將控制碼傳遞至書簽和 EvtSeekRelativeToBookmark 旗標。
3.  在迴圈中呼叫 [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) 函式，根據您在 [**EvtSeek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek)) 中指定的位移，列舉在加上書簽的事件之後開始 (的事件。

如需範例，請參閱 [在查詢中使用書簽](#using-a-bookmark-in-a-query)。

下列程式描述如何在訂用帳戶中使用書簽。

**在訂用帳戶中使用書簽**

1.  呼叫 [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) 函式來訂閱符合查詢的事件。 將控制碼傳遞至書簽和 EvtSubscribeStartAfterBookmark 旗標。
2.  如果您執行了 [**.Evt \_ 訂閱 \_ 回檔**](/windows/win32/api/winevt/nc-winevt-evt_subscribe_callback) 函式，您的回呼將會收到在加上書簽的事件之後開始的事件。
3.  如果您未執行回呼，請在迴圈中呼叫 [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) 函式，以列舉在加上書簽的事件之後開始的事件。

如需範例，請參閱 [在訂用帳戶中使用書簽](#using-a-bookmark-in-a-subscription)。

## <a name="using-a-bookmark-in-a-query"></a>在查詢中使用書簽

下列範例顯示如何在查詢中使用書簽。 此範例會展開 [查詢事件](querying-for-events.md)的範例。


```C++
// Enumerate all the events in the result set beginning with the bookmarked event. 
DWORD PrintResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;
    LPWSTR pwsBookmarkXml = NULL;
    EVT_HANDLE hBookmark = NULL;

    // Get the persisted bookmark XML string.
    pwsBookmarkXml = GetBookmarkedString();

    // If the bookmark string was persisted, create a bookmark and
    // seek to the bookmarked event in the result set.
    if (pwsBookmarkXml)
    {
        hBookmark = EvtCreateBookmark(pwsBookmarkXml);
        if (NULL == hBookmark)
        {
            wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
            goto cleanup;
        }

        if (!EvtSeek(hResults, 1, hBookmark, 0, EvtSeekRelativeToBookmark))
        {
            wprintf(L"EvtSeek failed with %lu\n", GetLastError());
            goto cleanup;
        }
    }

    // Enumerate the events in the result set after the bookmarked event.
    while (true)
    {
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (status = PrintEvent(hEvents[i]))
            {
                EvtClose(hEvents[i]);
                hEvents[i] = NULL;
            }
            else
            {
                goto cleanup;
            }
        }
    }

cleanup:

    if (ERROR_NO_MORE_ITEMS == status)
    {
        // Get the last event in the result set, use it to create a
        // bookmark, render the bookmark as an XML string, and persist the string.
        if (ERROR_SUCCESS != (status = SaveBookmark(hResults)))
            wprintf(L"\nFailed to save bookmark\n");
    }
    else
    {
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (NULL != hEvents[i])
                EvtClose(hEvents[i]);
        }
    }

    if (pwsBookmarkXml)
        free(pwsBookmarkXml);

    return status;
}

// Get the bookmark XML string from wherever you persisted it.
LPWSTR GetBookmarkedString(void)
{
    LPWSTR pwsBookmarkXML = NULL;

    // TODO: Add the code to get the bookmark XML string from storage.

    return pwsBookmarkXML;
}


// Persist the bookmark XML string. This example assumes that we've read through
// the result set and are persisting the last event as the bookmark.
DWORD SaveBookmark(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    DWORD dwReturned = 0;
    LPWSTR pBookmarkXml = NULL;
    EVT_HANDLE hBookmark = NULL;
    EVT_HANDLE hEvent = NULL;

    // Seek to the last event in the result set and get the event.
    if (!EvtSeek(hResults, 0, NULL, 0, EvtSeekRelativeToLast))
    {
        wprintf(L"EvtSeek failed with %lu\n", status = GetLastError());
        goto cleanup;
    }

    if (!EvtNext(hResults, 1, &hEvent, INFINITE, 0, &dwReturned))
    {
        wprintf(L"EvtNext failed with %lu\n", status = GetLastError());
        goto cleanup;
    }

    // Create a bookmark and update it with the last event in the result set.
    hBookmark = EvtCreateBookmark(NULL);
    if (NULL == hBookmark)
    {
        wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

    if (!EvtUpdateBookmark(hBookmark, hEvent))
    {
        wprintf(L"EvtUpdateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

    // Render the bookmark as an XML string that you can then persist.
    if (!EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pBookmarkXml = (LPWSTR)malloc(dwBufferSize);
            if (pBookmarkXml)
            {
                EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

    // TODO: Add code to persist bookmark XML string.

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

    if (hBookmark)
        EvtClose(hBookmark);

    if (hEvent)
        EvtClose(hEvent);

    return status;
}
```



## <a name="using-a-bookmark-in-a-subscription"></a>在訂用帳戶中使用書簽

下列範例顯示如何在發送訂閱中使用書簽。


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent);
DWORD PrintEvent(EVT_HANDLE hEvent);
EVT_HANDLE GetBookmark();
DWORD SaveBookmark(EVT_HANDLE hBookmark);


void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    EVT_HANDLE hBookmark = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"<xpath query goes here>";

    // Get the saved bookmark.
    hBookmark = GetBookmark();

    // Subscribe to existing and furture events beginning with the bookmarked event.
    // If the bookmark has not been persisted, pass an empty bookmark and the subscription
    // will begin with the second event that matches the query criteria.
    hSubscription = EvtSubscribe(NULL, NULL, pwsPath, pwsQuery, hBookmark, (PVOID)hBookmark, 
                                 (EVT_SUBSCRIBE_CALLBACK)SubscriptionCallback, EvtSubscribeStartAfterBookmark);
    if (NULL == hSubscription)
    {
        wprintf(L"EvtSubscribe failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"Hit any key to quit\n\n");
    while (!_kbhit())
        Sleep(10);

    status = SaveBookmark(hBookmark);

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);

    if (hBookmark)
        EvtClose(hBookmark);
 }


// The callback that receives the events that match the query criteria. Use the 
// context parameter to pass the handle to the bookmark, so you can update the bookmark
// with each event that you receive.
DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hBookmark = (EVT_HANDLE)pContext;

    switch(action)
    {
        // You should only get the EvtSubscribeActionError action if your subscription flags 
        // includes EvtSubscribeStrict and the channel contains missing event records.
        case EvtSubscribeActionError:
            if (ERROR_EVT_QUERY_RESULT_STALE == (DWORD)hEvent)
            {
                wprintf(L"The subscription callback was notified that event records are missing.\n");
                // Handle if this is an issue for your application.
            }
            else
            {
                wprintf(L"The subscription callback received the following Win32 error: %lu\n", (DWORD)hEvent);
            }

            break;

        case EvtSubscribeActionDeliver:
            if (ERROR_SUCCESS != (status = PrintEvent(hEvent)))
            {
                goto cleanup;
            }

            if (!EvtUpdateBookmark(hBookmark, hEvent))
            {
                wprintf(L"EvtUpdateBookmark failed with %lu\n", status = GetLastError());
                goto cleanup;
            }

            break;

        default:
            wprintf(L"SubscriptionCallback: Unknown action.\n");
    }

cleanup:

    if (ERROR_SUCCESS != status)
    {
        // End subscription - Use some kind of IPC mechanism to signal
        // your application to close the subscription handle.
    }

    return status; // The service ignores the returned status.
}


EVT_HANDLE GetBookmark(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hBookmark = NULL;
    LPWSTR pBookmarkXml = NULL;

    // Set pBookmarkXml to the XML string that you persisted in SaveBookmark.

    hBookmark = EvtCreateBookmark(pBookmarkXml);
    if (NULL == hBookmark)
    {
        wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

    return hBookmark;
}


DWORD SaveBookmark(EVT_HANDLE hBookmark)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pBookmarkXml = NULL;

    if (!EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pBookmarkXml = (LPWSTR)malloc(dwBufferSize);
            if (pBookmarkXml)
            {
                EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", status);
            goto cleanup;
        }
    }

    // Persist bookmark to a file or the registry.

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

    return status;
}


// Render the event as an XML string and print it.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", status);
            goto cleanup;
        }
    }

    wprintf(L"%s\n\n", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}
```



 

 