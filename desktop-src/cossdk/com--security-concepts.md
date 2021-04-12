---
description: COM + 提供數種安全性功能，可用來協助保護您的 COM + 應用程式，範圍從您設定的服務，到您可以在程式碼中呼叫的 Api。
ms.assetid: 686fb391-d337-41b4-bb51-b70f27a0c300
title: COM + 安全性概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca5126f4b715f84c2b8801c8ec1adc29b3cbb83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025996"
---
# <a name="com-security-concepts"></a><span data-ttu-id="35052-103">COM + 安全性概念</span><span class="sxs-lookup"><span data-stu-id="35052-103">COM+ Security Concepts</span></span>

<span data-ttu-id="35052-104">COM + 提供數種安全性功能，可用來協助保護您的 COM + 應用程式，範圍從您設定的服務，到您可以在程式碼中呼叫的 Api。</span><span class="sxs-lookup"><span data-stu-id="35052-104">COM+ provides several security features that you can use to help protect your COM+ applications, ranging from services you configure administratively to APIs you can call within code.</span></span>

<span data-ttu-id="35052-105">可能的話，針對 COM + 應用程式，最好使用自動安全性，例如宣告式角色型安全性和驗證，而不是在元件內設定安全性。</span><span class="sxs-lookup"><span data-stu-id="35052-105">Whenever possible, for COM+ applications, it is better to use automatic security, such as declarative role-based security and authentication, rather than configuring security within components.</span></span> <span data-ttu-id="35052-106">使用自動安全性可讓您更輕鬆地撰寫和維護元件、更輕鬆地設計整個應用程式的安全性，而且因為它是以系統管理員的方式設定，所以更容易修改應用程式的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="35052-106">Using automatic security makes it easier to write and maintain components, easier to design security across an entire application, and, because it is configured administratively, easier to modify an application's security policy.</span></span> <span data-ttu-id="35052-107">這些自動安全性服務可讓您將所有與安全性相關的功能留給您的元件。</span><span class="sxs-lookup"><span data-stu-id="35052-107">These automatic security services make it possible for you to leave all security-related functionality out of your components.</span></span> <span data-ttu-id="35052-108">當您可以開啟並適當地設定服務時，COM + 將會處理強制執行您所指定安全性原則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="35052-108">When you can turn on the services and configure them appropriately, COM+ will handle the details of enforcing the security policy you specify.</span></span>

<span data-ttu-id="35052-109">不過，當 COM + 中的自動安全性服務未精確地達成您需要的功能時，您可以擴充這些服務，並在 COM + 所提供的自動安全性平臺上進行擴充。</span><span class="sxs-lookup"><span data-stu-id="35052-109">However, when the automatic security services in COM+ don't do precisely what you need them to do, you can extend them, building on the automatic security platform provided by COM+.</span></span> <span data-ttu-id="35052-110">如果您選擇不使用自動安全性，或您想要使用它，但需要根據您的應用程式的安全性需求來建立它，您可以透過程式設計方式設定安全性的下列選項：</span><span class="sxs-lookup"><span data-stu-id="35052-110">In cases where you choose not to use automatic security or where you want to use it but need to build on it to suit your application's security requirements, you have the following options for configuring security programmatically:</span></span>

-   <span data-ttu-id="35052-111">以程式設計的角色為基礎的安全性，例如，當您的應用程式啟用以角色為基礎的安全性時，可使用的角色檢查。</span><span class="sxs-lookup"><span data-stu-id="35052-111">Programmatic role-based security—for example, role checking, which is available when role-based security is enabled for your application.</span></span>
-   <span data-ttu-id="35052-112">模擬—適用于當您想要使用用戶端的身分識別來存取受保護的資源時。</span><span class="sxs-lookup"><span data-stu-id="35052-112">Impersonation—for when you want to use a client's identity to access a protected resource.</span></span>
-   <span data-ttu-id="35052-113">以安全性呼叫內容資訊為基礎的審核功能，也可在啟用角色安全性時使用。</span><span class="sxs-lookup"><span data-stu-id="35052-113">Auditing features based on security call context information—also available when role-based security is enabled.</span></span>

