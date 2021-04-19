---
description: 某些 HTTP 伺服器和 proxy 需要驗證，才能允許存取網際網路上的資源。 Microsoft Windows HTTP Services (WinHTTP) 函數支援 HTTP 會話的伺服器和 proxy 驗證。
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: WinHTTP 中的驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75c6703e9d28902c5705f0b8ab8433193c4d085
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380824"
---
# <a name="authentication-in-winhttp"></a><span data-ttu-id="844ed-104">WinHTTP 中的驗證</span><span class="sxs-lookup"><span data-stu-id="844ed-104">Authentication in WinHTTP</span></span>

<span data-ttu-id="844ed-105">某些 HTTP 伺服器和 proxy 需要驗證，才能允許存取網際網路上的資源。</span><span class="sxs-lookup"><span data-stu-id="844ed-105">Some HTTP servers and proxies require authentication before allowing access to resources on the Internet.</span></span> <span data-ttu-id="844ed-106">Microsoft Windows HTTP Services (WinHTTP) 函數支援 HTTP 會話的伺服器和 proxy 驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-106">The Microsoft Windows HTTP Services (WinHTTP) functions support server and proxy authentication for HTTP sessions.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="844ed-107">關於 HTTP 驗證</span><span class="sxs-lookup"><span data-stu-id="844ed-107">About HTTP Authentication</span></span>

<span data-ttu-id="844ed-108">如果需要驗證，HTTP 應用程式會收到狀態碼 401 (server 需要驗證) 或 407 (proxy 需要驗證) 。</span><span class="sxs-lookup"><span data-stu-id="844ed-108">If authentication is required, the HTTP application receives a status code of 401 (server requires authentication) or 407 (proxy requires authentication).</span></span> <span data-ttu-id="844ed-109">除了狀態碼，proxy 或伺服器也會傳送一或多個驗證標頭： WWW-Authenticate (進行伺服器驗證) 或 Proxy-Authenticate (進行 proxy 驗證) 。</span><span class="sxs-lookup"><span data-stu-id="844ed-109">Along with the status code, the proxy or server sends one or more authenticate headers: WWW-Authenticate (for server authentication) or Proxy-Authenticate (for proxy authentication).</span></span>

<span data-ttu-id="844ed-110">每個驗證標頭都包含支援的驗證配置，以及適用于基本和摘要式配置的領域。</span><span class="sxs-lookup"><span data-stu-id="844ed-110">Each authenticate header contains a supported authentication scheme and, for the Basic and Digest schemes, a realm.</span></span> <span data-ttu-id="844ed-111">如果支援多個驗證配置，伺服器會傳回多個驗證標頭。</span><span class="sxs-lookup"><span data-stu-id="844ed-111">If multiple authentication schemes are supported, the server returns multiple authenticate headers.</span></span> <span data-ttu-id="844ed-112">領域值會區分大小寫，而且會定義一組接受相同認證的伺服器或 proxy。</span><span class="sxs-lookup"><span data-stu-id="844ed-112">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials are accepted.</span></span> <span data-ttu-id="844ed-113">例如，在需要伺服器驗證時，可能會傳回標頭 "WWW-驗證：基本領域 =" 範例 ""。</span><span class="sxs-lookup"><span data-stu-id="844ed-113">For example, the header "WWW-Authenticate: Basic Realm="example"" might be returned when server authentication is required.</span></span> <span data-ttu-id="844ed-114">此標頭會指定必須提供「範例」網域的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="844ed-114">This header specifies that user credentials must be supplied for the "example" domain.</span></span>

<span data-ttu-id="844ed-115">HTTP 應用程式可包含授權標頭欄位，並將要求傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="844ed-115">An HTTP application can include an authorization header field with a request it sends to the server.</span></span> <span data-ttu-id="844ed-116">授權標頭包含驗證配置，以及該配置所需的適當回應。</span><span class="sxs-lookup"><span data-stu-id="844ed-116">The authorization header contains the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="844ed-117">例如， \<username:password> 如果用戶端收到回應標頭 "WWW-驗證：基本領域 =" 範例 ""，就會將標頭 "Authorization： basic" 新增至要求，並傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="844ed-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and sent to the server if the client received the response header "WWW-Authenticate: Basic Realm="example"".</span></span>

