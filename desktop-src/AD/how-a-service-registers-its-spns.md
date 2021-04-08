---
title: 服務如何註冊其 Spn
description: 必須先在服務實例將用來登入的使用者或電腦帳戶上註冊 SPN，用戶端才能使用 SPN 來驗證服務的實例。
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- 服務如何註冊其 Spn AD
- 服務主體名稱 AD，服務如何註冊其 Spn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74410be3a024fc6accd1d8394e2ba8335be9f550
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839311"
---
# <a name="how-a-service-registers-its-spns"></a><span data-ttu-id="42fd1-105">服務如何註冊其 Spn</span><span class="sxs-lookup"><span data-stu-id="42fd1-105">How a Service Registers its SPNs</span></span>

<span data-ttu-id="42fd1-106">必須先在服務實例將用來登入的使用者或電腦帳戶上註冊 SPN，用戶端才能使用 SPN 來驗證服務的實例。</span><span class="sxs-lookup"><span data-stu-id="42fd1-106">Before a client can use an SPN to authenticate an instance of a service, the SPN must be registered on the user or computer account that the service instance will use to log on.</span></span> <span data-ttu-id="42fd1-107">通常，SPN 註冊是由以網域系統管理員許可權執行的服務安裝程式所完成。</span><span class="sxs-lookup"><span data-stu-id="42fd1-107">Typically, SPN registration is done by a service installation program running with domain administrator privileges.</span></span>

<span data-ttu-id="42fd1-108">在主機電腦上安裝服務實例的服務安裝程式通常會執行下列程式。</span><span class="sxs-lookup"><span data-stu-id="42fd1-108">The service installer that installs a service instance on a host computer typically performs the following procedure.</span></span>

<span data-ttu-id="42fd1-109">**註冊服務實例的 Spn**</span><span class="sxs-lookup"><span data-stu-id="42fd1-109">**To register SPNs for a service instance**</span></span>

1.  <span data-ttu-id="42fd1-110">呼叫 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 函數，為服務實例建立一個或多個唯一的 spn。</span><span class="sxs-lookup"><span data-stu-id="42fd1-110">Call the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to create one or more unique SPNs for the service instance.</span></span> <span data-ttu-id="42fd1-111">如需詳細資訊，請參閱 [唯一 spn 的名稱格式](name-formats-for-unique-spns.md)。</span><span class="sxs-lookup"><span data-stu-id="42fd1-111">For more information, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>
2.  <span data-ttu-id="42fd1-112">呼叫 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 函數，以在服務的登入帳戶上註冊名稱。</span><span class="sxs-lookup"><span data-stu-id="42fd1-112">Call the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function to register the names on the service's logon account.</span></span>

