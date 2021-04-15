---
description: 包含可針對目前 Microsoft Windows HTTP Services (WinHTTP) 會話設定或抓取的選項。
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: WinHttpRequestOption 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: 32ae65f43cd04027027e43d29c49ed0f68f29c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511485"
---
# <a name="winhttprequestoption-enumeration"></a><span data-ttu-id="17a6d-103">WinHttpRequestOption 列舉</span><span class="sxs-lookup"><span data-stu-id="17a6d-103">WinHttpRequestOption enumeration</span></span>

<span data-ttu-id="17a6d-104">**WinHttpRequestOption** 列舉包含可針對目前 MICROSOFT Windows HTTP Services (WinHTTP) 會話設定或抓取的選項。</span><span class="sxs-lookup"><span data-stu-id="17a6d-104">The **WinHttpRequestOption** enumeration includes options that can be set or retrieved for the current Microsoft Windows HTTP Services (WinHTTP) session.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17a6d-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a><span data-ttu-id="17a6d-106">常數</span><span class="sxs-lookup"><span data-stu-id="17a6d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="17a6d-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption \_ UserAgentString**</span><span class="sxs-lookup"><span data-stu-id="17a6d-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption\_UserAgentString**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-108">設定或抓取包含 [*使用者代理程式*](glossary.md)字串的 **VARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="17a6d-108">Sets or retrieves a **VARIANT** that contains the [*user agent*](glossary.md) string.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**WinHttpRequestOption \_ URL**</span><span class="sxs-lookup"><span data-stu-id="17a6d-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**WinHttpRequestOption\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-110">捕獲包含資源 URL 的 **VARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="17a6d-110">Retrieves a **VARIANT** that contains the URL of the resource.</span></span> <span data-ttu-id="17a6d-111">此值為唯讀;您無法使用這個屬性來設定 URL。</span><span class="sxs-lookup"><span data-stu-id="17a6d-111">This value is read-only; you cannot set the URL using this property.</span></span> <span data-ttu-id="17a6d-112">在呼叫 [**Open**](iwinhttprequest-open.md) 方法之前，無法讀取 URL。</span><span class="sxs-lookup"><span data-stu-id="17a6d-112">The URL cannot be read until the [**Open**](iwinhttprequest-open.md) method is called.</span></span> <span data-ttu-id="17a6d-113">此選項適用于在 [**傳送**](iwinhttprequest-send.md) 方法完成後檢查 URL，以確認是否發生任何重新導向。</span><span class="sxs-lookup"><span data-stu-id="17a6d-113">This option is useful for checking the URL after the [**Send**](iwinhttprequest-send.md) method is finished to verify that any redirection occurred.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption \_ URLCodePage**</span><span class="sxs-lookup"><span data-stu-id="17a6d-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption\_URLCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-115">設定或抓取識別 URL 字串 [*字碼頁*](glossary.md)的 **VARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="17a6d-115">Sets or retrieves a **VARIANT** that identifies the [*code page*](glossary.md) for the URL string.</span></span> <span data-ttu-id="17a6d-116">預設值為 UTF-8 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="17a6d-116">The default value is the UTF-8 code page.</span></span> <span data-ttu-id="17a6d-117">字碼頁是用來將以 [**Open**](iwinhttprequest-open.md) 方法傳遞的 Unicode URL 字串轉換成單一位元組的字串表示。</span><span class="sxs-lookup"><span data-stu-id="17a6d-117">The code page is used to convert the Unicode URL string, passed in the [**Open**](iwinhttprequest-open.md) method, to a single-byte string representation.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**</span><span class="sxs-lookup"><span data-stu-id="17a6d-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption\_EscapePercentInURL**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-119">設定或抓取 **VARIANT** ，指出是否將 URL 字串中的百分比字元轉換成 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="17a6d-119">Sets or retrieves a **VARIANT** that indicates whether percent characters in the URL string are converted to an escape sequence.</span></span> <span data-ttu-id="17a6d-120">此選項的預設值為 **VARIANT \_ TRUE** ，指定所有不安全的美國國家標準局 (ANSI) 字元，但百分比符號會轉換成 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="17a6d-120">The default value of this option is **VARIANT\_TRUE** which specifies all unsafe American National Standards Institute (ANSI) characters except the percent symbol are converted to an escape sequence.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**</span><span class="sxs-lookup"><span data-stu-id="17a6d-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption\_SslErrorIgnoreFlags**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-122">設定或抓取 **VARIANT** ，指出應忽略的伺服器憑證錯誤。</span><span class="sxs-lookup"><span data-stu-id="17a6d-122">Sets or retrieves a **VARIANT** that indicates which server certificate errors should be ignored.</span></span> <span data-ttu-id="17a6d-123">這可以是下列其中一個或多個旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="17a6d-123">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="17a6d-124">錯誤</span><span class="sxs-lookup"><span data-stu-id="17a6d-124">Error</span></span>                                                  | <span data-ttu-id="17a6d-125">值</span><span class="sxs-lookup"><span data-stu-id="17a6d-125">Value</span></span>  |
|--------------------------------------------------------|--------|
| <span data-ttu-id="17a6d-126">未知的憑證授權單位單位 (CA) 或未受信任的根</span><span class="sxs-lookup"><span data-stu-id="17a6d-126">Unknown certification authority (CA) or untrusted root</span></span> | <span data-ttu-id="17a6d-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="17a6d-127">0x0100</span></span> |
| <span data-ttu-id="17a6d-128">錯誤的使用方式</span><span class="sxs-lookup"><span data-stu-id="17a6d-128">Wrong usage</span></span>                                            | <span data-ttu-id="17a6d-129">0x0200</span><span class="sxs-lookup"><span data-stu-id="17a6d-129">0x0200</span></span> |
| <span data-ttu-id="17a6d-130">不正確一般名稱 (CN) </span><span class="sxs-lookup"><span data-stu-id="17a6d-130">Invalid common name (CN)</span></span>                               | <span data-ttu-id="17a6d-131">0x1000</span><span class="sxs-lookup"><span data-stu-id="17a6d-131">0x1000</span></span> |
| <span data-ttu-id="17a6d-132">不正確日期或憑證已過期</span><span class="sxs-lookup"><span data-stu-id="17a6d-132">Invalid date or certificate expired</span></span>                    | <span data-ttu-id="17a6d-133">0x2000</span><span class="sxs-lookup"><span data-stu-id="17a6d-133">0x2000</span></span> |



 

