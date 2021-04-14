---
title: 群組函式
description: 全域群組包含一個網域中的使用者帳戶，這些使用者帳戶會群組在一個群組帳戶名稱下。
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382509"
---
# <a name="group-functions"></a><span data-ttu-id="8c7a4-103">群組函式</span><span class="sxs-lookup"><span data-stu-id="8c7a4-103">Group Functions</span></span>

<span data-ttu-id="8c7a4-104">*全域群組* 包含一個網域中的使用者帳戶，這些使用者帳戶會群組在一個群組帳戶名稱下。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-104">A *global group* contains user accounts from one domain that are grouped together under one group account name.</span></span> <span data-ttu-id="8c7a4-105">全域群組只能包含成員 (從建立全域群組的網域) 的使用者;它不能包含本機群組。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-105">A global group can contain only members (users) from the domain where the global group is created; it cannot contain local groups.</span></span> <span data-ttu-id="8c7a4-106">全域群組可在自己的網域中，也可以在任何信任網域內使用。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-106">A global group is available within its own domain and within any trusting domain.</span></span>

<span data-ttu-id="8c7a4-107">網路管理群組功能會控制全域群組。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-107">The network management group functions control global groups.</span></span> <span data-ttu-id="8c7a4-108">群組函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-108">The group functions are listed following.</span></span>



| <span data-ttu-id="8c7a4-109">函式</span><span class="sxs-lookup"><span data-stu-id="8c7a4-109">Function</span></span>                                     | <span data-ttu-id="8c7a4-110">描述</span><span class="sxs-lookup"><span data-stu-id="8c7a4-110">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="8c7a4-111">**NetGroupAdd**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-111">**NetGroupAdd**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | <span data-ttu-id="8c7a4-112">建立全域群組。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-112">Creates a global group.</span></span>                                                           |
| [<span data-ttu-id="8c7a4-113">**NetGroupAddUser**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-113">**NetGroupAddUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | <span data-ttu-id="8c7a4-114">將一位使用者新增至現有的全域群組。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-114">Adds one user to an existing global group.</span></span>                                        |
| [<span data-ttu-id="8c7a4-115">**NetGroupDel**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-115">**NetGroupDel**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | <span data-ttu-id="8c7a4-116">移除群組是否有任何成員的全域群組。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-116">Removes a global group whether or not the group has any members.</span></span>                  |
| [<span data-ttu-id="8c7a4-117">**NetGroupDelUser**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-117">**NetGroupDelUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | <span data-ttu-id="8c7a4-118">從全域群組移除一個使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-118">Removes one user name from a global group.</span></span>                                        |
| [<span data-ttu-id="8c7a4-119">**NetGroupEnum**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-119">**NetGroupEnum**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | <span data-ttu-id="8c7a4-120">列出伺服器上的所有全域群組。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-120">Lists all global groups on a server.</span></span>                                              |
| [<span data-ttu-id="8c7a4-121">**NetGroupGetInfo**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-121">**NetGroupGetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | <span data-ttu-id="8c7a4-122">傳回特定全域群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-122">Returns information about a particular global group.</span></span>                              |
| [<span data-ttu-id="8c7a4-123">**NetGroupGetUsers**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-123">**NetGroupGetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | <span data-ttu-id="8c7a4-124">列出特定全域群組的所有成員。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-124">Lists all members of a particular global group.</span></span>                                   |
| [<span data-ttu-id="8c7a4-125">**NetGroupSetInfo**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-125">**NetGroupSetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | <span data-ttu-id="8c7a4-126">設定全域群組的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-126">Sets general information about a global group.</span></span>                                    |
| [<span data-ttu-id="8c7a4-127">**NetGroupSetUsers**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-127">**NetGroupSetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | <span data-ttu-id="8c7a4-128">指派成員給新的全域群組;取代現有群組的成員。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-128">Assigns members to a new global group; replaces the members of an existing group.</span></span> |



 

<span data-ttu-id="8c7a4-129">When you call the [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) function to create a global group, you must supply a group name.</span><span class="sxs-lookup"><span data-stu-id="8c7a4-129">When you call the [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) function to create a global group, you must supply a group name.</span></span> <span data-ttu-id="8c7a4-130">一開始，新的群組沒有任何成員。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-130">Initially, a new group has no members.</span></span>

<span data-ttu-id="8c7a4-131">使用者帳戶會自動隸屬于特殊的全域群組網域使用者。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-131">User accounts automatically belong to the special global group Domain Users.</span></span> <span data-ttu-id="8c7a4-132">此群組中的成員資格是由 [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)、 [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)和 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數間接控制。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-132">Membership in this group is indirectly controlled by the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), and [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) functions.</span></span>

<span data-ttu-id="8c7a4-133">通用群組帳戶資訊可在下列層級取得：</span><span class="sxs-lookup"><span data-stu-id="8c7a4-133">Global group account information is available at the following levels:</span></span>

-   [<span data-ttu-id="8c7a4-134">**群組 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-134">**GROUP\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [<span data-ttu-id="8c7a4-135">**群組 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-135">**GROUP\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [<span data-ttu-id="8c7a4-136">**群組 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-136">**GROUP\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [<span data-ttu-id="8c7a4-137">**群組 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-137">**GROUP\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [<span data-ttu-id="8c7a4-138">**群組 \_ 資訊 \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-138">**GROUP\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [<span data-ttu-id="8c7a4-139">**群組 \_ 資訊 \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-139">**GROUP\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

<span data-ttu-id="8c7a4-140">1002和1005層級僅適用于 [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-140">The 1002 and 1005 levels are valid only for the [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) function.</span></span>

<span data-ttu-id="8c7a4-141">全域群組成員資訊可在下列資訊層級取得：</span><span class="sxs-lookup"><span data-stu-id="8c7a4-141">Global group member information is available at the following information level:</span></span>

-   [<span data-ttu-id="8c7a4-142">**群組 \_ 使用者 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="8c7a4-142">**GROUP\_USERS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

<span data-ttu-id="8c7a4-143">如需詳細資訊，請參閱網路管理 [本機群組功能](local-group-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-143">For more information, see the network management [Local Group Functions](local-group-functions.md).</span></span>

<span data-ttu-id="8c7a4-144">如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理群組功能達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-144">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions.</span></span> <span data-ttu-id="8c7a4-145">如需詳細資訊，請參閱 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)。</span><span class="sxs-lookup"><span data-stu-id="8c7a4-145">For more information, see [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span></span>

 

 