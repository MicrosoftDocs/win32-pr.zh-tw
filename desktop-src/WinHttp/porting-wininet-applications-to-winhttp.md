---
description: 在需要存取 HTTP 用戶端堆疊的中介層和後端伺服器應用程式中，會將 Microsoft Windows HTTP 服務 (WinHTTP) 的目標。
ms.assetid: 5b0cf321-8f69-4526-a628-e6ca0f9d4a58
title: 將 WinINet 應用程式移植到 WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b111cd79e7ce7edfb09d43993ee2735ce09275f51c58bcfad319fb073dccc5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052006"
---
# <a name="porting-wininet-applications-to-winhttp"></a>將 WinINet 應用程式移植到 WinHTTP

在需要存取 HTTP 用戶端堆疊的中介層和後端伺服器應用程式中，會將 Microsoft Windows HTTP 服務 (WinHTTP) 的目標。 [Microsoft Windows Internet (WinINet) ](winhttp-start-page.md)提供用戶端應用程式的 HTTP 用戶端堆疊，以及檔案傳輸通訊協定 (FTP) 、SOCKSv4 和 Gopher 通訊協定的存取權。 本總覽有助於判斷將您的 WinINet 應用程式移植到 WinHTTP 是否有説明。 它也會說明特定的轉換需求。

