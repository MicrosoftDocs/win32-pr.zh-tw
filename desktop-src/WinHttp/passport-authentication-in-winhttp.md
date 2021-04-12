---
description: Microsoft Windows HTTP Services (WinHTTP) 完全支援 Microsoft Passport 驗證通訊協定的用戶端使用。 本主題提供 Passport 驗證相關的交易總覽，以及如何處理這些交易。
ms.assetid: 395d7aef-4da0-4664-8328-7d31ce58fedd
title: WinHTTP 中的 Passport 驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8fc00217c7c14fbd4635fab68398d2056c1ea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468677"
---
# <a name="passport-authentication-in-winhttp"></a><span data-ttu-id="250cc-104">WinHTTP 中的 Passport 驗證</span><span class="sxs-lookup"><span data-stu-id="250cc-104">Passport Authentication in WinHTTP</span></span>

<span data-ttu-id="250cc-105">Microsoft Windows HTTP Services (WinHTTP) 完全支援 Microsoft Passport 驗證通訊協定的用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="250cc-105">Microsoft Windows HTTP Services (WinHTTP) fully support the client side use of the Microsoft Passport authentication protocol.</span></span> <span data-ttu-id="250cc-106">本主題提供 Passport 驗證相關的交易總覽，以及如何處理這些交易。</span><span class="sxs-lookup"><span data-stu-id="250cc-106">This topic provides an overview of the transactions involved in Passport authentication and how to handle them.</span></span>

> [!Note]  
> <span data-ttu-id="250cc-107">在 WinHTTP 5.1 中，預設會停用 Passport 驗證。</span><span class="sxs-lookup"><span data-stu-id="250cc-107">In WinHTTP 5.1, Passport authentication is disabled by default.</span></span>

 

## <a name="passport-14"></a><span data-ttu-id="250cc-108">Passport 1。4</span><span class="sxs-lookup"><span data-stu-id="250cc-108">Passport 1.4</span></span>

<span data-ttu-id="250cc-109">Passport 是 Microsoft .NET 大樓 block 服務的核心元件。</span><span class="sxs-lookup"><span data-stu-id="250cc-109">Passport is a core component of the Microsoft .NET building block services.</span></span> <span data-ttu-id="250cc-110">它可讓企業在各式各樣的應用程式之間開發和提供分散式 Web 服務，並讓其成員在所有參與的網站上使用一個登入名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="250cc-110">It enables businesses to develop and offer distributed Web services across a wide range of applications and enables its members to use one sign-in name and password at all participating Web sites.</span></span>

<span data-ttu-id="250cc-111">WinHTTP 藉由執行 Passport 1.4 驗證的用戶端通訊協定，提供 Microsoft Passport 1.4 的平臺支援。</span><span class="sxs-lookup"><span data-stu-id="250cc-111">WinHTTP provides platform support for Microsoft Passport 1.4 by implementing the client-side protocol for Passport 1.4 authentication.</span></span> <span data-ttu-id="250cc-112">它會從與 Passport 基礎結構互動的詳細資料，以及 Windows XP 中儲存的使用者名稱和密碼，來釋出應用程式。</span><span class="sxs-lookup"><span data-stu-id="250cc-112">It frees applications from the details of interacting with the Passport infrastructure and the Stored User Names and Passwords in Windows XP.</span></span> <span data-ttu-id="250cc-113">與使用傳統驗證配置（例如基本或摘要）不同的是，此抽象概念可讓您從開發人員的觀點來使用 Passport。</span><span class="sxs-lookup"><span data-stu-id="250cc-113">This abstraction makes using Passport no different from a developer's perspective than using traditional authentication schemes like Basic or Digest.</span></span>

<span data-ttu-id="250cc-114">**WINDOWS XP：\*\*\*\*HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings \\ Passport \\ NumRegistrationRuns** 登錄機碼可識別 passport 驗證 Wizard 在需要 passport 驗證時所顯示的次數。</span><span class="sxs-lookup"><span data-stu-id="250cc-114">**Windows XP:** The **HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings\\Passport\\NumRegistrationRuns** registry key identifies the number of times the Passport Authentication Wizard is displayed when PassPort authentication is required.</span></span> <span data-ttu-id="250cc-115">如果此索引鍵的值設定為大於5的數位，則不會顯示嚮導。</span><span class="sxs-lookup"><span data-stu-id="250cc-115">If the value for this key is set to a number greater than 5, the wizard is not displayed.</span></span>

