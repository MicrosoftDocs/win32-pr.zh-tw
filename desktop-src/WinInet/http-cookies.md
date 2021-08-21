---
title: HTTP Cookie
description: HTTP cookie 為伺服器提供了一種機制，可在用戶端應用程式的系統上儲存及取出狀態資訊。
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ba5b2d3917ea8f140e334f5f78b1bd730908d25506d9023667403410833c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113712"
---
# <a name="http-cookies"></a>HTTP Cookie

HTTP cookie 為伺服器提供了一種機制，可在用戶端應用程式的系統上儲存及取出狀態資訊。 這項機制可讓 web 應用程式能夠儲存選取專案的相關資訊、使用者喜好設定、註冊資訊，以及稍後可以取出的其他資訊。

## <a name="cookie-related-headers"></a>Cookie-Related 標頭

有兩個標頭，Set-Cookie 和 Cookie，與 cookie 相關。 伺服器會傳送 Set-Cookie 標頭來回應 HTTP 要求，這是用來在使用者的系統上建立 cookie。 如果有 cookie 具有相符的網域和路徑，用戶端應用程式就會包含 Cookie 標頭，並將 HTTP 要求傳送至伺服器。

### <a name="set-cookie-header"></a>Set-Cookie 標頭

Set-Cookie 回應標頭會使用下列格式：

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

 = Set-Cookie 回應標頭中必須包含一或多個以分號分隔的字串序列 (，) 後面接著模式名稱 *值*。 伺服器可以使用這些字串順序，將資料儲存在用戶端的系統上。

到期日是使用格式 expires =*date* 來設定，其中 *Date* 是格林威治標準時間的到期日 (GMT) 。 如果未設定到期日，cookie 會在網際網路會話結束後過期。 否則，cookie 會保存在快取中，直到到期日為止。 日期必須使用下列格式：

*DAY*， *DD* - *MMM* - *YYYY* *HH*：*MM*：*SS* GMT

<dl> <dt>

<span id="DAY"></span><span id="day"></span>*一天*
</dt> <dd>

一周的哪一天 (太陽、星期一、週二、週三、星期四、星期五、週六) 。

</dd> <dt>

<span id="DD"></span><span id="dd"></span>*DD*
</dt> <dd>

月份的第一天 (，例如 01) 的第一天。

</dd> <dt>

<span id="MMM"></span><span id="mmm"></span>*嗯*
</dt> <dd>

本月的三個字母縮寫 (Jan、二月、Mar、四月、六月、六月、七月、六月、Sep、Oct、11月) 。

</dd> <dt>

<span id="YYYY"></span><span id="yyyy"></span>*年*
</dt> <dd>

年。

</dd> <dt>

<span id="HH"></span><span id="hh"></span>*HH*
</dt> <dd>

軍事時間 (22 的小時值會是 10:00 P.M.，例如) 。

</dd> <dt>

<span id="MM"></span><span id="mm"></span>*毫米*
</dt> <dd>

分鐘值。

</dd> <dt>

<span id="SS"></span><span id="ss"></span>*匯總*
</dt> <dd>

第二個值。

</dd> </dl>

使用模式網域 = 功能變數名稱指定功能變數名稱，對持續 *性 \_* cookie 而言是選擇性的，並且用來指出 cookie 有效的網域結尾。 會拒絕指定網域的會話 cookie。 如果指定的功能變數名稱結尾與要求相符，cookie 會嘗試比對路徑，以判斷是否應該傳送 cookie。 例如，如果功能變數名稱結尾是 microsoft.com，則會檢查 home.microsoft.com 和 support.microsoft.com 的要求，以查看指定的模式是否符合要求。 功能變數名稱中必須至少有兩個或三個句點，以防止 cookie 設定為廣泛使用的功能變數名稱結尾，例如 .com、. edu 和 co.jp。 允許的功能變數名稱類似于. microsoft.com、. someschool.edu 和 someserver.co.jp。 只有指定網域內的主機可以設定網域的 cookie。

使用模式路徑 =*部分 \_ 路徑* 設定路徑是選擇性的，而且可以用來指定 Cookie 有效的 url 子集。 如果指定了路徑，則會將 cookie 視為符合該路徑的任何要求。 例如，如果指定的路徑是/example，則路徑為/examplecode 和 code.htm/example/的要求將會相符。 如果未指定路徑，則會假設路徑為與 Set-Cookie 標頭相關聯之資源的路徑。

Cookie 也可以標示為安全，這會指定 cookie 只能傳送至 HTTPs 伺服器。

最後，您可以將 cookie 標示為 HttpOnly (屬性不區分大小寫) ，表示 cookie 不可編寫腳本，而且不應該顯示給用戶端應用程式（基於安全考慮）。 在 Windows 網際網路中，這表示 cookie 無法透過 **InternetGetCookie** 函式來抓取。

### <a name="cookie-header"></a>Cookie 標頭

Cookie 標頭包含在任何 HTTP 要求中，而 cookie 的網域和路徑符合要求。 Cookie 標頭的格式如下：

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

使用格式 *名稱* 值的一或多個字串順序 = 包含在 cookie 中設定的資訊。

## <a name="generating-cookies"></a>產生 Cookie

有三種方法可以產生 Microsoft Internet Explorer 的 cookie：使用 microsoft JScript、使用 WinINet 函式，以及使用 CGI 腳本。 所有方法都必須設定包含在 Set-Cookie 標頭中的資訊。

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a>使用 DHTML 物件模型產生 Cookie

使用動態 HTML (DHTML) 物件模型，可以藉由呼叫 document 物件的 **cookie** 屬性來設定 cookie，如下列範例所示。

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a>使用 WinInet 函數產生 Cookie

使用 [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) 函式的應用程式可以建立 cookie。 如需詳細資訊，請參閱 [設定 Cookie](managing-cookies.md)。

### <a name="generating-a-cookie-using-a-cgi-script"></a>使用 CGI 腳本產生 Cookie

Cookie 的產生方式是將 Set-Cookie 標頭包含在要求的 HTTP 回應中所包含的 CGI 腳本的一部分。

下列範例是 CGI 腳本，其中包含使用 Perl 的 Set-Cookie 標頭。

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 