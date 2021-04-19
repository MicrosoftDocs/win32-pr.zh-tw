---
title: 處理驗證
description: 某些 proxy 和伺服器需要驗證，才能授與存取網際網路上的資源。
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82d8cd93f1010c71560d856793ad06d8bc5d9d5
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380852"
---
# <a name="handling-authentication"></a>處理驗證

某些 proxy 和伺服器需要驗證，才能授與存取網際網路上的資源。 WinINet 函數支援 HTTP 會話的伺服器和 proxy 驗證。 Ftp 伺服器的驗證必須由 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 函數處理。 目前不支援 FTP 閘道驗證。

## <a name="about-http-authentication"></a>關於 HTTP 驗證

如果需要驗證，用戶端應用程式會收到狀態碼401（如果伺服器需要驗證）或407（如果 proxy 需要驗證的話）。 使用狀態碼時，proxy 或伺服器會傳送一個或多個驗證回應標頭，也就是 proxy 驗證的 Proxy 驗證 () 或 WWW-Authenticate (進行伺服器驗證) 。

每個驗證回應標頭都包含可用的驗證配置和領域。 如果支援多個驗證配置，伺服器會傳回多個驗證回應標頭。 領域值會區分大小寫，並定義 proxy 或伺服器上的保護空間。 例如，「WWW-驗證：基本領域 =」範例 "」標頭會是在需要伺服器驗證時所傳回的標頭範例。

傳送要求的用戶端應用程式可以藉由在要求中包含授權標頭欄位來自行驗證。 授權標頭會包含驗證配置，以及該配置所需的適當回應。 例如， \<username:password> 如果用戶端收到驗證回應標頭 "WWW-驗證：基本領域 =" 範例 ""，就會將標頭 "Authorization： basic" 新增至要求，並將其重新傳送至伺服器。

驗證架構有兩種一般類型：

-   基本驗證配置，其中的使用者名稱和密碼會以純文字傳送給伺服器。
-   挑戰-回應配置，可允許挑戰回應的格式。

基本驗證配置是以模型為基礎，用戶端必須使用每個領域的使用者名稱和密碼進行驗證。 如果傳送的授權標頭包含有效的使用者名稱和密碼，伺服器會為要求提供服務。

挑戰-回應配置可讓您進行更安全的驗證。 如果要求需要使用挑戰回應配置進行驗證，則會將適當的狀態碼和驗證標頭傳回給用戶端。 接著，用戶端必須使用 negotiate 重新傳送要求。 伺服器會傳回具有挑戰的適當狀態碼，然後用戶端會要求以適當的回應重新傳送要求，以取得所要求的服務。

下表列出驗證配置、驗證類型、支援它們的 DLL，以及配置的描述。



| 配置                                    | 類型               | DLL                  | Description                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 基本 (純文字)                          | basic              | Wininet.dll          | 使用 base64 編碼的字串，其中包含使用者名稱和密碼。                                                                                                                                                                                                                                                                             |
| Digest                                    | 挑戰-回應 | Digest.dll           | 挑戰-回應配置，會挑戰使用 nonce (伺服器指定的資料字串) 值。 有效的回應包含使用者名稱、密碼、指定的 nonce 值、HTTP 方法，以及要求的統一資源識別項 (URI) 的總和檢查碼。 摘要式驗證支援已在 Microsoft Internet Explorer 5 中推出。 |
| NT LAN Manager (NTLM)                      | 挑戰-回應 | Winsspi.dll          | 以使用者名稱為基礎的挑戰回應配置。                                                                                                                                                                                                                                                                             |
| Microsoft Network (MSN)                    | 挑戰-回應 | Msnsspc.dll          | MSN 的驗證配置。                                                                                                                                                                                                                                                                                                     |
|  (DPA) 的分散式密碼驗證 | 挑戰-回應 | Msapsspc.dll         | 類似于 MSN 驗證，也是由 Microsoft 網路使用。                                                                                                                                                                                                                                                                           |
| 遠端複雜密碼驗證 (RPA)     | CompuServe         | Rpawinet.dll，da.dll | CompuServe 驗證配置。 如需詳細資訊，請參閱 [RPA 機制規格](https://www.compuserve.com/)。                                                                                                                                                                                                    |



 

針對基本驗證以外的任何其他作業，除了安裝適當的 DLL 之外，還必須設定登錄機碼。

如果需要驗證，則應該在 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)的呼叫中使用 [網際網路 \_ 旗標 \_ 保留 \_ 連接](api-flags.md)旗標。 \_ \_ \_ NTLM 和其他類型的驗證都需要網際網路旗標保留連線旗標，才能在完成驗證程式時維持連接。 如果未維護連接，則必須使用 proxy 或伺服器重新開機驗證程式。

即使需要驗證， [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 和 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) 函式也會順利完成。 差別在於，在標頭檔和 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 中傳回的資料會收到一個 HTML 網頁，通知使用者狀態碼。

### <a name="registering-authentication-keys"></a>註冊驗證金鑰

INTERNET \_ OPEN \_ TYPE \_ PRECONFIG 會查看登錄值 **ProxyEnable**、 **ProxyServer** 和 **ProxyOverride**。 這些值位於 [ **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**] 下。

針對 Basic 以外的驗證架構，必須將金鑰新增至登錄的 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Internet Explorer** \\ **安全性**。 **DWORD** 值 **旗標** 應以適當的值設定。 下列清單顯示 **旗標** 值的可能值。

