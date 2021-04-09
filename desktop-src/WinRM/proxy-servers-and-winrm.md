---
title: Proxy 伺服器和 WinRM
description: Windows 遠端管理 (WinRM) 會使用 HTTP 和 HTTPS 在用戶端與伺服器電腦之間傳送訊息。 一般而言，WinRM 用戶端會將訊息直接傳送至 WinRM 伺服器。 WinRM 用戶端也可以設定為使用 proxy 伺服器。
ms.assetid: f8137b3a-7704-4b21-a923-6e2692e18d90
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e07bbfebb4c8f0eb9e77a8942d54677b55c60006
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682382"
---
# <a name="proxy-servers-and-winrm"></a><span data-ttu-id="ae27b-105">Proxy 伺服器和 WinRM</span><span class="sxs-lookup"><span data-stu-id="ae27b-105">Proxy Servers and WinRM</span></span>

<span data-ttu-id="ae27b-106">Windows 遠端管理 (WinRM) 會使用 HTTP 和 HTTPS 在用戶端與伺服器電腦之間傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="ae27b-106">Windows Remote Management (WinRM) uses HTTP and HTTPS to send messages between the client and server computers.</span></span> <span data-ttu-id="ae27b-107">一般而言，WinRM 用戶端會將訊息直接傳送至 WinRM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae27b-107">In general, the WinRM client sends messages directly to the WinRM server.</span></span> <span data-ttu-id="ae27b-108">WinRM 用戶端也可以設定為使用 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae27b-108">WinRM clients can be also configured to use a proxy server.</span></span>

<span data-ttu-id="ae27b-109">如需詳細資訊，請參閱下列各節：</span><span class="sxs-lookup"><span data-stu-id="ae27b-109">For more information, see the following sections:</span></span>