<span data-ttu-id="17a6d-134">在5.1 版的 WinHTTP 中，此選項的預設值為零，因此不會忽略任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="17a6d-134">The default value of this option in Version 5.1 of WinHTTP is zero, which results in no errors being ignored.</span></span> <span data-ttu-id="17a6d-135">在舊版的 WinHTTP 中，預設設定為0x3300，這會導致預設忽略所有伺服器憑證錯誤。</span><span class="sxs-lookup"><span data-stu-id="17a6d-135">In earlier versions of WinHTTP, the default setting was 0x3300, which resulted in all server certificate errors being ignored by default.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**</span><span class="sxs-lookup"><span data-stu-id="17a6d-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption\_SelectCertificate**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-137">設定 **VARIANT** ，指定傳送至伺服器進行驗證的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="17a6d-137">Sets a **VARIANT** that specifies the client certificate that is sent to a server for authentication.</span></span> <span data-ttu-id="17a6d-138">此選項表示以反斜線分隔之用戶端憑證的位置、 [*憑證存放區*](glossary.md)和主體。</span><span class="sxs-lookup"><span data-stu-id="17a6d-138">This option indicates the location, [*certificate store*](glossary.md), and subject of a client certificate delimited with backslashes.</span></span> <span data-ttu-id="17a6d-139">如需有關選取用戶端憑證的詳細資訊，請參閱 [WinHTTP 中的 SSL](ssl-in-winhttp.md)。</span><span class="sxs-lookup"><span data-stu-id="17a6d-139">For more information about selecting a client certificate, see [SSL in WinHTTP](ssl-in-winhttp.md).</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**</span><span class="sxs-lookup"><span data-stu-id="17a6d-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption\_EnableRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-141">設定或抓取 **VARIANT** ，指出當伺服器指定資源的新位置時，是否會自動重新導向要求。</span><span class="sxs-lookup"><span data-stu-id="17a6d-141">Sets or retrieves a **VARIANT** that indicates whether requests are automatically redirected when the server specifies a new location for the resource.</span></span> <span data-ttu-id="17a6d-142">此選項的預設值為 **VARIANT \_ TRUE** ，表示要求會自動重新導向。</span><span class="sxs-lookup"><span data-stu-id="17a6d-142">The default value of this option is **VARIANT\_TRUE** to indicate that requests are automatically redirected.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption \_ UrlEscapeDisable**</span><span class="sxs-lookup"><span data-stu-id="17a6d-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption\_UrlEscapeDisable**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-144">設定或抓取 **VARIANT** ，指出 URL 的路徑和查詢元件中不安全的字元是否會轉換成 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="17a6d-144">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the path and query components of a URL are converted to escape sequences.</span></span> <span data-ttu-id="17a6d-145">此選項的預設值為 **VARIANT \_ TRUE**，指定要轉換路徑和查詢中的字元。</span><span class="sxs-lookup"><span data-stu-id="17a6d-145">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the path and query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**</span><span class="sxs-lookup"><span data-stu-id="17a6d-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption\_UrlEscapeDisableQuery**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-147">設定或抓取 **VARIANT** ，指出 URL 的查詢元件中不安全的字元是否會轉換成 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="17a6d-147">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the query component of the URL are converted to escape sequences.</span></span> <span data-ttu-id="17a6d-148">此選項的預設值為 **VARIANT \_ TRUE**，指定要轉換查詢中的字元。</span><span class="sxs-lookup"><span data-stu-id="17a6d-148">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**</span><span class="sxs-lookup"><span data-stu-id="17a6d-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption\_SecureProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-150">設定或抓取表示可以使用哪些安全通訊協定的 **變異** 。</span><span class="sxs-lookup"><span data-stu-id="17a6d-150">Sets or retrieves a **VARIANT** that indicates which secure protocols can be used.</span></span> <span data-ttu-id="17a6d-151">此選項會選取用戶端可接受的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="17a6d-151">This option selects the protocols acceptable to the client.</span></span> <span data-ttu-id="17a6d-152">此通訊協定會在安全通訊端層 (SSL) 信號交換期間進行協商。</span><span class="sxs-lookup"><span data-stu-id="17a6d-152">The protocol is negotiated during the Secure Sockets Layer (SSL) handshake.</span></span> <span data-ttu-id="17a6d-153">這可以是下列其中一個或多個旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="17a6d-153">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="17a6d-154">通訊協定</span><span class="sxs-lookup"><span data-stu-id="17a6d-154">Protocol</span></span>                           | <span data-ttu-id="17a6d-155">值</span><span class="sxs-lookup"><span data-stu-id="17a6d-155">Value</span></span>  |
|------------------------------------|--------|
| <span data-ttu-id="17a6d-156">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="17a6d-156">SSL 2.0</span></span>                            | <span data-ttu-id="17a6d-157">0x0008</span><span class="sxs-lookup"><span data-stu-id="17a6d-157">0x0008</span></span> |
| <span data-ttu-id="17a6d-158">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="17a6d-158">SSL 3.0</span></span>                            | <span data-ttu-id="17a6d-159">0x0020</span><span class="sxs-lookup"><span data-stu-id="17a6d-159">0x0020</span></span> |
| <span data-ttu-id="17a6d-160">傳輸層安全性 (TLS) 1。0</span><span class="sxs-lookup"><span data-stu-id="17a6d-160">Transport Layer Security (TLS) 1.0</span></span> | <span data-ttu-id="17a6d-161">0x0080</span><span class="sxs-lookup"><span data-stu-id="17a6d-161">0x0080</span></span> |



 

