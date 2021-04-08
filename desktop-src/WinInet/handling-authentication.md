---
title: 處理驗證
description: 某些 proxy 和伺服器需要驗證，才能授與存取網際網路上的資源。
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8eaa38f61f0d97f1f543e0623313aa196aab7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104024258"
---
# <a name="handling-authentication"></a><span data-ttu-id="c985b-103">處理驗證</span><span class="sxs-lookup"><span data-stu-id="c985b-103">Handling Authentication</span></span>

<span data-ttu-id="c985b-104">某些 proxy 和伺服器需要驗證，才能授與存取網際網路上的資源。</span><span class="sxs-lookup"><span data-stu-id="c985b-104">Some proxies and servers require authentication before granting access to resources on the Internet.</span></span> <span data-ttu-id="c985b-105">WinINet 函數支援 HTTP 會話的伺服器和 proxy 驗證。</span><span class="sxs-lookup"><span data-stu-id="c985b-105">The WinINet functions support server and proxy authentication for http sessions.</span></span> <span data-ttu-id="c985b-106">Ftp 伺服器的驗證必須由 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 函數處理。</span><span class="sxs-lookup"><span data-stu-id="c985b-106">Authentication of ftp servers must be handled by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function.</span></span> <span data-ttu-id="c985b-107">目前不支援 FTP 閘道驗證。</span><span class="sxs-lookup"><span data-stu-id="c985b-107">Currently, FTP gateway authentication is not supported.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="c985b-108">關於 HTTP 驗證</span><span class="sxs-lookup"><span data-stu-id="c985b-108">About HTTP Authentication</span></span>

<span data-ttu-id="c985b-109">如果需要驗證，用戶端應用程式會收到狀態碼401（如果伺服器需要驗證）或407（如果 proxy 需要驗證的話）。</span><span class="sxs-lookup"><span data-stu-id="c985b-109">If authentication is required, the client application receives a status code 401, if the server requires authentication, or 407, if the proxy requires authentication.</span></span> <span data-ttu-id="c985b-110">使用狀態碼時，proxy 或伺服器會傳送一個或多個驗證回應標頭，也就是 proxy 驗證的 Proxy 驗證 () 或 WWW-Authenticate (進行伺服器驗證) 。</span><span class="sxs-lookup"><span data-stu-id="c985b-110">With the status code, the proxy or server sends one, or more, authenticate response headers—Proxy-Authenticate (for proxy authentication) or WWW-Authenticate (for server authentication).</span></span>

<span data-ttu-id="c985b-111">每個驗證回應標頭都包含可用的驗證配置和領域。</span><span class="sxs-lookup"><span data-stu-id="c985b-111">Each authenticate response header contains an available authentication scheme and a realm.</span></span> <span data-ttu-id="c985b-112">如果支援多個驗證配置，伺服器會傳回多個驗證回應標頭。</span><span class="sxs-lookup"><span data-stu-id="c985b-112">If multiple authentication schemes are supported, the server returns multiple authenticate response headers.</span></span> <span data-ttu-id="c985b-113">領域值會區分大小寫，並定義 proxy 或伺服器上的保護空間。</span><span class="sxs-lookup"><span data-stu-id="c985b-113">The realm value is case-sensitive and defines a protection space on the proxy or server.</span></span> <span data-ttu-id="c985b-114">例如，「WWW-驗證：基本領域 =」範例 "」標頭會是在需要伺服器驗證時所傳回的標頭範例。</span><span class="sxs-lookup"><span data-stu-id="c985b-114">For example, the header "WWW-Authenticate: Basic Realm="example"" would be an example of a header returned when server authentication is required.</span></span>

<span data-ttu-id="c985b-115">傳送要求的用戶端應用程式可以藉由在要求中包含授權標頭欄位來自行驗證。</span><span class="sxs-lookup"><span data-stu-id="c985b-115">The client application that sent the request can authenticate itself by including an Authorization header field with the request.</span></span> <span data-ttu-id="c985b-116">授權標頭會包含驗證配置，以及該配置所需的適當回應。</span><span class="sxs-lookup"><span data-stu-id="c985b-116">The Authorization header would contain the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="c985b-117">例如，如果用戶端收到驗證回應標頭 "WWW-驗證：基本領域 =" 範例 ""，就會將標頭「授權：基本 <使用者名稱：密碼>」新增至要求，並將其重新傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="c985b-117">For example, the header "Authorization: Basic <username:password>" would be added to the request and re-sent to the server if the client received the authenticate response header "WWW-Authenticate: Basic Realm="example"".</span></span>

