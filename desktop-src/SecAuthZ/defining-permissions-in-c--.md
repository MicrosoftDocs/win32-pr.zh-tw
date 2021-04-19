---
description: 使用授權管理員 API 在 c + + 中建立授權原則存放區來定義許可權的指示。
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: 在 c + + 中定義許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986646"
---
# <a name="defining-permissions-in-c"></a><span data-ttu-id="52535-103">在 c + + 中定義許可權</span><span class="sxs-lookup"><span data-stu-id="52535-103">Defining Permissions in C++</span></span>

<span data-ttu-id="52535-104">在授權管理員中，您可以藉由建立授權原則存放區來定義哪些使用者可以存取哪些應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="52535-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="52535-105">如需使用 Acl 定義許可權的相關資訊，請參閱 [在 c + + 中使用 Acl 定義許可權](defining-permissions-with-acls-in-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="52535-105">For information about defining permissions with ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md).</span></span>

<span data-ttu-id="52535-106">**若要定義存取權限**</span><span class="sxs-lookup"><span data-stu-id="52535-106">**To define access permissions**</span></span>

1.  <span data-ttu-id="52535-107">建立用來定義授權原則的存放區：</span><span class="sxs-lookup"><span data-stu-id="52535-107">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="52535-108">在 c + + 中建立授權原則存放區物件</span><span class="sxs-lookup"><span data-stu-id="52535-108">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  <span data-ttu-id="52535-109">在特定應用程式的授權原則存放區中建立區段：</span><span class="sxs-lookup"><span data-stu-id="52535-109">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="52535-110">在 c + + 中建立應用程式物件</span><span class="sxs-lookup"><span data-stu-id="52535-110">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)  
    </dl>
3.  <span data-ttu-id="52535-111">定義應用程式用來存取和修改資源的作業：</span><span class="sxs-lookup"><span data-stu-id="52535-111">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="52535-112">在 c + + 中定義作業</span><span class="sxs-lookup"><span data-stu-id="52535-112">Defining Operations in C++</span></span>](defining-operations-in-c--.md)  
    </dl>
4.  <span data-ttu-id="52535-113">將作業分組為使用者想要執行的高階工作：</span><span class="sxs-lookup"><span data-stu-id="52535-113">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="52535-114">在 c + + 中將作業分組為工作</span><span class="sxs-lookup"><span data-stu-id="52535-114">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  <span data-ttu-id="52535-115">定義包含工作群組的角色：</span><span class="sxs-lookup"><span data-stu-id="52535-115">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="52535-116">在 c + + 中將工作分組為角色</span><span class="sxs-lookup"><span data-stu-id="52535-116">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)  
    </dl><span data-ttu-id="52535-117">指派給角色的使用者具有執行指派給該角色之任何工作的許可權。</span><span class="sxs-lookup"><span data-stu-id="52535-117">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="52535-118">建立腳本，以便在執行時間存取工作的許可權：</span><span class="sxs-lookup"><span data-stu-id="52535-118">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="52535-119">在 c + + 中使用商務邏輯來限定存取權</span><span class="sxs-lookup"><span data-stu-id="52535-119">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)  
    </dl><span data-ttu-id="52535-120">此為選用步驟。</span><span class="sxs-lookup"><span data-stu-id="52535-120">This step is optional.</span></span>
7.  <span data-ttu-id="52535-121">定義使用者群組：</span><span class="sxs-lookup"><span data-stu-id="52535-121">Define groups of users:</span></span><dl>

[<span data-ttu-id="52535-122">在 c + + 中定義使用者群組</span><span class="sxs-lookup"><span data-stu-id="52535-122">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)  
    </dl><span data-ttu-id="52535-123">然後可以將這些群組指派給角色，以決定可執行檔工作。</span><span class="sxs-lookup"><span data-stu-id="52535-123">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="52535-124">將使用者新增至使用者群組：</span><span class="sxs-lookup"><span data-stu-id="52535-124">Add users to user groups:</span></span><dl>

[<span data-ttu-id="52535-125">在 c + + 中將使用者新增至應用程式群組</span><span class="sxs-lookup"><span data-stu-id="52535-125">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



