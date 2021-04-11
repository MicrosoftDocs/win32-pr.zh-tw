---
description: 說明存取控制模型的各個部分。
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: 存取控制模型的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3aa6d3547d486c33f4b31cdb5d5de24c7d27cec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848920"
---
# <a name="parts-of-the-access-control-model"></a><span data-ttu-id="03163-103">存取控制模型的元件</span><span class="sxs-lookup"><span data-stu-id="03163-103">Parts of the Access Control Model</span></span>

<span data-ttu-id="03163-104">存取控制模型有兩個基本部分：</span><span class="sxs-lookup"><span data-stu-id="03163-104">There are two basic parts of the access control model:</span></span>

-   <span data-ttu-id="03163-105">[存取權杖](access-tokens.md)，其中包含已登入使用者的相關資訊</span><span class="sxs-lookup"><span data-stu-id="03163-105">[Access tokens](access-tokens.md), which contain information about a logged-on user</span></span>
-   <span data-ttu-id="03163-106">[安全描述項](security-descriptors.md)，其中包含保護安全[物件](securable-objects.md)的安全性資訊</span><span class="sxs-lookup"><span data-stu-id="03163-106">[Security descriptors](security-descriptors.md), which contain the security information that protects a [securable object](securable-objects.md)</span></span>

<span data-ttu-id="03163-107">當使用者登入時，系統會 [*驗證*](/windows/desktop/SecGloss/a-gly) 使用者的帳戶名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="03163-107">When a user logs on, the system [*authenticates*](/windows/desktop/SecGloss/a-gly) the user's account name and password.</span></span> <span data-ttu-id="03163-108">如果登入成功，系統會建立存取權杖。</span><span class="sxs-lookup"><span data-stu-id="03163-108">If the logon is successful, the system creates an access token.</span></span> <span data-ttu-id="03163-109">代表此使用者執行的每個 [*進程*](/windows/desktop/SecGloss/p-gly) 都會有此存取權杖的複本。</span><span class="sxs-lookup"><span data-stu-id="03163-109">Every [*process*](/windows/desktop/SecGloss/p-gly) executed on behalf of this user will have a copy of this access token.</span></span> <span data-ttu-id="03163-110">存取權杖包含 [安全識別碼](security-identifiers.md) ，可識別使用者的帳戶，以及使用者所屬的任何群組帳戶。</span><span class="sxs-lookup"><span data-stu-id="03163-110">The access token contains [security identifiers](security-identifiers.md) that identify the user's account and any group accounts to which the user belongs.</span></span> <span data-ttu-id="03163-111">此權杖也包含使用者或使用者群組所持有的 [許可權](privileges.md) 清單。</span><span class="sxs-lookup"><span data-stu-id="03163-111">The token also contains a list of the [privileges](privileges.md) held by the user or the user's groups.</span></span> <span data-ttu-id="03163-112">當進程嘗試存取安全物件或執行需要許可權的系統管理工作時，系統會使用此權杖來識別相關聯的使用者。</span><span class="sxs-lookup"><span data-stu-id="03163-112">The system uses this token to identify the associated user when a process tries to access a securable object or perform a system administration task that requires privileges.</span></span>

<span data-ttu-id="03163-113">建立安全物件時，系統會為它指派一個 [*安全描述項*](/windows/desktop/SecGloss/s-gly) ，其中包含其建立者所指定的安全性資訊，或者，如果未指定，則為預設的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="03163-113">When a securable object is created, the system assigns it a [*security descriptor*](/windows/desktop/SecGloss/s-gly) that contains security information specified by its creator, or default security information if none is specified.</span></span> <span data-ttu-id="03163-114">應用程式可以使用函式來取得和設定現有物件的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="03163-114">Applications can use functions to retrieve and set the security information for an existing object.</span></span>

<span data-ttu-id="03163-115">安全描述項會識別物件的擁有者，也可以包含下列 [存取控制清單](access-control-lists.md)：</span><span class="sxs-lookup"><span data-stu-id="03163-115">A security descriptor identifies the object's owner and can also contain the following [access control lists](access-control-lists.md):</span></span>