<span data-ttu-id="c985b-118">驗證架構有兩種一般類型：</span><span class="sxs-lookup"><span data-stu-id="c985b-118">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="c985b-119">基本驗證配置，其中的使用者名稱和密碼會以純文字傳送給伺服器。</span><span class="sxs-lookup"><span data-stu-id="c985b-119">Basic authentication scheme, where the user name and password are sent in cleartext to the server.</span></span>
-   <span data-ttu-id="c985b-120">挑戰-回應配置，可允許挑戰回應的格式。</span><span class="sxs-lookup"><span data-stu-id="c985b-120">Challenge-response schemes, which allow for a challenge-response format.</span></span>

<span data-ttu-id="c985b-121">基本驗證配置是以模型為基礎，用戶端必須使用每個領域的使用者名稱和密碼進行驗證。</span><span class="sxs-lookup"><span data-stu-id="c985b-121">The Basic authentication scheme is based on the model that a client must authenticate itself with a user name and password for each realm.</span></span> <span data-ttu-id="c985b-122">如果傳送的授權標頭包含有效的使用者名稱和密碼，伺服器會為要求提供服務。</span><span class="sxs-lookup"><span data-stu-id="c985b-122">The server services the request if it is resent with an Authorization header that includes a valid user name and password.</span></span>

<span data-ttu-id="c985b-123">挑戰-回應配置可讓您進行更安全的驗證。</span><span class="sxs-lookup"><span data-stu-id="c985b-123">Challenge-response schemes enable more secure authentication.</span></span> <span data-ttu-id="c985b-124">如果要求需要使用挑戰回應配置進行驗證，則會將適當的狀態碼和驗證標頭傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="c985b-124">If a request requires authentication using a challenge-response scheme, the appropriate status code and Authenticate headers are returned to the client.</span></span> <span data-ttu-id="c985b-125">接著，用戶端必須使用 negotiate 重新傳送要求。</span><span class="sxs-lookup"><span data-stu-id="c985b-125">The client must then to resend the request with a negotiate.</span></span> <span data-ttu-id="c985b-126">伺服器會傳回具有挑戰的適當狀態碼，然後用戶端會要求以適當的回應重新傳送要求，以取得所要求的服務。</span><span class="sxs-lookup"><span data-stu-id="c985b-126">The server would return an appropriate status code with a challenge, and the client would then require to resend the request with the proper response to get the requested service.</span></span>

<span data-ttu-id="c985b-127">下表列出驗證配置、驗證類型、支援它們的 DLL，以及配置的描述。</span><span class="sxs-lookup"><span data-stu-id="c985b-127">The following table lists authentication schemes, the authentication type, the DLL that supports them, and a description of the scheme.</span></span>



