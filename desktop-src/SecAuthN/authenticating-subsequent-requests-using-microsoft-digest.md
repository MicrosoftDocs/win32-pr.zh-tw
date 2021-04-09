---
description: 伺服器會使用摘要式挑戰的不透明指示詞，將其共用安全性內容的參考傳送給用戶端。
ms.assetid: 543c4bed-b224-4da7-9746-12c9993a40af
title: 使用 Microsoft Digest 驗證後續要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eecccc3be68fb541994e63cdfc5035187e04aa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694240"
---
# <a name="authenticating-subsequent-requests-with-microsoft-digest"></a><span data-ttu-id="8afb5-103">使用 Microsoft Digest 驗證後續要求</span><span class="sxs-lookup"><span data-stu-id="8afb5-103">Authenticating Subsequent Requests with Microsoft Digest</span></span>

<span data-ttu-id="8afb5-104">伺服器會使用摘要式挑戰的不透明指示詞，將其共用 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 的參考傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="8afb5-104">The server sends the client a reference to their shared [*security context*](/windows/desktop/SecGloss/s-gly) using the opaque directive of the Digest challenge.</span></span> <span data-ttu-id="8afb5-105">成功驗證之後，用戶端必須在對目標伺服器的後續要求中指定此值。</span><span class="sxs-lookup"><span data-stu-id="8afb5-105">After a successful authentication, the client must specify this value in subsequent requests to the target server.</span></span> <span data-ttu-id="8afb5-106">將不透明的值包含在可使用現有安全性內容存取的資源要求中，就不需要在網域控制站重新進行驗證。</span><span class="sxs-lookup"><span data-stu-id="8afb5-106">Including the opaque value in requests for resources that are accessible using the existing security context eliminates the need to re-authenticate at the domain controller.</span></span> <span data-ttu-id="8afb5-107">這類要求會在伺服器上重新驗證，使用初始驗證後所快取的摘要 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly) 。</span><span class="sxs-lookup"><span data-stu-id="8afb5-107">Such requests are re-authenticated at the server, using the Digest [*session key*](/windows/desktop/SecGloss/s-gly) cached after the initial authentication.</span></span>

<span data-ttu-id="8afb5-108">下圖說明用戶端和伺服器在後續要求受存取保護的資源時，所採取的步驟。</span><span class="sxs-lookup"><span data-stu-id="8afb5-108">The following diagram illustrates the steps taken by client and server during a subsequent request for access-protected resources.</span></span>

![使用 microsoft 摘要式驗證後續要求](images/digest2.png)

<span data-ttu-id="8afb5-110">若要在成功驗證之後要求其他資源，用戶端會呼叫 Microsoft Digest [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函數來產生摘要挑戰回應。</span><span class="sxs-lookup"><span data-stu-id="8afb5-110">To request additional resources after a successful authentication, the client calls the Microsoft Digest [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a Digest challenge response.</span></span> <span data-ttu-id="8afb5-111">不透明的值會包含在以授權標頭形式傳送至伺服器之挑戰回應的不透明指示詞中， (顯示為 HTTP 要求) 。</span><span class="sxs-lookup"><span data-stu-id="8afb5-111">The opaque value is included in the opaque directive of the challenge response sent to the server as an Authorization header (shown as HTTP Request).</span></span>

<span data-ttu-id="8afb5-112">伺服器會呼叫 [**AcceptSecurityCoNtext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數來判斷用戶端是否有現有的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 。</span><span class="sxs-lookup"><span data-stu-id="8afb5-112">The server calls the [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function to determine whether there is an existing [*security context*](/windows/desktop/SecGloss/s-gly) for the client.</span></span> <span data-ttu-id="8afb5-113">找到現有的內容時，此函式會傳回 \_ \_ 完成 \_ 所需的 SEC E，指出伺服器必須接著呼叫 [**CompleteAuthToken**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) 函數。</span><span class="sxs-lookup"><span data-stu-id="8afb5-113">When an existing context is found, the function returns SEC\_E\_COMPLETE\_NEEDED to indicate the server must then call the [**CompleteAuthToken**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) function.</span></span> <span data-ttu-id="8afb5-114">此函式會使用 [初始驗證](initial-authentication-using-microsoft-digest.md)期間快取的摘要 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly)來執行用戶端驗證，而不是在網域控制站重新驗證。</span><span class="sxs-lookup"><span data-stu-id="8afb5-114">This function performs the client authentication using the Digest [*session key*](/windows/desktop/SecGloss/s-gly) cached during the [initial authentication](initial-authentication-using-microsoft-digest.md) instead of re-authenticating at the domain controller.</span></span>

 

 
