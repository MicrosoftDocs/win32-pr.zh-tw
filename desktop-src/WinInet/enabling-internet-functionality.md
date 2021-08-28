---
title: 啟用網際網路功能
description: 使用 WinINet 函式之前，應用程式應該嘗試使用 InternetAttemptConnect 函式來建立與網際網路的連接。
ms.assetid: 80747c0d-5a09-4ffa-a0ca-b051b82acbf8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f4780b508059c088e2948829662171fd6df46f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885492"
---
# <a name="enabling-internet-functionality"></a>啟用網際網路功能

使用 WinINet 函式之前，應用程式應該嘗試使用 [**InternetAttemptConnect**](/windows/desktop/api/Wininet/nf-wininet-internetattemptconnect) 函式來建立與網際網路的連接。 此函數會呼叫 [撥號] 對話方塊來起始網際網路連線，或檢查連接是否已存在。 如果此函式失敗，應用程式可進入離線模式，讓它能夠存取在先前連線到網際網路時所快取的資訊。

使用 [**InternetCheckConnection**](/windows/desktop/api/Wininet/nf-wininet-internetcheckconnectiona) 函式來檢查網際網路的連線。 它會嘗試 ping 傳遞給函式之 URL 所指定的伺服器。 如果 \_ 已設定旗標 ICC 強制連線旗標， \_ \_ 且 URL 為 **Null**，則此函式會檢查伺服器資料庫中是否有最近伺服器的專案。 如果有，則函式會偵測該伺服器。

接下來，使用 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函式來建立用戶端應用程式所使用之網際網路連接的特性。 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)會建立用來建立 [HTTP](http-sessions.md)[ftp](ftp-sessions.md)會話的根 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 不會測試網際網路的連線，以確認傳遞給函式的特性是否正確。

使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 函式來建立特定的會話。 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 會使用傳遞給它的引數，初始化指定之網站的會話，並建立屬於根控制碼之分支的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼。 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 不會嘗試存取或建立與指定網站的連接，但 FTP 會話的情況除外。 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)和 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 函式會使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 所建立的控制碼來建立與指定網站的連接。

## <a name="using-internetopen"></a>使用 InternetOpen

若要啟用與網際網路的連線，必須使用 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)建立根 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。 使用者代理程式的相關資訊 (呼叫網際網路功能的應用程式) 、網際網路的存取類型、proxy 名稱、主機和略過 proxy 的位址，以及將行為傳遞給 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)。

### <a name="setting-the-user-agent"></a>設定使用者代理程式

呼叫應用程式應該提供一個字串，其中包含存取網際網路的應用程式或實體的名稱，以存取 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)的 *lpszAgent* 參數。 這個字串是用來做為 HTTP 通訊協定中的使用者代理程式。 例如，Microsoft Internet Explorer 使用「Microsoft Internet Explorer」。

### <a name="setting-access-types"></a>設定存取類型

[**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 支援三種存取類型：

-   如果執行 \_ \_ \_ 應用程式的系統使用直接連線至網際網路，請使用網際網路開放式型別直接存取。 不會使用 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)的 *lpszProxyName* 和 *lpszProxyBypass* 參數，而且應該設定為 **Null**。
-   如果執行 \_ \_ \_ 應用程式的系統使用一或多個 PROXY 伺服器來存取網際網路，請使用 internet OPEN TYPE PROXY。 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 會使用 *lpszProxyName* 所指示的 proxy 伺服器，並針對 *lpszProxyBypass* 指定的任何主機名稱或 IP 位址略過 proxy。
-   使用 INTERNET \_ OPEN \_ TYPE \_ PRECONFIG 來指示您的應用程式從登錄中取得設定。 這通常是最好的選擇，因為大部分的應用程式（包括網頁瀏覽器）都會使用此選項。

INTERNET \_ OPEN \_ TYPE \_ PRECONFIG 會查看登錄值 **ProxyEnable**、 **ProxyServer** 和 **ProxyOverride**。 這些值位於「HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet 設定」之下。

如果 **ProxyEnable** 為零，則應用程式會使用網際網路 \_ 開放式 \_ 型別直接存取 \_ 。 否則，應用程式會使用網際網路 \_ 開放式 \_ 型別 \_ PROXY，並使用 **ProxyServer** 和 **ProxyOverride** 資訊。

只有在安裝 Internet Explorer 時，WinINet 函式才會提供 SOCKS 類型 proxy 的支援。 Internet Explorer 安裝包含支援 SOCKS proxy 所需的 Wsock32n.dll 檔案。 Wsock32n.dll 無法轉散發套件。

