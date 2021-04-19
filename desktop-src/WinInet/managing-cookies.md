---
title: 管理 Cookie
description: 在 HTTP 通訊協定下，伺服器或腳本會使用 cookie 來維護用戶端工作站上的狀態資訊。
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0418442e961f6f4d3d2bcddb2c607ac9cf7928
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967911"
---
# <a name="managing-cookies"></a><span data-ttu-id="e4dab-103">管理 Cookie</span><span class="sxs-lookup"><span data-stu-id="e4dab-103">Managing Cookies</span></span>

<span data-ttu-id="e4dab-104">在 HTTP 通訊協定下，伺服器或腳本會使用 cookie 來維護用戶端工作站上的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="e4dab-104">Under the http protocol, a server or a script uses cookies to maintain state information on the client workstation.</span></span> <span data-ttu-id="e4dab-105">WinINet 函式已針對此用途來執行持續性 cookie 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e4dab-105">The WinINet functions have implemented a persistent cookie database for this purpose.</span></span> <span data-ttu-id="e4dab-106">您可以使用它們來設定 cookie，並從 cookie 資料庫存取 cookie。</span><span class="sxs-lookup"><span data-stu-id="e4dab-106">They can be used to set cookies in and access cookies from the cookie database.</span></span> <span data-ttu-id="e4dab-107">如需詳細資訊，請參閱 [HTTP cookie](http-cookies.md)。</span><span class="sxs-lookup"><span data-stu-id="e4dab-107">For more information, see [HTTP Cookies](http-cookies.md).</span></span>

<span data-ttu-id="e4dab-108">您可以使用 [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) 和 [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) 函數來管理 cookie。</span><span class="sxs-lookup"><span data-stu-id="e4dab-108">The [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) and [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) functions can be used to manage cookies.</span></span>

## <a name="using-cookie-functions"></a><span data-ttu-id="e4dab-109">使用 Cookie 函數</span><span class="sxs-lookup"><span data-stu-id="e4dab-109">Using Cookie Functions</span></span>

<span data-ttu-id="e4dab-110">下列函式可讓應用程式在 cookie 資料庫中建立或取出 cookie。</span><span class="sxs-lookup"><span data-stu-id="e4dab-110">The following functions allow an application to create or retrieve cookies in the cookie database.</span></span>



| <span data-ttu-id="e4dab-111">函式</span><span class="sxs-lookup"><span data-stu-id="e4dab-111">Function</span></span>                                       | <span data-ttu-id="e4dab-112">描述</span><span class="sxs-lookup"><span data-stu-id="e4dab-112">Description</span></span>                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="e4dab-113">**InternetGetCookie**</span><span class="sxs-lookup"><span data-stu-id="e4dab-113">**InternetGetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | <span data-ttu-id="e4dab-114">抓取指定 URL 及其所有父 Url 的 cookie。</span><span class="sxs-lookup"><span data-stu-id="e4dab-114">Retrieves cookies for the specified URL and all its parent URLs.</span></span> |
| [<span data-ttu-id="e4dab-115">**InternetSetCookie**</span><span class="sxs-lookup"><span data-stu-id="e4dab-115">**InternetSetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | <span data-ttu-id="e4dab-116">在指定的 URL 上設定 cookie。</span><span class="sxs-lookup"><span data-stu-id="e4dab-116">Sets a cookie on the specified URL.</span></span>                              |



 

<span data-ttu-id="e4dab-117">請注意，這些函數不需要呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)。</span><span class="sxs-lookup"><span data-stu-id="e4dab-117">Note that these functions do not require a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="e4dab-118">具有到期日的 cookie 會儲存在 [使用者名稱] AppData 漫遊 microsoft windows cookie 目錄下的 [本機使用者] 帳戶中 \\ \\ \\ \\ \\ \\ ，而使用者的 [使用者 \\ 名稱] \\ AppData \\ 漫遊 \\ microsoft \\ windows \\ cookie \\ 低目錄，適用于在低許可權下執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e4dab-118">Cookies that have an expiration date are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span> <span data-ttu-id="e4dab-119">沒有到期日的 cookie 會儲存在記憶體中，而且只適用于建立它們的進程。</span><span class="sxs-lookup"><span data-stu-id="e4dab-119">Cookies that do not have an expiration date are stored in memory and are available only to the process in which they were created.</span></span>