-   [移植 WinINet 應用程式之前應考慮的事項](#things-to-consider-before-porting-your-wininet-application)
-   [對 WinINet 函數的 WinHTTP 對等專案](#winhttp-equivalents-to-wininet-functions)
-   [非同步要求的不同處理](#different-handling-of-asynchronous-requests)
-   [WinHTTP 回呼通知的差異](#differences-in-winhttp-callback-notifications)
-   [驗證差異](#authentication-differences)
-   [安全 HTTP 交易的差異](#differences-in-secure-http-transactions)

## <a name="things-to-consider-before-porting-your-wininet-application"></a>移植 WinINet 應用程式之前應考慮的事項

如果您的應用程式可受益于下列情況，請考慮將 WinINet 應用程式移植到 WinHTTP：

-   伺服器安全的 HTTP 用戶端堆疊。
-   最小化堆疊使用方式。
-   伺服器應用程式的擴充性。
-   與平臺相關的 Api 相依性較少。
-   支援執行緒模擬。
-   服務易記的 HTTP 堆疊。
-   存取可編寫腳本的 [**WinHttpRequest**](winhttprequest.md) 物件。

如果您的 WinINet 應用程式必須支援下列其中一項或多項作業，請勿考慮將您的 WinINet 應用程式移植到 WinHTTP：

-   來自 HTTP 堆疊的 FTP 或 Gopher 通訊協定。
-   支援使用 SOCKSv4 通訊協定與 SOCKS proxy 進行通訊。
-   自動撥號服務。

如果您決定將應用程式移植到 WinHTTP，下列各節會引導您完成轉換程式。

如需 WinINet 和 WinHTTP 的範例應用程式，請比較 WinINet 的 AsyncDemo 範例與 WinHTTP 的 AsyncDemo 範例。

## <a name="winhttp-equivalents-to-wininet-functions"></a>對 WinINet 函數的 WinHTTP 對等專案

下表列出與 HTTP 用戶端堆疊相關的 WinINet 函式，以及 WinHTTP 對等專案。

如果您的應用程式需要未列出的 WinINet 函式，請勿將應用程式移植至 WinHTTP。



| WinINet 函數                                                       | WinHTTP 對等專案                                                                                                                                                                                     | 值得注意的變更                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/wininet/nf-wininet-httpaddrequestheadersa)             | [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                                                                                                                                           | 無。                                                                                                                                                                                                                                                                                                                                |
| [**HttpEndRequest**](/windows/desktop/api/wininet/nf-wininet-httpendrequesta)                           | [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)                                                                                                                                               | 內容值會設定為 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 或 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)。 要求選項是以 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)設定。 傳送要求之後，必須呼叫 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 。                      |
| [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)                         | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                       | 內容值會設定為 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 或 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)。                                                                                                                                                                                                      |
| [**HttpQueryInfo**](/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa)                             | [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)                                                                                                                                                     | 無。                                                                                                                                                                                                                                                                                                                                |
| [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta)                         | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | 您可以使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)來設定內容值。                                                                                                                                                                                                                                                  |
| [**HttpSendRequestEx**](/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa)                     | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | 無法提供緩衝區。                                                                                                                                                                                                                                                                                                          |
| [**InternetCanonicalizeUrl**](/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla)         | 沒有對等項目                                                                                                                                                                                          | Url 現在會在 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)中放入標準格式。                                                                                                                                                                                                                                              |
| [**InternetCheckConnection**](/windows/desktop/api/wininet/nf-wininet-internetcheckconnectiona)         | 沒有對等項目                                                                                                                                                                                          | 未在 WinHTTP 中執行。                                                                                                                                                                                                                                                                                                          |
| [**InternetCloseHandle**](/windows/desktop/api/wininet/nf-wininet-internetclosehandle)                 | [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)                                                                                                                                                       | 在 WinHTTP 中關閉父控制碼，並不會以遞迴方式關閉子控制碼。                                                                                                                                                                                                                                                         |
| [**InternetCombineUrl**](/windows/desktop/api/wininet/nf-wininet-internetcombineurla)                   | 沒有對等項目                                                                                                                                                                                          | 您可以使用 [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) 函式來組合 url。                                                                                                                                                                                                                                                |
| [**InternetConfirmZoneCrossing**](/windows/desktop/api/wininet/nf-wininet-internetconfirmzonecrossing) | 沒有對等項目                                                                                                                                                                                          | 未在 WinHTTP 中執行。                                                                                                                                                                                                                                                                                                          |
| [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                                                                                               | 內容值會設定為 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 或 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)。 要求選項是以 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)設定。 使用者認證會以 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)設定。                                 |
| [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)                       | [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)                                                                                                                                                             | 與 ICU ESCAPE 旗標相反的行為 \_ ：使用 [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)時，此旗標會使 (% xx) 的 ESCAPE 序列轉換成字元，但使用 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)時，它會導致必須從 HTTP 要求中將的字元轉換成 ESCAPE 序列。 |
| [**InternetCreateUrl**](/windows/desktop/api/wininet/nf-wininet-internetcreateurla)                     | [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                           | 無。                                                                                                                                                                                                                                                                                                                                |
| [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg)                       | 沒有對等項目                                                                                                                                                                                          | 由於 WinHTTP 是以伺服器端應用程式為目標，因此它不會執行任何使用者介面。                                                                                                                                                                                                                                   |
| [**InternetGetCookie**](/windows/desktop/api/wininet/nf-wininet-internetgetcookiea)                     | 沒有對等項目                                                                                                                                                                                          | WinHTTP 不會在會話之間保存資料，也無法存取 WinINet cookie。                                                                                                                                                                                                                                                    |
| [**InternetOpen**](/windows/desktop/api/wininet/nf-wininet-internetopena)                               | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                                                                                     | 無。                                                                                                                                                                                                                                                                                                                                |
| [**InternetOpenUrl**](/windows/desktop/api/wininet/nf-wininet-internetopenurla)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)、 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)、 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)、 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) | 這項功能可在列出的 WinHTTP 函式中使用。                                                                                                                                                                                                                                                                     |
| [**InternetQueryDataAvailable**](/windows/desktop/api/wininet/nf-wininet-internetquerydataavailable)   | [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)                                                                                                                                         | 沒有保留的參數。                                                                                                                                                                                                                                                                                                              |
| [**InternetQueryOption**](/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona)                 | [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)                                                                                                                                                       | WinHTTP 提供一組不同于 WinINet 的選項。 如需 WinHTTP 提供的詳細資訊和選項，請參閱 [**選項旗標**](option-flags.md)。                                                                                                                                                                               |
| [**InternetReadFile**](/windows/desktop/api/wininet/nf-wininet-internetreadfile)                       | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | 無。                                                                                                                                                                                                                                                                                                                                |
| [**InternetReadFileEx**](/windows/desktop/api/wininet/nf-wininet-internetreadfileexa)                   | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | 緩衝區是以指標定址的記憶體區域，而不是結構。                                                                                                                                                                                                                                                  |
| [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona)                     | [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                           | 無。                                                                                                                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback)     | [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)                                                                                                                                           | 如需詳細資訊，請參閱本主題中的「非同步要求的不同處理方式」。                                                                                                                                                                                                                                               |
| [**InternetTimeFromSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimefromsystemtime)   | [**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)                                                                                                                                         | 無。                                                                                                                                                                                                                                                                                                                                |
| [**InternetTimeToSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimetosystemtime)       | [**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)                                                                                                                                             | 無。                                                                                                                                                                                                                                                                                                                                |
| [**InternetWriteFile**](/windows/desktop/api/wininet/nf-wininet-internetwritefile)                     | [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)                                                                                                                                                           | 無。                                                                                                                                                                                                                                                                                                                                |



 

