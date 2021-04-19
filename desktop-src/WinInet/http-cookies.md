---
title: HTTP Cookie
description: HTTP cookie 為伺服器提供了一種機制，可在用戶端應用程式的系統上儲存及取出狀態資訊。
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6855f0b105dc73760541bf9eb7a6da80dfb38e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106990894"
---
# <a name="http-cookies"></a><span data-ttu-id="746b2-103">HTTP Cookie</span><span class="sxs-lookup"><span data-stu-id="746b2-103">HTTP Cookies</span></span>

<span data-ttu-id="746b2-104">HTTP cookie 為伺服器提供了一種機制，可在用戶端應用程式的系統上儲存及取出狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="746b2-104">HTTP cookies provide the server with a mechanism to store and retrieve state information on the client application's system.</span></span> <span data-ttu-id="746b2-105">這項機制可讓 web 應用程式能夠儲存選取專案的相關資訊、使用者喜好設定、註冊資訊，以及稍後可以取出的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="746b2-105">This mechanism allows web-based applications the ability to store information about selected items, user preferences, registration information, and other information that can be retrieved later.</span></span>

## <a name="cookie-related-headers"></a><span data-ttu-id="746b2-106">Cookie-Related 標頭</span><span class="sxs-lookup"><span data-stu-id="746b2-106">Cookie-Related Headers</span></span>

<span data-ttu-id="746b2-107">有兩個標頭，Set-Cookie 和 Cookie，與 cookie 相關。</span><span class="sxs-lookup"><span data-stu-id="746b2-107">There are two headers, Set-Cookie and Cookie, that are related to cookies.</span></span> <span data-ttu-id="746b2-108">伺服器會傳送 Set-Cookie 標頭來回應 HTTP 要求，這是用來在使用者的系統上建立 cookie。</span><span class="sxs-lookup"><span data-stu-id="746b2-108">The Set-Cookie header is sent by the server in response to an HTTP request, which is used to create a cookie on the user's system.</span></span> <span data-ttu-id="746b2-109">如果有 cookie 具有相符的網域和路徑，用戶端應用程式就會包含 Cookie 標頭，並將 HTTP 要求傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="746b2-109">The Cookie header is included by the client application with an HTTP request sent to a server, if there is a cookie that has a matching domain and path.</span></span>

### <a name="set-cookie-header"></a><span data-ttu-id="746b2-110">Set-Cookie 標頭</span><span class="sxs-lookup"><span data-stu-id="746b2-110">Set-Cookie Header</span></span>

<span data-ttu-id="746b2-111">Set-Cookie 回應標頭會使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="746b2-111">The Set-Cookie response header uses the following format:</span></span>

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

<span data-ttu-id="746b2-112"> = Set-Cookie 回應標頭中必須包含一或多個以分號分隔的字串序列 (，) 後面接著模式名稱 *值*。</span><span class="sxs-lookup"><span data-stu-id="746b2-112">One or more string sequences (separated by semicolons) that follow the pattern *name*=*value* must be included in the Set-Cookie response header.</span></span> <span data-ttu-id="746b2-113">伺服器可以使用這些字串順序，將資料儲存在用戶端的系統上。</span><span class="sxs-lookup"><span data-stu-id="746b2-113">The server can use these string sequences to store data on the client's system.</span></span>

<span data-ttu-id="746b2-114">到期日是使用格式 expires =*date* 來設定，其中 *Date* 是格林威治標準時間的到期日 (GMT) 。</span><span class="sxs-lookup"><span data-stu-id="746b2-114">The expiration date is set by using the format expires=*date*, where *date* is the expiration date in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="746b2-115">如果未設定到期日，cookie 會在網際網路會話結束後過期。</span><span class="sxs-lookup"><span data-stu-id="746b2-115">If the expiration date is not set, the cookie expires after the Internet session ends.</span></span> <span data-ttu-id="746b2-116">否則，cookie 會保存在快取中，直到到期日為止。</span><span class="sxs-lookup"><span data-stu-id="746b2-116">Otherwise, the cookie is persisted in the cache until the expiration date.</span></span> <span data-ttu-id="746b2-117">日期必須使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="746b2-117">The date must use the following format:</span></span>

