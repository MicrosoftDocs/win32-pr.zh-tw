---
description: 使用軟體限制原則可讓您的企業更具 agile，因為它提供主動式架構來防止問題，而不是依賴在發生問題之後還原系統的昂貴替代方案的被動架構。 軟體限制原則是隨著 Microsoft Windows XP 的發行而推出，可協助保護系統免于不明且可能有危險的程式碼。 限制原則會提供一種機制，其中只有受信任的程式碼會獲得不受限制的使用者許可權存取權。 未知的程式碼可能會包含與目前安裝的程式衝突的病毒或程式碼，只允許在受限制的環境中執行 (通常稱為沙箱) 不允許存取任何安全性敏感的使用者權限。
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: 在 COM + 中使用軟體限制原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3620aba8cce2859d76ba07c2fa9655dd9036bdbb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468289"
---
# <a name="using-the-software-restriction-policy-in-com"></a><span data-ttu-id="056bd-106">在 COM + 中使用軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="056bd-106">Using the Software Restriction Policy in COM+</span></span>

<span data-ttu-id="056bd-107">使用軟體限制原則可讓您的企業更具 agile，因為它提供主動式架構來防止問題，而不是依賴在發生問題之後還原系統的昂貴替代方案的被動架構。</span><span class="sxs-lookup"><span data-stu-id="056bd-107">Properly using the software restriction policy can make your business more agile because it provides a proactive framework for preventing problems, rather than a reactive framework that relies on the costly alternative of restoring a system after a problem has occurred.</span></span> <span data-ttu-id="056bd-108">軟體限制原則是隨著 Microsoft Windows XP 的發行而推出，可協助保護系統免于不明且可能有危險的程式碼。</span><span class="sxs-lookup"><span data-stu-id="056bd-108">The software restriction policy was introduced with the release of Microsoft Windows XP to help protect systems from unknown and possibly dangerous code.</span></span> <span data-ttu-id="056bd-109">限制原則會提供一種機制，其中只有受信任的程式碼會獲得不受限制的使用者許可權存取權。</span><span class="sxs-lookup"><span data-stu-id="056bd-109">The restriction policy provides a mechanism where only trusted code is given unrestricted access to a user's privileges.</span></span> <span data-ttu-id="056bd-110">未知的程式碼可能會包含與目前安裝的程式衝突的病毒或程式碼，只允許在受限制的環境中執行 (通常稱為 *沙箱*) 不允許存取任何安全性敏感的使用者權限。</span><span class="sxs-lookup"><span data-stu-id="056bd-110">Unknown code, which might contain viruses or code that conflicts with currently installed programs, is allowed to run only in a constrained environment (often called a *sandbox*) where it is disallowed from accessing any security-sensitive user privileges.</span></span>

<span data-ttu-id="056bd-111">軟體限制原則取決於將信任層級指派給可在系統上執行的程式碼。</span><span class="sxs-lookup"><span data-stu-id="056bd-111">The software restriction policy depends on assigning trust levels to the code that can run on a system.</span></span> <span data-ttu-id="056bd-112">目前有兩個信任層級：不受限制且不允許。</span><span class="sxs-lookup"><span data-stu-id="056bd-112">Currently, two trust levels exist: Unrestricted and Disallowed.</span></span> <span data-ttu-id="056bd-113">具有不受限制之信任層級的程式碼會被授與不受限制地存取使用者的許可權，因此此信任層級應只套用至完全信任的程式碼。</span><span class="sxs-lookup"><span data-stu-id="056bd-113">Code that has an Unrestricted trust level is given unrestricted access to the user's privileges, so this trust level should be applied only to fully trusted code.</span></span> <span data-ttu-id="056bd-114">具有不允許信任層級的程式碼不允許存取任何安全性敏感使用者許可權，而且只能在沙箱中執行，以協助防止不受限制的程式碼將不允許的程式碼載入其位址空間中。</span><span class="sxs-lookup"><span data-stu-id="056bd-114">Code with a Disallowed trust level is disallowed from accessing any security-sensitive user privileges and can run only in a sandbox that helps prevent Unrestricted code from loading the Disallowed code into its address space.</span></span>