| <span data-ttu-id="c985b-128">配置</span><span class="sxs-lookup"><span data-stu-id="c985b-128">Scheme</span></span>                                    | <span data-ttu-id="c985b-129">類型</span><span class="sxs-lookup"><span data-stu-id="c985b-129">Type</span></span>               | <span data-ttu-id="c985b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c985b-130">DLL</span></span>                  | <span data-ttu-id="c985b-131">Description</span><span class="sxs-lookup"><span data-stu-id="c985b-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c985b-132">基本 (純文字) </span><span class="sxs-lookup"><span data-stu-id="c985b-132">Basic (cleartext)</span></span>                         | <span data-ttu-id="c985b-133">basic</span><span class="sxs-lookup"><span data-stu-id="c985b-133">basic</span></span>              | <span data-ttu-id="c985b-134">Wininet.dll</span><span class="sxs-lookup"><span data-stu-id="c985b-134">Wininet.dll</span></span>          | <span data-ttu-id="c985b-135">使用 base64 編碼的字串，其中包含使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="c985b-135">Uses a base64 encoded string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c985b-136">Digest</span><span class="sxs-lookup"><span data-stu-id="c985b-136">Digest</span></span>                                    | <span data-ttu-id="c985b-137">挑戰-回應</span><span class="sxs-lookup"><span data-stu-id="c985b-137">challenge-response</span></span> | <span data-ttu-id="c985b-138">Digest.dll</span><span class="sxs-lookup"><span data-stu-id="c985b-138">Digest.dll</span></span>           | <span data-ttu-id="c985b-139">挑戰-回應配置，會挑戰使用 nonce (伺服器指定的資料字串) 值。</span><span class="sxs-lookup"><span data-stu-id="c985b-139">A challenge-response scheme that challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="c985b-140">有效的回應包含使用者名稱、密碼、指定的 nonce 值、HTTP 方法，以及要求的統一資源識別項 (URI) 的總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="c985b-140">A valid response contains a checksum of the user name, the password, the given nonce value, the HTTP method, and the requested Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="c985b-141">摘要式驗證支援已在 Microsoft Internet Explorer 5 中推出。</span><span class="sxs-lookup"><span data-stu-id="c985b-141">Digest authentication support was introduced in Microsoft Internet Explorer 5.</span></span> |
| <span data-ttu-id="c985b-142">NT LAN Manager (NTLM) </span><span class="sxs-lookup"><span data-stu-id="c985b-142">NT LAN Manager (NTLM)</span></span>                     | <span data-ttu-id="c985b-143">挑戰-回應</span><span class="sxs-lookup"><span data-stu-id="c985b-143">challenge-response</span></span> | <span data-ttu-id="c985b-144">Winsspi.dll</span><span class="sxs-lookup"><span data-stu-id="c985b-144">Winsspi.dll</span></span>          | <span data-ttu-id="c985b-145">以使用者名稱為基礎的挑戰回應配置。</span><span class="sxs-lookup"><span data-stu-id="c985b-145">A challenge-response scheme that bases the challenge on the user name.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c985b-146">Microsoft Network (MSN) </span><span class="sxs-lookup"><span data-stu-id="c985b-146">Microsoft Network (MSN)</span></span>                   | <span data-ttu-id="c985b-147">挑戰-回應</span><span class="sxs-lookup"><span data-stu-id="c985b-147">challenge-response</span></span> | <span data-ttu-id="c985b-148">Msnsspc.dll</span><span class="sxs-lookup"><span data-stu-id="c985b-148">Msnsspc.dll</span></span>          | <span data-ttu-id="c985b-149">MSN 的驗證配置。</span><span class="sxs-lookup"><span data-stu-id="c985b-149">The Microsoft Network's authentication scheme.</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="c985b-150"> (DPA) 的分散式密碼驗證</span><span class="sxs-lookup"><span data-stu-id="c985b-150">Distributed Password Authentication (DPA)</span></span> | <span data-ttu-id="c985b-151">挑戰-回應</span><span class="sxs-lookup"><span data-stu-id="c985b-151">challenge-response</span></span> | <span data-ttu-id="c985b-152">Msapsspc.dll</span><span class="sxs-lookup"><span data-stu-id="c985b-152">Msapsspc.dll</span></span>         | <span data-ttu-id="c985b-153">類似于 MSN 驗證，也是由 Microsoft 網路使用。</span><span class="sxs-lookup"><span data-stu-id="c985b-153">Similar to MSN authentication and is also used by the Microsoft Network.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c985b-154">遠端複雜密碼驗證 (RPA) </span><span class="sxs-lookup"><span data-stu-id="c985b-154">Remote Passphrase Authentication (RPA)</span></span>    | <span data-ttu-id="c985b-155">CompuServe</span><span class="sxs-lookup"><span data-stu-id="c985b-155">CompuServe</span></span>         | <span data-ttu-id="c985b-156">Rpawinet.dll，da.dll</span><span class="sxs-lookup"><span data-stu-id="c985b-156">Rpawinet.dll, da.dll</span></span> | <span data-ttu-id="c985b-157">CompuServe 驗證配置。</span><span class="sxs-lookup"><span data-stu-id="c985b-157">CompuServe authentication scheme.</span></span> <span data-ttu-id="c985b-158">如需詳細資訊，請參閱 [RPA 機制規格](https://www.compuserve.com/)。</span><span class="sxs-lookup"><span data-stu-id="c985b-158">For more information, see the [RPA Mechanism Specifications](https://www.compuserve.com/).</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="c985b-159">針對基本驗證以外的任何其他作業，除了安裝適當的 DLL 之外，還必須設定登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="c985b-159">For anything other than Basic authentication, the registry keys must be set up in addition to installing the appropriate DLL.</span></span>

<span data-ttu-id="c985b-160">如果需要驗證，則應該在 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)的呼叫中使用 [網際網路 \_ 旗標 \_ 保留 \_ 連接](api-flags.md)旗標。</span><span class="sxs-lookup"><span data-stu-id="c985b-160">If authentication is required, the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag should be used in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="c985b-161">\_ \_ \_ NTLM 和其他類型的驗證都需要網際網路旗標保留連線旗標，才能在完成驗證程式時維持連接。</span><span class="sxs-lookup"><span data-stu-id="c985b-161">The INTERNET\_FLAG\_KEEP\_CONNECTION flag is required for NTLM and other types of authentication in order to maintain the connection while completing the authentication process.</span></span> <span data-ttu-id="c985b-162">如果未維護連接，則必須使用 proxy 或伺服器重新開機驗證程式。</span><span class="sxs-lookup"><span data-stu-id="c985b-162">If the connection is not maintained, the authentication process must be restarted with the proxy or server.</span></span>