<span data-ttu-id="746b2-118">*DAY*， *DD* - *MMM* - *YYYY* *HH*：*MM*：*SS* GMT</span><span class="sxs-lookup"><span data-stu-id="746b2-118">*DAY*, *DD*-*MMM*-*YYYY* *HH*:*MM*:*SS* GMT</span></span>

<dl> <dt>

<span data-ttu-id="746b2-119"><span id="DAY"></span><span id="day"></span>*一天*</span><span class="sxs-lookup"><span data-stu-id="746b2-119"><span id="DAY"></span><span id="day"></span>*DAY*</span></span>
</dt> <dd>

<span data-ttu-id="746b2-120">一周的哪一天 (太陽、星期一、週二、週三、星期四、星期五、週六) 。</span><span class="sxs-lookup"><span data-stu-id="746b2-120">The day of the week (Sun, Mon, Tue, Wed, Thu, Fri, Sat).</span></span>

</dd> <dt>

<span data-ttu-id="746b2-121"><span id="DD"></span><span id="dd"></span>*Dd*</span><span class="sxs-lookup"><span data-stu-id="746b2-121"><span id="DD"></span><span id="dd"></span>*DD*</span></span>
</dt> <dd>

<span data-ttu-id="746b2-122">月份的第一天 (，例如 01) 的第一天。</span><span class="sxs-lookup"><span data-stu-id="746b2-122">The day in the month (such as 01 for the first day of the month).</span></span>

</dd> <dt>

<span data-ttu-id="746b2-123"><span id="MMM"></span><span id="mmm"></span>*嗯*</span><span class="sxs-lookup"><span data-stu-id="746b2-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span></span>
</dt> <dd>

<span data-ttu-id="746b2-124">本月的三個字母縮寫 (Jan、二月、Mar、四月、六月、六月、七月、六月、Sep、Oct、11月) 。</span><span class="sxs-lookup"><span data-stu-id="746b2-124">The three-letter abbreviation for the month (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).</span></span>

</dd> <dt>

<span data-ttu-id="746b2-125"><span id="YYYY"></span><span id="yyyy"></span>*年*</span><span class="sxs-lookup"><span data-stu-id="746b2-125"><span id="YYYY"></span><span id="yyyy"></span>*YYYY*</span></span>
</dt> <dd>

<span data-ttu-id="746b2-126">年。</span><span class="sxs-lookup"><span data-stu-id="746b2-126">The year.</span></span>

</dd> <dt>

<span data-ttu-id="746b2-127"><span id="HH"></span><span id="hh"></span>*HH*</span><span class="sxs-lookup"><span data-stu-id="746b2-127"><span id="HH"></span><span id="hh"></span>*HH*</span></span>
</dt> <dd>

<span data-ttu-id="746b2-128">軍事時間 (22 的小時值會是 10:00 P.M.，例如) 。</span><span class="sxs-lookup"><span data-stu-id="746b2-128">The hour value in military time (22 would be 10:00 P.M., for example).</span></span>

</dd> <dt>

<span data-ttu-id="746b2-129"><span id="MM"></span><span id="mm"></span>*毫米*</span><span class="sxs-lookup"><span data-stu-id="746b2-129"><span id="MM"></span><span id="mm"></span>*MM*</span></span>
</dt> <dd>

<span data-ttu-id="746b2-130">分鐘值。</span><span class="sxs-lookup"><span data-stu-id="746b2-130">The minute value.</span></span>

</dd> <dt>

<span data-ttu-id="746b2-131"><span id="SS"></span><span id="ss"></span>*匯總*</span><span class="sxs-lookup"><span data-stu-id="746b2-131"><span id="SS"></span><span id="ss"></span>*SS*</span></span>
</dt> <dd>

<span data-ttu-id="746b2-132">第二個值。</span><span class="sxs-lookup"><span data-stu-id="746b2-132">The second value.</span></span>

</dd> </dl>