> [!Note]  
> <span data-ttu-id="844ed-118">雖然在此以純文字形式顯示，但使用者名稱和密碼實際上是以 [*base64 編碼*](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="844ed-118">Although they are shown here as plain text, the username and password are actually [*base64 encoded*](glossary.md).</span></span>

 

<span data-ttu-id="844ed-119">驗證架構有兩種一般類型：</span><span class="sxs-lookup"><span data-stu-id="844ed-119">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="844ed-120">基本驗證配置，在此配置中，使用者名稱和密碼會以純文字傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="844ed-120">Basic authentication scheme, in which the user name and password are sent in clear text to the server.</span></span>

    <span data-ttu-id="844ed-121">基本驗證配置是以用戶端必須用來識別每個領域的使用者名稱和密碼的模型為基礎。</span><span class="sxs-lookup"><span data-stu-id="844ed-121">The Basic authentication scheme is based on the model that a client must identify itself with a user name and password for each realm.</span></span> <span data-ttu-id="844ed-122">只有在要求是以包含有效使用者名稱和密碼的授權標頭傳送時，伺服器才會為要求提供服務。</span><span class="sxs-lookup"><span data-stu-id="844ed-122">The server services the request only if the request is sent with an authorization header that includes a valid user name and password.</span></span>

-   <span data-ttu-id="844ed-123">挑戰-回應配置（例如 Kerberos），伺服器會使用 [*驗證資料*](glossary.md)來挑戰用戶端。</span><span class="sxs-lookup"><span data-stu-id="844ed-123">Challenge-response schemes, such as Kerberos, in which the server challenges the client with [*authentication data*](glossary.md).</span></span> <span data-ttu-id="844ed-124">用戶端會使用使用者認證來轉換資料，並將轉換後的資料傳送回伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-124">The client transforms the data with the user credentials and sends the transformed data back to the server for authentication.</span></span>

    <span data-ttu-id="844ed-125">挑戰-回應配置可啟用更安全的驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-125">Challenge-response schemes enable a more secure authentication.</span></span> <span data-ttu-id="844ed-126">在挑戰-回應配置中，使用者名稱和密碼永遠不會透過網路傳輸。</span><span class="sxs-lookup"><span data-stu-id="844ed-126">In a challenge-response scheme, the username and password are never transmitted over the network.</span></span> <span data-ttu-id="844ed-127">在用戶端選取挑戰回應配置之後，伺服器會傳回適當的狀態碼，其中包含該配置的 [*驗證資料*](glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="844ed-127">After the client selects a challenge-response scheme, the server returns an appropriate status code with a challenge that contains the [*authentication data*](glossary.md) for that scheme.</span></span> <span data-ttu-id="844ed-128">然後，用戶端會以適當的回應重新傳送要求，以取得所要求的服務。</span><span class="sxs-lookup"><span data-stu-id="844ed-128">The client then resends the request with the proper response to obtain the requested service.</span></span> <span data-ttu-id="844ed-129">挑戰-回應配置可能需要多個交換才能完成。</span><span class="sxs-lookup"><span data-stu-id="844ed-129">Challenge-response schemes can take multiple exchanges to complete.</span></span>

<span data-ttu-id="844ed-130">下表包含 WinHTTP 支援的驗證配置、驗證類型，以及配置的描述。</span><span class="sxs-lookup"><span data-stu-id="844ed-130">The following table contains the authentication schemes that are supported by WinHTTP, the authentication type, and a description of the scheme.</span></span>



| <span data-ttu-id="844ed-131">配置</span><span class="sxs-lookup"><span data-stu-id="844ed-131">Scheme</span></span>            | <span data-ttu-id="844ed-132">類型</span><span class="sxs-lookup"><span data-stu-id="844ed-132">Type</span></span>               | <span data-ttu-id="844ed-133">Description</span><span class="sxs-lookup"><span data-stu-id="844ed-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="844ed-134">基本 (純文字) </span><span class="sxs-lookup"><span data-stu-id="844ed-134">Basic (plaintext)</span></span> | <span data-ttu-id="844ed-135">基本</span><span class="sxs-lookup"><span data-stu-id="844ed-135">Basic</span></span>              | <span data-ttu-id="844ed-136">使用 [*base64 編碼*](glossary.md) 的字串，其中包含使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="844ed-136">Uses a [*base64 encoded*](glossary.md) string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="844ed-137">Digest</span><span class="sxs-lookup"><span data-stu-id="844ed-137">Digest</span></span>            | <span data-ttu-id="844ed-138">挑戰-回應</span><span class="sxs-lookup"><span data-stu-id="844ed-138">Challenge-response</span></span> | <span data-ttu-id="844ed-139">使用 nonce (伺服器指定的資料字串) 值的挑戰。</span><span class="sxs-lookup"><span data-stu-id="844ed-139">Challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="844ed-140">有效的回應包含使用者名稱、密碼、指定的 nonce 值、 [*HTTP 動詞*](glossary.md)命令，以及要求的統一資源識別項 (URI) 的總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="844ed-140">A valid response contains a checksum of the user name, the password, the given nonce value, the [*HTTP verb*](glossary.md), and the requested Uniform Resource Identifier (URI).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="844ed-141">NTLM</span><span class="sxs-lookup"><span data-stu-id="844ed-141">NTLM</span></span>              | <span data-ttu-id="844ed-142">挑戰-回應</span><span class="sxs-lookup"><span data-stu-id="844ed-142">Challenge-response</span></span> | <span data-ttu-id="844ed-143">需要使用使用者認證來轉換 [*驗證資料*](glossary.md) ，以證明身分識別。</span><span class="sxs-lookup"><span data-stu-id="844ed-143">Requires the [*authentication data*](glossary.md) to be transformed with the user credentials to prove identity.</span></span> <span data-ttu-id="844ed-144">若要讓 NTLM 驗證正常運作，必須在相同的連接上進行數個交換。</span><span class="sxs-lookup"><span data-stu-id="844ed-144">For NTLM authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="844ed-145">因此，如果仲介 proxy 不支援 keep-alive 連接，則無法使用 NTLM 驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-145">Therefore, NTLM authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="844ed-146">如果 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 搭配 [**WINHTTP \_ 停用 \_ 保持 \_**](option-flags.md) 運作旗標來停用 keep-alive 語義，則 NTLM 驗證也會失敗。</span><span class="sxs-lookup"><span data-stu-id="844ed-146">NTLM authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="844ed-147">Passport</span><span class="sxs-lookup"><span data-stu-id="844ed-147">Passport</span></span>          | <span data-ttu-id="844ed-148">挑戰-回應</span><span class="sxs-lookup"><span data-stu-id="844ed-148">Challenge-response</span></span> | <span data-ttu-id="844ed-149">使用 [Microsoft Passport 1.4](passport-authentication-in-winhttp.md)。</span><span class="sxs-lookup"><span data-stu-id="844ed-149">Uses [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="844ed-150">交涉</span><span class="sxs-lookup"><span data-stu-id="844ed-150">Negotiate</span></span>         | <span data-ttu-id="844ed-151">挑戰-回應</span><span class="sxs-lookup"><span data-stu-id="844ed-151">Challenge-response</span></span> | <span data-ttu-id="844ed-152">如果伺服器和用戶端都使用 Windows 2000 或更新版本，則會使用 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-152">If both the server and client are using Windows 2000 or later, Kerberos authentication is used.</span></span> <span data-ttu-id="844ed-153">否則會使用 NTLM 驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-153">Otherwise NTLM authentication is used.</span></span> <span data-ttu-id="844ed-154">Kerberos 適用于 Windows 2000 和更新版本的作業系統，而且會被視為比 NTLM 驗證更安全。</span><span class="sxs-lookup"><span data-stu-id="844ed-154">Kerberos is available in Windows 2000 and later operating systems and is considered to be more secure than NTLM authentication.</span></span> <span data-ttu-id="844ed-155">若要讓 Negotiate 驗證正常運作，必須在相同的連接上進行數個交換。</span><span class="sxs-lookup"><span data-stu-id="844ed-155">For Negotiate authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="844ed-156">因此，如果仲介 proxy 不支援 keep-alive 連接，則無法使用 Negotiate 驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-156">Therefore, Negotiate authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="844ed-157">如果使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 搭配 [**WINHTTP \_ 停用 \_ 保持 \_**](option-flags.md) 運作旗標來停用 keep-alive 語義，則協商驗證也會失敗。</span><span class="sxs-lookup"><span data-stu-id="844ed-157">Negotiate authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span> <span data-ttu-id="844ed-158">「協商驗證」配置有時也稱為整合式 Windows 驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-158">The Negotiate authentication scheme is sometimes called Integrated Windows authentication.</span></span> |



 

## <a name="authentication-in-winhttp-applications"></a><span data-ttu-id="844ed-159">WinHTTP 應用程式中的驗證</span><span class="sxs-lookup"><span data-stu-id="844ed-159">Authentication in WinHTTP Applications</span></span>

<span data-ttu-id="844ed-160"> (API) 的 WinHTTP 應用程式開發介面提供兩個函式，可在需要驗證的情況下用來存取網際網路資源： [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) 和 [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)。</span><span class="sxs-lookup"><span data-stu-id="844ed-160">The WinHTTP application programming interface (API) provides two functions used to access Internet resources in situations where authentication is required: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) and [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span></span>

<span data-ttu-id="844ed-161">收到具有401或407狀態碼的回應時， [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) 可以用來剖析驗證標頭，以判斷支援的驗證配置和驗證目標。</span><span class="sxs-lookup"><span data-stu-id="844ed-161">When a response is received with a 401 or 407 status code, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) can be used to parse the authentication headers to determine the supported authentication schemes and the authentication target.</span></span> <span data-ttu-id="844ed-162">驗證目標是要求驗證的伺服器或 proxy。</span><span class="sxs-lookup"><span data-stu-id="844ed-162">The authentication target is the server or proxy that requests authentication.</span></span> <span data-ttu-id="844ed-163">**WinHttpQueryAuthSchemes** 也會根據伺服器建議的驗證配置喜好設定，從可用的配置中判斷第一個驗證配置。</span><span class="sxs-lookup"><span data-stu-id="844ed-163">**WinHttpQueryAuthSchemes** also determines the first authentication scheme, from the available schemes, based on the authentication scheme preferences suggested by the server.</span></span> <span data-ttu-id="844ed-164">這種選擇驗證配置的方法，是 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)所建議的行為。</span><span class="sxs-lookup"><span data-stu-id="844ed-164">This method for choosing an authentication scheme is the behavior suggested by [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

<span data-ttu-id="844ed-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) 可讓應用程式指定驗證配置，搭配有效的使用者名稱和密碼使用於目標伺服器或 proxy。</span><span class="sxs-lookup"><span data-stu-id="844ed-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) enables an application to specify the authentication scheme that is used along with a valid username and password for use on the target server or proxy.</span></span> <span data-ttu-id="844ed-166">設定認證並重新傳送要求之後，會自動產生必要的標頭，並將其新增至要求。</span><span class="sxs-lookup"><span data-stu-id="844ed-166">After setting the credentials and resending the request, the necessary headers are generated and added to the request automatically.</span></span> <span data-ttu-id="844ed-167">由於某些驗證配置需要多個交易 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 可能會傳回錯誤，因此會發生錯誤的 \_ WINHTTP 重 \_ 送 \_ 要求。</span><span class="sxs-lookup"><span data-stu-id="844ed-167">Because some authentication schemes require multiple transactions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) could return the error, ERROR\_WINHTTP\_RESEND\_REQUEST.</span></span> <span data-ttu-id="844ed-168">遇到此錯誤時，應用程式應繼續重新傳送要求，直到收到未包含401或407狀態碼的回應為止。</span><span class="sxs-lookup"><span data-stu-id="844ed-168">When this error is encountered, the application should continue to resend the request until a response is received that does not contain a 401 or 407 status code.</span></span> <span data-ttu-id="844ed-169">200狀態碼表示資源可供使用，且要求成功。</span><span class="sxs-lookup"><span data-stu-id="844ed-169">A 200 status code indicates that the resource is available and the request is successful.</span></span> <span data-ttu-id="844ed-170">請參閱 [**HTTP 狀態碼**](http-status-codes.md) ，以取得可傳回的其他狀態碼。</span><span class="sxs-lookup"><span data-stu-id="844ed-170">See [**HTTP Status Codes**](http-status-codes.md) for additional status codes that can be returned.</span></span>