<span data-ttu-id="35052-114">您使用哪些機制來協助保護指定的應用程式，將取決於該應用程式的特定需求。</span><span class="sxs-lookup"><span data-stu-id="35052-114">Which mechanisms you use to help protect a given application will depend on the particular requirements of that application.</span></span> <span data-ttu-id="35052-115">某些安全性選擇可能會影響您撰寫元件的方式，有些則會大幅影響應用程式的設計。</span><span class="sxs-lookup"><span data-stu-id="35052-115">Some security choices can affect how you write components, and some can significantly affect the application's design.</span></span> <span data-ttu-id="35052-116">在您決定如何為應用程式實施安全性策略之前，您應該先考慮其整體設計內容中的安全性需求，包括效能需求、資料存取、實體設計，以及選擇最適合的安全性功能組合。</span><span class="sxs-lookup"><span data-stu-id="35052-116">Before you make any decisions about how to implement a security strategy for an application, you should consider its security requirements in the context of its overall design—performance requirements, data access, physical design—and choose the most suitable combination of security features.</span></span> <span data-ttu-id="35052-117">如需有關如何執行程式設計安全性的詳細資訊，請參閱程式 [設計元件安全性](programmatic-component-security.md)。</span><span class="sxs-lookup"><span data-stu-id="35052-117">For more information about implementing programmatic security, see [Programmatic Component Security](programmatic-component-security.md).</span></span>

<span data-ttu-id="35052-118">您可以在這裡提供 COM + 安全性類別、功能和問題的簡短說明，以及本節中的主題連結，提供每個重要領域的詳細討論。</span><span class="sxs-lookup"><span data-stu-id="35052-118">Brief descriptions of COM+ security categories, features, and issues are provided here, with links to topics in this section that provide a detailed discussion of each of the important areas.</span></span>

> [!Note]  
> <span data-ttu-id="35052-119">雖然本節未討論過，但是佇列元件也會有特定的問題，這些問題與它們可用的安全性功能有關。</span><span class="sxs-lookup"><span data-stu-id="35052-119">Although not discussed in this section, queued components also have particular issues relating to what security features are available to them.</span></span> <span data-ttu-id="35052-120">如需詳細資訊，請參閱已 [排入佇列的元件安全性](queued-components-security.md) 和 [開發佇列元件](developing-queued-components.md)。</span><span class="sxs-lookup"><span data-stu-id="35052-120">For details, see [Queued Components Security](queued-components-security.md) and [Developing Queued Components](developing-queued-components.md).</span></span>

 

## <a name="role-based-security"></a><span data-ttu-id="35052-121">以角色為基礎的安全性</span><span class="sxs-lookup"><span data-stu-id="35052-121">Role-Based Security</span></span>

<span data-ttu-id="35052-122">以角色為基礎的安全性是 COM + 應用程式安全性的核心功能。</span><span class="sxs-lookup"><span data-stu-id="35052-122">Role-based security is the central feature of COM+ application security.</span></span> <span data-ttu-id="35052-123">您可以使用角色來管理應用程式的授權原則，如有必要，請選擇向下 (到方法層級，) 哪些使用者可以存取哪些資源。</span><span class="sxs-lookup"><span data-stu-id="35052-123">Using roles, you can administratively construct an authorization policy for an application, choosing (down to the method level, if necessary) which users can access which resources.</span></span> <span data-ttu-id="35052-124">此外，如果您的應用程式需要更細微的存取控制，角色就會提供在程式碼中強制執行安全性檢查的架構。</span><span class="sxs-lookup"><span data-stu-id="35052-124">Additionally, roles provide a framework for enforcing security-checking within code if your application requires finer-grained access control.</span></span>

<span data-ttu-id="35052-125">以角色為基礎的安全性建基於一般機制，可讓您在對您的元件發出呼叫的鏈中，取得有關所有上游呼叫端的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="35052-125">Role-based security is built on a general mechanism that enables you to retrieve security information regarding all upstream callers in the chain of calls to your component.</span></span> <span data-ttu-id="35052-126">如果您想要進行詳細的審核和記錄，這項功能特別有用。</span><span class="sxs-lookup"><span data-stu-id="35052-126">This facility is useful particularly if you wish to do detailed auditing and logging.</span></span> <span data-ttu-id="35052-127">如需 COM + 所提供之審核功能的描述，請參閱 [存取安全性呼叫內容資訊](accessing-security-call-context-information.md)。</span><span class="sxs-lookup"><span data-stu-id="35052-127">For a description of the auditing features provided by COM+, see [Accessing Security Call Context Information](accessing-security-call-context-information.md).</span></span>

<span data-ttu-id="35052-128">如需使用時應考慮以角色為基礎的安全性和管理問題的說明，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。</span><span class="sxs-lookup"><span data-stu-id="35052-128">For a description of role-based security and administration issues that you should consider when using it, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="client-authentication"></a><span data-ttu-id="35052-129">用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="35052-129">Client Authentication</span></span>