<span data-ttu-id="17a6d-162">此選項的預設值為0x0028，表示可以使用 SSL 2.0 或 SSL 3.0。</span><span class="sxs-lookup"><span data-stu-id="17a6d-162">The default value of this option is 0x0028, which indicates that SSL 2.0 or SSL 3.0 can be used.</span></span> <span data-ttu-id="17a6d-163">如果此選項設定為零，用戶端和伺服器就無法判斷可接受的安全性通訊協定，而下一個 [**傳送**](iwinhttprequest-send.md) 會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="17a6d-163">If this option is set to zero, the client and server are not able to determine an acceptable security protocol and the next [**Send**](iwinhttprequest-send.md) results in an error.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption \_ EnableTracing**</span><span class="sxs-lookup"><span data-stu-id="17a6d-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption\_EnableTracing**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-165">設定或抓取表示追蹤目前是否已啟用的 **變異** 。</span><span class="sxs-lookup"><span data-stu-id="17a6d-165">Sets or retrieves a **VARIANT** that indicates whether tracing is currently enabled.</span></span> <span data-ttu-id="17a6d-166">如需有關 Microsoft Windows HTTP Services (WinHTTP) 中追蹤設備的詳細資訊，請參閱 [WinHTTP 追蹤設備](winhttptracecfg-exe--a-trace-configuration-tool.md)。</span><span class="sxs-lookup"><span data-stu-id="17a6d-166">For more information about the trace facility in Microsoft Windows HTTP Services (WinHTTP), see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**</span><span class="sxs-lookup"><span data-stu-id="17a6d-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption\_RevertImpersonationOverSsl**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-168">控制 [**WinHttpRequest**](winhttprequest.md) 物件是否會在 SSL 憑證驗證作業期間，暫時還原用戶端模擬。</span><span class="sxs-lookup"><span data-stu-id="17a6d-168">Controls whether the [**WinHttpRequest**](winhttprequest.md) object temporarily reverts client impersonation for the duration of the SSL certificate authentication operations.</span></span> <span data-ttu-id="17a6d-169">**WinHttpRequest** 物件的預設設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="17a6d-169">The default setting for the **WinHttpRequest** object is **TRUE**.</span></span> <span data-ttu-id="17a6d-170">將此選項設定為 **FALSE** ，以在執行憑證驗證作業時保持模擬。</span><span class="sxs-lookup"><span data-stu-id="17a6d-170">Set this option to **FALSE** to keep impersonation while performing certificate authentication operations.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**</span><span class="sxs-lookup"><span data-stu-id="17a6d-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption\_EnableHttpsToHttpRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-172">控制 WinHTTP 是否允許重新導向。</span><span class="sxs-lookup"><span data-stu-id="17a6d-172">Controls whether or not WinHTTP allows redirects.</span></span> <span data-ttu-id="17a6d-173">根據預設，除了從安全的 (HTTPs) URL 傳送至不安全的 (HTTP) URL 以外，所有重新導向都會自動遵循。</span><span class="sxs-lookup"><span data-stu-id="17a6d-173">By default, all redirects are automatically followed, except those that transfer from a secure (https) URL to an non-secure (http) URL.</span></span> <span data-ttu-id="17a6d-174">將此選項設定為 **TRUE** ，以啟用 HTTPS 對 HTTP 重新導向。</span><span class="sxs-lookup"><span data-stu-id="17a6d-174">Set this option to **TRUE** to enable HTTPS to HTTP redirects.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**</span><span class="sxs-lookup"><span data-stu-id="17a6d-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption\_EnablePassportAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-176">啟用或停用 Passport 驗證的支援。</span><span class="sxs-lookup"><span data-stu-id="17a6d-176">Enables or disables support for Passport authentication.</span></span> <span data-ttu-id="17a6d-177">預設會停用 Passport 驗證的自動支援;將此選項設定為 **TRUE** ，以啟用 Passport 驗證支援。</span><span class="sxs-lookup"><span data-stu-id="17a6d-177">By default, automatic support for Passport authentication is disabled; set this option to **TRUE** to enable Passport authentication support.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**</span><span class="sxs-lookup"><span data-stu-id="17a6d-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption\_MaxAutomaticRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-179">設定或抓取 WinHTTP 遵循的重新導向數目上限;預設值為10。</span><span class="sxs-lookup"><span data-stu-id="17a6d-179">Sets or retrieves the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="17a6d-180">這項限制可防止未經授權的網站在大量重新導向之後讓 WinHTTP 用戶端停止。</span><span class="sxs-lookup"><span data-stu-id="17a6d-180">This limit prevents unauthorized sites from making the WinHTTP client stall following a large number of redirects.</span></span>