## <a name="different-handling-of-asynchronous-requests"></a>非同步要求的不同處理

請注意，在 WinINet 和 WinHTTP 中，某些函數可以同步或非同步方式完成非同步要求。 您的應用程式必須處理這兩種情況。 WinINet 和 WinHTTP 如何處理這些可能的非同步函式有很大的差異。

WinINet

-   同步完成：如果可能的非同步 WinINet 函式呼叫以同步方式完成，則函數的 OUT 參數會傳回作業的結果。 發生錯誤時，請在 WinINet 函式呼叫之後呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 來取得錯誤碼。

-   非同步完成：如果可能非同步函式呼叫以非同步方式完成，則會在回呼函式中存取作業的結果和任何錯誤。 回呼函式會在背景工作執行緒上執行，而不是在進行初始函式呼叫的執行緒上執行。

換句話說，您的應用程式必須重複邏輯，以在兩個位置處理這類作業的結果：兩者都緊接在函式呼叫和回呼函數中。

WinHTTP 藉由讓您只在回呼函式中執行操作邏輯來簡化此模型，不論作業是以同步方式或非同步方式完成，都會收到完成通知。 啟用非同步作業時，WinHTTP 函數的 OUT 參數不會傳回有意義的資料，而且必須設定為 **Null**。

從應用程式的觀點來看，WinHTTP 中的非同步和同步完成之間唯一的差異在於執行回呼函數的位置。

WinHTTP

-   同步完成：當作業同步完成時，會在與原始函數呼叫相同的執行緒中執行的回呼函式中傳回結果。

-   非同步完成：當作業以非同步方式完成時，會在背景工作執行緒中執行的回呼函數中傳回結果。

雖然大部分的錯誤也可以完全在回呼函式內進行處理，但由於錯誤不正確 \_ \_ 參數或藉由呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)而抓取的其他類似錯誤，因此必須針對函式準備 WinHTTP 應用程式以傳回 FALSE。

不同于 WinINet （可同時執行多個非同步作業），WinHTTP 會針對每個要求控制碼強制執行一個擱置中非同步作業的原則。 如果有一個作業暫止，並呼叫另一個 WinHTTP 函式，則第二個函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤 \_ 無效 \_ 的作業。

WinHTTP 藉由讓您只在回呼函式中執行操作邏輯來簡化此模型，不論作業是以同步方式或非同步方式完成，都會收到完成通知。 啟用非同步作業時，WinHTTP 函數的 OUT 參數不會傳回有意義的資料，而且必須設定為 **Null**。

## <a name="differences-in-winhttp-callback-notifications"></a>WinHTTP 回呼通知的差異

狀態回呼函式會透過通知旗標接收作業狀態的更新。 在 WinHTTP 中，會使用 [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)函數的 *dwNotificationFlags* 參數來選取通知。 使用 **WINHTTP \_ 回呼旗 \_ 標 \_ 所有 \_ 通知** 旗標，以通知所有狀態更新。

指出特定作業已完成的通知稱為完成通知，或只是完成。 在 WinINet 中，每次回呼函式收到完成時， *lpvStatusInformation* 參數都包含 [**網際網路 \_ 非同步 \_ 結果**](/windows/desktop/api/wininet/ns-wininet-internet_async_result) 結構。 在 WinHTTP 中，此結構不適用於所有的完成。 請務必參閱 [**WINHTTP \_ 狀態 \_ 回呼**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback)的參考頁面，其中包含通知的相關資訊，以及每個通知可預期的資料類型。

在 WinHTTP 中，單次完成（ **WinHTTP \_ 回呼 \_ 狀態 \_ 要求 \_ 錯誤**）表示作業失敗。 所有其他完成表示作業成功。