<span data-ttu-id="844ed-171">如果在將要求傳送到伺服器之前，已知可接受的驗證配置和認證，則應用程式可以呼叫 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) ，然後再呼叫 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)。</span><span class="sxs-lookup"><span data-stu-id="844ed-171">If an acceptable authentication scheme and credentials are known before a request is sent to the server, an application can call [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) before calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="844ed-172">在此情況下，WinHTTP 會在伺服器的初始要求中提供認證或 [*驗證資料*](glossary.md) ，以嘗試向伺服器進行預先驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-172">In this case, WinHTTP attempts pre-authentication with the server by providing credentials or [*authentication data*](glossary.md) in the initial request to the server.</span></span> <span data-ttu-id="844ed-173">預先驗證可以減少驗證程式中的交換次數，進而改善應用程式效能。</span><span class="sxs-lookup"><span data-stu-id="844ed-173">Pre-authentication can decrease the number of exchanges in the authentication process and therefore improve application performance.</span></span>

<span data-ttu-id="844ed-174">預先驗證可搭配下列驗證配置使用：</span><span class="sxs-lookup"><span data-stu-id="844ed-174">Preauthentication can be used with the following authentication schemes:</span></span>

-   <span data-ttu-id="844ed-175">基本-永遠可行。</span><span class="sxs-lookup"><span data-stu-id="844ed-175">Basic - always possible.</span></span>
-   <span data-ttu-id="844ed-176">將解析成 Kerberos-可能很可能;唯一的例外狀況是用戶端與網域控制站之間的時間誤差已關閉。</span><span class="sxs-lookup"><span data-stu-id="844ed-176">Negotiate resolving into Kerberos - very likely possible; the only exception is when the time-skews are off between the client and the domain controller.</span></span>
-   <span data-ttu-id="844ed-177"> (協商進入 NTLM) -永遠不可能發生。</span><span class="sxs-lookup"><span data-stu-id="844ed-177">(Negotiate resolving into NTLM) - never possible.</span></span>
-   <span data-ttu-id="844ed-178">只有在 Windows Server 2008 R2 中可以進行 NTLM。</span><span class="sxs-lookup"><span data-stu-id="844ed-178">NTLM - possible in Windows Server 2008 R2 only.</span></span>
-   <span data-ttu-id="844ed-179">摘要-永遠不可能。</span><span class="sxs-lookup"><span data-stu-id="844ed-179">Digest - never possible.</span></span>
-   <span data-ttu-id="844ed-180">Passport-永不可能;在最初的挑戰回應之後，WinHTTP 會使用 cookie 預先驗證 Passport。</span><span class="sxs-lookup"><span data-stu-id="844ed-180">Passport - never possible; after the initial challenge-response, WinHTTP uses cookies to pre-authenticate to Passport.</span></span>

