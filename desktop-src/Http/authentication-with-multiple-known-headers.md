---
title: 使用多個已知標頭進行驗證
description: HTTP \_ MULTIPLE \_ 已知 \_ 標頭結構可讓伺服器應用程式將多個驗證挑戰傳送給用戶端。
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8afbce3c2a41ea143003723acebc7eb83dc463d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "107001064"
---
# <a name="authentication-with-multiple-known-headers"></a><span data-ttu-id="560bd-103">使用多個已知標頭進行驗證</span><span class="sxs-lookup"><span data-stu-id="560bd-103">Authentication with Multiple Known Headers</span></span>

<span data-ttu-id="560bd-104">[**HTTP \_ MULTIPLE \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers)結構可讓伺服器應用程式將多個驗證挑戰傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="560bd-104">The [**HTTP\_MULTIPLE\_KNOWN\_HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) structure enables server applications to send multiple authentication challenges to the client.</span></span> <span data-ttu-id="560bd-105">應用程式可以透過單一驗證配置來挑戰用戶端，方法是在 [**HTTP \_ 回應**](http-response.md)所包含的 [**HTTP \_ 回應 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_response_headers)結構的 **KnownHeaders** 成員中提供 **HttpHeaderWwwAuthenticate** 列舉類型。</span><span class="sxs-lookup"><span data-stu-id="560bd-105">Applications can challenge the client with a single authentication scheme by supplying the **HttpHeaderWwwAuthenticate** enumeration type in the **KnownHeaders** member of the [**HTTP\_RESPONSE\_HEADERS**](/windows/desktop/api/Http/ns-http-http_response_headers) structure contained in [**HTTP\_RESPONSE**](http-response.md).</span></span> <span data-ttu-id="560bd-106">不過，當伺服器在使用多個驗證配置時遇到問題時，應用程式會使用 [**HTTP \_ multiple \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) 結構來提供驗證類型。</span><span class="sxs-lookup"><span data-stu-id="560bd-106">However, when the server challenges with multiple authentication schemes, the application uses the [**HTTP\_MULTIPLE\_KNOWN\_HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) structure to provide the authentication types.</span></span>

<span data-ttu-id="560bd-107">當 **HTTP \_ 回應 \_ 資訊 \_ 旗標 \_ 保留 \_ 順序** 旗標存在時，HTTP 會以指定的順序傳送驗證標頭。</span><span class="sxs-lookup"><span data-stu-id="560bd-107">When the **HTTP\_RESPONSE\_INFO\_FLAGS\_PRESERVE\_ORDER** flag is present, HTTP sends the authentication headers in the specified order.</span></span> <span data-ttu-id="560bd-108">如果旗標不存在，HTTP 會將驗證配置從最強到最弱排序，如下所示：</span><span class="sxs-lookup"><span data-stu-id="560bd-108">If the flag is not present, HTTP orders the authentication schemes from strongest to weakest as follows:</span></span>

1.  <span data-ttu-id="560bd-109">交涉</span><span class="sxs-lookup"><span data-stu-id="560bd-109">Negotiate</span></span>
2.  <span data-ttu-id="560bd-110">NTLM</span><span class="sxs-lookup"><span data-stu-id="560bd-110">NTLM</span></span>
3.  <span data-ttu-id="560bd-111">Digest</span><span class="sxs-lookup"><span data-stu-id="560bd-111">Digest</span></span>
4.  <span data-ttu-id="560bd-112">基本</span><span class="sxs-lookup"><span data-stu-id="560bd-112">Basic</span></span>

<span data-ttu-id="560bd-113">如果驗證配置不是這些配置的其中一個，則應用程式必須指定 **HTTP \_ 回應 \_ 資訊 \_ 旗標 \_ 保留 \_ 順序旗標** 。</span><span class="sxs-lookup"><span data-stu-id="560bd-113">If the authentication scheme is not one of these schemes, the application must specify the **HTTP\_RESPONSE\_INFO\_FLAGS\_PRESERVE\_ORDER** flag.</span></span>

<span data-ttu-id="560bd-114">[**Http \_ 多個 \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers)的 **KnownHeader** 成員指向 [**HTTP \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_known_header)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="560bd-114">The **KnownHeader** member of [**HTTP\_MULTIPLE\_KNOWN\_HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) points to an array of [**HTTP\_KNOWN\_HEADER**](/windows/desktop/api/Http/ns-http-http_known_header) structures.</span></span> <span data-ttu-id="560bd-115">**HTTP \_ 已知 \_ 標頭** 結構的 **pRawValue** 成員必須指向指定配置名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="560bd-115">The **pRawValue** member of the **HTTP\_KNOWN\_HEADER** structure must point to a string that specifies the scheme name.</span></span> <span data-ttu-id="560bd-116">HTTP 會剖析字串以判斷配置，並執行下列其中一個動作：</span><span class="sxs-lookup"><span data-stu-id="560bd-116">HTTP parses the string to determine the scheme and performs one of the following actions:</span></span>

