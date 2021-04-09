---
title: 使用 LocalSystem 帳戶做為服務登入帳戶
description: 以 LocalSystem 帳戶執行的其中一項優點是，服務對本機資源的存取權完全不受限制。
ms.assetid: 2bc2e16d-bd25-4ec6-91a2-8d03052df021
ms.tgt_platform: multiple
keywords:
- localsystem 帳戶
- localsystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bec3826984e28e29d3156b784da229f8e53e34e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931873"
---
# <a name="using-the-localsystem-account-as-a-service-logon-account"></a><span data-ttu-id="b9276-105">使用 LocalSystem 帳戶做為服務登入帳戶</span><span class="sxs-lookup"><span data-stu-id="b9276-105">Using the LocalSystem Account as a Service Logon Account</span></span>

<span data-ttu-id="b9276-106">以 LocalSystem 帳戶執行的其中一項優點是，服務對本機資源的存取權完全不受限制。</span><span class="sxs-lookup"><span data-stu-id="b9276-106">One advantage of running under the LocalSystem account is that the service has complete unrestricted access to local resources.</span></span> <span data-ttu-id="b9276-107">這也是 LocalSystem 的缺點，因為 LocalSystem 服務可以採取一些動作來關閉整個系統。</span><span class="sxs-lookup"><span data-stu-id="b9276-107">This is also the disadvantage of LocalSystem because a LocalSystem service can do things that would bring down the entire system.</span></span> <span data-ttu-id="b9276-108">尤其是在網域控制站 () DC 上以 LocalSystem 身分執行的服務，可不受限制地存取 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="b9276-108">In particular, a service running as LocalSystem on a domain controller (DC) has unrestricted access to Active Directory Domain Services.</span></span> <span data-ttu-id="b9276-109">這表示服務中的錯誤或服務的安全性攻擊可能會損毀系統，或者，如果服務是在 DC 上，則會損毀整個商業網路。</span><span class="sxs-lookup"><span data-stu-id="b9276-109">This means that bugs in the service, or security attacks on the service, can damage the system or, if the service is on a DC, damage the entire enterprise network.</span></span>