### <a name="listing-proxy-servers"></a>列出 Proxy 伺服器

WinINet 辨識兩種類型的 proxy： CERN 類型 proxy (僅限 HTTP) 和 TIS FTP proxy (FTP) 。 如果 Internet Explorer 已安裝，WinINet 也支援 SOCKS 類型 proxy。 根據預設， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會假設指定的 PROXY 是 CERN proxy。 如果存取類型設定為 INTERNET \_ open \_ type \_ DIRECT 或 internet \_ open \_ type \_ PRECONFIG，則 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)的 *lpszProxyName* 參數應該設定為 **Null**。 否則，傳遞給 *lpszProxyName* 的值必須包含以空格分隔之字串的 proxy。 Proxy 清單可以包含用來存取 proxy 的埠號碼。

若要列出特定通訊協定的 proxy，字串必須採用 "" &lt; protocol &gt; &lt; protocol： &gt; //<proxy \_ name> "" 格式。 有效的通訊協定為 HTTP、HTTPS 和 FTP。 例如，若要列出 FTP proxy，有效的字串會是 "" ftp = FTP：//ftp \_ proxy \_ name： 21 ""，其中 ftp \_ PROXY \_ 名稱是 ftp proxy 的名稱，而21是必須用來存取 proxy 的埠號碼。 如果 proxy 使用該通訊協定的預設通訊埠號碼，則可以省略埠號碼。 如果 proxy 名稱本身列出，則會使用它做為未指定特定 proxy 之任何通訊協定的預設 proxy。 例如，"" HTTP = https://http\_proxy other "" 會 \_ 對任何 HTTP 作業使用 HTTP proxy，其他所有通訊協定則會使用其他通訊協定。

根據預設，此函式會假設 *lpszProxyName* 所指定的 PROXY 是 CERN proxy。 應用程式可以指定一個以上的 proxy，包括不同通訊協定的不同 proxy。 例如，如果您指定 "" ftp = ftp：//ftp-gw HTTP = https://jericho:99 proxy ""，ftp 要求會透過 ftp-gw proxy （接聽埠21）發出，而 HTTP 要求則是透過名為 jericho 的 CERN proxy 來接聽，而此 proxy 會接聽埠99。 否則，HTTP 要求會透過名為 proxy 的 CERN proxy 來進行，它會接聽埠80。 請注意，如果應用程式只使用 FTP，就不需要指定 "" ftp = FTP：//ftp-gw： 21 "」。 它可以只指定 "" ftp-gw ""。 只有當應用程式針對 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所傳回的每個控制碼使用一個以上的通訊協定時，才需要指定通訊協定名稱。

### <a name="listing-the-proxy-bypass"></a>列出 Proxy 略過

不應傳送至 proxy 的主機名稱或 IP 位址可以列在 proxy 略過清單中。 這份清單可以包含萬用字元 " \* "，這會導致應用程式針對符合指定模式的位址略過 proxy 伺服器。 若要列出多個位址和主機名稱，請在 proxy 略過字串中以分號分隔它們。 如果指定 " &lt; local &gt; " 宏，函式會略過不包含句號的任何主機名稱的 proxy。

根據預設，WinINet 將會略過使用主機名稱 "localhost"、"回送"、"127.0.0.1" 或 " \[ ：： 1" 之要求的 proxy \] 。 這種行為存在的原因是，遠端 proxy 伺服器通常不會正確地解析這些位址。

**Internet Explorer 9：** 您可以使用「< 回送>」宏，從 proxy 略過清單中移除本機電腦。

下列範例顯示使用不同的 proxy 略過字串來 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 的範例呼叫。 每個呼叫上方的批註會描述略過字串對於從其所建立之 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼存取的主機名稱有何影響。


```C++
HINTERNET hInternetRoot;

/* bypass the proxy for any host name that does not 
    contain a period */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("<local>"), 0);

/* bypass the proxy for any host name that starts with the 
    letters "ms" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("ms*"), 0);

/* bypass the proxy for any host name that contains "int", 
    such as "internet" and "painter" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("*int*"), 0);

/* bypass the proxy for the host name "example" and any 
    host name that contains "test" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("example *test*"), 0);

/* Disable the loopback proxy bypass for localhost */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("127.0.0.1:8888"),TEXT("<-loopback>"), 0);
```



## <a name="using-internetconnect"></a>使用 InternetConnect

若要開始會話， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 函式必須從 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函數所傳回的根控制碼建立控制碼。 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 會設定伺服器位址、埠號碼、使用者名稱、密碼和服務類型。