<span data-ttu-id="35052-130">在授權用戶端能夠存取資源之前，您必須先確信它們是誰。</span><span class="sxs-lookup"><span data-stu-id="35052-130">Before you can authorize clients to be able to access resources, you must be confident that they are who they say they are.</span></span> <span data-ttu-id="35052-131">為了啟用此身分識別驗證，COM + 會提供驗證服務。</span><span class="sxs-lookup"><span data-stu-id="35052-131">To enable this identity verification, COM+ provides authentication services.</span></span> <span data-ttu-id="35052-132">雖然這些服務實際上是由 COM 和 Microsoft Windows 提供更基本的層級，但 COM + 應用程式可讓您以系統管理的方式開啟驗證服務，使其在應用程式的透明範圍中運作。</span><span class="sxs-lookup"><span data-stu-id="35052-132">While these services are actually provided at a more fundamental level by COM and Microsoft Windows, a COM+ application lets you simply turn on the authentication service administratively so that it works under the covers, transparent to the application.</span></span> <span data-ttu-id="35052-133">如需驗證服務的描述，請參閱 [用戶端驗證](client-authentication.md)。</span><span class="sxs-lookup"><span data-stu-id="35052-133">For a description of authentication services, see [Client Authentication](client-authentication.md).</span></span>

## <a name="client-impersonation-and-delegation"></a><span data-ttu-id="35052-134">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="35052-134">Client Impersonation and Delegation</span></span>

