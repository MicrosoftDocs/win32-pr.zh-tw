---
description: 角色在授權管理員中提供兩種不同的用途。
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: 角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848241"
---
# <a name="roles"></a><span data-ttu-id="52fda-103">角色</span><span class="sxs-lookup"><span data-stu-id="52fda-103">Roles</span></span>

<span data-ttu-id="52fda-104">角色在授權管理員中提供兩種不同的用途。</span><span class="sxs-lookup"><span data-stu-id="52fda-104">Roles serve two different purposes in Authorization Manager.</span></span> <span data-ttu-id="52fda-105">角色是使用者類別需要存取的一組工作或作業，而且也是一組符合該類別的使用者和群組。</span><span class="sxs-lookup"><span data-stu-id="52fda-105">A role is a set of tasks or operations to which a category of users requires access, and it is also a set of users and groups that fit into that category.</span></span>

-   [<span data-ttu-id="52fda-106">角色做為工作集</span><span class="sxs-lookup"><span data-stu-id="52fda-106">Roles as Sets of Tasks</span></span>](#roles-as-sets-of-tasks)
-   [<span data-ttu-id="52fda-107">角色做為使用者和群組的集合</span><span class="sxs-lookup"><span data-stu-id="52fda-107">Roles as Sets of Users and Groups</span></span>](#roles-as-sets-of-users-and-groups)
-   [<span data-ttu-id="52fda-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="52fda-108">Related topics</span></span>](#related-topics)

## <a name="roles-as-sets-of-tasks"></a><span data-ttu-id="52fda-109">角色做為工作集</span><span class="sxs-lookup"><span data-stu-id="52fda-109">Roles as Sets of Tasks</span></span>

<span data-ttu-id="52fda-110">授權原則會將 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件指派給 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) 物件，以建立一組工作。</span><span class="sxs-lookup"><span data-stu-id="52fda-110">An authorization policy assigns [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) objects to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to create sets of tasks.</span></span> <span data-ttu-id="52fda-111">所有指派給該 **IAzRole** 物件的使用者和群組，都具有存取這些 **IAzTask** 物件所包含之所有作業的許可權。</span><span class="sxs-lookup"><span data-stu-id="52fda-111">All users and groups assigned to that **IAzRole** object then have permission to access all operations contained by those **IAzTask** objects.</span></span>

<span data-ttu-id="52fda-112">因為 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) 物件代表一組工作，以及一組可存取這些工作的使用者和群組，所以授權管理員會提供一種方式來建立可指派給多個 **IAzRole** 物件的角色定義。</span><span class="sxs-lookup"><span data-stu-id="52fda-112">Because an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object represents both a set of tasks and a set of users and groups that have access to those tasks, Authorization Manager provides a way to create role definitions that can be assigned to more than one **IAzRole** object.</span></span> <span data-ttu-id="52fda-113">[**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask)物件可以包含其他 **IAzTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="52fda-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can contain other **IAzTask** objects.</span></span> <span data-ttu-id="52fda-114">然後，您可以將該 **IAzTask** 物件指派給一或多個 **IAzRole** 物件，以作為角色定義。</span><span class="sxs-lookup"><span data-stu-id="52fda-114">You can then use that **IAzTask** object as a role definition by assigning it to one or more **IAzRole** objects.</span></span> <span data-ttu-id="52fda-115">將 **IAzTask** 物件的 [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition)屬性設定為 **TRUE** ，讓許可證 **管理員** MMC 嵌入式管理單元使用者介面將 **IAzTask** 物件顯示為角色。</span><span class="sxs-lookup"><span data-stu-id="52fda-115">Set the [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property of the **IAzTask** object to **TRUE** to cause the **Authorization Manager** MMC snap-in user interface to display the **IAzTask** object as a role.</span></span>

## <a name="roles-as-sets-of-users-and-groups"></a><span data-ttu-id="52fda-116">角色做為使用者和群組的集合</span><span class="sxs-lookup"><span data-stu-id="52fda-116">Roles as Sets of Users and Groups</span></span>

<span data-ttu-id="52fda-117">將使用者和群組指派給 [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole)物件，藉由呼叫 [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember)或 [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername)方法，將指派給該 **IAzRole** 物件之工作的存取權授與這些使用者和群組。</span><span class="sxs-lookup"><span data-stu-id="52fda-117">Assign users and groups to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to grant those users and groups access to the tasks assigned to that **IAzRole** object by calling the [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) or [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) method.</span></span> <span data-ttu-id="52fda-118">藉由呼叫 [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember)方法，將 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)物件所代表的現有應用程式群組指派給 **IAzRole** 物件。</span><span class="sxs-lookup"><span data-stu-id="52fda-118">Assign existing application groups, represented by [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) objects, to an **IAzRole** object by calling the [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) method.</span></span> <span data-ttu-id="52fda-119">指派給 **IAzRole** 物件的所有使用者和群組都可存取指派給該角色的工作和作業。</span><span class="sxs-lookup"><span data-stu-id="52fda-119">All users and groups assigned to the **IAzRole** object have access to the tasks and operations assigned to that role.</span></span> <span data-ttu-id="52fda-120">如需應用程式群組的詳細資訊，請參閱 [使用者和群組](users-and-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="52fda-120">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="52fda-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="52fda-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52fda-122">在 c + + 中將工作分組為角色</span><span class="sxs-lookup"><span data-stu-id="52fda-122">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="52fda-123">在 c + + 中定義使用者群組</span><span class="sxs-lookup"><span data-stu-id="52fda-123">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> <dt>

[<span data-ttu-id="52fda-124">在 c + + 中將使用者新增至應用程式群組</span><span class="sxs-lookup"><span data-stu-id="52fda-124">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



