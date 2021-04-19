---
title: Kerberos v5 通訊協定
description: Kerberos v5 通訊協定
ms.assetid: a53a1edf-f374-4cbf-8050-7cde45284157
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d78c4bdc457007c04ad66163e2ebfd7f5397f9
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "106966844"
---
# <a name="kerberos-v5-protocol"></a><span data-ttu-id="230b3-103">Kerberos v5 通訊協定</span><span class="sxs-lookup"><span data-stu-id="230b3-103">Kerberos v5 Protocol</span></span>

<span data-ttu-id="230b3-104">Kerberos v5 驗證通訊協定具有 RPC \_ C \_ 驗證 \_ GSS Kerberos 的驗證服務識別碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="230b3-104">The Kerberos v5 authentication protocol has an authentication service identifier of RPC\_C\_AUTHN\_GSS\_KERBEROS.</span></span> <span data-ttu-id="230b3-105">Kerberos 通訊協定會定義用戶端與網路驗證服務的互動方式，並且是由網際網路工程任務推動小組在1993年9月的檔 [RFC 1510](https://www.ietf.org/rfc/rfc1510.txt)中 (IETF) 。</span><span class="sxs-lookup"><span data-stu-id="230b3-105">The Kerberos protocol defines how clients interact with a network authentication service and was standardized by the Internet Engineering Task Force (IETF) in September 1993, in document [RFC 1510](https://www.ietf.org/rfc/rfc1510.txt).</span></span> <span data-ttu-id="230b3-106">用戶端從 Kerberos 金鑰發佈中心 (KDC) 取得票證，並在建立連線時將這些票證呈交給伺服器。</span><span class="sxs-lookup"><span data-stu-id="230b3-106">Clients obtain tickets from the Kerberos Key Distribution Center (KDC), and they present these tickets to servers when connections are established.</span></span> <span data-ttu-id="230b3-107">Kerberos 票證代表用戶端的網路認證。</span><span class="sxs-lookup"><span data-stu-id="230b3-107">Kerberos tickets represent the client's network credentials.</span></span>

<span data-ttu-id="230b3-108">Kerberos 通訊協定與 NTLM 一樣，會使用功能變數名稱、使用者名稱和密碼來代表用戶端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="230b3-108">Like NTLM, the Kerberos protocol uses the domain name, user name, and password to represent the client's identity.</span></span> <span data-ttu-id="230b3-109">當使用者登入時，從 KDC 取得的初始 Kerberos 票證是以使用者密碼的加密雜湊為基礎。</span><span class="sxs-lookup"><span data-stu-id="230b3-109">The initial Kerberos ticket obtained from the KDC when the user logs on is based on an encrypted hash of the user's password.</span></span> <span data-ttu-id="230b3-110">快取此初始票證。</span><span class="sxs-lookup"><span data-stu-id="230b3-110">This initial ticket is cached.</span></span> <span data-ttu-id="230b3-111">當使用者嘗試連接到伺服器時，Kerberos 通訊協定會檢查票證快取是否有該伺服器的有效票證。</span><span class="sxs-lookup"><span data-stu-id="230b3-111">When the user tries to connect to a server, the Kerberos protocol checks the ticket cache for a valid ticket for that server.</span></span> <span data-ttu-id="230b3-112">如果無法使用，則會將使用者的初始票證連同指定之伺服器的票證要求傳送給 KDC。</span><span class="sxs-lookup"><span data-stu-id="230b3-112">If one is not available, the initial ticket for the user is sent to the KDC along with a request for a ticket for the specified server.</span></span> <span data-ttu-id="230b3-113">該會話票證會新增至快取，而且可以用來連接到相同的伺服器，直到票證到期為止。</span><span class="sxs-lookup"><span data-stu-id="230b3-113">That session ticket is added to the cache, and it can be used to connect to the same server until the ticket expires.</span></span>

<span data-ttu-id="230b3-114">當伺服器使用 Kerberos 通訊協定呼叫 [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) 時，會傳回用戶端的功能變數名稱和使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="230b3-114">When a server calls [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) using the Kerberos protocol, the client's domain name and user name are returned.</span></span> <span data-ttu-id="230b3-115">當伺服器呼叫 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)時，會傳回用戶端的權杖。</span><span class="sxs-lookup"><span data-stu-id="230b3-115">When a server calls [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), the client's token is returned.</span></span> <span data-ttu-id="230b3-116">這些行為與使用 NTLM 時相同。</span><span class="sxs-lookup"><span data-stu-id="230b3-116">These behaviors are the same as when using NTLM.</span></span>

<span data-ttu-id="230b3-117">Kerberos 通訊協定可以跨電腦界限運作。</span><span class="sxs-lookup"><span data-stu-id="230b3-117">The Kerberos protocol works across computer boundaries.</span></span> <span data-ttu-id="230b3-118">用戶端和伺服器電腦都必須位於網域中，而且這些網域必須具有信任關係。</span><span class="sxs-lookup"><span data-stu-id="230b3-118">The client and server computers must both be in domains, and those domains must have a trust relationship.</span></span>

<span data-ttu-id="230b3-119">Kerberos 通訊協定需要相互驗證並從遠端支援。</span><span class="sxs-lookup"><span data-stu-id="230b3-119">The Kerberos protocol requires mutual authentication and supports it remotely.</span></span> <span data-ttu-id="230b3-120">用戶端必須指定伺服器的主體名稱，且伺服器的身分識別必須完全符合該主體名稱。</span><span class="sxs-lookup"><span data-stu-id="230b3-120">The client must specify the principal name of the server, and the server's identity must match that principal name exactly.</span></span> <span data-ttu-id="230b3-121">如果用戶端為伺服器的主體名稱指定 **Null** ，或主體名稱與伺服器不符，則呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="230b3-121">If the client specifies **NULL** for the server's principal name or if the principal name doesn't match the server, the call will fail.</span></span>

<span data-ttu-id="230b3-122">使用 Kerberos 通訊協定時，可使用模擬層級識別、模擬和委派。</span><span class="sxs-lookup"><span data-stu-id="230b3-122">With the Kerberos protocol, the impersonation levels identify, impersonate, and delegate can be used.</span></span> <span data-ttu-id="230b3-123">當伺服器呼叫 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)時，傳回的權杖會在5分鐘到8小時之間的一段時間內有效。</span><span class="sxs-lookup"><span data-stu-id="230b3-123">When a server calls [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), the token returned is valid off the computer for some time period between 5 minutes and 8 hours.</span></span> <span data-ttu-id="230b3-124">在這段時間之後，只能在伺服器電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="230b3-124">After this time, it can be used on the server computer only.</span></span> <span data-ttu-id="230b3-125">如果伺服器是 "run as activator"，且啟用是使用 Kerberos 通訊協定完成，伺服器的權杖將會在啟用後的5分鐘到8小時之間到期。</span><span class="sxs-lookup"><span data-stu-id="230b3-125">If a server is "run as activator" and the activation is done with the Kerberos protocol, the server's token will expire between 5 minutes and 8 hours after activation.</span></span>

<span data-ttu-id="230b3-126">Windows 所執行的 Kerberos v5 驗證通訊協定支援 [掩蓋](cloaking.md)。</span><span class="sxs-lookup"><span data-stu-id="230b3-126">The Kerberos v5 authentication protocol implemented by WindowsÂ supports [cloaking](cloaking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="230b3-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="230b3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="230b3-128">COM 和安全性封裝</span><span class="sxs-lookup"><span data-stu-id="230b3-128">COM and Security Packages</span></span>](com-and-security-packages.md)
</dt> </dl>

 

 