<span data-ttu-id="c985b-163">即使需要驗證， [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 和 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) 函式也會順利完成。</span><span class="sxs-lookup"><span data-stu-id="c985b-163">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions complete successfully even when authentication is required.</span></span> <span data-ttu-id="c985b-164">差別在於，在標頭檔和 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 中傳回的資料會收到一個 HTML 網頁，通知使用者狀態碼。</span><span class="sxs-lookup"><span data-stu-id="c985b-164">The difference is, the data returned in the header files and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) would receive an HTML page informing the user of the status code.</span></span>

### <a name="registering-authentication-keys"></a><span data-ttu-id="c985b-165">註冊驗證金鑰</span><span class="sxs-lookup"><span data-stu-id="c985b-165">Registering Authentication Keys</span></span>

<span data-ttu-id="c985b-166">INTERNET \_ OPEN \_ TYPE \_ PRECONFIG 會查看登錄值 **ProxyEnable**、 **ProxyServer** 和 **ProxyOverride**。</span><span class="sxs-lookup"><span data-stu-id="c985b-166">INTERNET\_OPEN\_TYPE\_PRECONFIG looks at the registry values **ProxyEnable**, **ProxyServer**, and **ProxyOverride**.</span></span> <span data-ttu-id="c985b-167">這些值位於 [ **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**] 下。</span><span class="sxs-lookup"><span data-stu-id="c985b-167">These values are located under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Internet Settings**.</span></span>

<span data-ttu-id="c985b-168">針對 Basic 以外的驗證架構，必須將金鑰新增至登錄的 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Internet Explorer** \\ **安全性**。</span><span class="sxs-lookup"><span data-stu-id="c985b-168">For authentication schemes other than Basic, a key must be added to the registry under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="c985b-169">**DWORD** 值 **旗標** 應以適當的值設定。</span><span class="sxs-lookup"><span data-stu-id="c985b-169">A **DWORD** value, **Flags**, should be set with the appropriate value.</span></span> <span data-ttu-id="c985b-170">下列清單顯示 **旗標** 值的可能值。</span><span class="sxs-lookup"><span data-stu-id="c985b-170">The following list shows the possible values for the **Flags** value.</span></span>

-   <span data-ttu-id="c985b-171">外掛程式 \_ 驗證 \_ 旗 \_ 標 \_ \_ 每個 TCPIP 的唯一內容 \_ (值 = 0x01) </span><span class="sxs-lookup"><span data-stu-id="c985b-171">PLUGIN\_AUTH\_FLAGS\_UNIQUE\_CONTEXT\_PER\_TCPIP (value=0x01)</span></span>

    <span data-ttu-id="c985b-172">每個傳輸控制通訊協定/網際網路通訊協定 (TCP/IP) 通訊端包含不同的內容。</span><span class="sxs-lookup"><span data-stu-id="c985b-172">Each Transmission Control Protocol/Internet Protocol (TCP/IP) socket contains a different context.</span></span> <span data-ttu-id="c985b-173">否則，會針對每個領域或區塊 URL 範本傳遞新的內容。</span><span class="sxs-lookup"><span data-stu-id="c985b-173">Otherwise, a new context is passed for each realm or block URL template.</span></span>