-   外掛程式 \_ 驗證 \_ 旗 \_ 標 \_ \_ 每個 TCPIP 的唯一內容 \_ (值 = 0x01) 

    每個傳輸控制通訊協定/網際網路通訊協定 (TCP/IP) 通訊端包含不同的內容。 否則，會針對每個領域或區塊 URL 範本傳遞新的內容。

-   外掛程式 \_ 驗證 \_ 旗標 \_ 可以 \_ 處理 \_ UI (值 = 0x02) 

    此 DLL 可以處理自己的使用者輸入。

-   外掛程式 \_ 驗證 \_ 旗標 \_ 無法 \_ 處理 \_ 任何 \_ PASSWD (value = 0x04) 

    此 DLL 可以進行驗證，而不提示使用者輸入密碼。

-   外掛程式 \_ 驗證 \_ 旗標 \_ 沒有 \_ 領域 (值 = 0x08) 

    此 DLL 不使用標準 HTTP 領域字串。 任何顯示為領域的資料都是配置特定的資料。

-   外掛程式 \_ 驗證 \_ 旗 \_ 標 \_ 保持 \_ 不 \_ 需要的狀態 (值 = 0x10) 

    此 DLL 不需要持續連線，就能進行挑戰回應順序。

例如，若要加入 ntlm 驗證，必須在 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Internet Explorer** \\ **安全性** 中加入金鑰 ntlm。 在 **[ \_ HKEY \_ 本機電腦** \\ **軟體** \\ **Microsoft** \\ **Internet Explorer** \\ **安全性** \\ **NTLM**] 下，必須新增字串值 **DLLFile** 和 **DWORD** 值 **旗標**。 **DLLFile** 必須設定為 Winsspi.dll，且 **旗標** 必須設定為0x08。

### <a name="server-authentication"></a>伺服器驗證

當伺服器收到需要驗證的要求時，伺服器會傳回401狀態碼訊息。 在該訊息中，伺服器應該包含一或多個 WWW-Authenticate 回應標頭。 這些標頭包含伺服器可用的驗證方法。 WinINet 會選擇它所辨識的第一個方法。

除非通道是先使用 SSL 或 PCT 進行連結加密，否則基本驗證會提供弱式安全性。

[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)函式可用來取得使用者的使用者名稱和密碼資料，或自訂的使用者介面可以設計來取得資料。

自訂介面可以使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 函式來設定 [網際網路 \_ 選項 \_ 密碼](option-flags.md) 和 [網際網路選項使用者 \_ \_ 名稱](option-flags.md) 值，然後將要求重新傳送至伺服器。

### <a name="proxy-authentication"></a>Proxy 驗證

當用戶端嘗試使用需要驗證的 proxy 時，proxy 會將407狀態碼訊息傳回給用戶端。 在該訊息中，proxy 應該包含一或多個 Proxy-Authenticate 回應標頭。 這些標頭包含可從 proxy 取得的驗證方法。 WinINet 會選擇它所辨識的第一個方法。

[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)函式可用來取得使用者的使用者名稱和密碼資料，或是可以設計自訂的使用者介面。

自訂介面可以使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 函式來設定 [網際網路 \_ 選項 \_ proxy \_ 密碼](option-flags.md) 和 [網際網路 \_ 選項 proxy 使用者 \_ \_ 名稱](option-flags.md) 值，然後將要求重新傳送至 PROXY。

如果未設定 proxy 使用者名稱和密碼，WinINet 會嘗試使用伺服器的使用者名稱和密碼。 此行為可讓用戶端執行相同的自訂使用者介面，以用來處理伺服器驗證。

## <a name="handling-http-authentication"></a>處理 HTTP 驗證

您可以使用 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 或使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 的自訂函式來處理 HTTP 驗證，或新增自己的驗證標頭。 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 可以檢查與 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼相關聯的標頭，以找出隱藏的錯誤，例如來自 proxy 或伺服器的狀態碼。 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 可以用來設定 proxy 和伺服器的使用者名稱和密碼。 若為 MSN 和 DPA 驗證，則必須使用 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 來設定使用者名稱和密碼。

針對新增本身的 WWW-Authenticate 或 Proxy-Authenticate 標頭的任何自訂函數， [網際網路旗標不應將 \_ \_ 任何 \_ AUTH](api-flags.md) 旗標設定為停用驗證。

下列範例顯示如何使用 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 來處理 HTTP 驗證。


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



在此範例中，dwErrorCode 是用來儲存與 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)呼叫相關聯的任何錯誤。 即使 proxy 或伺服器需要驗證， [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)也會順利完成。 將 [錯誤] 旗標的 [旗標 \_ 錯誤 \_ UI] \_ \_ \_ 旗標傳遞給 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)時，函式會檢查標頭中是否有任何隱藏的錯誤。 這些隱藏的錯誤會包含任何驗證要求。 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 會顯示適當的對話方塊，提示使用者輸入必要的資料。 旗標 \_ 錯誤 \_ ui \_ 旗標 \_ 產生 \_ 資料和旗標 \_ 錯誤 \_ ui 旗標 \_ \_ 變更 \_ 選項旗標也應傳遞給 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)，如此函式就會為錯誤建立適當的資料結構，並將對話方塊的結果儲存在 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼中。

下列範例程式碼顯示如何使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)處理驗證。


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 