<span data-ttu-id="35052-135">在某些情況下，您的應用程式需要使用用戶端的身分識別來代表用戶端執行工作，例如，存取即將驗證原始用戶端的資料庫時。</span><span class="sxs-lookup"><span data-stu-id="35052-135">In some cases, your application needs to do work on behalf of a client using the client's identity—for example, when accessing a database that is going to authenticate the original client.</span></span> <span data-ttu-id="35052-136">這需要您的應用程式模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="35052-136">This requires your application to impersonate the client.</span></span> <span data-ttu-id="35052-137">COM + 提供的工具可啟用各種層級的模擬。</span><span class="sxs-lookup"><span data-stu-id="35052-137">COM+ provides facilities to enable various levels of impersonation.</span></span> <span data-ttu-id="35052-138">模擬是以系統管理員的方式設定，但您也必須使用應用程式元件的程式碼來提供模擬支援。</span><span class="sxs-lookup"><span data-stu-id="35052-138">Impersonation is configured administratively, but you also must provide support for impersonation with the code of your application's components.</span></span> <span data-ttu-id="35052-139">如需模擬和其使用相關問題的說明，請參閱 [用戶端模擬和委派](client-impersonation-and-delegation.md)。</span><span class="sxs-lookup"><span data-stu-id="35052-139">For a description of impersonation and issues concerning its use, see [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span>

## <a name="using-the-software-restriction-policy-in-com"></a><span data-ttu-id="35052-140">在 COM + 中使用軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="35052-140">Using the Software Restriction Policy in COM+</span></span>

<span data-ttu-id="35052-141">軟體限制原則可讓您在受限的環境中執行不受信任的程式碼，因此可能會造成有害的程式碼，使其無法誤用使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="35052-141">A software restriction policy provides a way to run untrusted, and therefore potentially harmful, code in a constrained environment so that it cannot misuse the privileges of the user.</span></span> <span data-ttu-id="35052-142">這樣做的方法是將信任層級指派給使用者可以執行的檔案。</span><span class="sxs-lookup"><span data-stu-id="35052-142">It does this by assigning trust levels to files that the user can run.</span></span> <span data-ttu-id="35052-143">例如，某些系統檔案可以是完全受信任的，且不受限制地存取使用者的許可權，而從網際網路下載的檔案可能完全不受信任，因此只允許在受限制的環境中執行，而不允許使用任何安全性敏感的使用者權限。</span><span class="sxs-lookup"><span data-stu-id="35052-143">For example, certain system files can be fully trusted and given unrestricted access to the privileges of the user, while a file that was downloaded from the Internet might be completely untrusted and therefore allowed to run only in a restricted environment where it is disallowed from using any security-sensitive user privileges.</span></span>

<span data-ttu-id="35052-144">全系統軟體限制原則是透過「本機安全性原則」系統管理工具來控制，讓系統管理員可以設定個別檔案的信任層級。</span><span class="sxs-lookup"><span data-stu-id="35052-144">The systemwide software restriction policy is controlled through the Local Security Policy administrative tool, which enables administrators to configure trust levels for individual files.</span></span> <span data-ttu-id="35052-145">但是，所有 COM + 伺服器應用程式都是在 dllhost.exe 檔案中執行。</span><span class="sxs-lookup"><span data-stu-id="35052-145">However, all COM+ server applications run in the dllhost.exe file.</span></span> <span data-ttu-id="35052-146">因此，COM + 會提供一種方法來指定每個伺服器應用程式的軟體限制原則，讓它們不需要相依于 dllhost.exe 檔案的限制原則。</span><span class="sxs-lookup"><span data-stu-id="35052-146">Therefore COM+ provides a way to specify the software restriction policy for each server application so that they do not need to depend on the restriction policy of the dllhost.exe file.</span></span> <span data-ttu-id="35052-147">如需有關如何在 COM + 中使用軟體限制原則的討論，請參閱 [在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)。</span><span class="sxs-lookup"><span data-stu-id="35052-147">For a discussion concerning how to use the software restriction policy in COM+, see [Using the Software Restriction Policy in COM+](using-the-software-restriction-policy-in-com-.md).</span></span>

## <a name="library-application-security"></a><span data-ttu-id="35052-148">程式庫應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="35052-148">Library Application Security</span></span>

<span data-ttu-id="35052-149">程式庫應用程式具有特殊的安全性考慮。</span><span class="sxs-lookup"><span data-stu-id="35052-149">Library applications have special security considerations.</span></span> <span data-ttu-id="35052-150">因為這些應用程式是在用戶端的進程中執行，所以會受到裝載進程強制執行的安全性影響，同時無法控制進程層級安全性。</span><span class="sxs-lookup"><span data-stu-id="35052-150">Because these applications run in the client's process, they are affected by the security enforced by the hosting process while unable to control process-level security.</span></span> <span data-ttu-id="35052-151">如需針對程式庫應用程式考慮因素的說明，請參閱連結 [庫應用程式安全性](library-application-security.md)。</span><span class="sxs-lookup"><span data-stu-id="35052-151">For a description of factors to consider for library applications, see [Library Application Security](library-application-security.md).</span></span>

## <a name="multi-tier-application-security"></a><span data-ttu-id="35052-152">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="35052-152">Multi-Tier Application Security</span></span>

<span data-ttu-id="35052-153">COM + 應用程式通常是中介層應用程式;也就是說，它們會在用戶端與後端資源（例如資料庫）之間移動資訊。</span><span class="sxs-lookup"><span data-stu-id="35052-153">COM+ applications are typically middle-tier applications; that is, they move information between clients and back-end resources such as databases.</span></span> <span data-ttu-id="35052-154">難以決定應如何強制執行安全性以及什麼程度。</span><span class="sxs-lookup"><span data-stu-id="35052-154">Difficult choices can be involved in determining where security should be enforced and to what degree.</span></span> <span data-ttu-id="35052-155">安全性本質上牽涉到效能取捨。</span><span class="sxs-lookup"><span data-stu-id="35052-155">Security inherently involves performance trade-offs.</span></span> <span data-ttu-id="35052-156">當您必須在資料層和仲介層強制執行安全性檢查時，其中一些最嚴重的情況會發生。</span><span class="sxs-lookup"><span data-stu-id="35052-156">Some of the most severe of these occur when you must enforce security checking at both the data tier and the middle-tier.</span></span> <span data-ttu-id="35052-157">如需考慮問題的討論，請參閱 [多層式應用程式安全性](multi-tier-application-security.md)。</span><span class="sxs-lookup"><span data-stu-id="35052-157">For a discussion of issues to consider, see [Multi-Tier Application Security](multi-tier-application-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="35052-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="35052-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35052-159">用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="35052-159">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="35052-160">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="35052-160">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="35052-161">COM + 安全性工作</span><span class="sxs-lookup"><span data-stu-id="35052-161">COM+ Security Tasks</span></span>](com--security-tasks.md)
</dt> <dt>

[<span data-ttu-id="35052-162">程式庫應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="35052-162">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="35052-163">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="35052-163">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="35052-164">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="35052-164">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="35052-165">以角色為基礎的安全性管理</span><span class="sxs-lookup"><span data-stu-id="35052-165">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="35052-166">在 COM + 中使用軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="35052-166">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



