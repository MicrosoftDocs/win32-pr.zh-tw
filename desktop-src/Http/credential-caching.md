---
title: 認證快取
description: 認證快取
ms.assetid: 6e411333-56fa-455b-a90a-f2b54f3c9545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a139d0cd90495de87f42de08687fd3157acaf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932403"
---
# <a name="credential-caching"></a><span data-ttu-id="9041b-103">認證快取</span><span class="sxs-lookup"><span data-stu-id="9041b-103">Credential Caching</span></span>

## <a name="credential-caching-on-ntlm-ka-connections"></a><span data-ttu-id="9041b-104">NTLM KA 連接上的認證快取</span><span class="sxs-lookup"><span data-stu-id="9041b-104">Credential Caching on NTLM KA Connections</span></span>

<span data-ttu-id="9041b-105">HTTP 伺服器 API 只會在 Keep-Alive (KA) 的 NTLM 驗證連接上快取認證。</span><span class="sxs-lookup"><span data-stu-id="9041b-105">The HTTP Server API caches credentials only on Keep-Alive (KA) connections for NTLM authentication.</span></span> <span data-ttu-id="9041b-106">根據預設，HTTP 伺服器 API 會快取在 KA 連接上傳送的第一個要求所取得的認證。</span><span class="sxs-lookup"><span data-stu-id="9041b-106">By default, the HTTP Server API caches the credentials obtained on the first request sent on a KA connection.</span></span> <span data-ttu-id="9041b-107">用戶端可以在不含授權標頭的 KA 連接上傳送後續要求，並根據先前建立的內容取得驗證。</span><span class="sxs-lookup"><span data-stu-id="9041b-107">The client can send subsequent requests on KA connections without an authorization header and obtain authentication based on the previously established context.</span></span> <span data-ttu-id="9041b-108">在此情況下，HTTP 伺服器 API 會根據快取的認證，將權杖傳送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="9041b-108">In this case, the HTTP Server API sends the token based on the cached credential to the application.</span></span> <span data-ttu-id="9041b-109">不會快取 proxy 所傳送之要求的認證。</span><span class="sxs-lookup"><span data-stu-id="9041b-109">Credentials for a request sent by a proxy are not cached.</span></span> <span data-ttu-id="9041b-110">應用程式會在對 HttpSetServerSessionProperty 或 HttpSetUrlGroupProperty 的呼叫中所提供的 [**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)結構中設定 **DisableNTLMCredentialCaching** 旗標，以停用 NTLM 認證快取。</span><span class="sxs-lookup"><span data-stu-id="9041b-110">The application disables NTLM credential caching by setting the **DisableNTLMCredentialCaching** flag in the [**HTTP\_SERVER\_AUTHENTICATION\_INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) structure that is supplied in calls to HttpSetServerSessionProperty or HttpSetUrlGroupProperty.</span></span> <span data-ttu-id="9041b-111">停用認證快取時，HTTP 伺服器 API 會捨棄快取的認證，並針對每個要求執行驗證。</span><span class="sxs-lookup"><span data-stu-id="9041b-111">When credential caching is disabled, the HTTP Server API discards the cached credentials and performs authentication for each request</span></span>

## <a name="ntlm-credential-caching-for-specific-urls"></a><span data-ttu-id="9041b-112">特定 Url 的 NTLM 認證快取</span><span class="sxs-lookup"><span data-stu-id="9041b-112">NTLM Credential Caching for Specific URLs</span></span>

<span data-ttu-id="9041b-113">應用程式會檢查 HTTP \_ 要求 \_ 驗證資訊結構的旗標參數，以判斷 HTTP 伺服器 API 傳回的要求認證是否已快取 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9041b-113">The application determines if the request credentials returned by the HTTP Server API are cached by inspecting the Flags parameter of the HTTP\_REQUEST\_AUTH\_INFO structure.</span></span> <span data-ttu-id="9041b-114">此參數表示從快取 \_ \_ \_ \_ \_ \_ \_ 取出傳回的 NTLM 權杖時，快取認證的 HTTP 要求驗證旗標權杖。</span><span class="sxs-lookup"><span data-stu-id="9041b-114">This parameter indicates HTTP\_REQUEST\_AUTH\_FLAG\_TOKEN\_FOR\_CACHED\_CRED when the returned NTLM token was retrieved from the cache.</span></span> <span data-ttu-id="9041b-115">認證快取是針對群組中所有 Url 的 URL 群組所指定。</span><span class="sxs-lookup"><span data-stu-id="9041b-115">Credential caching is specified on a URL group for all the URLs in the group.</span></span> <span data-ttu-id="9041b-116">不支援每個 URL 的認證快取，但應用程式可以藉由在 \_ \_ \_ \_ \_ \_ \_ HTTP \_ 要求 \_ 驗證 \_ 資訊結構中檢查快取認證旗標的 HTTP 要求驗證旗標權杖，判斷是否要在每個 url 上接受或拒絕快取的認證。</span><span class="sxs-lookup"><span data-stu-id="9041b-116">Credential caching on a per URL basis is not supported, however, applications can determine whether to accept or reject cached credentials on a per URL basis by checking the HTTP\_REQUEST\_AUTH\_FLAG\_TOKEN\_FOR\_CACHED\_CRED flag in the HTTP\_REQUEST\_AUTH\_INFO structure.</span></span> <span data-ttu-id="9041b-117">應用程式會將401驗證挑戰傳送給用戶端，以拒絕快取的認證。</span><span class="sxs-lookup"><span data-stu-id="9041b-117">The application rejects the cached credentials by sending a 401 authentication challenge to the client.</span></span> <span data-ttu-id="9041b-118">用戶端接著會使用授權標頭重新傳送要求，並使用 HTTP 伺服器 API 觸發新的驗證交握。</span><span class="sxs-lookup"><span data-stu-id="9041b-118">The client then resends the request with the authorization headers, triggering a new authentication handshake with the HTTP Server API.</span></span>

## <a name="basic-authentication"></a><span data-ttu-id="9041b-119">基本驗證</span><span class="sxs-lookup"><span data-stu-id="9041b-119">Basic Authentication</span></span>

<span data-ttu-id="9041b-120">當要求中包含基本驗證標頭時，HTTP 伺服器 API 會剖析標頭來取得使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="9041b-120">When a Basic authentication header is included in the request, the HTTP Server API parses the header to obtain the user name and password.</span></span> <span data-ttu-id="9041b-121">然後將使用者名稱剖析為使用者和網域部分。</span><span class="sxs-lookup"><span data-stu-id="9041b-121">The user name is then parsed into the user and domain portions.</span></span> <span data-ttu-id="9041b-122">HTTP 伺服器 API 會根據使用者名稱和網域金鑰，快取針對基本驗證取得的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="9041b-122">The HTTP Server API caches the access token, obtained for Basic authentication, based on the user name and domain key.</span></span> <span data-ttu-id="9041b-123">收到新的要求時，HTTP 伺服器 API 會根據使用者名稱和網域抓取存取權杖。</span><span class="sxs-lookup"><span data-stu-id="9041b-123">When a new request is received, the HTTP Server API retrieves the access token based on the user name and domain.</span></span> <span data-ttu-id="9041b-124">然後，會根據快取的密碼檢查要求中的密碼。</span><span class="sxs-lookup"><span data-stu-id="9041b-124">The password in the request is then checked against the cached password.</span></span> <span data-ttu-id="9041b-125">當達到存留時間 (TTL) 限制時，就會刪除快取的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="9041b-125">The cached access token is deleted when the time-to-live (TTL) limit is reached.</span></span>

 

 