<span data-ttu-id="056bd-115">設定系統的軟體限制原則是透過 [本機安全性原則] 系統管理工具來完成，而個別 COM + 應用程式的限制原則設定則是以程式設計方式或透過 [元件服務] 系統管理工具來完成。</span><span class="sxs-lookup"><span data-stu-id="056bd-115">Configuring the software restriction policy for a system is done through the Local Security Policy administrative tool, while the restriction policy configuration of individual COM+ applications is done either programmatically or through the Component Services administrative tool.</span></span> <span data-ttu-id="056bd-116">如果未指定 COM + 應用程式的限制原則信任層級，則會使用全系統設定來判斷應用程式的信任層級。</span><span class="sxs-lookup"><span data-stu-id="056bd-116">If the restriction policy trust level is not specified for a COM+ application, the systemwide settings will be used to determine the application's trust level.</span></span> <span data-ttu-id="056bd-117">由於具有不受限制的信任層級的 COM + 應用程式只能載入具有不受限制之信任層級的元件，因此 COM + 限制原則設定必須謹慎地與全系統設定協調：不允許的 COM + 應用程式可以載入具有任何信任層級的元件，但無法存取所有使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="056bd-117">The COM+ restriction policy settings must be carefully coordinated with the systemwide settings because a COM+ application that has an Unrestricted trust level can load only components with an Unrestricted trust level; a Disallowed COM+ application can load components with any trust level but cannot access all of the user's privileges.</span></span>

<span data-ttu-id="056bd-118">除了個別 COM + 應用程式的軟體限制原則信任層級以外，其他兩個屬性會決定如何將限制原則用於所有的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="056bd-118">In addition to the software restriction policy trust levels of individual COM+ applications, two other properties determine how the restriction policy is used for all COM+ applications.</span></span> <span data-ttu-id="056bd-119">如果已啟用 [SRPRunningObjectChecks](/windows/desktop/com/srprunningobjectchecks) ，將會檢查是否有適當的信任層級，來嘗試連接到執行中的物件。</span><span class="sxs-lookup"><span data-stu-id="056bd-119">If [SRPRunningObjectChecks](/windows/desktop/com/srprunningobjectchecks) is enabled, attempts to connect to running objects will be checked for appropriate trust levels.</span></span> <span data-ttu-id="056bd-120">執行中的物件不能有比用戶端物件更嚴格的信任層級。</span><span class="sxs-lookup"><span data-stu-id="056bd-120">The running object cannot have a less stringent trust level than the client object.</span></span> <span data-ttu-id="056bd-121">例如，如果用戶端物件具有不受限制的信任層級，則執行中的物件不能有不允許的信任層級。</span><span class="sxs-lookup"><span data-stu-id="056bd-121">For example, the running object cannot have a Disallowed trust level if the client object has an Unrestricted trust level.</span></span>

<span data-ttu-id="056bd-122">第二個屬性會決定軟體限制原則如何處理啟動為啟動的連接。</span><span class="sxs-lookup"><span data-stu-id="056bd-122">The second property determines how the software restriction policy handles activate-as-activator connections.</span></span> <span data-ttu-id="056bd-123">如果啟用 [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) ，則會將為伺服器物件設定的信任層級與用戶端物件的信任層級進行比較，並使用更嚴格的信任層級來執行伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="056bd-123">If [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) is enabled, the trust level that is configured for the server object is compared with the trust level of the client object and the more stringent trust level will be used to run the server object.</span></span> <span data-ttu-id="056bd-124">如果未啟用 SRPActivateAsActivatorChecks，不論設定的信任層級為何，伺服器物件都會以用戶端物件的信任層級執行。</span><span class="sxs-lookup"><span data-stu-id="056bd-124">If SRPActivateAsActivatorChecks is not enabled, the server object will run with the trust level of the client object regardless of the trust level with which it was configured.</span></span> <span data-ttu-id="056bd-125">預設會啟用 SRPRunningObjectChecks 和 SRPActivateAsActivatorChecks。</span><span class="sxs-lookup"><span data-stu-id="056bd-125">By default, both SRPRunningObjectChecks and SRPActivateAsActivatorChecks are enabled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="056bd-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="056bd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="056bd-127">用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="056bd-127">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="056bd-128">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="056bd-128">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="056bd-129">設定軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="056bd-129">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="056bd-130">程式庫應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="056bd-130">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="056bd-131">多層式應用程式安全性</span><span class="sxs-lookup"><span data-stu-id="056bd-131">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="056bd-132">程式設計元件安全性</span><span class="sxs-lookup"><span data-stu-id="056bd-132">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="056bd-133">以角色為基礎的安全性管理</span><span class="sxs-lookup"><span data-stu-id="056bd-133">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> </dl>

 

 
