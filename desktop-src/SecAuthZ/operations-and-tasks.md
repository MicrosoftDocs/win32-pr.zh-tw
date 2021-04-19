---
description: 操作是低層級的電腦動作。
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: 作業和工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996836"
---
# <a name="operations-and-tasks"></a><span data-ttu-id="79f83-103">作業和工作</span><span class="sxs-lookup"><span data-stu-id="79f83-103">Operations and Tasks</span></span>

<span data-ttu-id="79f83-104">操作是低層級的電腦動作。</span><span class="sxs-lookup"><span data-stu-id="79f83-104">An operation is a low-level computer action.</span></span> <span data-ttu-id="79f83-105">在授權管理員 API 中，作業是由 [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="79f83-105">In the Authorization Manager API, an operation is represented by an [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) object.</span></span> <span data-ttu-id="79f83-106">一般情況下，作業數目太多，而且太低層級以促進系統管理。</span><span class="sxs-lookup"><span data-stu-id="79f83-106">In general, operations are too many in number and too low-level to facilitate administration.</span></span> <span data-ttu-id="79f83-107">將作業分組至工作中，以簡化授權原則的管理。</span><span class="sxs-lookup"><span data-stu-id="79f83-107">Group operations into tasks to simplify administration of authorization policy.</span></span>

<span data-ttu-id="79f83-108">工作是以 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件來代表，而且可以包含一或多個 [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) 物件。</span><span class="sxs-lookup"><span data-stu-id="79f83-108">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object and can contain one or more [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) objects.</span></span> <span data-ttu-id="79f83-109">**IAzTask** 物件也可以包含其他 **IAzTask** 物件，讓工作可以進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="79f83-109">An **IAzTask** object can also contain other **IAzTask** objects, so that tasks can be nested.</span></span> <span data-ttu-id="79f83-110">為了方便管理， **IAzTask** 物件應該代表實際使用者想要執行的工作。</span><span class="sxs-lookup"><span data-stu-id="79f83-110">To facilitate administration, an **IAzTask** object should represent a task that a real user wants to perform.</span></span>

<span data-ttu-id="79f83-111">與代表該工作的 [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) 物件相關聯的商務規則腳本，可以在執行時間限定對工作所包含之作業的存取權。</span><span class="sxs-lookup"><span data-stu-id="79f83-111">Access to the operations contained by a task can be qualified at run time by a business rule script associated with the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents that task.</span></span> <span data-ttu-id="79f83-112">如需商務規則腳本的詳細資訊，請參閱 [商務規則](business-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="79f83-112">For more information about business rule scripts, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="79f83-113">[**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask)物件也可以藉由將其 [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition)屬性設定為 **TRUE** 來代表角色定義。</span><span class="sxs-lookup"><span data-stu-id="79f83-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can also represent a role definition by setting its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property to **TRUE**.</span></span> <span data-ttu-id="79f83-114">許可證 **管理員** MMC 嵌入式管理單元使用者介面會將該 **IAzTask** 物件顯示為角色。</span><span class="sxs-lookup"><span data-stu-id="79f83-114">The **Authorization Manager** MMC snap-in user interface then displays that **IAzTask** object as a role.</span></span> <span data-ttu-id="79f83-115">如需角色定義的詳細資訊，請參閱 [角色](roles.md)。</span><span class="sxs-lookup"><span data-stu-id="79f83-115">For more information about role definitions, see [Roles](roles.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79f83-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="79f83-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79f83-117">在 c + + 中定義作業</span><span class="sxs-lookup"><span data-stu-id="79f83-117">Defining Operations in C++</span></span>](defining-operations-in-c--.md)
</dt> <dt>

[<span data-ttu-id="79f83-118">在 c + + 中將作業分組為工作</span><span class="sxs-lookup"><span data-stu-id="79f83-118">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[<span data-ttu-id="79f83-119">在 c + + 中將工作分組為角色</span><span class="sxs-lookup"><span data-stu-id="79f83-119">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="79f83-120">使用者和群組</span><span class="sxs-lookup"><span data-stu-id="79f83-120">Users and Groups</span></span>](users-and-groups.md)
</dt> </dl>

 

 



