---
description: 藉由建立授權原則存放區，以使用授權管理員 API 在腳本中定義許可權的指示。
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: 在腳本中定義許可權
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e16f377ffa669da0b686ac28783e9a370efec94d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944824"
---
# <a name="defining-permissions-in-script"></a><span data-ttu-id="c8649-103">在腳本中定義許可權</span><span class="sxs-lookup"><span data-stu-id="c8649-103">Defining Permissions in Script</span></span>

<span data-ttu-id="c8649-104">在授權管理員中，您可以藉由建立授權原則存放區來定義哪些使用者可以存取哪些應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="c8649-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="c8649-105">**若要定義存取權限**</span><span class="sxs-lookup"><span data-stu-id="c8649-105">**To define access permissions**</span></span>

1.  <span data-ttu-id="c8649-106">建立用來定義授權原則的存放區：</span><span class="sxs-lookup"><span data-stu-id="c8649-106">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="c8649-107">在腳本中建立授權原則存放區</span><span class="sxs-lookup"><span data-stu-id="c8649-107">Creating an Authorization Policy Store in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  <span data-ttu-id="c8649-108">在特定應用程式的授權原則存放區中建立區段：</span><span class="sxs-lookup"><span data-stu-id="c8649-108">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="c8649-109">在腳本中建立應用程式物件</span><span class="sxs-lookup"><span data-stu-id="c8649-109">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)  
    </dl>
3.  <span data-ttu-id="c8649-110">定義應用程式用來存取和修改資源的作業：</span><span class="sxs-lookup"><span data-stu-id="c8649-110">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="c8649-111">在腳本中定義作業</span><span class="sxs-lookup"><span data-stu-id="c8649-111">Defining Operations in Script</span></span>](defining-operations-in-script.md)  
    </dl>
4.  <span data-ttu-id="c8649-112">將作業分組為使用者想要執行的高階工作：</span><span class="sxs-lookup"><span data-stu-id="c8649-112">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="c8649-113">將作業分組到腳本中的工作</span><span class="sxs-lookup"><span data-stu-id="c8649-113">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  <span data-ttu-id="c8649-114">定義包含工作群組的角色：</span><span class="sxs-lookup"><span data-stu-id="c8649-114">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="c8649-115">將工作分組到腳本中的角色</span><span class="sxs-lookup"><span data-stu-id="c8649-115">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)  
    </dl><span data-ttu-id="c8649-116">指派給角色的使用者具有執行指派給該角色之任何工作的許可權。</span><span class="sxs-lookup"><span data-stu-id="c8649-116">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="c8649-117">建立腳本，以便在執行時間存取工作的許可權：</span><span class="sxs-lookup"><span data-stu-id="c8649-117">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="c8649-118">使用腳本中的商務邏輯來限定存取權</span><span class="sxs-lookup"><span data-stu-id="c8649-118">Qualifying Access with Business Logic in Script</span></span>](qualifying-access-with-business-logic-in-script.md)  
    </dl><span data-ttu-id="c8649-119">此為選用步驟。</span><span class="sxs-lookup"><span data-stu-id="c8649-119">This step is optional.</span></span>
7.  <span data-ttu-id="c8649-120">定義使用者群組：</span><span class="sxs-lookup"><span data-stu-id="c8649-120">Define groups of users:</span></span><dl>

[<span data-ttu-id="c8649-121">在腳本中定義使用者群組</span><span class="sxs-lookup"><span data-stu-id="c8649-121">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)  
    </dl><span data-ttu-id="c8649-122">然後可以將這些群組指派給角色，以決定可執行檔工作。</span><span class="sxs-lookup"><span data-stu-id="c8649-122">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="c8649-123">將使用者新增至使用者群組：</span><span class="sxs-lookup"><span data-stu-id="c8649-123">Add users to user groups:</span></span><dl>

[<span data-ttu-id="c8649-124">將使用者新增至腳本中的應用程式群組</span><span class="sxs-lookup"><span data-stu-id="c8649-124">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