<span data-ttu-id="844ed-181">一般的 WinHTTP 應用程式會完成下列步驟，才能處理驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-181">A typical WinHTTP application completes the following steps in order to handle authentication.</span></span>

-   <span data-ttu-id="844ed-182">使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 和 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)來要求資源。</span><span class="sxs-lookup"><span data-stu-id="844ed-182">Request a resource with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) and [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>
-   <span data-ttu-id="844ed-183">使用 [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)檢查回應標頭。</span><span class="sxs-lookup"><span data-stu-id="844ed-183">Check the response headers with [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
-   <span data-ttu-id="844ed-184">如果傳回401或407狀態碼，表示需要驗證，請呼叫 [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) 來尋找可接受的配置。</span><span class="sxs-lookup"><span data-stu-id="844ed-184">If a 401 or 407 status code is returned indicating that authentication is required, call [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) to find an acceptable scheme.</span></span>
-   <span data-ttu-id="844ed-185">使用 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)設定 [驗證配置]、[使用者名稱] 和 [密碼]。</span><span class="sxs-lookup"><span data-stu-id="844ed-185">Set the authentication scheme, username, and password with [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span></span>
-   <span data-ttu-id="844ed-186">藉由呼叫 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)，以相同的要求控制碼重新傳送要求。</span><span class="sxs-lookup"><span data-stu-id="844ed-186">Resend the request with the same request handle by calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

<span data-ttu-id="844ed-187">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)所設定的認證只會用於一個要求。</span><span class="sxs-lookup"><span data-stu-id="844ed-187">The credentials set by [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) are only used for one request.</span></span> <span data-ttu-id="844ed-188">WinHTTP 不會快取要在其他要求中使用的認證，這表示必須撰寫應用程式來回應多個要求。</span><span class="sxs-lookup"><span data-stu-id="844ed-188">WinHTTP does not cache the credentials to use in other requests, which means that applications must be written that can respond to multiple requests.</span></span> <span data-ttu-id="844ed-189">如果重複使用已驗證的連線，其他要求可能不會有挑戰，但您的程式碼應該隨時都能回應要求。</span><span class="sxs-lookup"><span data-stu-id="844ed-189">If an authenticated connection is re-used, other requests may not be challenged, but your code should be able to respond to a request at any time.</span></span>

