---
title: HTTP 會話
description: 您可以使用 HTTP 來存取 WWW 上的資源。
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092844"
---
# <a name="http-sessions"></a>HTTP 會話

WinINet 可讓您存取 World Wide Web (WWW) 上的資源。 您可以使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (直接存取這些資源。如需詳細資訊，請參閱 [直接存取 url](handling-uniform-resource-locators.md)) 。

您可以使用 HTTP 來存取 WWW 上的資源。 HTTP 函式會處理基礎通訊協定，同時允許您的應用程式存取 WWW 上的資訊。 當 HTTP 通訊協定演進時，會更新基礎通訊協定以維護函式行為。

下圖顯示與 HTTP 通訊協定搭配使用之函數的關聯性。 陰影方塊代表會傳回 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼的函式，而一般方塊代表的函式會使用其相依的函式所建立的 **HINTERNET** 控制碼。

![用於 HTTP 的 wininet 函數](images/ax-wnt05.png)

如需詳細資訊，請參閱 [HINTERNET 控制碼](appendix-a-hinternet-handles.md)。

## <a name="using-the-wininet-functions-to-access-the-www"></a>使用 WinINet 函數存取 WWW

-   [起始與 WWW 的連接](#initiating-a-connection-to-the-www)
-   [開啟要求](#opening-a-request)
-   [新增要求標頭](#adding-request-headers)
-   [傳送要求](#sending-a-request)
-   [將資料張貼到伺服器](#posting-data-to-the-server)
-   [取得要求的相關資訊](#getting-information-about-a-request)
-   [從 WWW 下載資源](#downloading-resources-from-the-www)

下列函式會在 HTTP 會話期間用來存取 WWW。



| 函式                                               | 描述                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | 將 HTTP 要求標頭新增至 HTTP 要求控制碼。 此函數需要 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所建立的控制碼。                                                 |
| [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | 開啟 HTTP 要求控制碼。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。                                                                         |
| [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | 查詢 HTTP 要求的相關資訊。 此函式需要 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 或 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函數所建立的控制碼。 |
| [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | 將指定的 HTTP 要求傳送至 HTTP 伺服器。 此函數需要 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所建立的控制碼。                                                  |
| [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | 針對常見的網際網路錯誤情況，顯示預先定義的對話方塊。 此函式需要 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)呼叫中使用的控制碼。                     |



 

### <a name="initiating-a-connection-to-the-www"></a>起始與 WWW 的連接

若要啟動與 WWW 的連接，應用程式必須在 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所傳回的根 [**HINTERNET**](appendix-a-hinternet-handles.md)上呼叫 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函式。 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 必須宣告網際網路 \_ 服務 \_ HTTP 服務類型，以建立 HTTP 會話。 如需使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)的詳細資訊，請參閱 [使用 InternetConnect](enabling-internet-functionality.md)。

### <a name="opening-a-request"></a>開啟要求

[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)函式會開啟 HTTP 要求，並傳回其他 HTTP 函數可使用的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。 不同于其他開啟的函式 (例如 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)) ， [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 不會在呼叫時將要求傳送至網際網路。 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)函式會傳送要求，並透過網路建立連接。

[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 會採用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 和 HTTP 動詞命令、物件名稱、版本字串、查閱者、接受類型、旗標和內容值所建立的 HTTP 會話控制碼。

HTTP 動詞命令是要在要求中使用的字串。 要求中使用的常見 HTTP 動詞命令包括 GET、PUT 和 POST。 如果這個值設定為 **Null**， [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 會使用預設值 GET。

物件名稱是一個字串，其中包含指定之 HTTP 動詞命令的目標物件名稱。 這通常是檔案名、可執行模組或搜尋規範。 如果提供的物件名稱是空字串，則 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 會尋找預設頁面。

版本字串應包含 HTTP 版本。 如果此參數為 **Null**，則函數會使用 "" HTTP/1.1 ""。

訪客會指定取得物件名稱的檔位址。 如果此參數為 **Null**，則不會指定任何訪客。

以 **null** 終止的字串，包含接受類型表示應用程式接受的內容類型。 將此參數設定為 **Null** ，表示應用程式不接受任何內容類型。 如果提供空字串，應用程式表示它只接受 "" text/"" 類型的檔 \* 。 值 "" text/ \* "" 表示純文字檔，而不是圖片或其他二進位檔。

旗標值會控制快取、cookie 和安全性問題。 若為 Microsoft Network (MSN) 、NTLM 和其他類型的驗證，請設定 [網際網路 \_ 旗 \_ 標 \_ 保持連線](api-flags.md) 旗標。

如果在呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)時設定了 [INTERNET \_ 旗標 \_ ASYNC](api-flags.md)旗標，則應該針對適當的非同步作業設定非零的內容值。

下列範例是 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)的範例呼叫。

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a>新增要求標頭

[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa)函式可讓應用程式將一個或多個要求標頭加入至初始要求。 此函式可讓應用程式將額外的自由格式標頭附加至 HTTP 要求控制碼;它適用于需要精確控制傳送至 HTTP 伺服器之要求的精密應用程式。

[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) 需要由 [**HTTPOPENREQUEST**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)建立的 HTTP 要求控制碼、包含標頭的字串、標頭的長度，以及修飾詞。

### <a name="sending-a-request"></a>傳送要求

[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) 會建立與網際網路的連線，並將要求傳送至指定的網站。 此函數需要 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)建立的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) 也可以傳送額外的標頭或選擇性資訊。 選用資訊通常用於將資訊寫入伺服器的作業，例如 PUT 和 POST。

在 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)傳送要求之後，應用程式可以在 [**HINTERNET**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所建立的 [**HttpOpenRequest**](appendix-a-hinternet-handles.md)控制碼上，使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)、 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)和 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)函數來下載伺服器的資源。

### <a name="posting-data-to-the-server"></a>將資料張貼到伺服器

若要將資料張貼至伺服器，呼叫 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 的 HTTP 動詞命令必須是 POST 或 PUT。 接著，必須將包含 POST 資料的緩衝區位址傳遞至 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)中的 *lpOptional* 參數。 *DwOptionalLength* 參數應該設定為數據的大小。

您也可以使用 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)函數，在使用 [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)傳送的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼上張貼資料。

### <a name="getting-information-about-a-request"></a>取得要求的相關資訊

[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 可讓應用程式取得 HTTP 要求的相關資訊。 函數需要 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)或 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)所建立的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼、資訊層級值，以及緩衝區長度。 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 也接受緩衝區來儲存資訊和以零為基底的標頭索引，以列舉具有相同名稱的多個標頭。

### <a name="downloading-resources-from-the-www"></a>從 WWW 下載資源

使用 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 開啟要求，並使用 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)將其傳送至伺服器之後，應用程式可以使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)、 [**INTERNETQUERYDATAAVAILABLE**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)和 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) 函式，從 HTTP 伺服器下載資源。

下列範例會下載資源。 函數會接受目前視窗的控制碼、編輯方塊的識別碼，以及由 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)建立並由 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)傳送的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。 它會使用 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) 來判斷資源的大小，然後使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)進行下載。 然後，內容會顯示在編輯方塊中。


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 