-   <span data-ttu-id="c985b-174">外掛程式 \_ 驗證 \_ 旗標 \_ 可以 \_ 處理 \_ UI (值 = 0x02) </span><span class="sxs-lookup"><span data-stu-id="c985b-174">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_UI (value=0x02)</span></span>

    <span data-ttu-id="c985b-175">此 DLL 可以處理自己的使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="c985b-175">This DLL can handle its own user input.</span></span>

-   <span data-ttu-id="c985b-176">外掛程式 \_ 驗證 \_ 旗標 \_ 無法 \_ 處理 \_ 任何 \_ PASSWD (value = 0x04) </span><span class="sxs-lookup"><span data-stu-id="c985b-176">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_NO\_PASSWD (value=0x04)</span></span>

    <span data-ttu-id="c985b-177">此 DLL 可以進行驗證，而不提示使用者輸入密碼。</span><span class="sxs-lookup"><span data-stu-id="c985b-177">This DLL might be capable of doing an authentication without prompting the user for a password.</span></span>

-   <span data-ttu-id="c985b-178">外掛程式 \_ 驗證 \_ 旗標 \_ 沒有 \_ 領域 (值 = 0x08) </span><span class="sxs-lookup"><span data-stu-id="c985b-178">PLUGIN\_AUTH\_FLAGS\_NO\_REALM (value=0x08)</span></span>

    <span data-ttu-id="c985b-179">此 DLL 不使用標準 HTTP 領域字串。</span><span class="sxs-lookup"><span data-stu-id="c985b-179">This DLL does not use a standard http realm string.</span></span> <span data-ttu-id="c985b-180">任何顯示為領域的資料都是配置特定的資料。</span><span class="sxs-lookup"><span data-stu-id="c985b-180">Any data that appears to be a realm is scheme-specific data.</span></span>

-   <span data-ttu-id="c985b-181">外掛程式 \_ 驗證 \_ 旗 \_ 標 \_ 保持 \_ 不 \_ 需要的狀態 (值 = 0x10) </span><span class="sxs-lookup"><span data-stu-id="c985b-181">PLUGIN\_AUTH\_FLAGS\_KEEP\_ALIVE\_NOT\_REQUIRED (value=0x10)</span></span>

    <span data-ttu-id="c985b-182">此 DLL 不需要持續連線，就能進行挑戰回應順序。</span><span class="sxs-lookup"><span data-stu-id="c985b-182">This DLL does not require a persistent connection for its challenge-response sequence.</span></span>

<span data-ttu-id="c985b-183">例如，若要加入 ntlm 驗證，必須在 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Internet Explorer** \\ **安全性** 中加入金鑰 ntlm。</span><span class="sxs-lookup"><span data-stu-id="c985b-183">For example, to add NTLM authentication, the key NTLM must be added to **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="c985b-184">在 **[ \_ HKEY \_ 本機電腦** \\ **軟體** \\ **Microsoft** \\ **Internet Explorer** \\ **安全性** \\ **NTLM**] 下，必須新增字串值 **DLLFile** 和 **DWORD** 值 **旗標**。</span><span class="sxs-lookup"><span data-stu-id="c985b-184">Under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**\\**NTLM**, the string value, **DLLFile**, and a **DWORD** value, **Flags**, must be added.</span></span> <span data-ttu-id="c985b-185">**DLLFile** 必須設定為 Winsspi.dll，且 **旗標** 必須設定為0x08。</span><span class="sxs-lookup"><span data-stu-id="c985b-185">**DLLFile** must be set to Winsspi.dll, and **Flags** must be set to 0x08.</span></span>

### <a name="server-authentication"></a><span data-ttu-id="c985b-186">伺服器驗證</span><span class="sxs-lookup"><span data-stu-id="c985b-186">Server Authentication</span></span>