### <a name="example-retrieving-a-document"></a><span data-ttu-id="844ed-190">範例：抓取檔</span><span class="sxs-lookup"><span data-stu-id="844ed-190">Example: Retrieving a Document</span></span>

<span data-ttu-id="844ed-191">下列範例程式碼會嘗試從 HTTP 伺服器取出指定的檔。</span><span class="sxs-lookup"><span data-stu-id="844ed-191">The following sample code attempts to retrieve a specified document from an HTTP server.</span></span> <span data-ttu-id="844ed-192">狀態碼會從回應中取出，以判斷是否需要驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-192">The status code is retrieved from the response to determine if authentication is required.</span></span> <span data-ttu-id="844ed-193">如果找到200狀態碼，則可以使用檔。</span><span class="sxs-lookup"><span data-stu-id="844ed-193">If a 200 status code is found, the document is available.</span></span> <span data-ttu-id="844ed-194">如果發現狀態碼401或407，則必須先進行驗證，然後才能抓取檔。</span><span class="sxs-lookup"><span data-stu-id="844ed-194">If a status code of 401 or 407 is found, authentication is required before the document can be retrieved.</span></span> <span data-ttu-id="844ed-195">若為任何其他狀態碼，則會顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="844ed-195">For any other status code, an error message is displayed.</span></span> <span data-ttu-id="844ed-196">如需可能的狀態代碼清單，請參閱 [**HTTP 狀態碼**](http-status-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="844ed-196">See [**HTTP Status Codes**](http-status-codes.md) for a list of possible status codes.</span></span>


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a><span data-ttu-id="844ed-197">自動登入原則</span><span class="sxs-lookup"><span data-stu-id="844ed-197">Automatic Logon Policy</span></span>