<span data-ttu-id="250cc-116">下列各節說明從用戶端應用程式觀點來看 Passport 驗證的相關交易。</span><span class="sxs-lookup"><span data-stu-id="250cc-116">The following sections describe the transactions involved in Passport authentication from the point of view of a client application.</span></span> <span data-ttu-id="250cc-117">如需伺服器端 Passport 開發，請參閱 Passport SDK 檔集總覽。</span><span class="sxs-lookup"><span data-stu-id="250cc-117">For server-side Passport development, see the Passport SDK Documentation Overview.</span></span>

-   [<span data-ttu-id="250cc-118">初始要求</span><span class="sxs-lookup"><span data-stu-id="250cc-118">Initial Request</span></span>](#initial-request)
-   [<span data-ttu-id="250cc-119">Passport 登入伺服器</span><span class="sxs-lookup"><span data-stu-id="250cc-119">Passport Login Server</span></span>](#passport-login-server)
-   [<span data-ttu-id="250cc-120">驗證的要求</span><span class="sxs-lookup"><span data-stu-id="250cc-120">Authenticated Request</span></span>](#authenticated-request)

### <a name="initial-request"></a><span data-ttu-id="250cc-121">初始要求</span><span class="sxs-lookup"><span data-stu-id="250cc-121">Initial Request</span></span>

<span data-ttu-id="250cc-122">當用戶端要求需要 Passport 驗證的伺服器上的資源時，伺服器會檢查要求是否有 [*票證*](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="250cc-122">When a client requests a resource on a server that requires Passport authentication, the server checks the request for the presence of [*tickets*](glossary.md).</span></span> <span data-ttu-id="250cc-123">如果與要求一起傳送有效的 *票證* ，伺服器會以要求的資源回應。</span><span class="sxs-lookup"><span data-stu-id="250cc-123">If a valid *ticket* is sent with the request, the server responds with the requested resource.</span></span> <span data-ttu-id="250cc-124">如果用戶端上沒有 *票證* 存在，伺服器就會以302狀態碼回應。</span><span class="sxs-lookup"><span data-stu-id="250cc-124">If the *ticket* does not exist on the client, the server responds with a 302 status code.</span></span> <span data-ttu-id="250cc-125">回應包括挑戰標頭：「WWW-驗證： Passport 1.4」。</span><span class="sxs-lookup"><span data-stu-id="250cc-125">The response includes the challenge header, "WWW-Authenticate: Passport1.4".</span></span> <span data-ttu-id="250cc-126">未使用 Passport 的用戶端可能會遵循重新導向至 Passport 登入伺服器。</span><span class="sxs-lookup"><span data-stu-id="250cc-126">Clients that are not using Passport can follow the redirection to the Passport login server.</span></span> <span data-ttu-id="250cc-127">更先進的用戶端通常會聯繫 Passport 結點，以判斷 Passport 登入伺服器的位置。</span><span class="sxs-lookup"><span data-stu-id="250cc-127">More advanced clients typically contact the Passport nexus to determine the location of the Passport login server.</span></span>

> [!Note]  
> <span data-ttu-id="250cc-128">Microsoft Passport 網路的核心是 Passport 網站地圖，可加速 Passport 參與者網站的同步 *處理，以* 確保每個網站都具有網路設定和其他問題的最新詳細資料。</span><span class="sxs-lookup"><span data-stu-id="250cc-128">Central to the Microsoft Passport network is the Passport *Nexus*, which facilitates synchronization of Passport participant sites to assure that each site has the latest details on network configuration and other issues.</span></span> <span data-ttu-id="250cc-129">每個 Passport 元件 (Passport Manager、登入伺服器、補救伺服器等) 會定期與該結點進行通訊，以取得其所需的資訊，並與 Passport 網路中的其他元件適當地進行通訊。</span><span class="sxs-lookup"><span data-stu-id="250cc-129">Each Passport component (Passport Manager, Login servers, Update servers, and so on) periodically communicates with the Nexus to retrieve the information it needs to locate, and properly communicate with, the other components in the Passport network.</span></span> <span data-ttu-id="250cc-130">這項資訊會以稱為元件設定檔或 CCD 的 XML 檔的形式抓取。</span><span class="sxs-lookup"><span data-stu-id="250cc-130">This information is retrieved as an XML document called a Component Configuration Document, or CCD.</span></span>

 

<span data-ttu-id="250cc-131">下圖顯示 Passport 分支機搆的初始要求。</span><span class="sxs-lookup"><span data-stu-id="250cc-131">The following image shows the initial request to a Passport affiliate.</span></span>

![影像會顯示 passport 分支機搆的初始要求。](images/art-passport1.png)

### <a name="passport-login-server"></a><span data-ttu-id="250cc-133">Passport 登入伺服器</span><span class="sxs-lookup"><span data-stu-id="250cc-133">Passport Login Server</span></span>

<span data-ttu-id="250cc-134">Passport 登入伺服器會處理 Passport *網域授權* 單位中任何資源的所有 [*票證*](glossary.md)要求。</span><span class="sxs-lookup"><span data-stu-id="250cc-134">A Passport login server handles all requests for [*tickets*](glossary.md) for any resource in a Passport *domain authority*.</span></span> <span data-ttu-id="250cc-135">用戶端應用程式必須連線到登入伺服器才能取得適當的 *票證*，才能使用 Passport 來驗證要求。</span><span class="sxs-lookup"><span data-stu-id="250cc-135">Before a request can be authenticated using Passport, the client application must contact the login server to obtain the appropriate *tickets*.</span></span>

<span data-ttu-id="250cc-136">當用戶端要求 Passport 登入伺服器的 [*票證*](glossary.md) 時，登入伺服器通常會以401狀態碼回應，指出必須提供使用者認證。</span><span class="sxs-lookup"><span data-stu-id="250cc-136">When a client requests [*tickets*](glossary.md) from a Passport login server, the login server typically responds with a 401 status code to indicate that user credentials must be provided.</span></span> <span data-ttu-id="250cc-137">當提供這些認證時，登入伺服器會回應在伺服器上存取指定資源所需的 *票證* ，其中包含原始要求的資源。</span><span class="sxs-lookup"><span data-stu-id="250cc-137">When these credentials are provided, the login server responds with the *tickets* required to access the specified resource on the server that contains the originally requested resource.</span></span> <span data-ttu-id="250cc-138">登入伺服器也可以將用戶端重新導向至可提供所要求資源的另一部伺服器。</span><span class="sxs-lookup"><span data-stu-id="250cc-138">The login server can also redirect the client to another server that can provide the requested resource.</span></span>

![影像顯示 passport 登入伺服器的用戶端票證要求。](images/art-passport2.png)

### <a name="authenticated-request"></a><span data-ttu-id="250cc-140">驗證的要求</span><span class="sxs-lookup"><span data-stu-id="250cc-140">Authenticated Request</span></span>

<span data-ttu-id="250cc-141">當用戶端具有對應至指定伺服器的 [*票證*](glossary.md) 時，這些 *票證* 會隨附于該伺服器的所有要求。</span><span class="sxs-lookup"><span data-stu-id="250cc-141">When the client has the [*tickets*](glossary.md) that correspond to a given server, those *tickets* are included with all requests to that server.</span></span> <span data-ttu-id="250cc-142">如果 *票證* 在從 Passport 登入伺服器抓取之後未曾修改過，而且 *票證* 對資源伺服器是有效的，則資源伺服器會傳送包含所要求資源的回應，以及表示使用者已通過驗證以取得未來要求的 cookie。</span><span class="sxs-lookup"><span data-stu-id="250cc-142">If the *tickets* have not been modified since they were retrieved from the Passport login server, and the *tickets* are valid for the resource server, the resource server sends a response that includes both the requested resource and cookies that indicate that the user is authenticated for future requests.</span></span>

<span data-ttu-id="250cc-143">回應中的其他 cookie 是為了加速驗證程式。</span><span class="sxs-lookup"><span data-stu-id="250cc-143">The additional cookies in the response are intended to speed the authentication process.</span></span> <span data-ttu-id="250cc-144">相同 Passport 網域授權單位中伺服器上資源的相同會話中的其他要求全都包含這些額外的 cookie。</span><span class="sxs-lookup"><span data-stu-id="250cc-144">Additional requests in the same session for resources on servers in the same Passport Domain Authority all include these additional cookies.</span></span> <span data-ttu-id="250cc-145">在 cookie 過期之前，不需要再次將認證傳送到登入伺服器。</span><span class="sxs-lookup"><span data-stu-id="250cc-145">Credentials do not need to be sent to the login server again until the cookies expire.</span></span>

![影像會顯示對 passport 登入伺服器的驗證要求。](images/art-passport3.png)

## <a name="using-passport-in-winhttp"></a><span data-ttu-id="250cc-147">在 WinHTTP 中使用 Passport</span><span class="sxs-lookup"><span data-stu-id="250cc-147">Using Passport in WinHTTP</span></span>

<span data-ttu-id="250cc-148">WinHTTP 中的 Passport 驗證與其他驗證配置非常類似。</span><span class="sxs-lookup"><span data-stu-id="250cc-148">Passport authentication in WinHTTP is very similar to other authentication schemes.</span></span> <span data-ttu-id="250cc-149">請參閱 [winHTTP 中的驗證](authentication-in-winhttp.md) ，以取得 winHTTP 中的驗證總覽。</span><span class="sxs-lookup"><span data-stu-id="250cc-149">See [Authentication in WinHTTP](authentication-in-winhttp.md) for an overview of authentication in WinHTTP.</span></span>

<span data-ttu-id="250cc-150">在 WinHTTP 5.1 中，預設會停用 Passport 驗證，而且必須在使用之前以 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 明確地啟用。</span><span class="sxs-lookup"><span data-stu-id="250cc-150">In WinHTTP 5.1, Passport authentication is disabled by default and must be explicitly enabled with [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) before use.</span></span>

<span data-ttu-id="250cc-151">WinHTTP 會在內部處理 Passport 驗證的許多交易詳細資料。</span><span class="sxs-lookup"><span data-stu-id="250cc-151">WinHTTP handles many of the transaction details internally for Passport authentication.</span></span> <span data-ttu-id="250cc-152">在初始要求期間，當需要驗證時，伺服器會回應302狀態碼。</span><span class="sxs-lookup"><span data-stu-id="250cc-152">During the initial request, the server responds with a 302 status code when authentication is necessary.</span></span> <span data-ttu-id="250cc-153">302狀態碼實際上表示重新導向，而且是 Passport 通訊協定的一部分，以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="250cc-153">The 302 status code actually indicates a redirection and is part of the Passport protocol for backwards compatibility.</span></span> <span data-ttu-id="250cc-154">WinHTTP 會隱藏302狀態碼，並與 Passport 結點聯繫，然後連線到登入伺服器。</span><span class="sxs-lookup"><span data-stu-id="250cc-154">WinHTTP hides the 302 status code and contacts the Passport nexus, and then the login server.</span></span> <span data-ttu-id="250cc-155">當登入伺服器傳送的401狀態碼要求使用者認證時，會通知 WinHTTP 應用程式。</span><span class="sxs-lookup"><span data-stu-id="250cc-155">The WinHTTP application is notified of the 401 status code sent by the login server to request user credentials.</span></span> <span data-ttu-id="250cc-156">不過，在應用程式中，它看起來就像是來自要求資源的伺服器，401狀態。</span><span class="sxs-lookup"><span data-stu-id="250cc-156">To the application, however, it appears as if the 401 status originates from the server from which the resource was requested.</span></span> <span data-ttu-id="250cc-157">如此一來，WinHTTP 應用程式就不會察覺與其他伺服器之間的互動，而且可以使用處理其他驗證配置的相同程式碼來處理 Passport 驗證。</span><span class="sxs-lookup"><span data-stu-id="250cc-157">In this way, the WinHTTP application is unaware of interactions with other servers, and it can handle Passport authentication with the same code that handles other authentication schemes.</span></span>

<span data-ttu-id="250cc-158">一般而言，WinHTTP 應用程式會藉由提供驗證認證來回應401狀態碼。</span><span class="sxs-lookup"><span data-stu-id="250cc-158">Typically, a WinHTTP application responds to a 401 status code by supplying authentication credentials.</span></span> <span data-ttu-id="250cc-159">使用 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) 或 [**SetCredentials**](iwinhttprequest-setcredentials.md) 為 passport 驗證提供認證時，會實際將認證傳送到登入伺服器，而不是傳送到要求中所指定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="250cc-159">When credentials are supplied with [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) or [**SetCredentials**](iwinhttprequest-setcredentials.md) for passport authentication, the credentials are actually being sent to the login server, not to the server indicated in the request.</span></span>

<span data-ttu-id="250cc-160">不過，當回應407狀態碼時，WinHTTP 應用程式必須使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 來提供 proxy 認證，而不是 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)。</span><span class="sxs-lookup"><span data-stu-id="250cc-160">However, when responding to a 407 status code, a WinHTTP application must use [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to provide proxy credentials, rather than [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span></span> <span data-ttu-id="250cc-161">因為 **WinHttpSetOption** 是較不安全的方式來提供認證，所以通常應該避免。</span><span class="sxs-lookup"><span data-stu-id="250cc-161">Because **WinHttpSetOption** is a less secure way to supply credentials, it should normally be avoided.</span></span>

<span data-ttu-id="250cc-162">經過抓取之後， [*票證*](glossary.md) 會在內部進行管理，並會在未來的要求中自動傳送至適用的伺服器。</span><span class="sxs-lookup"><span data-stu-id="250cc-162">Once retrieved, [*tickets*](glossary.md) are managed internally and are automatically sent to applicable servers in future requests.</span></span>

> [!Note]  
> <span data-ttu-id="250cc-163">WinHTTP 可讓您藉由呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函式，為 [**winHTTP \_ 選項停用 \_ \_ 功能**](option-flags.md) 旗標，並指定 WINHTTP 停用重新導向的值，以停用自動重新 [**\_ \_ 導向**](option-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="250cc-163">WinHTTP enables you to disable automatic redirection by calling the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function for the [**WINHTTP\_OPTION\_DISABLE\_FEATURE**](option-flags.md) flag and specifying a value of [**WINHTTP\_DISABLE\_REDIRECTS**](option-flags.md).</span></span> <span data-ttu-id="250cc-164">停用重新導向不會干擾 WinHTTP 在內部為 Passport 交易處理的重新導向。</span><span class="sxs-lookup"><span data-stu-id="250cc-164">Disabling redirection does not interfere with the redirection that WinHTTP handles internally for Passport transactions.</span></span>

 

<span data-ttu-id="250cc-165">即使應用程式停用自動重新導向，WinHTTP 仍可順利完成 Passport 驗證。</span><span class="sxs-lookup"><span data-stu-id="250cc-165">WinHTTP can successfully complete the Passport authentication even if an application disables auto redirection.</span></span> <span data-ttu-id="250cc-166">不過，在完成 Passport 驗證之後，必須從 Passport 登入伺服器 URL 將隱含的重新導向回到原始 URL。</span><span class="sxs-lookup"><span data-stu-id="250cc-166">However, after the Passport authentication is complete, an implicit redirect must occur from the Passport login server URL back to the original URL.</span></span> <span data-ttu-id="250cc-167">此重新導向不是由 302 HTTP 回應所觸發，但在 Passport 通訊協定中是隱含的。</span><span class="sxs-lookup"><span data-stu-id="250cc-167">This redirect is not triggered by a 302 HTTP response, but is implicit in the Passport protocol.</span></span>

<span data-ttu-id="250cc-168">WinHTTP 會特別處理這種隱含的重新導向。</span><span class="sxs-lookup"><span data-stu-id="250cc-168">WinHTTP handles this implicit redirect specially.</span></span> <span data-ttu-id="250cc-169">如果應用程式已停用自動重新導向，則在這個特殊情況下，WinHTTP 要求應用程式提供 WinHTTP 「許可權」來自動重新導向。</span><span class="sxs-lookup"><span data-stu-id="250cc-169">If an application has disabled automatic redirection, WinHTTP requires that the application give WinHTTP "permission" to redirect automatically in this special case.</span></span>

<span data-ttu-id="250cc-170">為了在驗證之後讓 WinHTTP 重新導向回到原始 URL，應用程式必須使用 [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)註冊回呼函式。</span><span class="sxs-lookup"><span data-stu-id="250cc-170">In order to have WinHTTP redirect back to the original URL after authentication, the application must register a callback function using [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span> <span data-ttu-id="250cc-171">WinHTTP 接著可以使用 WINHTTP 回呼狀態重新導向回呼來通知應用程式 \_ \_ \_ ，這可讓應用程式取消重新導向。</span><span class="sxs-lookup"><span data-stu-id="250cc-171">WinHTTP can then notify the application with a WINHTTP\_CALLBACK\_STATUS\_REDIRECT callback, which allows the application to cancel the redirect.</span></span> <span data-ttu-id="250cc-172">應用程式不需要在回呼函數中提供任何功能;回呼的註冊足以讓 WinHTTP 遵循這個特殊案例重新導向。</span><span class="sxs-lookup"><span data-stu-id="250cc-172">An application does not need to provide any functionality in the callback function; registration of the callback is sufficient to enable WinHTTP to follow this special-case redirect.</span></span>

<span data-ttu-id="250cc-173">\_ \_ \_ 如果應用程式未設定回呼函式，則會產生錯誤 WINHTTP 登入失敗訊息。</span><span class="sxs-lookup"><span data-stu-id="250cc-173">The ERROR\_WINHTTP\_LOGIN\_FAILURE message is generated if a callback function is not set by the application.</span></span>

### <a name="passport-cobranding"></a><span data-ttu-id="250cc-174">Passport Cobranding</span><span class="sxs-lookup"><span data-stu-id="250cc-174">Passport Cobranding</span></span>

<span data-ttu-id="250cc-175">不同于 WinHTTP 所支援的傳統驗證配置，Passport 可以廣泛地 [*在*](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="250cc-175">Unlike traditional authentication schemes supported by WinHTTP, Passport can be extensively [*cobranded*](glossary.md).</span></span> <span data-ttu-id="250cc-176">收到指出挑戰的401狀態碼時，應用程式可以取出 *cobranding* 圖形和文字。</span><span class="sxs-lookup"><span data-stu-id="250cc-176">Upon receiving a 401 status code that indicates a challenge, an application can retrieve the *cobranding* graphic and text.</span></span> <span data-ttu-id="250cc-177">使用 WINHTTP 選項[](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) \_ \_ PASSPORT \_ cobranding \_ URL 旗標來呼叫 WinHttpQueryOption，以取出 cobranding 圖形的 URL。</span><span class="sxs-lookup"><span data-stu-id="250cc-177">Retrieve a URL for the *cobranding* graphic by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL flag.</span></span> <span data-ttu-id="250cc-178">使用 WINHTTP  [](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) \_ 選項 \_ PASSPORT \_ cobranding \_ text 旗標呼叫 WinHttpQueryOption，以取出 cobranding 文字。</span><span class="sxs-lookup"><span data-stu-id="250cc-178">Retrieve the *cobranding* text by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT flag.</span></span> <span data-ttu-id="250cc-179">這些專案可以用來自訂認證收集對話方塊。</span><span class="sxs-lookup"><span data-stu-id="250cc-179">These items can be used to customize a credential-gathering dialog.</span></span>

### <a name="stored-user-names-and-passwords"></a><span data-ttu-id="250cc-180">儲存的使用者名稱與密碼</span><span class="sxs-lookup"><span data-stu-id="250cc-180">Stored User Names and Passwords</span></span>

<span data-ttu-id="250cc-181">Windows XP 引進了預存使用者名稱和密碼的概念。</span><span class="sxs-lookup"><span data-stu-id="250cc-181">Windows XP introduced the concept of Stored User Names and Passwords.</span></span> <span data-ttu-id="250cc-182">如果使用者的 Passport 認證是透過 **Passport 註冊嚮導** 或標準 **認證對話方塊** 來儲存，則會儲存在儲存的使用者名稱和密碼中。</span><span class="sxs-lookup"><span data-stu-id="250cc-182">If a user's Passport credentials are saved through the **Passport Registration Wizard** or the standard **Credential Dialog**, it is saved in the Stored User Names and Passwords.</span></span> <span data-ttu-id="250cc-183">在 Windows XP 或更新版本上使用 WinHTTP 時，如果未明確設定認證，WinHTTP 會自動使用預存使用者名稱和密碼中的認證。</span><span class="sxs-lookup"><span data-stu-id="250cc-183">When using WinHTTP on Windows XP or later, WinHTTP automatically uses the credentials in the Stored User Names and Passwords if credentials are not explicitly set.</span></span> <span data-ttu-id="250cc-184">這類似于支援 NTLM/Kerberos 的預設登入認證。</span><span class="sxs-lookup"><span data-stu-id="250cc-184">This is similar to the support of default logon credentials for NTLM/Kerberos.</span></span> <span data-ttu-id="250cc-185">不過，使用預設的 Passport 認證並不受自動登入原則設定的規定。</span><span class="sxs-lookup"><span data-stu-id="250cc-185">However, use of default Passport credentials is not subject to the automatic logon policy settings.</span></span>

### <a name="disabling-passport-authentication"></a><span data-ttu-id="250cc-186">停用 Passport 驗證</span><span class="sxs-lookup"><span data-stu-id="250cc-186">Disabling Passport Authentication</span></span>

<span data-ttu-id="250cc-187">有些應用程式可能需要停用 Passport 驗證的功能。</span><span class="sxs-lookup"><span data-stu-id="250cc-187">Some applications might require the ability to disable Passport authentication.</span></span> <span data-ttu-id="250cc-188">例如，當 Passport 分支機搆以最初的302狀態碼回應時，最好是遵循指示的重新導向並轉譯 HTML Passport 驗證頁面，而不是讓 WinHTTP 在內部處理驗證。</span><span class="sxs-lookup"><span data-stu-id="250cc-188">For example, when a Passport affiliate responds with the initial 302 status code, it might be preferable to follow the indicated redirection and render the HTML Passport authentication page rather than allowing WinHTTP to handle the authentication internally.</span></span> <span data-ttu-id="250cc-189">在 WinHTTP 中停用 Passport 驗證，方法是呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函式與 winHTTP \_ 選項 [ \_ 設定 \_ PASSPORT 驗證] \_ 選項，並傳遞值 winHTTP \_ DISABLE \_ passport \_ auth。</span><span class="sxs-lookup"><span data-stu-id="250cc-189">Passport authentication is disabled in WinHTTP by calling the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function with the WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH option and passing the value WINHTTP\_DISABLE\_PASSPORT\_AUTH.</span></span> <span data-ttu-id="250cc-190">您稍後可以使用 WINHTTP \_ 啟用 PASSPORT 驗證來重新啟用它 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="250cc-190">It can later be re-enabled with WINHTTP\_ENABLE\_PASSPORT\_AUTH.</span></span>

<span data-ttu-id="250cc-191">使用 [**WinHttpRequest**](winhttprequest.md) 物件時，無法停用 Passport 驗證。</span><span class="sxs-lookup"><span data-stu-id="250cc-191">Passport authentication cannot be disabled when using the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

<span data-ttu-id="250cc-192">如本節稍早所述，在 WinHTTP 5.1 中預設會停用 Passport 驗證，而且必須在使用之前明確啟用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 。</span><span class="sxs-lookup"><span data-stu-id="250cc-192">As noted earlier in this section, Passport authentication is disabled by default in WinHTTP 5.1, and must be explicitly enabled with [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) before use.</span></span>

## <a name="passport-configuration-overrides-used-for-testing"></a><span data-ttu-id="250cc-193">用於測試的 Passport 設定覆寫</span><span class="sxs-lookup"><span data-stu-id="250cc-193">Passport Configuration Overrides Used for Testing</span></span>

<span data-ttu-id="250cc-194">WinHTTP 依賴它從 passport 結點伺服器下載的設定資訊，以支援 Passport 1.4 驗證。</span><span class="sxs-lookup"><span data-stu-id="250cc-194">WinHTTP relies on the configuration information it downloads from the passport nexus server to support Passport 1.4 authentication.</span></span> <span data-ttu-id="250cc-195">根據預設，此安全 (SSL) server nexus.passport.com，而設定資源是 rdr/pprdr .asp，也就是所謂的「即時」 passport 設定。</span><span class="sxs-lookup"><span data-stu-id="250cc-195">By default this secure (SSL) server is nexus.passport.com, and the configuration resource is rdr/pprdr.asp, which is known as the "live" passport configuration.</span></span> <span data-ttu-id="250cc-196">此資訊的格式是自訂 HTTP 標頭 "PassportURLs"，後面接著逗點分隔的屬性/值配對。</span><span class="sxs-lookup"><span data-stu-id="250cc-196">The format of the information is a custom HTTP header "PassportURLs", followed by comma delimited attribute-value pairs.</span></span>

<span data-ttu-id="250cc-197">例如，"" 會傳回 https://nexus.passport.com/rdr/pprdr.asp 下列設定資訊：</span><span class="sxs-lookup"><span data-stu-id="250cc-197">For example, "https://nexus.passport.com/rdr/pprdr.asp" returns the following configuration information:</span></span>

``` syntax
PassportURLs: DARealm=Passport.net,
DALogin=login.passport.com/login2.asp,
DAReg=https://register.passport.com/defaultwiz.asp,
Properties=https://memberservices.passport.com/ppsecure/MSRV_EditProfile.asp,
Privacy=https://www.passport.com/consumer/privacypolicy.asp,
GeneralRedir=https://nexusrdr.passport.com/redir.asp,
Help=https://memberservices.passport.com/UI/MSRV_UI_Help.asp,
ConfigVersion=2
\r\n
```

<span data-ttu-id="250cc-198">與 WinHTTP 相關的部分是 DARealm、DALogin 和 ConfigVersion。</span><span class="sxs-lookup"><span data-stu-id="250cc-198">The parts that are relevant to WinHTTP are DARealm, DALogin, and ConfigVersion.</span></span> <span data-ttu-id="250cc-199">基於效能考慮，系統會在 WinHTTP 會話的存留期間快取它們。</span><span class="sxs-lookup"><span data-stu-id="250cc-199">For performance reasons, they are cached for the lifetime of a WinHTTP session.</span></span> <span data-ttu-id="250cc-200">這三個值可以由應用程式覆寫，而這些應用程式必須與其他 passport 基礎結構搭配運作，而非「即時」生產環境設定，方法是變更以下的適當登錄設定：</span><span class="sxs-lookup"><span data-stu-id="250cc-200">These three values can be overridden by applications that are required to work with another passport infrastructure other than the "live" production setup by changing the appropriate registry settings under</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
LoginServerRealm (REG_SZ)    For example: abc.net
LoginServerUrl (REG_SZ)      For example: https://private-login.passport.com/login2.asp
ConfigVersion (REG_DWORD)    For example: 10
```

<span data-ttu-id="250cc-201">如果登錄中有 LoginServerUrl，WinHTTP 將不會與伺服器上的其他設定值連線。</span><span class="sxs-lookup"><span data-stu-id="250cc-201">If LoginServerUrl is present in the registry, WinHTTP does not contact the nexus server for other configuration values.</span></span> <span data-ttu-id="250cc-202">在此情況下，您也應該透過登錄來設定 LoginServerRealm 和 ConfigVersion，以修正值。</span><span class="sxs-lookup"><span data-stu-id="250cc-202">In this case, LoginServerRealm and ConfigVersion should also be set through the registry to correct values.</span></span>

<span data-ttu-id="250cc-203">基於測試目的，應用程式可能需要從私用的結點伺服器下載 passport 設定。</span><span class="sxs-lookup"><span data-stu-id="250cc-203">An application may, for testing purposes, be required to download passport configuration from a private nexus server.</span></span> <span data-ttu-id="250cc-204">這可以藉由覆寫下列兩個登錄值來完成：</span><span class="sxs-lookup"><span data-stu-id="250cc-204">This can be done by overriding two registry values under</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
NexusHost (REG_SZ)    e.g. private-nexus.passport.com
NexusObj(REG_SZ)      e.g. config/passport.asp
```

## <a name="related-topics"></a><span data-ttu-id="250cc-205">相關主題</span><span class="sxs-lookup"><span data-stu-id="250cc-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="250cc-206">WinHTTP 中的驗證</span><span class="sxs-lookup"><span data-stu-id="250cc-206">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> </dl>

 

 



