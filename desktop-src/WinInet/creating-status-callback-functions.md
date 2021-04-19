---
title: 建立狀態回呼函數
description: 本教學課程說明如何建立狀態回呼函式，以用來監視網際網路要求的狀態。
ms.assetid: 518d0800-5ea6-4327-8459-901e6d9a8a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e46040d9b6f93645e2730af287a1955343ec3a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106967300"
---
# <a name="creating-status-callback-functions"></a>建立狀態回呼函數

本教學課程說明如何建立狀態回呼函式，以用來監視網際網路要求的狀態。

狀態回呼函式會在源自任何傳遞非零內容值之 WinINet 函式的網際網路要求上接收狀態回呼。


以下是建立狀態回呼函式的必要步驟：

1.  [定義內容值。](#defining-the-context-value)
2.  [建立狀態回呼函數。](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a>定義內容值

內容值可以是任何不帶正負號的長整數值。 在理想情況下，內容值應該識別剛完成的要求，以及任何相關聯資源的位置（如有需要）。

使用內容值最有用的方式之一，就是傳遞結構的位址，並將它轉換成 **DWORD \_ 指標**。 您可以使用此結構來儲存要求的相關資訊，以便將其傳遞至狀態回呼函數。

下列結構是可能的內容值範例。 考慮使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函式來選擇結構的成員。


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



在此範例中，狀態回呼函式可以存取視窗控制碼，讓它能夠顯示使用者介面。 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)建立的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼可傳遞至另一個函式，該函式可下載資源和可用來傳遞要求相關資訊的字元陣列。

結構的成員可以變更為符合特定應用程式的需求，因此在此範例中不受限制。

### <a name="creating-the-status-callback-function"></a>建立狀態回呼函數

狀態回呼函數必須遵循 [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)的格式。 若要這樣做：

1.  為您的狀態回呼函數撰寫函式宣告。

    下列範例顯示範例宣告。

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  判斷您的狀態回呼函式會有什麼作用。 針對正在進行非同步呼叫的應用程式，狀態回呼函式必須處理 [網際網路 \_ 狀態 \_ 要求完成] \_ 值，表示非同步要求已完成。 狀態回呼函數也可以用來追蹤網際網路要求的進度。

    一般而言，最好使用 switch 語句搭配 *dwInternetStatus* 做為參數值，並使用 case 語句的狀態值。 根據您的應用程式所呼叫的函式類型而定，您可以忽略某些狀態值。 如需不同狀態值的定義，請參閱 [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)的 *dwInternetStatus* 參數底下的清單。

    下列 switch 語句是如何處理狀態回呼的範例。

    ``` syntax
    switch (dwInternetStatus)
    {
        case INTERNET_STATUS_REQUEST_COMPLETE:
            // Add code
            break;
        default:
            // Add code
            break;
    }
    ```

3.  建立程式碼來處理狀態值。

    處理每個狀態值的程式碼，主要取決於您要使用的狀態回呼函數。 針對只追蹤要求進度的應用程式，您可能只需要將字串寫入清單方塊。 針對非同步作業，程式碼必須處理回呼中傳回的部分資料。

    下列狀態回呼函式會使用 switch 函式來決定狀態值是什麼，並建立字串，其中包含狀態值的名稱和先前呼叫的函式，該函式會儲存在要求內容結構的 szMemo 成員中 \_ 。

    ```C++
    void __stdcall CallMaster(
        HINTERNET hInternet,
        DWORD_PTR dwContext,
        DWORD dwInternetStatus,
        LPVOID lpvStatusInformation,
        DWORD dwStatusInformationLength
    )
    {
        UNREFERENCED_PARAMETER(hInternet);
        UNREFERENCED_PARAMETER(lpvStatusInformation);
        UNREFERENCED_PARAMETER(dwStatusInformationLength);

        REQUEST_CONTEXT *cpContext;
        cpContext = (REQUEST_CONTEXT*)dwContext;
        char szStatusText[80];

        switch (dwInternetStatus)
        {
            case INTERNET_STATUS_CLOSING_CONNECTION:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CLOSING_CONNECTION",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_CONNECTED_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTED_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTING_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTING_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTION_CLOSED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTION_CLOSED",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CLOSING:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CLOSING",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CREATED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CREATED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_INTERMEDIATE_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s INTERMEDIATE_RESPONSE",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_NAME_RESOLVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s NAME_RESOLVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RECEIVING_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RECEIVING_RESPONSE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESPONSE_RECEIVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESPONSE_RECEIVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REDIRECT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REDIRECT",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_REQUEST_COMPLETE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_COMPLETE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REQUEST_SENT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_SENT",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESOLVING_NAME:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESOLVING_NAME",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_SENDING_REQUEST:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s SENDING_REQUEST",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_STATE_CHANGE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s STATE_CHANGE",
                                  cpContext->szMemo );
                break;
            default:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s Unknown Status %d Given",
                                  cpContext->szMemo,
                                  dwInternetStatus);
                break;
        }

        SendDlgItemMessage( cpContext->hWindow,
                          cpContext->nStatusList,
                          LB_ADDSTRING,
                          0, (LPARAM)szStatusText );

    }
    ```

    

4.  您可以使用 [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) 函式，在您要接收其狀態回呼的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼上設定狀態回呼函數。

    下列範例示範如何設定狀態回呼函數。

    ```C++
    HINTERNET hOpen;                       // Root HINTERNET handle
    INTERNET_STATUS_CALLBACK iscCallback;  // Holds the callback function

    // Create the root HINTERNET handle.
    hOpen = InternetOpen( TEXT("Test Application"),
                          INTERNET_OPEN_TYPE_PRECONFIG,
                          NULL, NULL, 0);

    // Set the status callback function.
    iscCallback = InternetSetStatusCallback( hOpen, (INTERNET_STATUS_CALLBACK)CallMaster );
    ```

    

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立狀態回呼函數](creating-status-callback-functions.md)
</dt> <dt>

[**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 