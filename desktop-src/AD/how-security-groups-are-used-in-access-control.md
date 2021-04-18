---
title: 如何在存取控制中使用安全性群組
description: 當使用者或群組基於安全性目的使用時， (SID) 的安全識別碼是使用者或安全性群組的物件識別碼。
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- 如何在存取控制中使用安全性群組
- 存取控制，使用的安全性群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966171"
---
# <a name="how-security-groups-are-used-in-access-control"></a><span data-ttu-id="465b3-105">如何在存取控制中使用安全性群組</span><span class="sxs-lookup"><span data-stu-id="465b3-105">How Security Groups are Used in Access Control</span></span>

<span data-ttu-id="465b3-106">當使用者或群組基於安全性目的使用時， (SID) 的安全識別碼是使用者或安全性群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="465b3-106">The security identifier (SID) is the object identifier of the user or security group when the user or group is used for security purposes.</span></span> <span data-ttu-id="465b3-107">使用者或群組的名稱不會用來做為系統內的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="465b3-107">The name of the user or group is not used as the unique identifier within the system.</span></span> <span data-ttu-id="465b3-108">SID 會儲存在 user objects 和 security group 物件的 **objectSid** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="465b3-108">The SID is stored in the **objectSid** attribute of user objects and security group objects.</span></span> <span data-ttu-id="465b3-109">建立使用者或群組時，Active Directory 伺服器會產生 **objectSid** 。</span><span class="sxs-lookup"><span data-stu-id="465b3-109">The Active Directory server generates the **objectSid** when the user or group is created.</span></span> <span data-ttu-id="465b3-110">系統可確保 Sid 在樹系中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="465b3-110">The system ensures that the SIDs are unique across a forest.</span></span> <span data-ttu-id="465b3-111">請注意， **objectGuid** 是使用者、群組或任何其他目錄物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="465b3-111">Be aware that the **objectGuid** is the unique identifier of a user, group, or any other directory object.</span></span> <span data-ttu-id="465b3-112">如果使用者或群組移至另一個網域，則 SID 會變更; **objectGuid** 維持不變。</span><span class="sxs-lookup"><span data-stu-id="465b3-112">The SID changes if a user or group is moved to another domain; the **objectGuid** remains the same.</span></span>

<span data-ttu-id="465b3-113">當使用者或群組被授與資源的存取權，例如印表機或檔案共用時，會將使用者或群組的 SID 新增至存取控制專案 (ACE) 在資源的任意存取控制清單中定義授與的許可權 (DACL) 。</span><span class="sxs-lookup"><span data-stu-id="465b3-113">When a user or group is given permission to access a resource, such as a printer or a file share, the SID of the user or group is added to the access control entry (ACE) defining the granted permission in the resource's discretionary access control list (DACL).</span></span> <span data-ttu-id="465b3-114">在 Active Directory Domain Services 中，每個物件都有 **nTSecurityDescriptor** 屬性，它會儲存 DACL，以定義該物件的存取權或該物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="465b3-114">In Active Directory Domain Services, each object has an **nTSecurityDescriptor** attribute that stores a DACL defining the access to that particular object or attributes on that object.</span></span> <span data-ttu-id="465b3-115">如需有關在 Active Directory Domain Services 中設定物件之存取控制的詳細資訊，請參閱 [控制 Active Directory Domain Services 中物件的存取權](controlling-access-to-objects-in-active-directory-domain-services.md)。</span><span class="sxs-lookup"><span data-stu-id="465b3-115">For more information about setting access control on objects in Active Directory Domain Services, see [Controlling Access to Objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="465b3-116">當使用者登入 Windows 2000 網域時，作業系統會產生存取權杖。</span><span class="sxs-lookup"><span data-stu-id="465b3-116">When a user logs on to a Windows 2000 domain, the operating system generates an access token.</span></span> <span data-ttu-id="465b3-117">此存取權杖可用來決定使用者可以存取的資源。</span><span class="sxs-lookup"><span data-stu-id="465b3-117">This access token is used to determine which resources the user may access.</span></span> <span data-ttu-id="465b3-118">使用者存取權杖包含下列資料：</span><span class="sxs-lookup"><span data-stu-id="465b3-118">The user access token includes the following data:</span></span>

-   <span data-ttu-id="465b3-119">使用者 SID。</span><span class="sxs-lookup"><span data-stu-id="465b3-119">User SID.</span></span>
-   <span data-ttu-id="465b3-120">使用者為其成員之所有全域和通用安全性群組的 Sid。</span><span class="sxs-lookup"><span data-stu-id="465b3-120">SIDs of all global and universal security groups that the user is a member of.</span></span>
-   <span data-ttu-id="465b3-121">所有嵌套全域和通用安全性群組的 Sid。</span><span class="sxs-lookup"><span data-stu-id="465b3-121">SIDs of all nested global and universal security groups.</span></span>

<span data-ttu-id="465b3-122">代表此使用者執行的每個處理常式都有此存取權杖的複本。</span><span class="sxs-lookup"><span data-stu-id="465b3-122">Every process executed on behalf of this user has a copy of this access token.</span></span>

<span data-ttu-id="465b3-123">當使用者嘗試存取電腦上的資源時，使用者用來存取資源的服務將會根據在使用者登入時建立的存取權杖來建立新的存取權杖來模擬使用者。</span><span class="sxs-lookup"><span data-stu-id="465b3-123">When the user attempts to access resources on a computer, the service through which the user accesses the resource will impersonate the user by creating a new access token based on the access token created at user logon time.</span></span> <span data-ttu-id="465b3-124">這個新的存取權杖也會包含下列 Sid：</span><span class="sxs-lookup"><span data-stu-id="465b3-124">This new access token will also contain the following SIDs:</span></span>

-   <span data-ttu-id="465b3-125">目標網域中使用者所屬的所有網域本機群組的 Sid。</span><span class="sxs-lookup"><span data-stu-id="465b3-125">SIDs for all domain local groups in the target domain that the user is a member of.</span></span>
-   <span data-ttu-id="465b3-126">目的電腦上使用者所屬之所有電腦本機群組的 Sid。</span><span class="sxs-lookup"><span data-stu-id="465b3-126">SIDs for all machine local groups on the target computer that the user is a member of.</span></span>

<span data-ttu-id="465b3-127">服務會使用這個新的存取權杖來評估資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="465b3-127">The service uses this new access token to evaluate access to the resource.</span></span> <span data-ttu-id="465b3-128">如果存取權杖中的 SID 出現在 DACL 中的任何 Ace 中，則服務會為使用者提供這些 Ace 中指定的許可權。</span><span class="sxs-lookup"><span data-stu-id="465b3-128">If a SID in the access token appears in any ACEs in the DACL, the service gives the user the permissions specified in those ACEs.</span></span>

 

 




