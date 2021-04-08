---
title: 管理使用者
description: 系統會建立使用者帳戶，並將其儲存為 Active Directory Domain Services 中的物件。
ms.assetid: 57c83e4d-2d9f-4f22-97e2-27e2d277f014
ms.tgt_platform: multiple
keywords:
- Active Directory，使用管理使用者
- 使用者廣告
- 使用者 AD，管理使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1105132c6836e108a416331b2f4a6ad666c03d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839296"
---
# <a name="managing-users"></a><span data-ttu-id="fb5c1-106">管理使用者</span><span class="sxs-lookup"><span data-stu-id="fb5c1-106">Managing Users</span></span>

<span data-ttu-id="fb5c1-107">系統會建立使用者帳戶，並將其儲存為 Active Directory Domain Services 中的物件。</span><span class="sxs-lookup"><span data-stu-id="fb5c1-107">User accounts are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="fb5c1-108">這些使用者物件代表使用者和電腦。</span><span class="sxs-lookup"><span data-stu-id="fb5c1-108">These user objects represent users and computers.</span></span> <span data-ttu-id="fb5c1-109">本節定義使用者是什麼以及如何使用它們，並說明如何以程式設計方式管理 Active Directory Domain Services 中的使用者。</span><span class="sxs-lookup"><span data-stu-id="fb5c1-109">This section defines what users are and how they are used, and explains how to programmatically manage users in Active Directory Domain Services.</span></span> <span data-ttu-id="fb5c1-110">本節將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="fb5c1-110">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="fb5c1-111">Active Directory Domain Services 中的使用者</span><span class="sxs-lookup"><span data-stu-id="fb5c1-111">Users in Active Directory Domain Services</span></span>](users-in-active-directory-domain-services.md)
-   [<span data-ttu-id="fb5c1-112">安全性主體</span><span class="sxs-lookup"><span data-stu-id="fb5c1-112">Security Principals</span></span>](security-principals.md)
-   [<span data-ttu-id="fb5c1-113">什麼是使用者？</span><span class="sxs-lookup"><span data-stu-id="fb5c1-113">What is a User?</span></span>](what-is-a-user.md)
-   [<span data-ttu-id="fb5c1-114">系結至 Users 容器的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="fb5c1-114">Example Code for Binding to the Users Container</span></span>](example-code-for-binding-to-the-users-container.md)
-   [<span data-ttu-id="fb5c1-115">User 物件屬性</span><span class="sxs-lookup"><span data-stu-id="fb5c1-115">User Object Attributes</span></span>](user-object-attributes.md)
-   [<span data-ttu-id="fb5c1-116">建立使用者</span><span class="sxs-lookup"><span data-stu-id="fb5c1-116">Creating a User</span></span>](creating-a-user.md)
-   <span data-ttu-id="fb5c1-117">刪除使用者。</span><span class="sxs-lookup"><span data-stu-id="fb5c1-117">Deleting a user.</span></span> <span data-ttu-id="fb5c1-118">使用者會在與 Active Directory Domain Services 中的任何其他物件相同的情況中刪除。</span><span class="sxs-lookup"><span data-stu-id="fb5c1-118">A user is deleted in the same was as any other object in Active Directory Domain Services.</span></span> <span data-ttu-id="fb5c1-119">如需有關刪除物件的詳細資訊，請參閱 [在 Active Directory Domain Services 中建立和刪除物件](creating-and-deleting-objects-in-active-directory-domain-services.md)。</span><span class="sxs-lookup"><span data-stu-id="fb5c1-119">For more information about deleting objects, see [Creating and Deleting Objects in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span></span>
-   [<span data-ttu-id="fb5c1-120">列舉使用者</span><span class="sxs-lookup"><span data-stu-id="fb5c1-120">Enumerating Users</span></span>](enumerating-users.md)
-   [<span data-ttu-id="fb5c1-121">查詢使用者</span><span class="sxs-lookup"><span data-stu-id="fb5c1-121">Querying for Users</span></span>](querying-for-users.md)
-   <span data-ttu-id="fb5c1-122">移動使用者。</span><span class="sxs-lookup"><span data-stu-id="fb5c1-122">Moving users.</span></span> <span data-ttu-id="fb5c1-123">使用者與任何其他 Active Directory 物件的移動方式相同。</span><span class="sxs-lookup"><span data-stu-id="fb5c1-123">A user is moved in the same was as any other Active Directory object.</span></span> <span data-ttu-id="fb5c1-124">如需移動 Active Directory 物件的詳細資訊，請參閱 [移動物件](moving-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="fb5c1-124">For more information about moving Active Directory objects, see [Moving Objects](moving-objects.md).</span></span>
-   [<span data-ttu-id="fb5c1-125">管理成員伺服器與 Windows 2000 Professional 上的使用者</span><span class="sxs-lookup"><span data-stu-id="fb5c1-125">Managing Users on Member Servers and Windows 2000 Professional</span></span>](managing-users-on-member-servers-and-windows-2000-professional.md)

 

 




