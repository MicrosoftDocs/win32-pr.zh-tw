---
description: 使用授權管理員 API 在腳本中建立授權原則存放區的指示。
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: 在腳本中建立授權原則存放區
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114540"
---
# <a name="creating-an-authorization-policy-store-in-script"></a><span data-ttu-id="554e6-103">在腳本中建立授權原則存放區</span><span class="sxs-lookup"><span data-stu-id="554e6-103">Creating an Authorization Policy Store in Script</span></span>

<span data-ttu-id="554e6-104">在安裝應用程式之前或期間建立授權原則。</span><span class="sxs-lookup"><span data-stu-id="554e6-104">Create an authorization policy before or during the installation of an application.</span></span>

<span data-ttu-id="554e6-105">當您使用授權管理員 API 建立授權原則時，請遵循下列主題中提供的指示。</span><span class="sxs-lookup"><span data-stu-id="554e6-105">When you use the Authorization Manager API to create an authorization policy, follow the instructions provided in the following topics.</span></span>



| <span data-ttu-id="554e6-106">主題</span><span class="sxs-lookup"><span data-stu-id="554e6-106">Topic</span></span>                                                                                                                  | <span data-ttu-id="554e6-107">描述</span><span class="sxs-lookup"><span data-stu-id="554e6-107">Description</span></span>                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="554e6-108">在腳本中建立授權原則存放區物件</span><span class="sxs-lookup"><span data-stu-id="554e6-108">Creating an Authorization Policy Store Object in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md) | <span data-ttu-id="554e6-109">授權原則存放區包含應用程式或應用程式群組之安全性原則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="554e6-109">An authorization policy store contains information about the security policy of an application or group of applications.</span></span>                                                                                                                                       |
| [<span data-ttu-id="554e6-110">在腳本中建立應用程式物件</span><span class="sxs-lookup"><span data-stu-id="554e6-110">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)                               | <span data-ttu-id="554e6-111">針對使用授權原則存放區的每個應用程式，您必須建立 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) 物件，並將它儲存至原則存放區。</span><span class="sxs-lookup"><span data-stu-id="554e6-111">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>                                                                                                |
| [<span data-ttu-id="554e6-112">在腳本中定義作業</span><span class="sxs-lookup"><span data-stu-id="554e6-112">Defining Operations in Script</span></span>](defining-operations-in-script.md)                                                     | <span data-ttu-id="554e6-113">作業是應用程式的低層級函式或方法。</span><span class="sxs-lookup"><span data-stu-id="554e6-113">An operation is a low-level function or method of an application.</span></span>                                                                                                                                                                                              |
| [<span data-ttu-id="554e6-114">將作業分組到腳本中的工作</span><span class="sxs-lookup"><span data-stu-id="554e6-114">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)                               | <span data-ttu-id="554e6-115">工作是應用程式使用者需要完成的高層級動作。</span><span class="sxs-lookup"><span data-stu-id="554e6-115">A task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="554e6-116">工作是由作業所組成，這是應用程式的低層級函式和方法。</span><span class="sxs-lookup"><span data-stu-id="554e6-116">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span>                                                                                    |
| [<span data-ttu-id="554e6-117">將工作分組到腳本中的角色</span><span class="sxs-lookup"><span data-stu-id="554e6-117">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)                                         | <span data-ttu-id="554e6-118">角色代表使用者類別以及這些使用者已獲授權執行的工作。</span><span class="sxs-lookup"><span data-stu-id="554e6-118">A role represents a category of users and the tasks those users are authorized to perform.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="554e6-119">在腳本中定義使用者群組</span><span class="sxs-lookup"><span data-stu-id="554e6-119">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)                                           | <span data-ttu-id="554e6-120">[**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)物件代表一組使用者。</span><span class="sxs-lookup"><span data-stu-id="554e6-120">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="554e6-121">然後，您可以將角色共同指派給這個使用者群組。</span><span class="sxs-lookup"><span data-stu-id="554e6-121">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="554e6-122">**IAzApplicationGroup** 物件也可以包含其他 **IAzApplicationGroup** 物件做為成員。</span><span class="sxs-lookup"><span data-stu-id="554e6-122">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> |
| [<span data-ttu-id="554e6-123">將使用者新增至腳本中的應用程式群組</span><span class="sxs-lookup"><span data-stu-id="554e6-123">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)                   | <span data-ttu-id="554e6-124">應用程式群組是一組使用者和使用者群組。</span><span class="sxs-lookup"><span data-stu-id="554e6-124">An application group is a group of users and user groups.</span></span> <span data-ttu-id="554e6-125">應用程式群組可以包含其他應用程式群組，讓使用者群組可以進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="554e6-125">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="554e6-126">應用程式群組是由 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="554e6-126">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>    |



 

 

 