-   <span data-ttu-id="03163-116"> (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) ，識別允許或拒絕存取物件的使用者和群組</span><span class="sxs-lookup"><span data-stu-id="03163-116">A [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that identifies the users and groups allowed or denied access to the object</span></span>
-   <span data-ttu-id="03163-117">[*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (SACL) ，可 [控制系統如何](audit-generation.md)嘗試存取物件。</span><span class="sxs-lookup"><span data-stu-id="03163-117">A [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL) that controls how the system [audits](audit-generation.md) attempts to access the object</span></span>

<span data-ttu-id="03163-118">ACL 包含 (Ace) 的 [存取控制專案](access-control-entries.md) 清單。</span><span class="sxs-lookup"><span data-stu-id="03163-118">An ACL contains a list of [access control entries](access-control-entries.md) (ACEs).</span></span> <span data-ttu-id="03163-119">每個 ACE 都會指定一組 [存取權限](access-rights-and-access-masks.md) ，而且會包含 SID 來識別允許、拒絕或審核許可權的 [信任者](trustees.md) 。</span><span class="sxs-lookup"><span data-stu-id="03163-119">Each ACE specifies a set of [access rights](access-rights-and-access-masks.md) and contains a SID that identifies a [trustee](trustees.md) for whom the rights are allowed, denied, or audited.</span></span> <span data-ttu-id="03163-120">信任者可以是使用者帳戶、群組帳戶或登入 [*會話*](/windows/desktop/SecGloss/l-gly)。</span><span class="sxs-lookup"><span data-stu-id="03163-120">A trustee can be a user account, group account, or [*logon session*](/windows/desktop/SecGloss/l-gly).</span></span>

<span data-ttu-id="03163-121">使用函式來操作安全描述項、Sid 和 Acl 的內容，而不是直接存取它們。</span><span class="sxs-lookup"><span data-stu-id="03163-121">Use functions to manipulate the contents of security descriptors, SIDs, and ACLs rather than accessing them directly.</span></span> <span data-ttu-id="03163-122">這有助於確保這些結構的語法正確，並防止安全性系統的未來增強功能破壞現有的程式碼。</span><span class="sxs-lookup"><span data-stu-id="03163-122">This helps ensure that these structures remain syntactically accurate and prevents future enhancements to the security system from breaking existing code.</span></span>

<span data-ttu-id="03163-123">下列主題提供存取控制模型各部分的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="03163-123">The following topics provide information about parts of the access control model:</span></span>

-   [<span data-ttu-id="03163-124">存取權杖</span><span class="sxs-lookup"><span data-stu-id="03163-124">Access Tokens</span></span>](access-tokens.md)
-   [<span data-ttu-id="03163-125">安全性描述項</span><span class="sxs-lookup"><span data-stu-id="03163-125">Security Descriptors</span></span>](security-descriptors.md)
-   [<span data-ttu-id="03163-126">存取控制清單</span><span class="sxs-lookup"><span data-stu-id="03163-126">Access Control Lists</span></span>](access-control-lists.md)
-   [<span data-ttu-id="03163-127">存取控制專案</span><span class="sxs-lookup"><span data-stu-id="03163-127">Access Control Entries</span></span>](access-control-entries.md)
-   [<span data-ttu-id="03163-128">存取權限和存取遮罩</span><span class="sxs-lookup"><span data-stu-id="03163-128">Access Rights and Access Masks</span></span>](access-rights-and-access-masks.md)
-   [<span data-ttu-id="03163-129">AccessCheck 的運作方式</span><span class="sxs-lookup"><span data-stu-id="03163-129">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
-   [<span data-ttu-id="03163-130">集中式授權原則</span><span class="sxs-lookup"><span data-stu-id="03163-130">Centralized Authorization Policy</span></span>](centralized-authorization-policy.md)
-   [<span data-ttu-id="03163-131">安全識別碼</span><span class="sxs-lookup"><span data-stu-id="03163-131">Security Identifiers</span></span>](security-identifiers.md)

 

 