<span data-ttu-id="844ed-198">自動登入 (自動登入) 原則會決定 WinHTTP 在要求中包含預設認證時，可接受的時間。</span><span class="sxs-lookup"><span data-stu-id="844ed-198">The automatic logon (auto-logon) policy determines when it is acceptable for WinHTTP to include the default credentials in a request.</span></span> <span data-ttu-id="844ed-199">預設認證是目前的執行緒權杖或會話權杖，取決於是否在同步或非同步模式中使用 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="844ed-199">The default credentials are either the current thread token or the session token depending on whether WinHTTP is used in synchronous or asynchronous mode.</span></span> <span data-ttu-id="844ed-200">執行緒 token 是在同步模式中使用，而會話權杖則是在非同步模式中使用。</span><span class="sxs-lookup"><span data-stu-id="844ed-200">The thread token is used in synchronous mode, and the session token is used in asynchronous mode.</span></span> <span data-ttu-id="844ed-201">這些預設認證通常是用來登入 Microsoft Windows 的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="844ed-201">These default credentials are often the username and password used to log on to Microsoft Windows.</span></span>

<span data-ttu-id="844ed-202">已執行自動登入原則，以避免將這些認證用於對不受信任的伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-202">The auto-logon policy was implemented to prevent these credentials from being casually used to authenticate against an untrusted server.</span></span> <span data-ttu-id="844ed-203">根據預設，安全性層級會設定為 WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 中等，這可讓預設認證僅用於內部網路要求。</span><span class="sxs-lookup"><span data-stu-id="844ed-203">By default, the security level is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM, which allows the default credentials to be used only for Intranet requests.</span></span> <span data-ttu-id="844ed-204">自動登入原則僅適用于 NTLM 和協商驗證配置。</span><span class="sxs-lookup"><span data-stu-id="844ed-204">The auto-logon policy only applies to the NTLM and Negotiate authentication schemes.</span></span> <span data-ttu-id="844ed-205">認證永遠不會與其他配置自動傳輸。</span><span class="sxs-lookup"><span data-stu-id="844ed-205">Credentials are never automatically transmitted with other schemes.</span></span>