WinINet 和 WinHTTP 都會使用使用者定義的內容值，將主要執行緒的資訊傳遞給狀態回呼函式，該函式可在背景工作執行緒上執行。 在 WinINet 中，狀態回呼函式所使用的內容值是藉由呼叫數個函式的其中一個來設定。 在 WinHTTP 中，內容值只會使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 或 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)來設定。 基於這個原因，WinHTTP 可能會在設定內容值之前發生通知。 如果回呼函數在設定內容值之前收到通知，應用程式必須準備好在回呼函數的 *dwCoNtext* 參數中接收 **Null** 。

## <a name="authentication-differences"></a>驗證差異

在 WinINet 中，使用者認證是藉由呼叫 [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona) 函式來設定，並使用與下列程式碼範例中所提供類似的程式碼。

``` syntax
// Use the WinINet InternetSetOption function to set the 
// user credentials to the user name contained in strUsername 
// and the password to the contents of strPassword.
       
InternetSetOption( hRequest, INTERNET_OPTION_PROXY_USERNAME, 
                   strUsername, strlen(strUsername) + 1 );

InternetSetOption( hRequest, INTERNET_OPTION_PROXY_PASSWORD, 
                   strPassword, strlen(strPassword) + 1 );
```

為了提供相容性，您可以使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函式在 WinHTTP 中設定使用者認證，但不建議這麼做，因為這可能會造成安全性弱點。

相反地，當應用程式在 WinHTTP 中收到401狀態碼時，建議的設定認證方法是先識別使用 [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) 的驗證配置，然後使用 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)來設定認證。 下列程式碼範例示範如何執行這項作業。

``` syntax
DWORD dwSupportedSchemes;
DWORD dwPrefered;
DWORD dwTarget;

// Obtain the supported and first schemes.
WinHttpQueryAuthSchemes( hRequest, &dwSupportedSchemes, &dwPrefered, &dwTarget );

// Set the credentials before resending the request.
WinHttpSetCredentials( hRequest, dwTarget, dwPrefered, strUsername, strPassword, NULL );
```

因為在 WinHTTP 中沒有對等 [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg) ，透過使用者介面取得認證的應用程式必須提供自己的介面。

和 WinINet 不同的是，WinHTTP 不會快取密碼。 必須針對每個要求提供有效的使用者認證。

WinHTTP 不支援 WinINet 所支援的 (DPA) 配置的分散式密碼驗證。 但是，WinHTTP 支援 Microsoft Passport 1.4。 如需在 WinHTTP 中使用 Passport 驗證的詳細資訊，請參閱 [winHTTP 中的 Passport 驗證](passport-authentication-in-winhttp.md)。

WinHTTP 不依賴 Internet Explorer 設定來判斷自動登入原則。 相反地，自動登入原則會以 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)設定。 如需 WinHTTP 中的驗證（包括自動登入原則）的詳細資訊，請參閱 [winHTTP 中的驗證](authentication-in-winhttp.md)。

## <a name="differences-in-secure-http-transactions"></a>安全 HTTP 交易的差異

在 WinINet 中，使用 [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)或 [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)來起始安全會話，但在 WinHTTP 中，您必須使用 **winHTTP 旗標 \_ \_ 安全** 旗標來呼叫 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 。

在安全的 HTTP 交易中，伺服器憑證可以用來向用戶端驗證服務器。 在 WinINet 中，如果伺服器憑證包含錯誤， [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta) 會失敗並提供憑證錯誤的詳細資料。

在 WinHttp 中，會根據版本處理伺服器憑證錯誤，如下所示：

-   從 WinHttp 5.1 開始，如果伺服器憑證失敗或包含錯誤， [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 的呼叫會報告回呼函式中的 **WinHttp \_ 回呼 \_ 狀態 \_ 安全 \_ 失敗** 。 如果忽略 **WinHttpSendRequest** 所產生的錯誤，後續對 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 的呼叫會失敗，並出現錯誤 WINHTTP 作業已 \_ 取消的 \_ \_ 錯誤。
-   在 WinHTTP 5.0 中，伺服器憑證的錯誤預設不會導致要求失敗。 相反地，在具有 **WINHTTP \_ 回呼 \_ 狀態 \_ 安全 \_ 失敗** 通知的回呼函式中報告錯誤。

在某些較早的平臺上，WinINet 支援私用通訊技術 (PCT) 和/或 Fortezza 通訊協定，但不 Windows XP。

WinHTTP 不支援任何平臺上的 PCT 和 Fortezza 通訊協定，而是依賴安全通訊端層 (SSL) 2.0、SSL 3.0 或傳輸層安全性 (TLS) 1.0。

 

 