<span data-ttu-id="e4dab-120">如 [HTTP cookie](http-cookies.md) 主題所述， [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) 函式不會將伺服器標示為不可編寫腳本的 cookie 傳回 Set-Cookie 標頭中的 "HttpOnly" 屬性。</span><span class="sxs-lookup"><span data-stu-id="e4dab-120">As noted in the [HTTP Cookies](http-cookies.md) topic, the [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) function does not return cookies that have been marked by the server as non-scriptable with the "HttpOnly" attribute in the Set-Cookie header.</span></span>

### <a name="getting-a-cookie"></a><span data-ttu-id="e4dab-121">取得 Cookie</span><span class="sxs-lookup"><span data-stu-id="e4dab-121">Getting a Cookie</span></span>

<span data-ttu-id="e4dab-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) 會傳回指定之 URL 及其所有父 url 的 cookie。</span><span class="sxs-lookup"><span data-stu-id="e4dab-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) returns the cookies for the specified URL and all its parent URLs.</span></span>

<span data-ttu-id="e4dab-123">下列範例示範 [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e4dab-123">The following example demonstrates a call to [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span></span>


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



### <a name="setting-a-cookie"></a><span data-ttu-id="e4dab-124">設定 Cookie</span><span class="sxs-lookup"><span data-stu-id="e4dab-124">Setting a Cookie</span></span>

<span data-ttu-id="e4dab-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) 是用來在指定的 URL 上設定 cookie。</span><span class="sxs-lookup"><span data-stu-id="e4dab-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) is used to set a cookie on the specified URL.</span></span> <span data-ttu-id="e4dab-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) 可以同時建立持續性和會話 cookie。</span><span class="sxs-lookup"><span data-stu-id="e4dab-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) can create both persistent and session cookies.</span></span>

<span data-ttu-id="e4dab-127">持續性 cookie 的到期日。</span><span class="sxs-lookup"><span data-stu-id="e4dab-127">Persistent cookies have an expiration date.</span></span> <span data-ttu-id="e4dab-128">這些 cookie 會儲存在本機使用者帳戶下的 [使用者 \\ 名稱] \\ AppData \\ 漫遊 \\ microsoft \\ Windows \\ cookies 目錄，以及使用者的 [使用者 \\ 名稱] \\ AppData \\ 漫遊 \\ microsoft \\ windows \\ cookie \\ 低目錄，以供在低許可權下執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e4dab-128">These cookies are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span>

<span data-ttu-id="e4dab-129">會話 cookie 儲存在記憶體中，而且只能由建立它們的進程存取。</span><span class="sxs-lookup"><span data-stu-id="e4dab-129">Session cookies are stored in memory and can be accessed only by the process that created them.</span></span>

<span data-ttu-id="e4dab-130">Cookie 的資料應該採用下列格式：</span><span class="sxs-lookup"><span data-stu-id="e4dab-130">The data for the cookie should be in the format:</span></span>

``` syntax
NAME=VALUE
```

<span data-ttu-id="e4dab-131">若為到期日，格式必須是：</span><span class="sxs-lookup"><span data-stu-id="e4dab-131">For the expiration date, the format must be:</span></span>

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

<span data-ttu-id="e4dab-132">DAY 是星期幾的三個字母縮寫、DD 是月份的日期、MMM 是月份的三個字母縮寫、YYYY 是年份，而 HH： MM： SS 是一天的軍事時間。</span><span class="sxs-lookup"><span data-stu-id="e4dab-132">DAY is the three-letter abbreviation for the day of the week, DD is the day of the month, MMM is the three-letter abbreviation for the month, YYYY is the year, and HH:MM:SS is the time of the day in military time.</span></span>

<span data-ttu-id="e4dab-133">下列範例示範兩個 [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea)呼叫。</span><span class="sxs-lookup"><span data-stu-id="e4dab-133">The following example demonstrates two calls to [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span></span> <span data-ttu-id="e4dab-134">第一個呼叫會建立會話 cookie，而第二個呼叫會建立持續性 cookie。</span><span class="sxs-lookup"><span data-stu-id="e4dab-134">The first call creates a session cookie and the second creates a persistent cookie.</span></span>


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
> <span data-ttu-id="e4dab-135">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="e4dab-135">WinINet does not support server implementations.</span></span> <span data-ttu-id="e4dab-136">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="e4dab-136">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e4dab-137">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="e4dab-137">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 