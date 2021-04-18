---
description: 摘要存取通訊協定
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: 摘要存取通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86aa8f05580c27c866c0568dbc67c4d5ba5c2016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550463"
---
# <a name="the-digest-access-protocol"></a><span data-ttu-id="b71b6-103">摘要存取通訊協定</span><span class="sxs-lookup"><span data-stu-id="b71b6-103">The Digest Access Protocol</span></span>

<span data-ttu-id="b71b6-104">[RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)所指定的摘要存取通訊協定是由 Microsoft Digest 的 [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 所執行。</span><span class="sxs-lookup"><span data-stu-id="b71b6-104">The Digest Access protocol specified by [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt) is implemented by the Microsoft Digest [*security support provider*](../secgloss/s-gly.md) (SSP).</span></span> <span data-ttu-id="b71b6-105">這項功能是由一組 [Microsoft 安全性支援提供者介面](sspi.md) 所組成， (SSPI) 用戶端/伺服器應用程式呼叫的安全性內容功能：</span><span class="sxs-lookup"><span data-stu-id="b71b6-105">The implementation consists of a set of [Microsoft Security Support Provider Interface](sspi.md) (SSPI) security context functions that client/server applications call to:</span></span>

-   <span data-ttu-id="b71b6-106">建立訊息交換的 [*安全性內容*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="b71b6-106">Establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span>
-   <span data-ttu-id="b71b6-107">取得摘要 SSP 所需的資料物件，例如 [*認證*](../secgloss/c-gly.md) 和內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="b71b6-107">Obtain data objects required by the Digest SSP, such as [*credentials*](../secgloss/c-gly.md) and context handles.</span></span>
-   <span data-ttu-id="b71b6-108">存取訊息 [*完整性*](../secgloss/i-gly.md) 和機密性機制。</span><span class="sxs-lookup"><span data-stu-id="b71b6-108">Access message [*integrity*](../secgloss/i-gly.md) and confidentiality mechanisms.</span></span>

<span data-ttu-id="b71b6-109">摘要式存取驗證會在配對的要求/回應交易內進行，要求是源自用戶端，以及源自伺服器的回應。</span><span class="sxs-lookup"><span data-stu-id="b71b6-109">Digest Access authentication takes place within paired request/response transactions, with requests originating on the client and responses originating on the server.</span></span> <span data-ttu-id="b71b6-110">成功的摘要式存取驗證需要兩個要求/回應配對。</span><span class="sxs-lookup"><span data-stu-id="b71b6-110">A successful Digest Access authentication requires two request/response pairs.</span></span>

<span data-ttu-id="b71b6-111">當摘要 SSP 用於 HTTP 驗證時，不會在第一個和第二個要求/回應配對之間維護連接。</span><span class="sxs-lookup"><span data-stu-id="b71b6-111">When the Digest SSP is used for HTTP authentication, there is no connection maintained between the first and second request/response pair.</span></span> <span data-ttu-id="b71b6-112">換句話說，伺服器不會在傳送第一個回應之後等候第二個要求。</span><span class="sxs-lookup"><span data-stu-id="b71b6-112">In other words, the server does not wait for the second request after it sends the first response.</span></span>

<span data-ttu-id="b71b6-113">下圖顯示用戶端和伺服器在 HTTP 路徑上執行的步驟，以使用摘要 SSP 完成驗證。</span><span class="sxs-lookup"><span data-stu-id="b71b6-113">The following illustration shows the steps taken on the HTTP path by a client and server to complete an authentication using the Digest SSP.</span></span> <span data-ttu-id="b71b6-114">SASL 機制會使用相互驗證，因此驗證資料會傳回用戶端的最後 ASC 伺服器呼叫，以確認用戶端與正確的伺服器通訊。</span><span class="sxs-lookup"><span data-stu-id="b71b6-114">The SASL mechanism makes use of mutual authentication, so authentication data is sent back on the final ASC server call to the client that verifies that the client is communicating with the correct server.</span></span>

![摘要存取通訊協定](images/digest1.png)

<span data-ttu-id="b71b6-116">此程式會從用戶端開始，並傳送 HTTP 要求1以從伺服器要求受存取保護的資源。</span><span class="sxs-lookup"><span data-stu-id="b71b6-116">The process starts with the client requesting an access-protected resource from the server by sending HTTP Request 1.</span></span>

<span data-ttu-id="b71b6-117">伺服器會接收 HTTP 要求1，並判斷資源需要未包含在要求中的驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="b71b6-117">The server receives HTTP Request 1 and determines that the resource requires authentication information that was not included in the request.</span></span> <span data-ttu-id="b71b6-118">伺服器會產生用戶端的挑戰，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b71b6-118">The server generates a challenge for the client as follows:</span></span>

1.  <span data-ttu-id="b71b6-119">伺服器會藉由呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函數來取得其 [*認證*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b71b6-119">The server obtains its [*credentials*](../secgloss/c-gly.md) by calling the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span>
2.  <span data-ttu-id="b71b6-120">伺服器會藉由呼叫 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數來產生摘要挑戰。</span><span class="sxs-lookup"><span data-stu-id="b71b6-120">The server generates the Digest challenge by calling the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>
3.  <span data-ttu-id="b71b6-121">伺服器會將 WWW-Authenticate 標頭傳送給用戶端要求的回應， (顯示為 HTTP 回應 1) 。</span><span class="sxs-lookup"><span data-stu-id="b71b6-121">The server sends a WWW-Authenticate header as its response to the client's request (shown as HTTP Response 1).</span></span> <span data-ttu-id="b71b6-122">標頭包含摘要挑戰和不透明的指示詞，其中包含針對用戶端所建立之部分 [*安全性內容*](../secgloss/s-gly.md) 的參考。</span><span class="sxs-lookup"><span data-stu-id="b71b6-122">The header contains the Digest challenge and an opaque directive that contains a reference to a partial [*security context*](../secgloss/s-gly.md) established for the client.</span></span> <span data-ttu-id="b71b6-123">標頭會以401狀態碼傳送，指出用戶端要求產生了未授權的存取錯誤。</span><span class="sxs-lookup"><span data-stu-id="b71b6-123">The header is sent with a 401 status code that indicates that the client request generated an unauthorized access error.</span></span> <span data-ttu-id="b71b6-124">如需有關摘要挑戰的詳細資訊，請參閱 [摘要挑戰的內容](contents-of-a-digest-challenge.md) ，並 [產生摘要挑戰](generating-the-digest-challenge.md)。</span><span class="sxs-lookup"><span data-stu-id="b71b6-124">For more information about the Digest challenge, see [Contents of a Digest Challenge](contents-of-a-digest-challenge.md) and [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>
4.  <span data-ttu-id="b71b6-125">用戶端會接收 HTTP 回應1、將伺服器所傳送的摘要挑戰解壓縮，並產生摘要挑戰回應，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b71b6-125">The client receives HTTP Response 1, extracts the Digest challenge sent by the server, and generates a Digest challenge response as follows:</span></span>
    1.  <span data-ttu-id="b71b6-126">藉由呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) 函數或以互動方式提示使用者提供認證，即可取得使用者的認證。</span><span class="sxs-lookup"><span data-stu-id="b71b6-126">The user's credentials are obtained either by calling the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function or by interactively prompting the user for credentials.</span></span>
    2.  <span data-ttu-id="b71b6-127">挑戰和認證資訊會傳遞給 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函數，這會產生摘要挑戰回應。</span><span class="sxs-lookup"><span data-stu-id="b71b6-127">The challenge and credentials information are passed to the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function, which generates the Digest challenge response.</span></span>
5.  <span data-ttu-id="b71b6-128">用戶端會將包含挑戰回應的授權標頭傳送至伺服器， (顯示為 HTTP 要求 2) 。</span><span class="sxs-lookup"><span data-stu-id="b71b6-128">The client sends an Authorization header that contains the challenge response to the server (shown as HTTP Request 2).</span></span> <span data-ttu-id="b71b6-129">如需有關摘要挑戰回應的詳細資訊，請參閱 [摘要挑戰回應的內容](contents-of-a-digest-challenge-response.md) ，以及 [產生摘要挑戰回應](generating-the-digest-challenge-response.md)。</span><span class="sxs-lookup"><span data-stu-id="b71b6-129">For more information about the Digest challenge response, see [Contents of a Digest Challenge Response](contents-of-a-digest-challenge-response.md) and [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).</span></span>
6.  <span data-ttu-id="b71b6-130">伺服器會接收 HTTP 要求2、將用戶端所傳送的挑戰回應解壓縮，然後藉由呼叫 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數來驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="b71b6-130">The server receives HTTP Request 2, extracts the challenge response sent by the client, and authenticates the information by calling the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span> <span data-ttu-id="b71b6-131">如需有關驗證程式的詳細資訊，請參閱 [使用 Microsoft Digest 的初始驗證](initial-authentication-using-microsoft-digest.md)。</span><span class="sxs-lookup"><span data-stu-id="b71b6-131">For details about the authentication process, see [Initial Authentication using Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span></span>
7.  <span data-ttu-id="b71b6-132">伺服器會將 HTTP 回應2傳送回用戶端，作為摘要存取通訊協定所需的第二個和最後一個回應。</span><span class="sxs-lookup"><span data-stu-id="b71b6-132">The server sends HTTP Response 2 back to the client as the second and final response required by the Digest Access protocol.</span></span> <span data-ttu-id="b71b6-133">如果驗證成功，則此回應包含要求的資源。</span><span class="sxs-lookup"><span data-stu-id="b71b6-133">If the authentication is successful, this response contains the requested resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b71b6-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="b71b6-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b71b6-135">摘要挑戰回應的內容</span><span class="sxs-lookup"><span data-stu-id="b71b6-135">Contents of a Digest Challenge Response</span></span>](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