-   <span data-ttu-id="560bd-117">如果字串包含不明的驗證類型，或如果設定群組上未啟用驗證類型 () 與要求相關聯的 URL 群組或伺服器會話，HTTP 伺服器 API 會將 **pRawValue** 中的字串附加至 WWW-Authenticate 標頭。</span><span class="sxs-lookup"><span data-stu-id="560bd-117">If the string contains an unknown authentication type, or if the authentication type is not enabled on the configuration group (either the URL group or server session) associated with the request, the HTTP Server API appends the string in **pRawValue** to the WWW-Authenticate header.</span></span> <span data-ttu-id="560bd-118">例如，如果應用程式指定不支援的驗證配置，且 **pRawValue** 包含字串 "CustomAuthString"，則會將下列文字附加至驗證標頭：</span><span class="sxs-lookup"><span data-stu-id="560bd-118">For example, if the application specifies an unsupported authentication scheme, and **pRawValue** contains the string "CustomAuthString", the following text is appended to the authentication header:</span></span>

    <span data-ttu-id="560bd-119">WWW 驗證： CustomAuthSchemeCRLF</span><span class="sxs-lookup"><span data-stu-id="560bd-119">WWW-Authenticate: CustomAuthSchemeCRLF</span></span>

    <span data-ttu-id="560bd-120">如果應用程式未啟用基本驗證，且 **pRawValue** 包含字串 "basic realm =" BasicRealm ""，則驗證標頭包含下列文字：</span><span class="sxs-lookup"><span data-stu-id="560bd-120">If the application does not have Basic authentication enabled, and **pRawValue** contains the string "Basic realm="BasicRealm"", the authentication header contains the following text:</span></span>

    <span data-ttu-id="560bd-121">WWW-驗證：基本領域 = "BasicRealm"</span><span class="sxs-lookup"><span data-stu-id="560bd-121">WWW-Authenticate: Basic realm="BasicRealm"</span></span>

-   <span data-ttu-id="560bd-122">如果字串包含已知的驗證類型，而且存在於設定群組 (URL 群組或伺服器會話) 與要求相關聯，HTTP 伺服器 API 就會產生 WWW-Authenticate 標頭。</span><span class="sxs-lookup"><span data-stu-id="560bd-122">If the string contains a known authentication type and is present on the configuration group (either the URL group or the server session) associated with the request, the HTTP Server API generates the WWW-Authenticate header.</span></span> <span data-ttu-id="560bd-123">例如，如果在 **pRawValue** 中指定的字串為 "digest"，且在伺服器會話上啟用了 Digest，則 HTTP 伺服器 API 會將下列文字附加至驗證標頭：</span><span class="sxs-lookup"><span data-stu-id="560bd-123">For example if the string specified in **pRawValue** is "Digest", and Digest is enabled on the server session, the HTTP Server API appends the following text to the authentication header:</span></span>

    <span data-ttu-id="560bd-124">WWW-驗證：摘要領域 = " testrealm@host.com "</span><span class="sxs-lookup"><span data-stu-id="560bd-124">WWW-Authenticate: Digest realm="testrealm@host.com"</span></span>

<span data-ttu-id="560bd-125">如果 [**HTTP \_ 已知 \_ 標頭**](/windows/desktop/api/Http/ns-http-http_known_header)的 **pRawValue** 成員中的配置為 Negotiate 或 NTLM，則驗證配置名稱即已足夠。</span><span class="sxs-lookup"><span data-stu-id="560bd-125">If the scheme in the **pRawValue** member of [**HTTP\_KNOWN\_HEADER**](/windows/desktop/api/Http/ns-http-http_known_header) is Negotiate or NTLM, the authentication scheme name is sufficient.</span></span> <span data-ttu-id="560bd-126">如果指定的配置是基本的，則會將領域名稱附加至配置名稱;應用程式不需要在 **pRawValue** 中提供領域名稱。</span><span class="sxs-lookup"><span data-stu-id="560bd-126">If the specified scheme is Basic, the realm name is appended to the scheme name; the application doesn't need to supply the realm name in **pRawValue**.</span></span> <span data-ttu-id="560bd-127">如果指定的配置為 Digest，HTTP 會呼叫 [**AcceptSecurityCoNtext**](../SecAuthN/acceptsecuritycontext--general.md) ，以產生附加至配置名稱的挑戰。</span><span class="sxs-lookup"><span data-stu-id="560bd-127">If the specified scheme is Digest, HTTP calls [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) to generate the challenge that is appended to the scheme name.</span></span> <span data-ttu-id="560bd-128">您可以從對應的設定群組驗證資訊取得基本 (領域) 和摘要 (領域和功能變數名稱) 配置的參數。</span><span class="sxs-lookup"><span data-stu-id="560bd-128">The parameters for Basic (realm) and Digest (realm and domain name) scheme are obtained from the corresponding configuration group authentication information.</span></span>

<span data-ttu-id="560bd-129">當應用程式將多個驗證挑戰傳送至未知要求標頭中的用戶端時，HTTP 伺服器 API 會將這些挑戰傳送給用戶端，而不需要介入。</span><span class="sxs-lookup"><span data-stu-id="560bd-129">When the application sends multiple authentication challenges to the client in Unknown request headers, the HTTP Server API sends these to the client without intervention.</span></span> <span data-ttu-id="560bd-130">但不建議使用這種方式。</span><span class="sxs-lookup"><span data-stu-id="560bd-130">However this usage is not recommended.</span></span>

 

 




