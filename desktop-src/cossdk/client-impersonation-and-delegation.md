---
description: 在某些情況下，伺服器應用程式必須在用戶端上代表其存取的資源出示用戶端身分識別，通常是為了對用戶端身分識別執行存取檢查或驗證。
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: 用戶端模擬和委派
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7557dcde4cadf559dd8e116cf4e7bece4221aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973394"
---
# <a name="client-impersonation-and-delegation"></a><span data-ttu-id="9e4e3-103">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="9e4e3-103">Client Impersonation and Delegation</span></span>

<span data-ttu-id="9e4e3-104">在某些情況下，伺服器應用程式需要對其代表用戶端存取的資源出示用戶端的身分識別，通常是為了針對用戶端的身分識別來執行存取檢查或驗證。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-104">In some circumstances, a server application needs to present a client's identity to resources it accesses on the client's behalf, usually to cause access checks or authentication to be performed against the client's identity.</span></span> <span data-ttu-id="9e4e3-105">在特定範圍內，伺服器可以在用戶端的身分識別下採取動作，這是一種稱為模擬用戶端的動作。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-105">To a certain extent, the server can act under the client's identity—an action referred to as impersonating the client.</span></span>

<span data-ttu-id="9e4e3-106">模擬是執行緒在安全性內容中執行的 *能力，與* 擁有線程的進程不同。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-106">*Impersonation* is the ability of a thread to execute in a security context different from that of the process owning the thread.</span></span> <span data-ttu-id="9e4e3-107">伺服器執行緒會使用代表用戶端認證的存取權杖，並透過此存取權杖存取用戶端可以存取的資源。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-107">The server thread uses an access token representing the client's credentials, and with this, it can access resources that the client can access.</span></span>

<span data-ttu-id="9e4e3-108">使用模擬可確保伺服器可以精確地達成用戶端的功能。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-108">Using impersonation ensures that the server can do precisely what the client can do.</span></span> <span data-ttu-id="9e4e3-109">資源的存取權可能會受到限制或展開，取決於用戶端有許可權進行的作業。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-109">Access to resources may be either restricted or expanded, depending on what the client has permission to do.</span></span>

<span data-ttu-id="9e4e3-110">連接到資料庫時，您可以選擇讓伺服器模擬用戶端，讓資料庫可以驗證和授權用戶端。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-110">You might choose to have a server impersonate a client when connecting to a database so that the database can authenticate and authorize the client for itself.</span></span> <span data-ttu-id="9e4e3-111">或者，如果您的應用程式存取以安全描述項保護的檔案，並讓用戶端取得這些檔案中資訊的授權存取，應用程式就可以在存取檔案之前模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-111">Or, if your application accesses files that are protected with a security descriptor and to enable the client to obtain authorized access to information in these files, the application can impersonate the client before accessing the files.</span></span>

## <a name="how-to-implement-impersonation"></a><span data-ttu-id="9e4e3-112">如何執行模擬</span><span class="sxs-lookup"><span data-stu-id="9e4e3-112">How to Implement Impersonation</span></span>

<span data-ttu-id="9e4e3-113">模擬需要用戶端和伺服器 (的參與，而且在某些情況下，系統管理員) 。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-113">Impersonation requires participation by both client and server (and, in some cases, system administrators).</span></span> <span data-ttu-id="9e4e3-114">用戶端必須指出其意願讓伺服器使用其身分識別，而伺服器必須以程式設計的方式明確地假設用戶端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-114">The client must indicate its willingness to let the server use its identity, and the server must explicitly assume the client's identity programmatically.</span></span> <span data-ttu-id="9e4e3-115">如需詳細資訊，請參閱用戶端模擬和伺服器端[需求](server-side-requirements-for-impersonation.md)的[用戶端需求](client-side-requirements-for-impersonation.md)。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-115">For details, see the topics [Client-Side Requirements for Impersonation](client-side-requirements-for-impersonation.md) and [Server-Side Requirements for Impersonation](server-side-requirements-for-impersonation.md).</span></span>

## <a name="administrative-requirements-for-delegate-level-impersonation"></a><span data-ttu-id="9e4e3-116">Delegate-Level 模擬的系統管理需求</span><span class="sxs-lookup"><span data-stu-id="9e4e3-116">Administrative Requirements for Delegate-Level Impersonation</span></span>

<span data-ttu-id="9e4e3-117">若要有效地使用模擬、 *委派*（透過網路模擬用戶端）的最強大形式，必須在 Active Directory 服務中正確設定用戶端和伺服器使用者帳戶，以支援其 (，除了用戶端授與委派層級模擬) 的許可權，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9e4e3-117">To effectively use the most powerful form of impersonation, *delegation*, which is the impersonation of clients over the network, the client and server user accounts must be properly configured in the Active Directory Service to support it (in addition to the client granting authority to do delegate-level impersonation), as follows:</span></span>

-   <span data-ttu-id="9e4e3-118">伺服器身分識別在 Active Directory 服務中必須標示為「受信任的委派」。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-118">The server identity must be marked as "Trusted for delegation" in the Active Directory Service.</span></span>
-   <span data-ttu-id="9e4e3-119">在 Active Directory 服務中，用戶端身分識別不得標示為「帳戶是機密的，無法委派」。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-119">The client identity must not be marked as "Account is sensitive and cannot be delegated" in the Active Directory Service.</span></span>