<span data-ttu-id="746b2-133">使用模式網域 = 功能變數名稱指定功能變數名稱，對持續 *性 \_* cookie 而言是選擇性的，並且用來指出 cookie 有效的網域結尾。</span><span class="sxs-lookup"><span data-stu-id="746b2-133">Specifying the domain name, using the pattern domain=*domain\_name*, is optional for persistent cookies and is used to indicate the end of the domain for which the cookie is valid.</span></span> <span data-ttu-id="746b2-134">會拒絕指定網域的會話 cookie。</span><span class="sxs-lookup"><span data-stu-id="746b2-134">Session cookies that specify a domain are rejected.</span></span> <span data-ttu-id="746b2-135">如果指定的功能變數名稱結尾與要求相符，cookie 會嘗試比對路徑，以判斷是否應該傳送 cookie。</span><span class="sxs-lookup"><span data-stu-id="746b2-135">If the specified domain name ending matches the request, the cookie tries to match the path to determine if the cookie should be sent.</span></span> <span data-ttu-id="746b2-136">例如，如果功能變數名稱結尾是 microsoft.com，則會檢查 home.microsoft.com 和 support.microsoft.com 的要求，以查看指定的模式是否符合要求。</span><span class="sxs-lookup"><span data-stu-id="746b2-136">For example, if the domain name ending is .microsoft.com, requests to home.microsoft.com and support.microsoft.com would be checked to see if the specified pattern matches the request.</span></span> <span data-ttu-id="746b2-137">功能變數名稱中必須至少有兩個或三個句點，以防止 cookie 設定為廣泛使用的功能變數名稱結尾，例如 .com、. edu 和 co.jp。</span><span class="sxs-lookup"><span data-stu-id="746b2-137">The domain name must have at least two or three periods in it to prevent cookies from being set for widely used domain name endings, such as .com, .edu, and co.jp.</span></span> <span data-ttu-id="746b2-138">允許的功能變數名稱類似于. microsoft.com、. someschool.edu 和 someserver.co.jp。</span><span class="sxs-lookup"><span data-stu-id="746b2-138">Allowable domain names would be similar to .microsoft.com, .someschool.edu, and .someserver.co.jp.</span></span> <span data-ttu-id="746b2-139">只有指定網域內的主機可以設定網域的 cookie。</span><span class="sxs-lookup"><span data-stu-id="746b2-139">Only hosts within the specified domain can set a cookie for a domain.</span></span>

<span data-ttu-id="746b2-140">使用模式路徑 =*部分 \_ 路徑* 設定路徑是選擇性的，而且可以用來指定 Cookie 有效的 url 子集。</span><span class="sxs-lookup"><span data-stu-id="746b2-140">Setting the path, using the pattern path=*some\_path*, is optional and can be used to specify a subset of the URLs for which the cookie is valid.</span></span> <span data-ttu-id="746b2-141">如果指定了路徑，則會將 cookie 視為符合該路徑的任何要求。</span><span class="sxs-lookup"><span data-stu-id="746b2-141">If a path is specified, the cookie is considered valid for any requests that match that path.</span></span> <span data-ttu-id="746b2-142">例如，如果指定的路徑是/example，則路徑為/examplecode 和 code.htm/example/的要求將會相符。</span><span class="sxs-lookup"><span data-stu-id="746b2-142">For example, if the specified path is /example, requests with the paths /examplecode and /example/code.htm would match.</span></span> <span data-ttu-id="746b2-143">如果未指定路徑，則會假設路徑為與 Set-Cookie 標頭相關聯之資源的路徑。</span><span class="sxs-lookup"><span data-stu-id="746b2-143">If no path is specified, the path is assumed to be the path of the resource associated with the Set-Cookie header.</span></span>

<span data-ttu-id="746b2-144">Cookie 也可以標示為安全，這會指定 cookie 只能傳送至 HTTPs 伺服器。</span><span class="sxs-lookup"><span data-stu-id="746b2-144">The cookie can also be marked as secure, which specifies that the cookie can be sent only to https servers.</span></span>

<span data-ttu-id="746b2-145">最後，您可以將 cookie 標示為 HttpOnly (屬性不區分大小寫) ，表示 cookie 不可編寫腳本，而且不應該顯示給用戶端應用程式（基於安全考慮）。</span><span class="sxs-lookup"><span data-stu-id="746b2-145">Finally, a cookie can be marked as HttpOnly (attributes are not case-sensitive), to indicate that the cookie is non-scriptable and should not be revealed to the client application, for security reasons.</span></span> <span data-ttu-id="746b2-146">在 Windows 網際網路中，這表示 cookie 無法透過 **InternetGetCookie** 函式抓取。</span><span class="sxs-lookup"><span data-stu-id="746b2-146">Within Windows Internet, this means that the cookie cannot be retrieved through the **InternetGetCookie** function.</span></span>

