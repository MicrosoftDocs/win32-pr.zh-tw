---
description: 由於 COM + 程式庫應用程式是由另一個進程（可能有自己的安全性設定）所裝載，因此程式庫應用程式的安全性需要特別考慮。
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: 程式庫應用程式安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510516"
---
# <a name="library-application-security"></a><span data-ttu-id="75055-103">程式庫應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="75055-103">Library Application Security</span></span>

<span data-ttu-id="75055-104">由於 COM + 程式庫應用程式是由另一個進程（可能有自己的安全性設定）所裝載，因此程式庫應用程式的安全性需要特別考慮。</span><span class="sxs-lookup"><span data-stu-id="75055-104">Because a COM+ library application is hosted by another process, which may have its own security settings, security for library applications requires special consideration.</span></span>

<span data-ttu-id="75055-105">下列條件約束適用于程式庫應用程式安全性：</span><span class="sxs-lookup"><span data-stu-id="75055-105">The following constraints apply to library application security:</span></span>

-   <span data-ttu-id="75055-106">程式庫應用程式會在用戶端進程安全性權杖下執行，而不是在自己的使用者身分識別下執行。</span><span class="sxs-lookup"><span data-stu-id="75055-106">Library applications run under the client process security token rather than under their own user identity.</span></span> <span data-ttu-id="75055-107">他們擁有的許可權與用戶端的許可權一樣多。</span><span class="sxs-lookup"><span data-stu-id="75055-107">They have only as much privilege as the client has.</span></span>
-   <span data-ttu-id="75055-108">程式庫應用程式不會控制進程層級安全性。</span><span class="sxs-lookup"><span data-stu-id="75055-108">Library applications do not control process-level security.</span></span> <span data-ttu-id="75055-109">系統不會將角色中的任何使用者新增至程式的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="75055-109">No users in roles will be added to the security descriptor for the process.</span></span> <span data-ttu-id="75055-110">程式庫應用程式執行自己的存取檢查的唯一方法是使用元件層級安全性。</span><span class="sxs-lookup"><span data-stu-id="75055-110">The only way for a library application to perform its own access checks is to use component-level security.</span></span> <span data-ttu-id="75055-111"> (查看 [安全性界限](security-boundaries.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="75055-111">(See [Security Boundaries](security-boundaries.md).)</span></span>
-   <span data-ttu-id="75055-112">您可以啟用或停用驗證，將程式庫應用程式設定為參與或不參與主機進程驗證。</span><span class="sxs-lookup"><span data-stu-id="75055-112">Library applications can be configured to either participate or not participate in host process authentication, by enabling or disabling authentication.</span></span> <span data-ttu-id="75055-113"> (參閱 [啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="75055-113">(See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).)</span></span>
-   <span data-ttu-id="75055-114">程式庫應用程式無法設定模擬等級;它們會使用主機進程的。</span><span class="sxs-lookup"><span data-stu-id="75055-114">Library applications cannot set an impersonation level; they use that of the host process.</span></span>

## <a name="using-library-applications-to-limit-application-privilege"></a><span data-ttu-id="75055-115">使用程式庫應用程式來限制應用程式許可權</span><span class="sxs-lookup"><span data-stu-id="75055-115">Using Library Applications to Limit Application Privilege</span></span>

<span data-ttu-id="75055-116">在某些情況下，您可能會想要將應用程式明確設定為程式庫應用程式，使其在裝載進程的身分識別下執行。</span><span class="sxs-lookup"><span data-stu-id="75055-116">In some cases, you may want to configure an application specifically as a library application so that it runs under the identity of the hosting process.</span></span> <span data-ttu-id="75055-117">這麼做基本上會限制應用程式，使其只能存取其用戶端、主機進程可以存取的資源。</span><span class="sxs-lookup"><span data-stu-id="75055-117">Doing so fundamentally limits the application so that it can access only those resources that its client, the host process, can access.</span></span> <span data-ttu-id="75055-118">程式庫應用程式元件在其上執行的執行緒預設會使用進程 token，因此當它們在應用程式外部呼叫或存取資源（例如，以安全描述項保護的檔案）時，它們就會顯示為用戶端。</span><span class="sxs-lookup"><span data-stu-id="75055-118">The threads that the library application components run on will use the process token by default, and therefore when they make calls outside of the application or access resources such as files guarded with a security descriptor, they will appear to be the client.</span></span> <span data-ttu-id="75055-119">對於執行敏感性工作的應用程式而言，這可能是控制其動作範圍的簡易方式。</span><span class="sxs-lookup"><span data-stu-id="75055-119">For applications that perform sensitive work, this may be an easy way to control the scope of their actions.</span></span>

## <a name="effectively-securing-library-applications"></a><span data-ttu-id="75055-120">有效保護程式庫應用程式的安全</span><span class="sxs-lookup"><span data-stu-id="75055-120">Effectively Securing Library Applications</span></span>

<span data-ttu-id="75055-121">針對程式庫應用程式設定以角色為基礎的安全性和驗證時，有一些特殊的考慮，讓它們能如預期般執行。</span><span class="sxs-lookup"><span data-stu-id="75055-121">There are special considerations in configuring role-based security and authentication for library applications so that they perform as expected.</span></span> <span data-ttu-id="75055-122">如需詳細資訊，請參閱設定連結 [庫應用程式的安全性](configuring-security-for-library-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="75055-122">For details, see [Configuring Security for Library Applications](configuring-security-for-library-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75055-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="75055-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75055-124">用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="75055-124">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="75055-125">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="75055-125">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="75055-126">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="75055-126">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="75055-127">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="75055-127">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="75055-128">以角色為基礎的安全性管理</span><span class="sxs-lookup"><span data-stu-id="75055-128">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="75055-129">在 COM + 中使用軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="75055-129">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



