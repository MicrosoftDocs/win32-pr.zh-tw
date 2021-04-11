---
description: 用戶端內容初始化
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: 用戶端內容初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615ce5c157371f1ebfec685d6227bd11a1d76531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114948"
---
# <a name="client-context-initialization"></a><span data-ttu-id="c3fbe-103">用戶端內容初始化</span><span class="sxs-lookup"><span data-stu-id="c3fbe-103">Client Context Initialization</span></span>

<span data-ttu-id="c3fbe-104">為了建立安全連線，用戶端會先 [*取得輸出認證*](/windows/desktop/SecGloss/c-gly) 控制碼，然後再將驗證要求傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-104">To establish a secure connection, the client acquires an outbound [*credentials*](/windows/desktop/SecGloss/c-gly) handle before sending an authentication request to the server.</span></span> <span data-ttu-id="c3fbe-105">伺服器會從驗證要求建立用戶端的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-105">The server creates a security context for the client from the authentication request.</span></span> <span data-ttu-id="c3fbe-106">有兩個與驗證設定相關的用戶端 SSPI 函數：</span><span class="sxs-lookup"><span data-stu-id="c3fbe-106">There are two client-side SSPI functions involved in authentication setup:</span></span>

-   <span data-ttu-id="c3fbe-107">[**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) 會取得先前取得之登入 [*認證*](/windows/desktop/SecGloss/c-gly)的參考。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-107">[**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) obtains a reference to previously obtained logon [*credentials*](/windows/desktop/SecGloss/c-gly).</span></span>
-   <span data-ttu-id="c3fbe-108">[**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 會建立初始驗證要求安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-108">[**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) creates the initial authentication request security tokens.</span></span>

<span data-ttu-id="c3fbe-109">您可以在 [使用 SSPI 搭配 Windows 通訊端用戶端](using-sspi-with-a-windows-sockets-client.md)的 **GenClientCoNtext** 函式中，看到此進程的程式碼。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-109">Code for this process can be seen in the **GenClientContext** function in [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md).</span></span>

<span data-ttu-id="c3fbe-110">如果用戶端程式除了本身的登入認證（例如不同的使用者名稱、功能變數名稱和密碼）之外，還需要使用認證，它會在 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)呼叫中提供它們，並指定額外 [**的認證。 \_ \_ \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a)</span><span class="sxs-lookup"><span data-stu-id="c3fbe-110">If a client program needs to use credentials in addition to its own logon credentials, such as a different user name, domain name, and password, it provides them in the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) call with a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure specifying the additional credentials.</span></span> <span data-ttu-id="c3fbe-111">如需認證功能的詳細資訊，請參閱 [認證管理](authentication-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-111">For more information on credentials functions, see [Credential Management](authentication-functions.md).</span></span>

> [!Note]  
> <span data-ttu-id="c3fbe-112"> [**\_ \_ \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) \_ \_ \_ \_ 當結構中的字串是 ASCI 或 OEM 時，每秒的 winnt 驗證身分識別結構的旗標成員都可以設定為 sec 的 winnt auth identity ANSI。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-112">The **Flags** member of the [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure can be set to SEC\_WINNT\_AUTH\_IDENTITY\_ANSI when strings in the structure are ASCI or OEM.</span></span> <span data-ttu-id="c3fbe-113">如果使用 MultiByteToWideChar 函式將 ANSI 字串第一次轉換成 unicode，則 ANSI 字串可以與 **sec \_ winnt \_ auth \_ identity** 結構的 Flags 成員一起使用 \_ \_ \_ \_ 。 [](/windows/desktop/SecGloss/u-gly) [](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)</span><span class="sxs-lookup"><span data-stu-id="c3fbe-113">ANSI strings can be used with the **Flags** member of the **SEC\_WINNT\_AUTH\_IDENTITY** structure set to SEC\_WINNT\_AUTH\_IDENTITY\_UNICODE if they are first converted to [*Unicode*](/windows/desktop/SecGloss/u-gly) by using the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function.</span></span>

 

<span data-ttu-id="c3fbe-114">為了起始驗證的第一個階段，用戶端會呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 來取得要在連線要求訊息中傳送至伺服器的初始安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-114">To initiate the first leg of the authentication, the client calls [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) to obtain an initial security token to be sent in a connection request message to the server.</span></span>

<span data-ttu-id="c3fbe-115">用戶端會使用輸出緩衝區描述項中收到的安全性權杖資訊來產生要傳送至伺服器的訊息。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-115">The client uses the security token information received in the output buffer descriptor to generate a message to send to the server.</span></span> <span data-ttu-id="c3fbe-116">訊息的結構（就不同的緩衝區的放置等而言）是 [*應用程式協定*](/windows/desktop/SecGloss/a-gly) 的一部分，而且必須由雙方理解。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-116">The construction of the message, in terms of placement of various buffers and so forth, is part of the [*application protocol*](/windows/desktop/SecGloss/a-gly) and must be understood by both parties.</span></span>

<span data-ttu-id="c3fbe-117">用戶端會從 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 檢查傳回狀態，以查看驗證是否會在單一呼叫中完成。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-117">The client checks the return status from [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) to see if authentication will complete in a single call.</span></span> <span data-ttu-id="c3fbe-118">當我繼續需要秒的傳回狀態 \_ 時 \_ \_ ，表示安全性通訊協定需要多個驗證訊息。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-118">A return status of SEC\_I\_CONTINUE\_NEEDED indicates that the security protocol requires multiple authentication messages.</span></span> <span data-ttu-id="c3fbe-119">如需內容函數的詳細資訊，請參閱 [內容管理](authentication-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="c3fbe-119">For more information on context functions, see [Context Management](authentication-functions.md).</span></span>

 

 