### <a name="cookie-header"></a><span data-ttu-id="746b2-147">Cookie 標頭</span><span class="sxs-lookup"><span data-stu-id="746b2-147">Cookie Header</span></span>

<span data-ttu-id="746b2-148">Cookie 標頭包含在任何 HTTP 要求中，而 cookie 的網域和路徑符合要求。</span><span class="sxs-lookup"><span data-stu-id="746b2-148">The Cookie header is included with any HTTP requests that have a cookie whose domain and path match the request.</span></span> <span data-ttu-id="746b2-149">Cookie 標頭的格式如下：</span><span class="sxs-lookup"><span data-stu-id="746b2-149">The Cookie header has the following format:</span></span>

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

<span data-ttu-id="746b2-150">使用格式 *名稱* 值的一或多個字串順序 = 包含在 cookie 中設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="746b2-150">One or more string sequences, using the format *name*=*value*, contain the information that was set in the cookie.</span></span>

## <a name="generating-cookies"></a><span data-ttu-id="746b2-151">產生 Cookie</span><span class="sxs-lookup"><span data-stu-id="746b2-151">Generating Cookies</span></span>

<span data-ttu-id="746b2-152">有三種方法可以產生 Microsoft Internet Explorer 的 cookie：使用 Microsoft JScript、使用 WinINet 函式，以及使用 CGI 腳本。</span><span class="sxs-lookup"><span data-stu-id="746b2-152">There are three methods for generating cookies for Microsoft Internet Explorer: using Microsoft JScript, using the WinINet functions, and using a CGI script.</span></span> <span data-ttu-id="746b2-153">所有方法都必須設定包含在 Set-Cookie 標頭中的資訊。</span><span class="sxs-lookup"><span data-stu-id="746b2-153">All of the methods need to set the information that is included in the Set-Cookie header.</span></span>

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a><span data-ttu-id="746b2-154">使用 DHTML 物件模型產生 Cookie</span><span class="sxs-lookup"><span data-stu-id="746b2-154">Generating a Cookie Using the DHTML Object Model</span></span>

<span data-ttu-id="746b2-155">使用動態 HTML (DHTML) 物件模型，可以藉由呼叫 document 物件的 **cookie** 屬性來設定 cookie，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="746b2-155">Using the Dynamic HTML (DHTML) object model, cookies can be set by calling the **cookie** property of the document object, as shown in the following example.</span></span>

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a><span data-ttu-id="746b2-156">使用 WinInet 函數產生 Cookie</span><span class="sxs-lookup"><span data-stu-id="746b2-156">Generating a Cookie Using the WinInet Functions</span></span>

<span data-ttu-id="746b2-157">使用 [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) 函式的應用程式可以建立 cookie。</span><span class="sxs-lookup"><span data-stu-id="746b2-157">Cookies can be created by applications using the [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) function.</span></span> <span data-ttu-id="746b2-158">如需詳細資訊，請參閱 [設定 Cookie](managing-cookies.md)。</span><span class="sxs-lookup"><span data-stu-id="746b2-158">For more information, see [Setting a Cookie](managing-cookies.md).</span></span>

### <a name="generating-a-cookie-using-a-cgi-script"></a><span data-ttu-id="746b2-159">使用 CGI 腳本產生 Cookie</span><span class="sxs-lookup"><span data-stu-id="746b2-159">Generating a Cookie Using a CGI Script</span></span>

<span data-ttu-id="746b2-160">Cookie 的產生方式是將 Set-Cookie 標頭包含在要求的 HTTP 回應中所包含的 CGI 腳本的一部分。</span><span class="sxs-lookup"><span data-stu-id="746b2-160">Cookies are generated by including a Set-Cookie header as part of a CGI script included in the HTTP response to a request.</span></span>

<span data-ttu-id="746b2-161">下列範例是 CGI 腳本，其中包含使用 Perl 的 Set-Cookie 標頭。</span><span class="sxs-lookup"><span data-stu-id="746b2-161">The following example is a CGI script that includes a Set-Cookie header using Perl.</span></span>

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> <span data-ttu-id="746b2-162">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="746b2-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="746b2-163">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="746b2-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="746b2-164">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="746b2-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 