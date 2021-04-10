---
description: 驗證是判斷呼叫者實際上是&郵件的程式 \# ; 驗證身分識別宣告的真實性。
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: 用戶端驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd24edf341fc2033807587b01fd37420d781d5f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936374"
---
# <a name="client-authentication"></a><span data-ttu-id="25c8d-103">用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="25c8d-103">Client Authentication</span></span>

<span data-ttu-id="25c8d-104">驗證是一種判斷呼叫者實際上是他們聲稱的程式，也就是驗證身分識別宣告的真實性。</span><span class="sxs-lookup"><span data-stu-id="25c8d-104">Authentication is the process of determining that callers are actually who they say they are—verifying the authenticity of a claim of identity.</span></span> <span data-ttu-id="25c8d-105">一般而言，這可以由伺服器和用戶端來完成，每個都驗證另一個。</span><span class="sxs-lookup"><span data-stu-id="25c8d-105">In general, this can be done by both server and client, each authenticating the other.</span></span> <span data-ttu-id="25c8d-106">但是針對授權用戶端的伺服器應用程式（如同以角色為基礎的安全性）也是很重要的，也就是進行驗證。</span><span class="sxs-lookup"><span data-stu-id="25c8d-106">But it is especially important for a server application that is authorizing clients, as with role-based security, to do authentication as well.</span></span> <span data-ttu-id="25c8d-107">驗證用戶端是有意義的授權原則的先決條件。</span><span class="sxs-lookup"><span data-stu-id="25c8d-107">Authenticating clients is a prerequisite for a meaningful authorization policy.</span></span> <span data-ttu-id="25c8d-108">您可以進行所有您想要的角色檢查，但如果您不知道您正在檢查的用戶端身分識別是否為真，則您的應用程式基本上會依賴「接受」系統。</span><span class="sxs-lookup"><span data-stu-id="25c8d-108">You can do all the role checking you want, but if you don't know for certain that the client identity you are checking is authentic, your application is basically relying on the honor system.</span></span>

<span data-ttu-id="25c8d-109">針對 COM + 應用程式，您可以開啟並設定系統管理的驗證，之後就能以透明的方式在應用程式中運作。</span><span class="sxs-lookup"><span data-stu-id="25c8d-109">For COM+ applications, authentication is something you can turn on and configure administratively, after which it works transparently to the application.</span></span> <span data-ttu-id="25c8d-110">您可以使用 [元件服務] 系統管理工具或系統管理功能，以管理的方式指定驗證層級。</span><span class="sxs-lookup"><span data-stu-id="25c8d-110">You specify an authentication level administratively by using the Component Services administrative tool or the Administrative functions.</span></span> <span data-ttu-id="25c8d-111">如需設定驗證的詳細資訊，請參閱 [設定伺服器應用程式的驗證層級](setting-an-authentication-level-for-a-server-application.md) 及 [啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)層級。</span><span class="sxs-lookup"><span data-stu-id="25c8d-111">For details about setting authentication, see [Setting an Authentication Level for a Server Application](setting-an-authentication-level-for-a-server-application.md) and [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).</span></span>

<span data-ttu-id="25c8d-112">根據應用程式的類型是伺服器或程式庫應用程式，設定驗證表示不同的專案。</span><span class="sxs-lookup"><span data-stu-id="25c8d-112">Setting authentication means different things depending on whether the type of application is a server or library application.</span></span>

## <a name="setting-authentication-for-com-server-applications"></a><span data-ttu-id="25c8d-113">設定 COM + 伺服器應用程式的驗證</span><span class="sxs-lookup"><span data-stu-id="25c8d-113">Setting Authentication for COM+ Server Applications</span></span>

<span data-ttu-id="25c8d-114">若是 COM + 伺服器應用程式，您可以設定驗證層級，以決定當用戶端呼叫應用程式內的元件時，將如何執行驗證。</span><span class="sxs-lookup"><span data-stu-id="25c8d-114">For a COM+ server application, you set an authentication level that determines how authentication will be performed when clients call into components within the application.</span></span> <span data-ttu-id="25c8d-115">您可以從數種驗證層級中選擇，以提供不同程度的安全性，範圍從無驗證到每個封包的加密，以及所有方法呼叫參數。</span><span class="sxs-lookup"><span data-stu-id="25c8d-115">You can choose from several authentication levels that provide varying degrees of security, ranging from no authentication to encryption of every packet and all method call parameters.</span></span> <span data-ttu-id="25c8d-116">如需詳細資訊，請參閱 [設定伺服器應用程式的驗證層級](setting-an-authentication-level-for-a-server-application.md)。</span><span class="sxs-lookup"><span data-stu-id="25c8d-116">For more information, see [Setting an Authentication Level for a Server Application](setting-an-authentication-level-for-a-server-application.md).</span></span>

<span data-ttu-id="25c8d-117">更高的安全性會有一些效能成本，但在設定應用程式時，您應該考慮這一點。</span><span class="sxs-lookup"><span data-stu-id="25c8d-117">Higher security comes with some performance cost, however, which you should take into consideration when configuring your application.</span></span> <span data-ttu-id="25c8d-118">COM + 會在用戶端和伺服器所指定的驗證層級之間進行協調。</span><span class="sxs-lookup"><span data-stu-id="25c8d-118">COM+ will negotiate between the authentication level specified by client and server.</span></span> <span data-ttu-id="25c8d-119">這項協商的執行方式有一個優點，就是讓您能夠從伺服器端自行進行系統管理控制驗證。</span><span class="sxs-lookup"><span data-stu-id="25c8d-119">The way this negotiation is carried out has the benefit of enabling you to administratively control authentication from the server side alone.</span></span> <span data-ttu-id="25c8d-120">如需詳細資訊，請參閱 [驗證層級的協商](negotiation-of-authentication-level.md)。</span><span class="sxs-lookup"><span data-stu-id="25c8d-120">For details, see [Negotiation of Authentication Level](negotiation-of-authentication-level.md).</span></span>