<span data-ttu-id="c985b-187">當伺服器收到需要驗證的要求時，伺服器會傳回401狀態碼訊息。</span><span class="sxs-lookup"><span data-stu-id="c985b-187">When a server receives a request that requires authentication, the server returns a 401 status code message.</span></span> <span data-ttu-id="c985b-188">在該訊息中，伺服器應該包含一或多個 WWW-Authenticate 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="c985b-188">In that message, the server should include one or more WWW-Authenticate response headers.</span></span> <span data-ttu-id="c985b-189">這些標頭包含伺服器可用的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="c985b-189">These headers include the authentication methods the server has available.</span></span> <span data-ttu-id="c985b-190">WinINet 會選擇它所辨識的第一個方法。</span><span class="sxs-lookup"><span data-stu-id="c985b-190">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="c985b-191">除非通道是先使用 SSL 或 PCT 進行連結加密，否則基本驗證會提供弱式安全性。</span><span class="sxs-lookup"><span data-stu-id="c985b-191">Basic authentication provides weak security unless the channel is first link-encrypted with SSL or PCT.</span></span>

<span data-ttu-id="c985b-192">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)函式可用來取得使用者的使用者名稱和密碼資料，或自訂的使用者介面可以設計來取得資料。</span><span class="sxs-lookup"><span data-stu-id="c985b-192">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed to obtain the data.</span></span>

<span data-ttu-id="c985b-193">自訂介面可以使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 函式來設定 [網際網路 \_ 選項 \_ 密碼](option-flags.md) 和 [網際網路選項使用者 \_ \_ 名稱](option-flags.md) 值，然後將要求重新傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="c985b-193">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_USERNAME](option-flags.md) values and then resend the request to the server.</span></span>

### <a name="proxy-authentication"></a><span data-ttu-id="c985b-194">Proxy 驗證</span><span class="sxs-lookup"><span data-stu-id="c985b-194">Proxy Authentication</span></span>

<span data-ttu-id="c985b-195">當用戶端嘗試使用需要驗證的 proxy 時，proxy 會將407狀態碼訊息傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="c985b-195">When a client attempts to use a proxy that requires authentication, the proxy returns a 407 status code message to the client.</span></span> <span data-ttu-id="c985b-196">在該訊息中，proxy 應該包含一或多個 Proxy-Authenticate 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="c985b-196">In that message, the proxy should include one or more Proxy-Authenticate response headers.</span></span> <span data-ttu-id="c985b-197">這些標頭包含可從 proxy 取得的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="c985b-197">These headers include the authentication methods available from the proxy.</span></span> <span data-ttu-id="c985b-198">WinINet 會選擇它所辨識的第一個方法。</span><span class="sxs-lookup"><span data-stu-id="c985b-198">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="c985b-199">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)函式可用來取得使用者的使用者名稱和密碼資料，或是可以設計自訂的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="c985b-199">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed.</span></span>

<span data-ttu-id="c985b-200">自訂介面可以使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 函式來設定 [網際網路 \_ 選項 \_ proxy \_ 密碼](option-flags.md) 和 [網際網路 \_ 選項 proxy 使用者 \_ \_ 名稱](option-flags.md) 值，然後將要求重新傳送至 PROXY。</span><span class="sxs-lookup"><span data-stu-id="c985b-200">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PROXY\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_PROXY\_USERNAME](option-flags.md) values and then resend the request to the proxy.</span></span>

<span data-ttu-id="c985b-201">如果未設定 proxy 使用者名稱和密碼，WinINet 會嘗試使用伺服器的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="c985b-201">If no proxy user name and password are set, WinINet attempts to use the user name and password for the server.</span></span> <span data-ttu-id="c985b-202">此行為可讓用戶端執行相同的自訂使用者介面，以用來處理伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="c985b-202">This behavior enables clients to implement the same customized user interface used to handle server authentication.</span></span>

## <a name="handling-http-authentication"></a><span data-ttu-id="c985b-203">處理 HTTP 驗證</span><span class="sxs-lookup"><span data-stu-id="c985b-203">Handling HTTP Authentication</span></span>

