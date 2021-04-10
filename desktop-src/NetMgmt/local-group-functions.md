---
title: 本機群組函數
description: 本機群組可以包含來自一或多個網域的使用者帳戶或通用群組帳戶。  (的全域群組只能包含來自一個網域的使用者。 ) 本機群組只會在其專屬網域內共用一般許可權和許可權。
ms.assetid: ed4c59d6-6532-4190-9807-95678053fc72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd13a23b322a860d6896a213b27fb6263586412
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682486"
---
# <a name="local-group-functions"></a><span data-ttu-id="2a547-104">本機群組函數</span><span class="sxs-lookup"><span data-stu-id="2a547-104">Local Group Functions</span></span>

<span data-ttu-id="2a547-105">*本機群組* 可以包含來自一或多個網域的使用者帳戶或通用群組帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a547-105">A *local group* can contain user accounts or global group accounts from one or more domains.</span></span> <span data-ttu-id="2a547-106"> (的全域群組只能包含來自一個網域的使用者。 ) 本機群組只會在其專屬網域內共用一般許可權和許可權。</span><span class="sxs-lookup"><span data-stu-id="2a547-106">(Global groups can contain users from only one domain.) A local group shares common privileges and rights only within its own domain.</span></span>

<span data-ttu-id="2a547-107">網路管理本機群組功能可控制本機群組的成員，方法是只能在定義本機群組的系統本機上呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="2a547-107">The network management local group functions control members of local groups in a way that the functions can only be called locally on the system on which the local group is defined.</span></span> <span data-ttu-id="2a547-108">在工作站上，或在不是網域控制站的伺服器上，您只能使用該系統上定義的本機群組。</span><span class="sxs-lookup"><span data-stu-id="2a547-108">On a workstation, or on a server that is not a domain controller, you can use only a local group defined on that system.</span></span>

<span data-ttu-id="2a547-109">在 Active Directory 中，在原生模式下的網域（本機群組）稱為「 *網域本機群組*」。</span><span class="sxs-lookup"><span data-stu-id="2a547-109">In Active Directory, domains that are in native mode, local groups are called *domain local groups*.</span></span> <span data-ttu-id="2a547-110">所有網域控制站、成員伺服器和已加入網域的工作站都可使用網域本機群組。</span><span class="sxs-lookup"><span data-stu-id="2a547-110">Domain local groups are available on all domain controllers, member servers, and workstations joined to the domain.</span></span> <span data-ttu-id="2a547-111">Active Directory 混合模式網域是在主域控制站上定義，並複寫到網域中的所有其他網域控制站。</span><span class="sxs-lookup"><span data-stu-id="2a547-111">Active Directory mixed-mode domains are defined on the primary domain controller and replicated to all other domain controllers in the domain.</span></span> <span data-ttu-id="2a547-112">因此，本機群組可在其建立所在網域內的所有網域控制站上使用。</span><span class="sxs-lookup"><span data-stu-id="2a547-112">Therefore, a local group is available on all domain controllers within the domain in which it was created..</span></span>

<span data-ttu-id="2a547-113">本機群組函數會建立或刪除本機群組，以及檢查或調整本機群組的成員資格。</span><span class="sxs-lookup"><span data-stu-id="2a547-113">The local group functions create or delete local groups, and review or adjust the memberships of local groups.</span></span> <span data-ttu-id="2a547-114">這些函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="2a547-114">These functions are listed following.</span></span>