<span data-ttu-id="b9276-110">基於這些理由，在機密安裝上的網域系統管理員將會注意到允許服務以 LocalSystem 身分執行。</span><span class="sxs-lookup"><span data-stu-id="b9276-110">For these reasons, domain administrators at sensitive installations will be cautious about allowing services to run as LocalSystem.</span></span> <span data-ttu-id="b9276-111">事實上，它們可能會對它有原則，特別是在 Dc 上。</span><span class="sxs-lookup"><span data-stu-id="b9276-111">In fact, they may have policies against it, especially on DCs.</span></span> <span data-ttu-id="b9276-112">如果您的服務必須以 LocalSystem 的身分執行，則您服務的檔應該向網域系統管理員證明，這是授與服務許可權以提高許可權執行的原因。</span><span class="sxs-lookup"><span data-stu-id="b9276-112">If your service must run as LocalSystem, the documentation for your service should justify to domain administrators the reasons for granting the service the right to run at elevated privileges.</span></span> <span data-ttu-id="b9276-113">服務絕對不應該在網域控制站上以 LocalSystem 的身分執行。</span><span class="sxs-lookup"><span data-stu-id="b9276-113">Services should never run as LocalSystem on a domain controller.</span></span> <span data-ttu-id="b9276-114">如需詳細資訊和示範服務或服務安裝程式如何判斷它是否正在網域控制站上執行的程式碼範例，請參閱 [測試是否正在網域控制站上執行](testing-whether-running-on-a-domain-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="b9276-114">For more information and a code example that shows how a service or service installer can determine if it is running on a domain controller, see [Testing Whether Running on a Domain Controller](testing-whether-running-on-a-domain-controller.md).</span></span>

<span data-ttu-id="b9276-115">當服務在屬於網域成員的電腦上以 LocalSystem 帳戶執行時，服務會將任何網路存取權授與電腦帳戶，或電腦帳戶所屬的任何群組。</span><span class="sxs-lookup"><span data-stu-id="b9276-115">When a service runs under the LocalSystem account on a computer that is a domain member, the service has whatever network access is granted to the computer account, or to any groups of which the computer account is a member.</span></span> <span data-ttu-id="b9276-116">請注意，在 Windows 2000 中，網域電腦帳戶是與使用者帳戶類似的服務主體。</span><span class="sxs-lookup"><span data-stu-id="b9276-116">Be aware that in Windows 2000, a domain computer account is a service principal, similar to a user account.</span></span> <span data-ttu-id="b9276-117">這表示電腦帳戶可以位於安全性群組中，而安全描述項中的 ACE 可以授與電腦帳戶的存取權。</span><span class="sxs-lookup"><span data-stu-id="b9276-117">This means that a computer account can be in a security group, and an ACE in a security descriptor can grant access to a computer account.</span></span> <span data-ttu-id="b9276-118">請注意，不建議將電腦帳戶新增至群組，原因有兩個：</span><span class="sxs-lookup"><span data-stu-id="b9276-118">Be aware that adding computer accounts to groups is not recommended for two reasons:</span></span>

-   <span data-ttu-id="b9276-119">如果電腦離開然後重新加入網域，電腦帳戶可能會被刪除並重新建立。</span><span class="sxs-lookup"><span data-stu-id="b9276-119">Computer accounts are subject to deletion and re-creation if the computer leaves and then rejoins the domain.</span></span>
-   <span data-ttu-id="b9276-120">如果您將電腦帳戶新增至群組，則在該電腦上以 LocalSystem 身分執行的所有服務都會被允許該群組的存取權限。</span><span class="sxs-lookup"><span data-stu-id="b9276-120">If you add a computer account to a group, all services running as LocalSystem on that computer are permitted the access rights of the group.</span></span> <span data-ttu-id="b9276-121">這是因為所有 LocalSystem 服務都會共用其主機伺服器的電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="b9276-121">This is because all LocalSystem services share the computer account of their host server.</span></span> <span data-ttu-id="b9276-122">基於這個理由，電腦帳戶不能成為任何網域系統管理員群組的成員，這點特別重要。</span><span class="sxs-lookup"><span data-stu-id="b9276-122">For this reason, it is particularly important that computer accounts not be made members of any domain administrator groups.</span></span>

<span data-ttu-id="b9276-123">電腦帳戶通常有少數許可權，而且不屬於群組。</span><span class="sxs-lookup"><span data-stu-id="b9276-123">Computer accounts typically have few privileges and do not belong to groups.</span></span> <span data-ttu-id="b9276-124">Active Directory Domain Services 中的預設 ACL 保護允許對電腦帳戶進行最基本的存取。</span><span class="sxs-lookup"><span data-stu-id="b9276-124">The default ACL protection in Active Directory Domain Services permits minimal access for computer accounts.</span></span> <span data-ttu-id="b9276-125">因此，在 Dc 以外的電腦上，以 LocalSystem 身分執行的服務只有 Active Directory Domain Services 的存取權。</span><span class="sxs-lookup"><span data-stu-id="b9276-125">Consequently, services running as LocalSystem, on computers other than DCs, have only minimal access to Active Directory Domain Services.</span></span>

<span data-ttu-id="b9276-126">如果您的服務是在 LocalSystem 下執行，您必須在成員伺服器上測試您的服務，以確保您的服務具有足夠的許可權可讀取/寫入 Active Directory 網網域控制站。</span><span class="sxs-lookup"><span data-stu-id="b9276-126">If your service runs under LocalSystem, you must test your service on a member server to ensure that your service has sufficient rights to read/write to Active Directory Domain Controllers.</span></span> <span data-ttu-id="b9276-127">網域控制站不應該是您用來測試服務的唯一 Windows 電腦。</span><span class="sxs-lookup"><span data-stu-id="b9276-127">A domain controller should not be the only Windows computer on which you test your service.</span></span> <span data-ttu-id="b9276-128">請注意，在 Windows 網域控制站上以 LocalSystem 身分執行的服務具有 Active Directory Domain Services 的完整存取權，而成員伺服器則是在擁有較少許可權的電腦帳戶內容中執行。</span><span class="sxs-lookup"><span data-stu-id="b9276-128">Be aware that a service running under LocalSystem on a Windows domain controller has complete access to Active Directory Domain Services and that a member server runs in the context of the computer account which has substantially fewer rights.</span></span>

 

 




