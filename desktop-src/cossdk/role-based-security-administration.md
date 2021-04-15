---
description: Role-Based 安全性管理
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Role-Based 安全性管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510671"
---
# <a name="role-based-security-administration"></a><span data-ttu-id="0ce8e-103">Role-Based 安全性管理</span><span class="sxs-lookup"><span data-stu-id="0ce8e-103">Role-Based Security Administration</span></span>

<span data-ttu-id="0ce8e-104">以角色為基礎的安全性是由 COM + 提供的自動服務，可讓您對 COM + 應用程式進行系統管理和強制執行存取控制原則。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-104">Role-based security is an automatic service provided by COM+ that enables you to administratively construct and enforce an access control policy for your COM+ application.</span></span> <span data-ttu-id="0ce8e-105">使用彈性且可擴充的安全性設定模型，以角色為基礎的安全性可提供更大的優勢，而不會在您的元件內強制執行所有安全性，並提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="0ce8e-105">With a flexible and extensible security configuration model, role-based security offers a considerable advantage over enforcing all security within your components and provides the following benefits:</span></span>

-   <span data-ttu-id="0ce8e-106">您可以使用 [元件服務] 系統管理工具或系統管理功能，以系統管理的方式設定安全性。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-106">You can configure security administratively, using either the Component Services administrative tool or the Administrative functions.</span></span>
-   <span data-ttu-id="0ce8e-107">當方法層級的角色保護提供足夠的存取控制時，您不需要在元件中撰寫安全性相關的邏輯。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-107">You don't have to write security-related logic into your components when role protection at the method level provides you with fine enough access control.</span></span>
-   <span data-ttu-id="0ce8e-108">您不需要將安全性納入介面或元件設計中。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-108">You don't have to factor security into interface or component design.</span></span> <span data-ttu-id="0ce8e-109">相反地，您可以依方法逐一設定安全性。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-109">Instead, you can set security on a method-by-method basis.</span></span>
-   <span data-ttu-id="0ce8e-110">您可以將焦點放在您想要強制執行的安全性原則結構，而透過角色，該原則可以明確地表示給部署您應用程式的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-110">You can focus on the structure of the security policy you want to enforce, and through roles, that policy can be clearly expressed to the administrators deploying your application.</span></span>
-   <span data-ttu-id="0ce8e-111">您可以輕鬆地修改安全性原則，以適應不斷演進的應用程式安全性需求。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-111">You can easily modify a security policy to adapt to evolving security requirements for an application.</span></span>
-   <span data-ttu-id="0ce8e-112">如果需要，您可以使用以角色為基礎的安全性做為支援平臺，以程式設計方式建立更細微的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-112">You can build more granular security policies programmatically if you need to, using role-based security as a supporting platform.</span></span>
-   <span data-ttu-id="0ce8e-113">您可以利用以角色為基礎的安全性來進行詳細的審核，因為您可以取得整個上游呼叫鏈的呼叫端安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-113">You can leverage role-based security to do detailed auditing, because you can obtain caller security information for an entire chain of upstream calls.</span></span>

> [!Note]  
> <span data-ttu-id="0ce8e-114">系統應用程式之系統管理員角色中的使用者必須是本機系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-114">Users in the Administrator role for the System Application must be members of the local administrators group.</span></span> <span data-ttu-id="0ce8e-115">此外，從 Windows Server 2003，COM + 系統應用程式的驗證功能包含 EOAC \_ DISABLE AAA 的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-115">Also, as of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="0ce8e-116">此值會在啟動系統應用程式時，在 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 呼叫中使用停用的 (AAA) 啟用。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-116">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="0ce8e-117">將驗證功能設定為 EOAC \_ DISABLE \_ AAA，可讓在特殊許可權帳戶下執行的應用程式 (例如 LocalSystem) ，以協助防止其身分識別用來啟動未受信任的元件。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-117">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

 

<span data-ttu-id="0ce8e-118">請參閱本節中的下列主題，以取得以角色為基礎的安全性如何運作的相關資訊，以及使用它來為應用程式建立安全性原則時應考慮的問題：</span><span class="sxs-lookup"><span data-stu-id="0ce8e-118">See the following topics in this section for information about how role-based security works and issues to consider when using it to construct a security policy for an application:</span></span>

-   [<span data-ttu-id="0ce8e-119">使用角色進行用戶端授權</span><span class="sxs-lookup"><span data-stu-id="0ce8e-119">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
-   [<span data-ttu-id="0ce8e-120">有效設計角色</span><span class="sxs-lookup"><span data-stu-id="0ce8e-120">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
-   [<span data-ttu-id="0ce8e-121">安全性界限</span><span class="sxs-lookup"><span data-stu-id="0ce8e-121">Security Boundaries</span></span>](security-boundaries.md)
-   [<span data-ttu-id="0ce8e-122">安全性呼叫內容資訊</span><span class="sxs-lookup"><span data-stu-id="0ce8e-122">Security Call Context Information</span></span>](security-call-context-information.md)
-   [<span data-ttu-id="0ce8e-123">資訊安全內容屬性</span><span class="sxs-lookup"><span data-stu-id="0ce8e-123">Security Context Property</span></span>](security-context-property.md)

<span data-ttu-id="0ce8e-124">如需有關為應用程式設定以角色為基礎的安全性所需步驟的詳細說明，請參閱設定 [Role-Based 安全性](configuring-role-based-security.md)。</span><span class="sxs-lookup"><span data-stu-id="0ce8e-124">For detailed how-to descriptions of the steps involved in configuring role-based security for an application, see [Configuring Role-Based Security](configuring-role-based-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ce8e-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ce8e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ce8e-126">用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="0ce8e-126">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="0ce8e-127">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="0ce8e-127">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="0ce8e-128">程式庫應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="0ce8e-128">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="0ce8e-129">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="0ce8e-129">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="0ce8e-130">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="0ce8e-130">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="0ce8e-131">在 COM + 中使用軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="0ce8e-131">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