<span data-ttu-id="42fd1-113">[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 會將 spn 註冊為目錄中使用者或電腦帳戶物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="42fd1-113">[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) registers SPNs as a property of a user or computer account object in the directory.</span></span> <span data-ttu-id="42fd1-114">**使用者** 和 **電腦** 物件具有 **servicePrincipalName** 屬性，它是用來儲存所有與使用者或電腦帳戶相關聯之 spn 的多重值屬性。</span><span class="sxs-lookup"><span data-stu-id="42fd1-114">**user** and **computer** objects have a **servicePrincipalName** attribute, which is a multi-valued attribute for storing all the SPNs associated with a user or computer account.</span></span> <span data-ttu-id="42fd1-115">如果服務是在使用者帳戶下執行，則 Spn 會儲存在該帳戶的 **servicePrincipalName** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="42fd1-115">If the service runs under a user account, the SPNs are stored in the **servicePrincipalName** attribute of that account.</span></span> <span data-ttu-id="42fd1-116">如果服務是在 LocalSystem 帳戶中執行，則 Spn 會儲存在服務主機電腦帳戶的 **servicePrincipalName** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="42fd1-116">If the service runs in the LocalSystem account, the SPNs are stored in the **servicePrincipalName** attribute of the account of the service's host computer.</span></span> <span data-ttu-id="42fd1-117">**DsWriteAccountSpn** 呼叫端必須指定用來儲存 spn 之帳戶物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="42fd1-117">The **DsWriteAccountSpn** caller must specify the distinguished name of the account object under which the SPNs are stored.</span></span>

<span data-ttu-id="42fd1-118">為了確保登錄的 Spn 是安全的，無法直接寫入 **servicePrincipalName** 屬性;它只能透過呼叫 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)寫入。</span><span class="sxs-lookup"><span data-stu-id="42fd1-118">To ensure that registered SPNs are secure, the **servicePrincipalName** attribute cannot be written directly; it can only be written by calling [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna).</span></span> <span data-ttu-id="42fd1-119">呼叫端必須具有目標帳戶之 **servicePrincipalName** 屬性的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="42fd1-119">The caller must have write-access to the **servicePrincipalName** attribute of the target account.</span></span> <span data-ttu-id="42fd1-120">一般而言，寫入權限預設只會授與網域系統管理員。</span><span class="sxs-lookup"><span data-stu-id="42fd1-120">Typically, write access is granted by default only to domain administrators.</span></span> <span data-ttu-id="42fd1-121">不過，有一個特殊情況，即系統允許在 LocalSystem 帳戶下執行的服務，在服務主機的電腦帳戶上註冊自己的 Spn。</span><span class="sxs-lookup"><span data-stu-id="42fd1-121">However, there is a special case in which the system allows a service running under the LocalSystem account to register its own SPNs on the computer account of the service's host.</span></span> <span data-ttu-id="42fd1-122">在此情況下，所寫入的 SPN 必須有 " <service class> / <host> " 和 "host" 格式，而且 &lt; &gt; 必須是本機電腦的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="42fd1-122">In this case, the SPN being written must have the form "<service class>/<host>" and "&lt;host&gt;" must be the DNS name of the local computer.</span></span>

<span data-ttu-id="42fd1-123">[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 也可以移除帳戶中的 spn。</span><span class="sxs-lookup"><span data-stu-id="42fd1-123">[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) can also remove SPNs from an account.</span></span> <span data-ttu-id="42fd1-124">Operation 參數會指出是否要將 Spn 新增至帳戶、從帳戶移除，或用來完全取代帳戶的所有目前 Spn。</span><span class="sxs-lookup"><span data-stu-id="42fd1-124">An operation parameter indicates whether the SPNs are to be added to the account, removed from the account, or used to completely replace all current SPNs for the account.</span></span> <span data-ttu-id="42fd1-125">卸載服務實例時，請移除任何針對該實例註冊的 Spn。</span><span class="sxs-lookup"><span data-stu-id="42fd1-125">When a service instance is uninstalled, remove any SPNs registered for that instance.</span></span>

<span data-ttu-id="42fd1-126">如需註冊或取消註冊服務 Spn 的詳細資訊和程式碼範例，請參閱 [註冊服務的 spn](registering-the-spns-for-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="42fd1-126">For more information and a code example that registers or unregisters a service's SPNs, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

<span data-ttu-id="42fd1-127">使用簡單 SPN 格式 "" 的主機服務 <service class> / <host> ，可以選擇使用 [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna)函式，這兩個方法都會建立並註冊服務實例的 spn。</span><span class="sxs-lookup"><span data-stu-id="42fd1-127">Host-based services that use the simple SPN format "<service class>/<host>", have the option of using the [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) function, which both creates and registers SPNs for a service instance.</span></span> <span data-ttu-id="42fd1-128">**DsServerRegisterSpn** 是呼叫 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 和 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)的 helper 函數。</span><span class="sxs-lookup"><span data-stu-id="42fd1-128">**DsServerRegisterSpn** is a helper function that calls [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) and [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna).</span></span>

<span data-ttu-id="42fd1-129">如需詳細資訊，請參閱 [服務登入帳戶](service-logon-accounts.md)。</span><span class="sxs-lookup"><span data-stu-id="42fd1-129">For more information, see [Service Logon Accounts](service-logon-accounts.md).</span></span>

 

 




