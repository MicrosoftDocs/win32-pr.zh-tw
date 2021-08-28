---
title: 管理 Cookie
description: 在 HTTP 通訊協定下，伺服器或腳本會使用 cookie 來維護用戶端工作站上的狀態資訊。
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0931de8b1d9d25862344658bddaacf5fd1d4325f9343176acb0206dcb3e1e383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113618"
---
# <a name="managing-cookies"></a>管理 Cookie

在 HTTP 通訊協定下，伺服器或腳本會使用 cookie 來維護用戶端工作站上的狀態資訊。 WinINet 函式已針對此用途來執行持續性 cookie 資料庫。 您可以使用它們來設定 cookie，並從 cookie 資料庫存取 cookie。 如需詳細資訊，請參閱 [HTTP cookie](http-cookies.md)。

您可以使用 [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) 和 [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) 函數來管理 cookie。

## <a name="using-cookie-functions"></a>使用 Cookie 函數

下列函式可讓應用程式在 cookie 資料庫中建立或取出 cookie。



| 函式                                       | 描述                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | 抓取指定 URL 及其所有父 Url 的 cookie。 |
| [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | 在指定的 URL 上設定 cookie。                              |



 

請注意，這些函數不需要呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)。 具有到期日的 cookie 會儲存在 [使用者名稱] AppData 漫遊 microsoft Windows Cookies] 目錄下的 [本機使用者] 帳戶中 \\ \\ \\ \\ \\ \\ ，而使用者的 [使用者 \\ 名稱] \\ AppData \\ 漫遊 \\ microsoft \\ Windows \\ Cookies \\ 低目錄適用于在低許可權下執行的應用程式。 沒有到期日的 cookie 會儲存在記憶體中，而且只適用于建立它們的進程。

如 [HTTP cookie](http-cookies.md) 主題所述， [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) 函式不會將伺服器標示為不可編寫腳本的 cookie 傳回 Set-Cookie 標頭中的 "HttpOnly" 屬性。

### <a name="getting-a-cookie"></a>取得 Cookie

[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) 會傳回指定之 URL 及其所有父 url 的 cookie。

下列範例示範 [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea)的呼叫。


```C++
TCHAR szURL[256];         // buffer to hold the URL
LPTSTR lpszData = NULL;   // buffer to hold the cookie data
DWORD dwSize=0;           // variable to get the buffer size needed

// Insert code to retrieve the URL.

retry:

// The first call to InternetGetCookie will get the required
// buffer size needed to download the cookie data.
if (!InternetGetCookie(szURL, NULL, lpszData, &dwSize))
{
    // Check for an insufficient buffer error.
    if (GetLastError()== ERROR_INSUFFICIENT_BUFFER)
    {
        // Allocate the necessary buffer.
        lpszData = new TCHAR[dwSize];

        // Try the call again.
        goto retry;
    }
    else
    {
        // Insert error handling code.
    }
}
else
{
    // Insert code to display the cookie data.

    // Release the memory allocated for the buffer.
    delete[]lpszData;
}
```



### <a name="setting-a-cookie"></a>設定 Cookie

[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) 是用來在指定的 URL 上設定 cookie。 [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) 可以同時建立持續性和會話 cookie。

持續性 cookie 的到期日。 這些 cookie 會儲存在本機使用者帳戶下的「使用者 \\ 名稱」 \\ AppData \\ 漫遊 \\ microsoft \\ Windows \\ cookies 目錄，而使用者的「使用者 \\ 名稱」 \\ AppData \\ 漫遊 \\ microsoft \\ Windows \\ cookies \\ 低目錄適用于在低許可權下執行的應用程式。

會話 cookie 儲存在記憶體中，而且只能由建立它們的進程存取。

Cookie 的資料應該採用下列格式：

``` syntax
NAME=VALUE
```

若為到期日，格式必須是：

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

DAY 是星期幾的三個字母縮寫、DD 是月份的日期、MMM 是月份的三個字母縮寫、YYYY 是年份，而 HH： MM： SS 是一天的軍事時間。

下列範例示範兩個 [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea)呼叫。 第一個呼叫會建立會話 cookie，而第二個呼叫會建立持續性 cookie。


```C++
BOOL bReturn;

// Create a session cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
            TEXT("TestData = Test"));

// Create a persistent cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
           TEXT("TestData = Test; expires = Sat,01-Jan-2000 00:00:00 GMT"));

```



> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 