<span data-ttu-id="17a6d-181">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 不支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="17a6d-181">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**</span><span class="sxs-lookup"><span data-stu-id="17a6d-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption\_MaxResponseHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-183">設定或抓取伺服器回應之標頭部分大小上限的系結集合。</span><span class="sxs-lookup"><span data-stu-id="17a6d-183">Sets or retrieves a bound set on the maximum size of the header portion of the server's response.</span></span> <span data-ttu-id="17a6d-184">這項系結會透過傳送無限標頭資料的回應，來保護用戶端免于嘗試停止用戶端的惡意伺服器。</span><span class="sxs-lookup"><span data-stu-id="17a6d-184">This bound protects the client from a malicious server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="17a6d-185">預設值為 64 KB。</span><span class="sxs-lookup"><span data-stu-id="17a6d-185">The default value is 64 KB.</span></span>

<span data-ttu-id="17a6d-186">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 不支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="17a6d-186">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**</span><span class="sxs-lookup"><span data-stu-id="17a6d-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption\_MaxResponseDrainSize**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-188">設定或抓取將從回應清空的資料量的系結，以便重複使用連接。</span><span class="sxs-lookup"><span data-stu-id="17a6d-188">Sets or retrieves a bound on the amount of data that will be drained from responses in order to reuse a connection.</span></span> <span data-ttu-id="17a6d-189">預設值是 1 MB。</span><span class="sxs-lookup"><span data-stu-id="17a6d-189">The default is 1 MB.</span></span>