<span data-ttu-id="844ed-206">您可以使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函式搭配 WINHTTP 選項自動登入 [**\_ \_ \_ 原則**](option-flags.md) 旗標來設定自動登入原則。</span><span class="sxs-lookup"><span data-stu-id="844ed-206">The auto-logon policy can be set using the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function with the [**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**](option-flags.md) flag.</span></span> <span data-ttu-id="844ed-207">此旗標只適用于要求控制碼。</span><span class="sxs-lookup"><span data-stu-id="844ed-207">This flag applies only to the request handle.</span></span> <span data-ttu-id="844ed-208">當原則設定為 WINHTTP 自動登 \_ 入 \_ 安全性 \_ 等級時 \_ ，預設認證可以傳送至所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="844ed-208">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW, default credentials can be sent to all servers.</span></span> <span data-ttu-id="844ed-209">當原則設定為 WINHTTP 自動登 \_ 入 \_ 安全性 \_ 等級 \_ 高時，預設認證無法用於驗證。</span><span class="sxs-lookup"><span data-stu-id="844ed-209">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH, default credentials cannot be used for authentication.</span></span> <span data-ttu-id="844ed-210">強烈建議您在中層級使用自動登入。</span><span class="sxs-lookup"><span data-stu-id="844ed-210">It is strongly recommended that you use the auto-logon at the MEDIUM level.</span></span>

## <a name="stored-user-names-and-passwords"></a><span data-ttu-id="844ed-211">儲存的使用者名稱與密碼</span><span class="sxs-lookup"><span data-stu-id="844ed-211">Stored User Names and Passwords</span></span>

<span data-ttu-id="844ed-212">Windows XP 引進了預存使用者名稱和密碼的概念。</span><span class="sxs-lookup"><span data-stu-id="844ed-212">Windows XP introduced the concept of Stored User Names and Passwords.</span></span> <span data-ttu-id="844ed-213">如果使用者的 Passport 認證是透過 **Passport 註冊嚮導** 或標準 **認證對話方塊** 來儲存，則會儲存在儲存的使用者名稱和密碼中。</span><span class="sxs-lookup"><span data-stu-id="844ed-213">If a user's Passport credentials are saved through the **Passport Registration Wizard** or the standard **Credential Dialog**, it is saved in the Stored User Names and Passwords.</span></span> <span data-ttu-id="844ed-214">在 Windows XP 或更新版本上使用 WinHTTP 時，如果未明確設定認證，WinHTTP 會自動使用預存使用者名稱和密碼中的認證。</span><span class="sxs-lookup"><span data-stu-id="844ed-214">When using WinHTTP on Windows XP or later, WinHTTP automatically uses the credentials in the Stored User Names and Passwords if credentials are not explicitly set.</span></span> <span data-ttu-id="844ed-215">這類似于支援 NTLM/Kerberos 的預設登入認證。</span><span class="sxs-lookup"><span data-stu-id="844ed-215">This is similar to the support of default logon credentials for NTLM/Kerberos.</span></span> <span data-ttu-id="844ed-216">不過，使用預設的 Passport 認證並不受自動登入原則設定的規定。</span><span class="sxs-lookup"><span data-stu-id="844ed-216">However, use of default Passport credentials is not subject to the automatic logon policy settings.</span></span>

 

 