> [!Note]  
> <span data-ttu-id="25c8d-121">您絕對不應該使用 COM + 應用程式中的 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ，以程式設計方式指定驗證層級。</span><span class="sxs-lookup"><span data-stu-id="25c8d-121">You should never specify an authentication level programmatically by using [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) within a COM+ application.</span></span> <span data-ttu-id="25c8d-122">COM + 會為您呼叫 **CoInitializeSecurity** ，而且每個進程只能呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="25c8d-122">COM+ calls **CoInitializeSecurity** for you, and this can be called only once per process.</span></span>

 

<span data-ttu-id="25c8d-123">基礎驗證服務是由 COM 和 Microsoft Windows 提供。</span><span class="sxs-lookup"><span data-stu-id="25c8d-123">The underlying authentication services are provided by COM and Microsoft Windows.</span></span> <span data-ttu-id="25c8d-124">在驗證服務中，協力廠商為使用者提供憑證，證明到使用者身分識別的真實性。</span><span class="sxs-lookup"><span data-stu-id="25c8d-124">In an authentication service, a third party supplies a certificate for a user, attesting to the authenticity of the user's identity.</span></span> <span data-ttu-id="25c8d-125">這項認證與憑證授權單位單位一樣可靠，而且與驅動程式的授權或 passport 一樣，也可以作為認證檔，其相依于簽發者的授權單位。</span><span class="sxs-lookup"><span data-stu-id="25c8d-125">This certification is as credible as the certifying authority, and—in much the same way as a driver's license or a passport serves as a certifying document—it depends on the issuer's authority.</span></span> <span data-ttu-id="25c8d-126">如需有關驗證服務的詳細資訊，請參閱 COM 檔中的 [com 和安全性封裝](/windows/desktop/com/com-and-security-packages) 。</span><span class="sxs-lookup"><span data-stu-id="25c8d-126">For more detailed information about authentication services, see [COM and Security Packages](/windows/desktop/com/com-and-security-packages) in the COM documentation.</span></span>

## <a name="setting-authentication-for-com-library-applications"></a><span data-ttu-id="25c8d-127">設定 COM + 程式庫應用程式的驗證</span><span class="sxs-lookup"><span data-stu-id="25c8d-127">Setting Authentication for COM+ Library Applications</span></span>

<span data-ttu-id="25c8d-128">針對 COM + 程式庫應用程式，您可以啟用或停用驗證，以判斷應用程式是否會受限於裝載進程所執行的驗證。</span><span class="sxs-lookup"><span data-stu-id="25c8d-128">For a COM+ library application, you enable or disable authentication to determine whether the application will be subject to the authentication performed by the hosting process.</span></span> <span data-ttu-id="25c8d-129">雖然 COM + 程式庫應用程式的驗證大多是由裝載進程所控制，但您可以設定程式庫應用程式，使其不會參與驗證。</span><span class="sxs-lookup"><span data-stu-id="25c8d-129">Although authentication for a COM+ library application is largely controlled by the hosting process, you can configure the library application so that it will not participate in authentication.</span></span> <span data-ttu-id="25c8d-130">也就是說，對應用程式的呼叫可以驗證或未經驗證，在後者的情況下，用戶端的「驗證」一律會成功。</span><span class="sxs-lookup"><span data-stu-id="25c8d-130">That is, calls into the application can be authenticated or unauthenticated, and in the latter case, "authentication" of clients always succeeds.</span></span> <span data-ttu-id="25c8d-131">如需詳細資訊，請參閱 [啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)。</span><span class="sxs-lookup"><span data-stu-id="25c8d-131">For more information, see [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).</span></span>

<span data-ttu-id="25c8d-132">此外，您可能會想要或需要在資料庫或某些下游應用程式上驗證用戶端，而在 COM + 應用程式上單獨驗證用戶端可能還不夠。</span><span class="sxs-lookup"><span data-stu-id="25c8d-132">Additionally, you may want or be required to authenticate the client at the database or at some downstream application—authenticating clients at the COM+ application alone might not suffice.</span></span> <span data-ttu-id="25c8d-133">如果是這種情況，您必須模擬用戶端，以便將用戶端的身分識別傳播到下游。</span><span class="sxs-lookup"><span data-stu-id="25c8d-133">If this is the case, you need to impersonate the client so that the client's identity is propagated downstream.</span></span> <span data-ttu-id="25c8d-134">如需模擬的詳細資訊，請參閱 [用戶端模擬和委派](client-impersonation-and-delegation.md)。</span><span class="sxs-lookup"><span data-stu-id="25c8d-134">For detailed information about impersonation, see [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span> <span data-ttu-id="25c8d-135">如需有關決定是否要在資料層進行驗證的問題討論，請參閱 [多層式應用程式安全性](multi-tier-application-security.md)。</span><span class="sxs-lookup"><span data-stu-id="25c8d-135">For a discussion of issues involved in deciding whether to do authentication at the data tier, see [Multi-Tier Application Security](multi-tier-application-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="25c8d-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="25c8d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25c8d-137">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="25c8d-137">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="25c8d-138">程式庫應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="25c8d-138">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="25c8d-139">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="25c8d-139">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="25c8d-140">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="25c8d-140">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="25c8d-141">以角色為基礎的安全性管理</span><span class="sxs-lookup"><span data-stu-id="25c8d-141">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="25c8d-142">在 COM + 中使用軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="25c8d-142">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