<span data-ttu-id="9e4e3-120">這些設定功能讓網域系統管理員有更高程度的委派控制權，也就是，假設有多少信任 (，因此涉及安全性風險) 。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-120">These configuration features give the domain administrator a high degree of control over delegation, which is desirable, given how much trust (and hence security risk) is involved.</span></span> <span data-ttu-id="9e4e3-121">如需委派的詳細資訊，請參閱 [委派和](/windows/desktop/com/delegation-and-impersonation)模擬。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-121">For more detail about delegation, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

## <a name="cloaking"></a><span data-ttu-id="9e4e3-122">隱形</span><span class="sxs-lookup"><span data-stu-id="9e4e3-122">Cloaking</span></span>

<span data-ttu-id="9e4e3-123">除了用戶端透過模擬等級授與伺服器的授權單位之外，伺服器的掩蓋功能主要決定模擬的行為。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-123">Along with the authority a client grants a server through the impersonation level, the server's cloaking capability largely determines how impersonation will behave.</span></span> <span data-ttu-id="9e4e3-124">當伺服器呼叫用戶端（本身或用戶端）發出呼叫時，會影響伺服器實際呈現的身分識別。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-124">Cloaking affects what identity is actually presented by the server when it makes calls on the client's behalf—its own or the client's.</span></span> <span data-ttu-id="9e4e3-125">如需詳細資訊，請參閱「 [掩蔽](cloaking.md)」。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-125">For details, see [Cloaking](cloaking.md).</span></span>

## <a name="performance-implications"></a><span data-ttu-id="9e4e3-126">效能影響</span><span class="sxs-lookup"><span data-stu-id="9e4e3-126">Performance Implications</span></span>

<span data-ttu-id="9e4e3-127">模擬可能會大幅影響效能和調整。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-127">Impersonation can significantly affect performance and scaling.</span></span> <span data-ttu-id="9e4e3-128">通常在呼叫上模擬用戶端比直接進行呼叫更昂貴。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-128">It is generally more expensive to impersonate a client on a call than to make the call directly.</span></span> <span data-ttu-id="9e4e3-129">以下是一些要考慮的問題：</span><span class="sxs-lookup"><span data-stu-id="9e4e3-129">Following are some of the issues to consider:</span></span>

-   <span data-ttu-id="9e4e3-130">以複雜模式傳遞身分識別的計算額外負荷，尤其是在啟用動態遮蓋的情況下。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-130">The computational overhead of passing around identity in complicated patterns, particularly if dynamic cloaking is enabled.</span></span>
-   <span data-ttu-id="9e4e3-131">在許多地方強制執行重複的安全性檢查（而不是集中在中介層）的一般複雜性。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-131">The general complexity of enforcing redundant security checking in numerous places, instead of just centrally in the middle tier.</span></span>
-   <span data-ttu-id="9e4e3-132">在開啟模擬用戶端時，資料庫連接之類的資源無法跨多個用戶端重複使用—這是很大的障礙，可進行適當的調整。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-132">Resources such as database connections, when opened impersonating a client, cannot be reused across multiple clients—a very large roadblock to scaling well.</span></span>

<span data-ttu-id="9e4e3-133">有時候，唯一有效的解決方法是使用模擬，但應謹慎考慮這項決策。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-133">Sometimes the only effective solution to a problem is to use impersonation, but this decision should be carefully weighed.</span></span> <span data-ttu-id="9e4e3-134">如需這些問題的進一步討論，請參閱 [多層式應用程式安全性](multi-tier-application-security.md)。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-134">For a further discussion of these issues, see [Multi-Tier Application Security](multi-tier-application-security.md).</span></span>

## <a name="queued-components"></a><span data-ttu-id="9e4e3-135">已排入佇列的元件</span><span class="sxs-lookup"><span data-stu-id="9e4e3-135">Queued Components</span></span>

<span data-ttu-id="9e4e3-136">已[排入佇列的元件](com--queued-components.md)不支援模擬。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-136">[Queued components](com--queued-components.md) do not support impersonation.</span></span> <span data-ttu-id="9e4e3-137">當用戶端呼叫已排入佇列的物件時，實際上會對記錄器進行呼叫，這會將它封裝成訊息的一部分。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-137">When a client makes a call to a queued object, the call is actually made to the recorder, which packages it as part of a message to the server.</span></span> <span data-ttu-id="9e4e3-138">然後，接聽程式會從佇列讀取訊息，並將它傳遞給播放程式，叫用實際的伺服器元件，並進行相同的方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-138">The listener then reads the message from the queue and passes it to the player, which invokes the actual server component and makes the same method call.</span></span> <span data-ttu-id="9e4e3-139">因此，當伺服器接收到呼叫時，原始用戶端權杖無法透過模擬來使用。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-139">As such, when the server receives the call, the original client token is unavailable via impersonation.</span></span> <span data-ttu-id="9e4e3-140">但是，以角色為基礎的安全性仍然適用，而且使用 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) 介面的程式設計安全性也可以運作。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-140">Role-based security still applies, however, and programmatic security using the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface will work.</span></span> <span data-ttu-id="9e4e3-141">如需詳細資訊，請參閱已 [排入佇列的元件安全性](queued-components-security.md)。</span><span class="sxs-lookup"><span data-stu-id="9e4e3-141">For details, see [Queued Components Security](queued-components-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e4e3-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e4e3-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e4e3-143">用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="9e4e3-143">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="9e4e3-144">程式庫應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="9e4e3-144">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="9e4e3-145">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="9e4e3-145">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="9e4e3-146">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="9e4e3-146">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="9e4e3-147">以角色為基礎的安全性管理</span><span class="sxs-lookup"><span data-stu-id="9e4e3-147">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="9e4e3-148">在 COM + 中使用軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="9e4e3-148">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