<span data-ttu-id="c985b-204">您可以使用 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 或使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 的自訂函式來處理 HTTP 驗證，或新增自己的驗證標頭。</span><span class="sxs-lookup"><span data-stu-id="c985b-204">HTTP authentication can be handled with either [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or a customized function that uses [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) or adds its own authentication headers.</span></span> <span data-ttu-id="c985b-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 可以檢查與 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼相關聯的標頭，以找出隱藏的錯誤，例如來自 proxy 或伺服器的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="c985b-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can examine the headers associated with an [**HINTERNET**](appendix-a-hinternet-handles.md) handle to find hidden errors, such as status codes from a proxy or server.</span></span> <span data-ttu-id="c985b-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 可以用來設定 proxy 和伺服器的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="c985b-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) can be used to set the user name and password for the proxy and server.</span></span> <span data-ttu-id="c985b-207">若為 MSN 和 DPA 驗證，則必須使用 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 來設定使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="c985b-207">For MSN and DPA authentication, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) must be used to set the user name and password.</span></span>

<span data-ttu-id="c985b-208">針對新增本身的 WWW-Authenticate 或 Proxy-Authenticate 標頭的任何自訂函數， [網際網路旗標不應將 \_ \_ 任何 \_ AUTH](api-flags.md) 旗標設定為停用驗證。</span><span class="sxs-lookup"><span data-stu-id="c985b-208">For any customized function that adds its own WWW-Authenticate or Proxy-Authenticate headers, the [INTERNET\_FLAG\_NO\_AUTH](api-flags.md) flag should be set to disable authentication.</span></span>

<span data-ttu-id="c985b-209">下列範例顯示如何使用 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 來處理 HTTP 驗證。</span><span class="sxs-lookup"><span data-stu-id="c985b-209">The following example shows how [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can be used to handle HTTP authentication.</span></span>


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



<span data-ttu-id="c985b-210">在此範例中，dwErrorCode 是用來儲存與 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)呼叫相關聯的任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="c985b-210">In the example, dwErrorCode is used to store any errors associated with the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="c985b-211">即使 proxy 或伺服器需要驗證， [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)也會順利完成。</span><span class="sxs-lookup"><span data-stu-id="c985b-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completes successfully, even if the proxy or server requires authentication.</span></span> <span data-ttu-id="c985b-212">將 [錯誤] 旗標的 [旗標 \_ 錯誤 \_ UI] \_ \_ \_ 旗標傳遞給 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)時，函式會檢查標頭中是否有任何隱藏的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c985b-212">When the FLAGS\_ERROR\_UI\_FILTER\_FOR\_ERRORS flag is passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), the function checks the headers for any hidden errors.</span></span> <span data-ttu-id="c985b-213">這些隱藏的錯誤會包含任何驗證要求。</span><span class="sxs-lookup"><span data-stu-id="c985b-213">These hidden errors would include any requests for authentication.</span></span> <span data-ttu-id="c985b-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 會顯示適當的對話方塊，提示使用者輸入必要的資料。</span><span class="sxs-lookup"><span data-stu-id="c985b-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) displays the appropriate dialog box to prompt the user for the necessary data.</span></span> <span data-ttu-id="c985b-215">旗標 \_ 錯誤 \_ ui \_ 旗標 \_ 產生 \_ 資料和旗標 \_ 錯誤 \_ ui 旗標 \_ \_ 變更 \_ 選項旗標也應傳遞給 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)，如此函式就會為錯誤建立適當的資料結構，並將對話方塊的結果儲存在 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼中。</span><span class="sxs-lookup"><span data-stu-id="c985b-215">The FLAGS\_ERROR\_UI\_FLAGS\_GENERATE\_DATA and FLAGS\_ERROR\_UI\_FLAGS\_CHANGE\_OPTIONS flags should also be passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), so that the function constructs the appropriate data structure for the error and stores the results of the dialog box in the [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="c985b-216">下列範例程式碼顯示如何使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)處理驗證。</span><span class="sxs-lookup"><span data-stu-id="c985b-216">The following example code shows how authentication could be handled using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


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
> <span data-ttu-id="c985b-217">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="c985b-217">WinINet does not support server implementations.</span></span> <span data-ttu-id="c985b-218">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="c985b-218">In addition, it should not be used from a service.</span></span> <span data-ttu-id="c985b-219">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="c985b-219">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 