[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會使用 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所建立的根 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼來建立會話控制碼。 如果在呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)時設定了 [INTERNET \_ 旗標 \_ ASYNC](api-flags.md)旗標，則對 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)的呼叫應該包含非零的內容值。

伺服器名稱可包含主機名稱 (例如，"www.servername.com" ) 或網站的 IP 號碼（以 ASCII 點分隔的十進位格式） (例如 "10.0.1.45" ) 。

伺服器埠是傳輸控制通訊協定/網際網路通訊協定 (TCP/IP) 埠號碼，以連接到伺服器。 [](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)如果使用網際網路通訊 \_ \_ 埠號碼值無效，InternetConnect 會針對選取的服務類型使用預設埠 \_ 。 下表包含 WinINet 的伺服器埠預設值。




| 值 | 意義 | 
|-------|---------|
| INTERNET_DEFAULT_FTP_PORT | 使用 ftp 伺服器的預設埠 (埠 21) 。 | 
| INTERNET_DEFAULT_GOPHER_PORT | 使用 (埠 70) 的 Gopher 伺服器的預設埠。<blockquote>[!Note]<br />WindowsXP 和 Windows Server 2003 R2 及更早版本。</blockquote><br /> | 
| INTERNET_DEFAULT_HTTP_PORT | 使用 HTTP 伺服器的預設埠 (埠 80) 。 | 
| INTERNET_DEFAULT_HTTPS_PORT | 使用 HTTPs 伺服器的預設埠 (埠 443) 。 | 
| INTERNET_DEFAULT_SOCKS_PORT | 使用 (埠 1080) 的 SOCKS 防火牆伺服器的預設埠。 | 




 

### <a name="defining-the-user-name-and-password"></a>定義使用者名稱和密碼

*LpszUsername* 的值是以 **null** 終止之字串的位址，其中包含要登入之使用者的名稱。 如果這個參數是 **Null**，則函式會使用適當的預設值，但 HTTP 除外。 HTTP 中的 **Null** 參數會導致伺服器傳回錯誤。 若是 FTP 通訊協定，預設值為 anonymous。

*LpszPassword* 的值是以 **null** 終止之字串的位址，其中包含登入密碼。 如果 *lpszUsername* 和 *LpszPassword* 都是 **Null**，則函式會使用預設的匿名密碼。 在 FTP 的案例中，預設的匿名密碼是使用者的電子郵件名稱。 如果 *lpszUsername* 不是 **Null** ，而且 *lpszPassword* 為 **null**，則函式會使用空白密碼。 *LpszUsername* 和 *lpszPassword* 有四個可能的設定，這些設定會產生下表所示的行為。



| *lpszUsername*      | *lpszPassword*      | 傳送至 FTP 伺服器的使用者名稱 | 傳送至 FTP 伺服器的密碼 |
|---------------------|---------------------|------------------------------|-----------------------------|
| **NULL**            | **NULL**            | 匿名                  | 使用者的電子郵件名稱           |
| 非 **Null** 字串 | **NULL**            | *lpszUsername*               | ""                          |
| **NULL**            | 非 **Null** 字串 | ERROR                        | ERROR                       |
| 非 **Null** 字串 | 非 **Null** 字串 | *lpszUsername*               | *lpszPassword*              |



 

您可以使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 和 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 函數來變更這項資訊。 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 會變更使用者名稱和密碼值，而 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 會顯示要求適當使用者名稱和密碼的對話方塊。

### <a name="defining-the-session"></a>定義會話

若要定義正在建立的會話，請設定 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)的服務類型、旗標和內容值。

有兩種服務類型可供 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)：網際網路 \_ 服務 \_ FTP 和網際網路 \_ 服務 \_ HTTP。 \_ \_ HTTP 和 HTTPS 會話都使用網際網路服務 HTTP。

[網際網路 \_旗標 \_ 被動](api-flags.md) 是 WinINet 函式所使用的唯一服務特定旗標。 此旗標可在服務類型為網際網路 \_ 服務 FTP 以 \_ 使用被動 FTP 語義時設定。

對於所有同步作業而言， *dwCoNtext* 的值應該設定為零。 如果在呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)的呼叫中設定 [網際網路 \_ 旗標 \_ ASYNC](api-flags.md)旗標來建立異步操作，則應該為 *dwCoNtext* 提供非零值。 如需非同步作業的詳細資訊，請參閱 [設定非同步作業](common-functions.md)。

針對 FTP 會話， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 會嘗試建立與網際網路上伺服器的連線。 針對 HTTP 會話， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 會在另一個函數嘗試從伺服器取得資訊之前，不會建立連接。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

