---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106984946"
---
# <a name="ntlmssp"></a><span data-ttu-id="b9b69-103">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="b9b69-103">NTLMSSP</span></span>

<span data-ttu-id="b9b69-104">NTLMSSP （其驗證服務識別碼是 RPC \_ C \_ 驗證 \_ WINNT）是所有 DCOM 版本都提供的安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="b9b69-104">NTLMSSP, whose authentication service identifier is RPC\_C\_AUTHN\_WINNT, is a security support provider that is available on all versions of DCOM.</span></span> <span data-ttu-id="b9b69-105">它會使用 NTLM 通訊協定進行驗證。</span><span class="sxs-lookup"><span data-stu-id="b9b69-105">It uses the NTLM protocol for authentication.</span></span> <span data-ttu-id="b9b69-106">NTLM 永遠不會在驗證期間將使用者的密碼傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="b9b69-106">NTLM never actually transmits the user's password to the server during authentication.</span></span> <span data-ttu-id="b9b69-107">因此，在模擬期間，伺服器無法使用密碼來存取使用者可存取的網路資源。</span><span class="sxs-lookup"><span data-stu-id="b9b69-107">Therefore, the server cannot use the password during impersonation to access network resources that the user would have access to.</span></span> <span data-ttu-id="b9b69-108">只能存取本機資源。</span><span class="sxs-lookup"><span data-stu-id="b9b69-108">Only local resources can be accessed.</span></span>

<span data-ttu-id="b9b69-109">NTLM 可在本機和跨電腦運作。</span><span class="sxs-lookup"><span data-stu-id="b9b69-109">NTLM works both locally and across computers.</span></span> <span data-ttu-id="b9b69-110">也就是說，如果用戶端和伺服器位於不同的電腦上，則 NTLM 仍然可以確保用戶端是其宣稱的身分。</span><span class="sxs-lookup"><span data-stu-id="b9b69-110">That is, if the client and server are on different computers, NTLM can still make sure the client is who it claims to be.</span></span>

<span data-ttu-id="b9b69-111">使用 NTLM 時，用戶端的身分識別會以功能變數名稱、使用者名稱及密碼或權杖來表示。</span><span class="sxs-lookup"><span data-stu-id="b9b69-111">With NTLM, the client's identity is represented by a domain name, user name, and a password or token.</span></span> <span data-ttu-id="b9b69-112">當伺服器呼叫 [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)時，會傳回用戶端的功能變數名稱和使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b9b69-112">When a server calls [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), the client's domain name and user name are returned.</span></span> <span data-ttu-id="b9b69-113">不過，當伺服器呼叫 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)時，會傳回用戶端的權杖。</span><span class="sxs-lookup"><span data-stu-id="b9b69-113">However, when a server calls [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), the client's token is returned.</span></span> <span data-ttu-id="b9b69-114">如果用戶端與伺服器之間沒有信任關係，而且伺服器具有與用戶端相同名稱和密碼的本機帳戶，則該帳戶將用來代表用戶端。</span><span class="sxs-lookup"><span data-stu-id="b9b69-114">If there is no trust relationship between client and server and if the server has a local account with the same name and password as the client, that account will be used to represent the client.</span></span>

<span data-ttu-id="b9b69-115">NTLM 支援跨執行緒和跨進程的相互驗證 (只能在本機) 。</span><span class="sxs-lookup"><span data-stu-id="b9b69-115">NTLM supports mutual authentication cross-thread and cross-process (locally only).</span></span> <span data-ttu-id="b9b69-116">如果用戶端在 \\ 呼叫 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)的情況下，以網域使用者的形式指定伺服器的主體名稱，則伺服器的身分識別必須符合該主體名稱，否則呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="b9b69-116">If the client specifies the principal name of the server in the form domain\\user in a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), the server's identity must match that principal name or the call will fail.</span></span> <span data-ttu-id="b9b69-117">如果用戶端指定 **Null**，則不會檢查伺服器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="b9b69-117">If the client specifies **NULL**, the server's identity will not be checked.</span></span>

<span data-ttu-id="b9b69-118">NTLM 另外支援在本機) 的委派模擬層級跨執行緒和跨進程 (。</span><span class="sxs-lookup"><span data-stu-id="b9b69-118">NTLM additionally supports the delegate impersonation level cross-thread and cross-process (locally only).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9b69-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b9b69-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9b69-120">COM 和安全性封裝</span><span class="sxs-lookup"><span data-stu-id="b9b69-120">COM and Security Packages</span></span>](com-and-security-packages.md)
</dt> </dl>

 

 