| <span data-ttu-id="2a547-115">函式</span><span class="sxs-lookup"><span data-stu-id="2a547-115">Function</span></span>                                                   | <span data-ttu-id="2a547-116">描述</span><span class="sxs-lookup"><span data-stu-id="2a547-116">Description</span></span>                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="2a547-117">**NetLocalGroupAdd**</span><span class="sxs-lookup"><span data-stu-id="2a547-117">**NetLocalGroupAdd**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | <span data-ttu-id="2a547-118">建立本機群組。</span><span class="sxs-lookup"><span data-stu-id="2a547-118">Creates a local group.</span></span>                                                  |
| [<span data-ttu-id="2a547-119">**NetLocalGroupAddMembers**</span><span class="sxs-lookup"><span data-stu-id="2a547-119">**NetLocalGroupAddMembers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | <span data-ttu-id="2a547-120">將一或多個使用者或全域群組新增至現有的本機群組。</span><span class="sxs-lookup"><span data-stu-id="2a547-120">Adds one or more users or global groups to an existing local group.</span></span>     |
| [<span data-ttu-id="2a547-121">**NetLocalGroupDel**</span><span class="sxs-lookup"><span data-stu-id="2a547-121">**NetLocalGroupDel**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | <span data-ttu-id="2a547-122">刪除本機群組，從群組中移除所有現有的成員。</span><span class="sxs-lookup"><span data-stu-id="2a547-122">Deletes a local group, removing all existing members from the group.</span></span>    |
| [<span data-ttu-id="2a547-123">**NetLocalGroupDelMembers**</span><span class="sxs-lookup"><span data-stu-id="2a547-123">**NetLocalGroupDelMembers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | <span data-ttu-id="2a547-124">從現有的本機群組移除一或多個成員。</span><span class="sxs-lookup"><span data-stu-id="2a547-124">Removes one or more members from an existing local group.</span></span>               |
| [<span data-ttu-id="2a547-125">**NetLocalGroupEnum**</span><span class="sxs-lookup"><span data-stu-id="2a547-125">**NetLocalGroupEnum**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | <span data-ttu-id="2a547-126">傳回伺服器上每個本機群組帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a547-126">Returns information about each local group account on a server.</span></span>         |
| [<span data-ttu-id="2a547-127">**NetLocalGroupGetInfo**</span><span class="sxs-lookup"><span data-stu-id="2a547-127">**NetLocalGroupGetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | <span data-ttu-id="2a547-128">傳回伺服器上特定本機群組帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a547-128">Returns information about a particular local group account on a server.</span></span> |
| [<span data-ttu-id="2a547-129">**NetLocalGroupGetMembers**</span><span class="sxs-lookup"><span data-stu-id="2a547-129">**NetLocalGroupGetMembers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | <span data-ttu-id="2a547-130">列出指定之本機群組的所有成員。</span><span class="sxs-lookup"><span data-stu-id="2a547-130">Lists all members of a specified local group.</span></span>                           |
| [<span data-ttu-id="2a547-131">**NetLocalGroupSetInfo**</span><span class="sxs-lookup"><span data-stu-id="2a547-131">**NetLocalGroupSetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | <span data-ttu-id="2a547-132">設定有關本機群組的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="2a547-132">Sets general information about a local group.</span></span>                           |
| [<span data-ttu-id="2a547-133">**NetLocalGroupSetMembers**</span><span class="sxs-lookup"><span data-stu-id="2a547-133">**NetLocalGroupSetMembers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | <span data-ttu-id="2a547-134">指派成員到本機群組。</span><span class="sxs-lookup"><span data-stu-id="2a547-134">Assigns members to a local group.</span></span>                                       |



 

<span data-ttu-id="2a547-135">您可以藉由指定成員 (SID) 的安全識別碼，將成員新增至本機群組。</span><span class="sxs-lookup"><span data-stu-id="2a547-135">You can add a member to a local group by specifying the security identifier (SID) of the member.</span></span> <span data-ttu-id="2a547-136">若要將成員帳戶名稱轉譯為 SID，請呼叫 [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) 函數。</span><span class="sxs-lookup"><span data-stu-id="2a547-136">To translate a member account name to a SID, call the [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) function.</span></span>

<span data-ttu-id="2a547-137">當您藉由呼叫 [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd) 函數來建立本機群組時，必須提供本機群組名稱。</span><span class="sxs-lookup"><span data-stu-id="2a547-137">When you create a local group by calling the [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd) function, you must supply a local group name.</span></span> <span data-ttu-id="2a547-138">一開始，本機群組沒有成員。</span><span class="sxs-lookup"><span data-stu-id="2a547-138">Initially, the local group has no members.</span></span>

<span data-ttu-id="2a547-139">本機群組帳戶資訊可在下列層級取得：</span><span class="sxs-lookup"><span data-stu-id="2a547-139">Local group account information is available at the following levels:</span></span>

-   [<span data-ttu-id="2a547-140">**LOCALGROUP \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="2a547-140">**LOCALGROUP\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_0)
-   [<span data-ttu-id="2a547-141">**LOCALGROUP \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="2a547-141">**LOCALGROUP\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1)
-   [<span data-ttu-id="2a547-142">**LOCALGROUP \_ 資訊 \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="2a547-142">**LOCALGROUP\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1002)

<span data-ttu-id="2a547-143">本機群組成員資格資訊可在下列資訊層級取得：</span><span class="sxs-lookup"><span data-stu-id="2a547-143">Local group membership information is available at the following information levels:</span></span>

-   [<span data-ttu-id="2a547-144">**LOCALGROUP \_ 成員 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="2a547-144">**LOCALGROUP\_MEMBERS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_0)
-   [<span data-ttu-id="2a547-145">**LOCALGROUP \_ 成員 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="2a547-145">**LOCALGROUP\_MEMBERS\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_1)
-   [<span data-ttu-id="2a547-146">**LOCALGROUP \_ 成員 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="2a547-146">**LOCALGROUP\_MEMBERS\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_2)
-   [<span data-ttu-id="2a547-147">**LOCALGROUP \_ 成員 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="2a547-147">**LOCALGROUP\_MEMBERS\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_3)

<span data-ttu-id="2a547-148">您可以藉由呼叫 [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) 函式來取得使用者所屬的本機群組名稱，並指定下列資訊層級：</span><span class="sxs-lookup"><span data-stu-id="2a547-148">You can retrieve the names of the local groups to which a user belongs by calling the [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) function, specifying the following information level:</span></span>

[<span data-ttu-id="2a547-149">**LOCALGROUP \_ 使用者 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="2a547-149">**LOCALGROUP\_USERS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_users_info_0)

<span data-ttu-id="2a547-150">如需詳細資訊，請參閱網路管理 [群組功能](group-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="2a547-150">For more information, see the network management [Group Functions](group-functions.md).</span></span>

<span data-ttu-id="2a547-151">如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理本機群組功能達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="2a547-151">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management local group functions.</span></span> <span data-ttu-id="2a547-152">如需詳細資訊，請參閱 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)。</span><span class="sxs-lookup"><span data-stu-id="2a547-152">For more information, see [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span></span>

 

 