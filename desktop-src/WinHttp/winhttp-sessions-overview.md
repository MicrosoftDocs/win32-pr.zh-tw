---
description: Microsoft Windows HTTP Services (WinHTTP) 會公開一組 C/c + + 函式，可讓您的應用程式存取 Web 上的 HTTP 資源。 本主題概要說明如何使用這些函數來與 HTTP 伺服器互動。
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: WinHTTP 會話總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f7c2a3845b34ac306c1fb8d87441955ab9f4cfe0e1ea250737f62f993cd43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743900"
---
# <a name="winhttp-sessions-overview"></a>WinHTTP 會話總覽

Microsoft Windows HTTP Services (WinHTTP) 會公開一組 C/c + + 函式，可讓您的應用程式存取 Web 上的 HTTP 資源。 本主題概要說明如何使用這些函數來與 HTTP 伺服器互動。

-   [使用 WinHTTP API 來存取 Web](#using-the-winhttp-api-to-access-the-web)
-   [正在初始化 WinHTTP](#initializing-winhttp)
-   [開啟要求](#opening-a-request)
-   [新增要求標頭](#adding-request-headers)
-   [傳送要求](#sending-a-request)
-   [將資料張貼到伺服器](#posting-data-to-the-server)
-   [取得要求的相關資訊](#getting-information-about-a-request)
-   [從 Web 下載資源](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a>使用 WinHTTP API 來存取 Web

下圖顯示當與 HTTP 伺服器互動時，通常會呼叫 WinHTTP 函數的順序。 陰影方塊表示產生 [HINTERNET](hinternet-handles-in-winhttp.md) 控制碼的函式，而一般方塊代表使用這些控制碼的函式。

![建立控制碼的函式](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a>正在初始化 WinHTTP

在與伺服器互動之前，必須先呼叫 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)來初始化 WinHTTP。 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) 會建立會話內容來維護 HTTP 會話的詳細資料，並傳回會話控制碼。 [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)函式會使用此控制碼，指定目標 HTTP 或安全超文字傳輸通訊協定 (HTTPS) 伺服器。

> [!Note]  
> 在對特定資源提出要求之前，對 [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) 的呼叫不會產生與 HTTP 伺服器的實際連接。

 

## <a name="opening-a-request"></a>開啟要求

[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)函式會開啟特定資源的 HTTP 要求，並傳回其他 HTTP 函數可使用的 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼。 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 不會在呼叫時將要求傳送至伺服器。 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)函式會透過網路實際建立連線，並傳送要求。

下列範例顯示使用預設選項之 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 的範例呼叫。

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a>新增要求標頭

[**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)函式可讓應用程式將額外的自由格式要求標頭附加至 HTTP 要求控制碼。 它適用于需要精確控制傳送至 HTTP 伺服器之要求的精密應用程式。

[**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)函式需要 [**WINHTTPOPENREQUEST**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立的 HTTP 要求控制碼、包含標頭的字串、標頭的長度，以及任何修飾詞。

下列修飾詞可以搭配 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)使用。



| 修飾詞                                                                                         | Description                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WINHTTP \_ ADDREQ \_ 旗標 \_ 新增**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | 如果標頭不存在，則加入標頭。 使用於 [**WINHTTP \_ ADDREQ \_ 旗標 \_ REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)。                                                                                                                                                                                                               |
| [**新的 WINHTTP \_ ADDREQ \_ 旗標 \_ \_ \_ 新增**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | 只有當標頭不存在時，才新增標頭;否則會傳回錯誤。                                                                                                                                                                                                                                                           |
| [**WINHTTP \_ ADDREQ \_ 旗標 \_ 聯合**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | 合併相同名稱的標頭。                                                                                                                                                                                                                                                                                                              |
| [**WINHTTP \_ ADDREQ \_ 旗 \_ 標 \_ 與 \_ 逗號聯合**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | 使用逗號合併相同名稱的標頭。 例如，新增 "Accept： text/ \* "，後面接著 "accept： audio/ \* " 且此旗標會形成單一標頭 "Accept： text/ \* ，audio/ \* "，導致第一個找到的標頭合併。 它是由呼叫應用程式所組成，以確保與合併/分開的標頭相關的配置一致。 |
| [**WINHTTP \_ ADDREQ \_ 旗 \_ 標 \_ 與 \_ 分號合併**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | 使用分號合併相同名稱的標頭。                                                                                                                                                                                                                                                                                            |
| [**WINHTTP \_ ADDREQ \_ 旗標 \_ 取代**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | 取代或移除標頭。 如果標頭值是空的，而且找到標頭，則會將它移除。 如果標頭值不是空的，則會取代標頭值。                                                                                                                                                                            |



 

## <a name="sending-a-request"></a>傳送要求

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)函式會建立與伺服器的連接，並將要求傳送至指定的網站。 此函數需要 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立的 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼。 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 也可以傳送額外的標頭或選擇性資訊。 選用資訊通常用於將資訊寫入伺服器的作業，例如 PUT 和 POST。

在 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)函式傳送要求之後，應用程式可以使用 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼上的 [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)和 [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)函數來下載伺服器的資源。

## <a name="posting-data-to-the-server"></a>將資料張貼到伺服器

若要將資料張貼至伺服器，呼叫 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)的 [*HTTP 動詞*](glossary.md)命令必須是 post 或 PUT。 當呼叫 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 時， *dwTotalLength* 參數應該設定為數據的大小（以位元組為單位）。 然後使用 [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) 將資料張貼至伺服器。

或者，將 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)的 *lpOptional* 參數設定為包含要張貼至伺服器之資料的緩衝區位址。 使用這項技術時，您必須將 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)的 *dwOptionalLength* 和 *dwTotalLength* 參數設定為要張貼之資料的大小。 以這種方式呼叫 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ，就不需要呼叫 [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)。

## <a name="getting-information-about-a-request"></a>取得要求的相關資訊

[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)函式可讓應用程式取得 HTTP 要求的相關資訊。 函數需要 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立的 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼、資訊層級值，以及緩衝區長度。 [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) 也接受緩衝區來儲存資訊和以零為基底的標頭索引，以列舉具有相同名稱的多個標頭。

使用在 [[**查詢資訊旗標**](query-info-flags.md)] 頁面上找到的任何資訊層級值，並以修飾詞來控制資訊儲存在 [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)的 *lpvBuffer* 參數中的格式。

## <a name="downloading-resources-from-the-web"></a>從 Web 下載資源

使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 函式開啟要求，並使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)將其傳送至伺服器，並準備要求控制碼以接收 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)的回應之後，應用程式就可以使用 [**WINHTTPREADDATA**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) 和 [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) 函式，從 HTTP 伺服器下載資源。

下列範例程式碼示範如何下載具有安全交易語義的資源。 範例程式碼會初始化 (API) 的 WinHTTP 應用程式開發介面、選取目標 HTTPS 伺服器，然後開啟並傳送此安全資源的要求。 [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) 可搭配要求控制碼使用，以判斷可供下載的資料量，然後使用 [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) 來讀取該資料。 此程式會重複執行，直到整份檔被抓取並顯示為止。


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



