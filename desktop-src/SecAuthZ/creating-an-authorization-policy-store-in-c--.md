---
description: 使用授權管理員 API 在 c + + 中建立授權原則存放區的指示。
ms.assetid: a350f25a-7cda-4879-82d1-151a3da7d8ec
title: 在 c + + 中建立授權原則存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdff3ba26457510440c8d0e603bc993a4878281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114137"
---
# <a name="creating-an-authorization-policy-store-in-c"></a><span data-ttu-id="dc136-103">在 c + + 中建立授權原則存放區</span><span class="sxs-lookup"><span data-stu-id="dc136-103">Creating an Authorization Policy Store in C++</span></span>

<span data-ttu-id="dc136-104">在安裝應用程式之前或期間建立授權原則。</span><span class="sxs-lookup"><span data-stu-id="dc136-104">Create an authorization policy before or during the installation of an application.</span></span>

<span data-ttu-id="dc136-105">當您使用授權管理員 API 建立授權原則時，請遵循下列主題中提供的指示。</span><span class="sxs-lookup"><span data-stu-id="dc136-105">When you use the Authorization Manager API to create an authorization policy, follow the instructions provided in the following topics.</span></span>



| <span data-ttu-id="dc136-106">主題</span><span class="sxs-lookup"><span data-stu-id="dc136-106">Topic</span></span>                                                                                                            | <span data-ttu-id="dc136-107">描述</span><span class="sxs-lookup"><span data-stu-id="dc136-107">Description</span></span>                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc136-108">在 c + + 中建立授權原則存放區物件</span><span class="sxs-lookup"><span data-stu-id="dc136-108">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md) | <span data-ttu-id="dc136-109">授權原則存放區包含應用程式或應用程式群組之安全性原則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dc136-109">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="dc136-110">這項資訊包含與存放區相關聯的應用程式、作業、工作、使用者和使用者群組。</span><span class="sxs-lookup"><span data-stu-id="dc136-110">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span>              |
| [<span data-ttu-id="dc136-111">在 c + + 中建立應用程式物件</span><span class="sxs-lookup"><span data-stu-id="dc136-111">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)                               | <span data-ttu-id="dc136-112">授權原則存放區包含一或多個應用程式的授權原則資訊。</span><span class="sxs-lookup"><span data-stu-id="dc136-112">An authorization policy store contains authorization policy information for one or more applications.</span></span> <span data-ttu-id="dc136-113">針對每個使用該原則存放區的應用程式，您必須建立 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) 物件，並將它儲存至原則存放區。</span><span class="sxs-lookup"><span data-stu-id="dc136-113">For each application that uses that policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span> |
| [<span data-ttu-id="dc136-114">在 c + + 中定義作業</span><span class="sxs-lookup"><span data-stu-id="dc136-114">Defining Operations in C++</span></span>](defining-operations-in-c--.md)                                                     | <span data-ttu-id="dc136-115">在授權管理員中，操作是應用程式的低層級函式或方法。</span><span class="sxs-lookup"><span data-stu-id="dc136-115">In Authorization Manager, an operation is a low-level function or method of an application.</span></span>                                                                                                                                                               |
| [<span data-ttu-id="dc136-116">在 c + + 中將作業分組為工作</span><span class="sxs-lookup"><span data-stu-id="dc136-116">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)                               | <span data-ttu-id="dc136-117">在授權管理員中，工作是應用程式使用者需要完成的高層級動作。</span><span class="sxs-lookup"><span data-stu-id="dc136-117">In Authorization Manager, a task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="dc136-118">工作是由作業所組成，這是應用程式的低層級函式和方法。</span><span class="sxs-lookup"><span data-stu-id="dc136-118">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span>                                                     |
| [<span data-ttu-id="dc136-119">在 c + + 中將工作分組為角色</span><span class="sxs-lookup"><span data-stu-id="dc136-119">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)                                         | <span data-ttu-id="dc136-120">在授權管理員中，角色代表使用者類別以及這些使用者已獲授權執行的工作。</span><span class="sxs-lookup"><span data-stu-id="dc136-120">In Authorization Manager, a role represents a category of users and the tasks those users are authorized to perform.</span></span>                                                                                                                                      |
| [<span data-ttu-id="dc136-121">在 c + + 中定義使用者群組</span><span class="sxs-lookup"><span data-stu-id="dc136-121">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)                                           | <span data-ttu-id="dc136-122">在授權管理員中， [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件代表一組使用者。</span><span class="sxs-lookup"><span data-stu-id="dc136-122">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="dc136-123">然後，您可以將角色共同指派給這個使用者群組。</span><span class="sxs-lookup"><span data-stu-id="dc136-123">Roles can then be assigned to this group of users collectively.</span></span>                                                                       |
| [<span data-ttu-id="dc136-124">在 c + + 中將使用者新增至應用程式群組</span><span class="sxs-lookup"><span data-stu-id="dc136-124">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)                   | <span data-ttu-id="dc136-125">在授權管理員中，應用程式群組是一組使用者和使用者群組。</span><span class="sxs-lookup"><span data-stu-id="dc136-125">In Authorization Manager, an application group is a group of users and user groups.</span></span> <span data-ttu-id="dc136-126">應用程式群組可以包含其他應用程式群組，讓使用者群組可以進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="dc136-126">An application group can contain other application groups, so groups of users can be nested.</span></span>                                                                          |



 

 

 