-   [<span data-ttu-id="ae27b-110">設定 WinRM 2.0 的 Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="ae27b-110">Configuring a Proxy Server for WinRM 2.0</span></span>](#configuring-a-proxy-server-for-winrm-20)
    -   [<span data-ttu-id="ae27b-111">以 HTTPS 為基礎的 Proxy 連接</span><span class="sxs-lookup"><span data-stu-id="ae27b-111">HTTPS-Based Proxy Connections</span></span>](#https-based-proxy-connections)
    -   [<span data-ttu-id="ae27b-112">以 HTTP 為基礎的 Proxy 連接</span><span class="sxs-lookup"><span data-stu-id="ae27b-112">HTTP-Based Proxy Connections</span></span>](#http-based-proxy-connections)
-   [<span data-ttu-id="ae27b-113">設定 WinRM 1.1 及更早版本的 Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="ae27b-113">Configuring a Proxy Server for WinRM 1.1 and Earlier</span></span>](#configuring-a-proxy-server-for-winrm-11-and-earlier)

## <a name="configuring-a-proxy-server-for-winrm-20"></a><span data-ttu-id="ae27b-114">設定 WinRM 2.0 的 Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="ae27b-114">Configuring a Proxy Server for WinRM 2.0</span></span>

<span data-ttu-id="ae27b-115">WinRM 2.0 支援廣泛的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="ae27b-115">WinRM 2.0 supports a wide range of proxy configurations.</span></span> <span data-ttu-id="ae27b-116">例如，WinRM 支援 HTTP 和 HTTPS 傳輸的 proxy，以及已驗證和未驗證的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae27b-116">For example, WinRM supports proxies for HTTP and HTTPS transports and for authenticated and unauthenticated proxy servers.</span></span>

### <a name="https-based-proxy-connections"></a><span data-ttu-id="ae27b-117">HTTPS-Based Proxy 連接</span><span class="sxs-lookup"><span data-stu-id="ae27b-117">HTTPS-Based Proxy Connections</span></span>

<span data-ttu-id="ae27b-118">為了獲得更好的安全性和以連線為基礎的親和性，應使用 HTTPS 作為傳輸機制。</span><span class="sxs-lookup"><span data-stu-id="ae27b-118">For better security and connection-based affinity, HTTPS should be used as the transport mechanism.</span></span>

<span data-ttu-id="ae27b-119">如果 proxy 伺服器需要驗證，則 WinRM 用戶端和伺服器必須使用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="ae27b-119">If the proxy server requires authentication, the WinRM clients and servers must use HTTPS.</span></span>

> [!Note]  
> <span data-ttu-id="ae27b-120">Proxy 伺服器的驗證與目的地伺服器的驗證無關。</span><span class="sxs-lookup"><span data-stu-id="ae27b-120">Authentication to the proxy server is independent from the authentication to the destination server.</span></span>

 

### <a name="http-based-proxy-connections"></a><span data-ttu-id="ae27b-121">HTTP-Based Proxy 連接</span><span class="sxs-lookup"><span data-stu-id="ae27b-121">HTTP-Based Proxy Connections</span></span>

<span data-ttu-id="ae27b-122">如果不需要 proxy 伺服器驗證，可以使用 HTTP 或 HTTPs 進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="ae27b-122">If no proxy server authentication is required, either HTTP or HTTPs can be used for transport.</span></span> <span data-ttu-id="ae27b-123">不過，透過 proxy 伺服器從 WinRM 用戶端到 WinRM 伺服器的 HTTP 型連線可能會有問題。</span><span class="sxs-lookup"><span data-stu-id="ae27b-123">However, HTTP-based connections from a WinRM client to a WinRM server through a proxy server can be problematic.</span></span>

<span data-ttu-id="ae27b-124">使用以 HTTP 為基礎的連接時可能會發生下列問題：</span><span class="sxs-lookup"><span data-stu-id="ae27b-124">The following issues might be encountered when using HTTP-based connections:</span></span>

-   <span data-ttu-id="ae27b-125">Proxy 伺服器不支援以連線為基礎的驗證，這可能會導致目的地伺服器的驗證失敗，並出現「拒絕存取」錯誤。</span><span class="sxs-lookup"><span data-stu-id="ae27b-125">The proxy server does not support connection-based authentication, which can cause the authentication against the destination server to fail with an access denied error.</span></span>
-   <span data-ttu-id="ae27b-126">需要一組以上的認證，才能連接到目的地伺服器和 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae27b-126">More than one set of credentials is needed to connect to the destination server and to the proxy server.</span></span>
-   <span data-ttu-id="ae27b-127">以 HTTP 為基礎的 proxy 伺服器可能不支援維護相關聯的用戶端和伺服器連接的能力。</span><span class="sxs-lookup"><span data-stu-id="ae27b-127">HTTP-based proxy servers might not support the ability to maintain the associated client-based and server-based connections.</span></span> <span data-ttu-id="ae27b-128">如果 proxy 沒有將用戶端高度連結到伺服器並維護 TCP/IP 連接，未經驗證的用戶端可能會取得資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="ae27b-128">If the proxy does not strongly link a client to a server and maintain the TCP/IP connection, unauthenticated clients might gain access to data.</span></span> <span data-ttu-id="ae27b-129">此外，缺乏連接親和性可能會導致伺服器的驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="ae27b-129">Also, the lack of connection affinity might cause the authentication to fail against the server.</span></span>

<span data-ttu-id="ae27b-130">如果必須使用 HTTP 做為傳輸，則 proxy 伺服器應支援下列設定，以達到更好的 WinRM 回應，並防止 WinRM 用戶端的拒絕存取失敗：</span><span class="sxs-lookup"><span data-stu-id="ae27b-130">If HTTP must be used as the transport, the proxy server should support the following configuration to achieve a better WinRM response and to prevent access denied failures for WinRM clients:</span></span>

-   <span data-ttu-id="ae27b-131">HTTP/1.1 的支援。</span><span class="sxs-lookup"><span data-stu-id="ae27b-131">Support for HTTP/1.1.</span></span> <span data-ttu-id="ae27b-132">在用戶端與伺服器之間對應連線親和性時，HTTP/1.1 更嚴格。</span><span class="sxs-lookup"><span data-stu-id="ae27b-132">HTTP/1.1 is more stringent in mapping connection affinity between client and server.</span></span>
-   <span data-ttu-id="ae27b-133">用於協商、Kerberos 和 CredSSP 驗證的連接型驗證。</span><span class="sxs-lookup"><span data-stu-id="ae27b-133">Connection-based authentication for Negotiate, Kerberos, and CredSSP authentication.</span></span>

    <span data-ttu-id="ae27b-134">要求的驗證需要在用戶端與伺服器之間進行多次來回行程。</span><span class="sxs-lookup"><span data-stu-id="ae27b-134">Authentication of a request requires multiple round-trips between the client and server.</span></span> <span data-ttu-id="ae27b-135">驗證 (WinRM) server 將回應傳送給用戶端，而該用戶端不是401回應 (未經授權) ，則會在驗證時完成大部分的驗證。</span><span class="sxs-lookup"><span data-stu-id="ae27b-135">Most negotiation for authentication is complete after the authenticating (WinRM) server sends a response to the client that is not a 401 response (Unauthorized).</span></span> <span data-ttu-id="ae27b-136">如果 WinRM 伺服器將回應傳回至不是401回應的用戶端，則 proxy 不應關閉連接。</span><span class="sxs-lookup"><span data-stu-id="ae27b-136">If the WinRM server returns a response to the client that is not a 401 response, the proxy should not close the connection.</span></span>

    <span data-ttu-id="ae27b-137">在傳送實際的封包資料之前，可以在用戶端與伺服器之間傳送多個要求/回應配對。</span><span class="sxs-lookup"><span data-stu-id="ae27b-137">Multiple request/response pairs can be sent between client and server before the actual packet data is sent.</span></span> <span data-ttu-id="ae27b-138">WinRM 2.0 使用具有加密的 Negotiate 和 Kerberos 驗證配置，這可能會增加額外的來回行程。</span><span class="sxs-lookup"><span data-stu-id="ae27b-138">WinRM 2.0 uses the Negotiate and Kerberos authentication schemes with encryption, which can add extra round-trips.</span></span> <span data-ttu-id="ae27b-139">在驗證完成之前，無法將資料傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae27b-139">Data cannot be sent to the server until the authentication is complete.</span></span>

    <span data-ttu-id="ae27b-140">WinRM 伺服器會傳回200層級的回應，表示驗證已完成。</span><span class="sxs-lookup"><span data-stu-id="ae27b-140">The WinRM server returns a 200-level response that indicates that the authentication is complete.</span></span> <span data-ttu-id="ae27b-141">以 HTTP 為基礎的 proxy 伺服器可能會在收到來自 WinRM 伺服器的200層級回應後，結束以連線為基礎的驗證親和性，並關閉 TCP/IP 連接。</span><span class="sxs-lookup"><span data-stu-id="ae27b-141">HTTP-based proxy servers might end the connection-based authentication affinity and close the TCP/IP connection after receiving the 200-level response from the WinRM server.</span></span> <span data-ttu-id="ae27b-142">從用戶端到伺服器的最後一次往返不包含原始的要求封包。</span><span class="sxs-lookup"><span data-stu-id="ae27b-142">The final round-trip from client to server does not include the original request packet.</span></span> <span data-ttu-id="ae27b-143">如果 proxy 伺服器關閉連線，伺服器將會嘗試重新驗證用戶端，而且用戶端要求可能永遠不會傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae27b-143">If the proxy server closes the connection, the server will attempt to re-authenticate the client and the client request might never be sent to the server.</span></span> <span data-ttu-id="ae27b-144">如果未維護以連線為基礎的親和性，則對目的地伺服器的驗證可能會失敗，並出現「拒絕存取」錯誤。</span><span class="sxs-lookup"><span data-stu-id="ae27b-144">If the connection-based affinity is not maintained, authentication against the destination server can fail with an access denied error.</span></span>

-   <span data-ttu-id="ae27b-145">連接持續性。</span><span class="sxs-lookup"><span data-stu-id="ae27b-145">Connection persistence.</span></span> <span data-ttu-id="ae27b-146">Proxy 的用戶端 TCP/IP 連接應該會繼續對應到伺服器的相同 TCP/IP 連接。」</span><span class="sxs-lookup"><span data-stu-id="ae27b-146">The client TCP/IP connection to the proxy should continue to map to the same TCP/IP connection from the proxy to the server.</span></span> <span data-ttu-id="ae27b-147">維護此連線有助於達成更高層級的效能。</span><span class="sxs-lookup"><span data-stu-id="ae27b-147">Maintaining this connection helps to achieve a higher level of performance.</span></span> <span data-ttu-id="ae27b-148">如果未維護連接，則每個要求都必須重新驗證，這可能會影響效能。</span><span class="sxs-lookup"><span data-stu-id="ae27b-148">If the connection is not maintained, every request must be re-authenticated, which might affect performance.</span></span>

### <a name="encryption-and-winrm-20"></a><span data-ttu-id="ae27b-149">加密和 WinRM 2。0</span><span class="sxs-lookup"><span data-stu-id="ae27b-149">Encryption and WinRM 2.0</span></span>

<span data-ttu-id="ae27b-150">WinRM 2.0 支援使用 Negotiate、Kerberos 和 CredSSP 驗證配置透過 HTTP 進行加密。</span><span class="sxs-lookup"><span data-stu-id="ae27b-150">WinRM 2.0 supports encryption over HTTP by using the Negotiate, Kerberos, and CredSSP authentication schemes.</span></span> <span data-ttu-id="ae27b-151">如果 WinRM 伺服器支援 HTTP，而且是透過 proxy 存取，則 WinRM 伺服器必須強制加密，而不允許未加密的網路流量。</span><span class="sxs-lookup"><span data-stu-id="ae27b-151">If a WinRM server supports HTTP and is accessed through a proxy, the WinRM server must enforce encryption and not allow unencrypted network traffic.</span></span>

<span data-ttu-id="ae27b-152">在任何情況下，不應該透過 proxy 伺服器傳送未加密的 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="ae27b-152">Under no circumstances should unencrypted HTTP requests be sent through proxy servers.</span></span> <span data-ttu-id="ae27b-153">當資料必須通過 proxy 伺服器才能傳送到目的地伺服器時，下列安全性問題很重要：</span><span class="sxs-lookup"><span data-stu-id="ae27b-153">When data must pass through a proxy server before being sent to the destination server, the following security issues are very important:</span></span>

-   <span data-ttu-id="ae27b-154">惡意的 proxy 伺服器可能會檢查每個要求/回應配對，包括認證。</span><span class="sxs-lookup"><span data-stu-id="ae27b-154">It is possible that a malicious proxy server could examine every request/response pair, including credentials.</span></span>
-   <span data-ttu-id="ae27b-155">如果在 WinRM 用戶端和 proxy 伺服器之間，以及在 proxy 伺服器與目的地伺服器之間，TCP/IP 連接不是強的，則未經授權的用戶端可以使用從 proxy 伺服器到目的地伺服器的相同驗證連線來連線到目的地伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae27b-155">If the TCP/IP connections are not strongly mapped between both the WinRM client and the proxy server and between the proxy server and the destination server, an unauthorized client could connect to the destination server by using the same authenticated connection from the proxy server to the destination server.</span></span> <span data-ttu-id="ae27b-156">目的地伺服器可能會允許未經驗證的用戶端存取資料。</span><span class="sxs-lookup"><span data-stu-id="ae27b-156">The destination server might allow the unauthenticated client access to data.</span></span> <span data-ttu-id="ae27b-157">如果強制加密，目的地伺服器會將拒絕存取訊息傳送給未經驗證的用戶端。</span><span class="sxs-lookup"><span data-stu-id="ae27b-157">If encryption is enforced, the destination server sends an access denied message to the unauthenticated client.</span></span>

<span data-ttu-id="ae27b-158">使用加密可減輕這些潛在的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="ae27b-158">Using encryption would mitigate these potential security issues.</span></span>

## <a name="configuring-a-proxy-server-for-winrm-11-and-earlier"></a><span data-ttu-id="ae27b-159">設定 WinRM 1.1 及更早版本的 Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="ae27b-159">Configuring a Proxy Server for WinRM 1.1 and Earlier</span></span>

<span data-ttu-id="ae27b-160">如果需要 proxy 才能連線到 WinRM 伺服器，WinRM 用戶端會依賴 Windows HTTP 服務 (WinHTTP) proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="ae27b-160">If a proxy is required to reach the WinRM server, the WinRM client relies on the Windows HTTP services (WinHTTP) proxy configuration.</span></span> <span data-ttu-id="ae27b-161">根據預設，WinHTTP 未設定為使用 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae27b-161">By default, WinHTTP is not configured to use a proxy server.</span></span> <span data-ttu-id="ae27b-162">您可以使用 [ProxyCfg.exe](/previous-versions/windows/desktop/ms761351(v=vs.85)) 或 [netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) 命令列公用程式來變更 WinHTTP proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="ae27b-162">WinHTTP proxy configuration can be changed by using the [ProxyCfg.exe](/previous-versions/windows/desktop/ms761351(v=vs.85)) or [netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) command-line utilities.</span></span>

<span data-ttu-id="ae27b-163">**WinRM 1.1 及更早版本：** WinRM 不會使用 Internet Explorer proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="ae27b-163">**WinRM 1.1 and Earlier:** WinRM does not use the Internet Explorer proxy settings.</span></span>

 

 