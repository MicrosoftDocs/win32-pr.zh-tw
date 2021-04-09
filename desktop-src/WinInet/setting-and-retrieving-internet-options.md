---
title: 設定及抓取網際網路選項
description: 本主題說明如何使用 InternetSetOption 和 InternetQueryOption 函式來設定和捕獲網際網路選項。
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- 設定及抓取網際網路選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842603"
---
# <a name="setting-and-retrieving-internet-options"></a>設定及抓取網際網路選項

本主題說明如何使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 和 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 函式來設定和捕獲網際網路選項。

您可以在 Microsoft Internet Explorer 的指定 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼或目前的設定中，設定或抓取網際網路選項。

-   [執行步驟](#implementation-steps)
    -   [選擇網際網路選項](#choosing-internet-options)
    -   [選擇 HINTERNET 控制碼](#choosing-the-hinternet-handle)
    -   [設定或取出選項](#setting-or-retrieving-the-options)
-   [HINTERNET 控制碼的範圍](#scope-of-hinternet-handle)
-   [設定個別選項](#setting-individual-options)
-   [正在抓取個別選項](#retrieving-individual-options)
    -   [完整範例](#complete-sample)
-   [設定連接選項](#setting-connection-options)
-   [正在抓取連接選項](#retrieving-connection-options)
-   [相關主題](#related-topics)

## <a name="implementation-steps"></a>執行步驟

若要設定或取得網際網路選項，請完成下列步驟：

-   [選擇網際網路選項](#choosing-internet-options)
-   [選擇 HINTERNET 控制碼](#choosing-the-hinternet-handle)
-   [設定或取出選項](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a>選擇網際網路選項

由於有這麼多的網際網路選項，選擇正確的選項相當重要。 許多網際網路選項都會影響 WinINet 函式和 Internet Explorer 的行為：

例如，您可以：

-   藉由設定使用者名稱和密碼來處理基本伺服器和 proxy 驗證。
-   設定或取出伺服器用來識別用戶端應用程式或瀏覽器功能的使用者代理程式字串。
-   取得指定之 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼的控制碼類型。

如需詳細資訊和網際網路選項的清單，請參閱 [**選項旗標**](option-flags.md)。

在 Internet Explorer 5 和更新版本中，您可以使用 [ [**依據連接選項的網際網路] \_ \_ \_ 選項 \_ 清單**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) 和 [網際網路] 的 [連結] [**\_ \_ \_ 選項**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) 結構，從特定網際網路連線設定或抓取某些選項。 如需詳細資訊以及可從特定網際網路連線設定或抓取的選項清單，請參閱網際網路的 **>dwoptions** 成員（ [**\_ 每個連接 \_ \_ 選項**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) 結構）。

### <a name="choosing-the-hinternet-handle"></a>選擇 HINTERNET 控制碼

用來設定或抓取網際網路選項的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，會決定作業的範圍。 所有透過這個控制碼建立的控制碼都會繼承這個控制碼上設定的選項。

例如，需要驗證 proxy 的用戶端應用程式，在每次應用程式嘗試存取網際網路資源時，可能不需要設定 proxy 使用者名稱和密碼。 如果指定連接上的所有要求都是由相同的 proxy 處理，則在連線類型 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼上設定 proxy 使用者名稱和密碼（也就是由呼叫 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼），會允許任何衍生自這個 **HINTERNET** 控制碼的呼叫使用相同的 proxy 使用者名稱和密碼。 每次 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)建立 **HINTERNET** 控制碼時，設定 proxy 使用者名稱和密碼需要額外且不必要的額外負荷。 請注意，如果應用程式使用需要驗證的 proxy，則應該在每個新連接上設定 proxy 認證。

### <a name="setting-or-retrieving-the-options"></a>設定或取出選項

當您決定要使用的網際網路選項和 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼時，請取出這些網際網路選項。 若要設定或取出選項，請呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 或 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)。

## <a name="scope-of-hinternet-handle"></a>HINTERNET 控制碼的範圍

用來設定或抓取網際網路選項的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，會決定選項的有效動作。

這些控制碼有三個層級：

-   呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) 所建立的根 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼 (會包含會影響此 WinINet 實例的所有網際網路選項。
-   連接至伺服器的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼， (由 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)的呼叫所建立) 
-   與資源相關聯的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼，或特定伺服器上的資源列舉。

除了各種 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼之外，應用程式也可以使用 **Null** 來設定或抓取 Internet Explorer 和 WinINet 函式所使用之網際網路選項的預設值。 當使用 **Null** 做為控制碼時，設定網際網路選項會變更目前儲存在登錄中的選項預設值。 用戶端應用程式不應該使用登錄功能來變更網際網路選項的預設值，因為未來可能會改變選項的儲存方式。

下表列出 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼的類型，以及與其相關聯之網際網路選項的範圍。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>控制碼類型</th>
<th>影響範圍</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>NULL</strong></td>
<td>Internet Explorer 的預設選項設定。</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_FTP</td>
<td>FTP 伺服器的這個連接的選項設定。 這些選項會影響從此 <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> 控制碼起始的任何作業，例如檔案下載。</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_CONNECT_GOPHER</td>
<td>此連接到 Gopher 伺服器的選項設定。 這些選項會影響從此 <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> 控制碼起始的任何作業，例如檔案下載。
<blockquote>
[!Note]<br />
僅限 windows XP 及 Windows Server 2003 R2 及更早版本。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_HTTP</td>
<td>此連接至 HTTP 伺服器的選項設定。 這些選項會影響從此 <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> 控制碼起始的任何作業，例如檔案下載。</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FILE_REQUEST</td>
<td>與此檔案要求相關聯的選項設定。</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FILE</td>
<td>與此 FTP 資源下載相關聯的選項設定。</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FILE_HTML</td>
<td>與此 FTP 資源下載相關聯的選項設定會以 HTML 格式格式化。</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FIND</td>
<td>與此搜尋 FTP 伺服器上的檔案相關聯的選項設定。</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FIND_HTML</td>
<td>在以 HTML 格式格式化的 FTP 伺服器上，與這個檔案搜尋相關聯的選項設定。</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE</td>
<td>與此 Gopher 資源下載相關聯的選項設定。
<blockquote>
[!Note]<br />
僅限 windows XP 及 Windows Server 2003 R2 及更早版本。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</td>
<td>與此 Gopher 資源下載相關聯的選項設定會以 HTML 格式格式化。
<blockquote>
[!Note]<br />
僅限 windows XP 及 Windows Server 2003 R2 及更早版本。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND</td>
<td>與此在 Gopher 伺服器上搜尋檔案相關聯的選項設定。
<blockquote>
[!Note]<br />
僅限 windows XP 及 Windows Server 2003 R2 及更早版本。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</td>
<td>在以 HTML 格式格式化的 Gopher 伺服器上，與此搜尋檔案相關聯的選項設定。
<blockquote>
[!Note]<br />
僅限 windows XP 及 Windows Server 2003 R2 及更早版本。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_HTTP_REQUEST</td>
<td>與此 HTTP 要求相關聯的選項設定。</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_INTERNET</td>
<td>與此 WinINet 函數實例相關聯的選項設定。</td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a>設定個別選項

決定您想要設定的網際網路選項以及這些選項所要影響的範圍之後，設定 [網際網路選項] 並不複雜。 您只需要使用所需的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼、網際網路選項旗標，以及包含您想要設定之資訊的緩衝區來呼叫 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)函式。

下列範例顯示如何在指定的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼上設定 proxy 使用者名稱和密碼。


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a>正在抓取個別選項

您可以使用 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 函式來取出網際網路選項。 若要取得網際網路選項：

1.  判斷取出網際網路選項資訊所需的緩衝區大小。

    緩衝區大小可透過使用 **Null** 作為緩衝區位址，並以零的緩衝區大小傳遞給緩衝區大小來決定。

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)所傳回的值是取得資訊所需的記憶體數量（以位元組為單位）。

2.  配置緩衝區的記憶體。
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  取得資料。
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  釋放記憶體。
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a>完整範例

以下是前一節中使用的完整範例。 這個範例會示範如何取出預設的使用者代理程式字串。


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a>設定連接選項

在 Internet Explorer 5 和更新版本中，可以針對特定連接設定網際網路選項。 先前，所有連線都共用相同的網際網路選項設定。 若要設定特定連接的選項：

1.  建立 [**\_ 每個 \_ CONN \_ 選項 \_ 清單**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) 結構的網際網路。
2.  針對您想要為連線設定的個別網際網路選項配置記憶體。
3.  設定 [網際網路] [**中 \_ 每 \_ 個 \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) [連接] 選項結構的選項。
4.  使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)設定選項。

下列程式碼範例顯示如何設定 LAN 連接的 proxy 資料。


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a>正在抓取連接選項

在 Internet Explorer 5 和更新版本中，可以從特定連線中取出網際網路選項。 從特定連接取出選項：

1.  建立 [**\_ 每個 \_ CONN \_ 選項 \_ 清單**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) 結構的網際網路。
2.  配置個別網際網路選項的記憶體，以從連接中取出。
3.  使用 [網際網路] [**\_ \_ \_ 選項**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) 結構來指定選項。
4.  使用 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)取出選項。
5.  利用選項資料。
6.  使用 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函式釋放配置用來保存選項資料的記憶體。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[處理驗證](handling-authentication.md)
</dt> <dt>

[HINTERNET 控制碼](appendix-a-hinternet-handles.md)
</dt> </dl>

 