<span data-ttu-id="17a6d-190">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 不支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="17a6d-190">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="17a6d-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption\_EnableHttp1\_1**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-192">設定或抓取布林值，指出是否應該使用 HTTP/1.1 或 HTTP/1.0。</span><span class="sxs-lookup"><span data-stu-id="17a6d-192">Sets or retrieves a boolean value that indicates whether HTTP/1.1 or HTTP/1.0 should be used.</span></span> <span data-ttu-id="17a6d-193">預設值為 **TRUE**，因此預設會使用 HTTP/1.1。</span><span class="sxs-lookup"><span data-stu-id="17a6d-193">The default is **TRUE**, so that HTTP/1.1 is used by default.</span></span>

<span data-ttu-id="17a6d-194">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 不支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="17a6d-194">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="17a6d-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**</span><span class="sxs-lookup"><span data-stu-id="17a6d-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption\_EnableCertificateRevocationCheck**</span></span>
</dt> <dd>

<span data-ttu-id="17a6d-196">啟用 SSL 協商期間的伺服器憑證撤銷檢查。</span><span class="sxs-lookup"><span data-stu-id="17a6d-196">Enables server certificate revocation checking during SSL negotiation.</span></span> <span data-ttu-id="17a6d-197">當伺服器呈現憑證時，會執行檢查，以判斷憑證是否已被其簽發者撤銷。</span><span class="sxs-lookup"><span data-stu-id="17a6d-197">When the server presents a certificate, a check is performed to determine whether the certificate has been revoked by its issuer.</span></span> <span data-ttu-id="17a6d-198">如果憑證確實撤銷，或撤銷檢查失敗，因為無法下載憑證撤銷清單 (CRL) ，要求會失敗;這類撤銷錯誤無法隱藏。</span><span class="sxs-lookup"><span data-stu-id="17a6d-198">If the certificate is indeed revoked, or the revocation check fails because the Certificate Revocation List (CRL) cannot be downloaded, the request fails; such revocation errors cannot be suppressed.</span></span>

<span data-ttu-id="17a6d-199">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 不支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="17a6d-199">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17a6d-200">備註</span><span class="sxs-lookup"><span data-stu-id="17a6d-200">Remarks</span></span>

<span data-ttu-id="17a6d-201">藉由指定上述其中一個常數作為 [**option**](iwinhttprequest-option.md) 屬性的參數，來設定選項。</span><span class="sxs-lookup"><span data-stu-id="17a6d-201">Set an option by specifying one of the preceding constants as the parameter of the [**Option**](iwinhttprequest-option.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="17a6d-202">針對 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="17a6d-202">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17a6d-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="17a6d-203">Requirements</span></span>



| <span data-ttu-id="17a6d-204">需求</span><span class="sxs-lookup"><span data-stu-id="17a6d-204">Requirement</span></span> | <span data-ttu-id="17a6d-205">值</span><span class="sxs-lookup"><span data-stu-id="17a6d-205">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="17a6d-206">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17a6d-206">Minimum supported client</span></span><br/> | <span data-ttu-id="17a6d-207">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17a6d-207">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="17a6d-208">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17a6d-208">Minimum supported server</span></span><br/> | <span data-ttu-id="17a6d-209">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="17a6d-209">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="17a6d-210">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="17a6d-210">Redistributable</span></span><br/>          | <span data-ttu-id="17a6d-211">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="17a6d-211">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="17a6d-212">Idl</span><span class="sxs-lookup"><span data-stu-id="17a6d-212">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17a6d-213"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="17a6d-213"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17a6d-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17a6d-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a6d-215">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="17a6d-215">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




