---
title: 使用者函式
description: 網路管理使用者功能可控制安全性資料庫中的使用者帳戶，也就是安全性帳戶管理員 (SAM) 資料庫，或在網域控制站的情況下 Active Directory。 使用者函數如下所示。
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a3349673d09e42fbfe7a5dc949d1bcff53b828
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969926"
---
# <a name="user-functions"></a><span data-ttu-id="78939-104">使用者函式</span><span class="sxs-lookup"><span data-stu-id="78939-104">User Functions</span></span>

<span data-ttu-id="78939-105">網路管理使用者功能可控制安全性資料庫中的使用者帳戶，也就是安全性帳戶管理員 (SAM) 資料庫，或在網域控制站的情況下 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="78939-105">The network management user functions control a user's account in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.</span></span> <span data-ttu-id="78939-106">使用者函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="78939-106">The user functions are listed following.</span></span>



| <span data-ttu-id="78939-107">函式</span><span class="sxs-lookup"><span data-stu-id="78939-107">Function</span></span>                                               | <span data-ttu-id="78939-108">描述</span><span class="sxs-lookup"><span data-stu-id="78939-108">Description</span></span>                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="78939-109">**NetUserAdd**</span><span class="sxs-lookup"><span data-stu-id="78939-109">**NetUserAdd**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | <span data-ttu-id="78939-110">新增使用者帳戶，並指派密碼和許可權層級。</span><span class="sxs-lookup"><span data-stu-id="78939-110">Adds a user account and assigns a password and privilege level.</span></span>     |
| [<span data-ttu-id="78939-111">**NetUserChangePassword**</span><span class="sxs-lookup"><span data-stu-id="78939-111">**NetUserChangePassword**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | <span data-ttu-id="78939-112">變更指定網路伺服器或網域的使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="78939-112">Changes a user's password for a specified network server or domain.</span></span> |
| [<span data-ttu-id="78939-113">**NetUserDel**</span><span class="sxs-lookup"><span data-stu-id="78939-113">**NetUserDel**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | <span data-ttu-id="78939-114">從伺服器刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="78939-114">Deletes a user account from the server.</span></span>                             |
| [<span data-ttu-id="78939-115">**NetUserEnum**</span><span class="sxs-lookup"><span data-stu-id="78939-115">**NetUserEnum**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | <span data-ttu-id="78939-116">列出伺服器上的所有使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="78939-116">Lists all user accounts on a server.</span></span>                                |
| [<span data-ttu-id="78939-117">**NetUserGetGroups**</span><span class="sxs-lookup"><span data-stu-id="78939-117">**NetUserGetGroups**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | <span data-ttu-id="78939-118">傳回使用者所屬通用群組名的清單。</span><span class="sxs-lookup"><span data-stu-id="78939-118">Returns a list of global group names to which a user belongs.</span></span>       |
| [<span data-ttu-id="78939-119">**NetUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="78939-119">**NetUserGetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | <span data-ttu-id="78939-120">傳回伺服器上特定使用者帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="78939-120">Returns information about a particular user account on a server.</span></span>    |
| [<span data-ttu-id="78939-121">**NetUserGetLocalGroups**</span><span class="sxs-lookup"><span data-stu-id="78939-121">**NetUserGetLocalGroups**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | <span data-ttu-id="78939-122">傳回使用者所屬的本機群組名稱清單。</span><span class="sxs-lookup"><span data-stu-id="78939-122">Returns a list of local group names to which a user belongs.</span></span>        |
| [<span data-ttu-id="78939-123">**NetUserSetGroups**</span><span class="sxs-lookup"><span data-stu-id="78939-123">**NetUserSetGroups**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | <span data-ttu-id="78939-124">設定指定之使用者帳戶的全域群組成員資格。</span><span class="sxs-lookup"><span data-stu-id="78939-124">Sets global group memberships for a specified user account.</span></span>         |
| [<span data-ttu-id="78939-125">**NetUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="78939-125">**NetUserSetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | <span data-ttu-id="78939-126">設定使用者帳戶的密碼和其他元素。</span><span class="sxs-lookup"><span data-stu-id="78939-126">Sets the password and other elements of a user account.</span></span>             |



 

<span data-ttu-id="78939-127">存取網路資源的每個使用者或應用程式都必須具有安全性資料庫中的帳戶。</span><span class="sxs-lookup"><span data-stu-id="78939-127">Each user or application that accesses network resources must have an account in the security database.</span></span> <span data-ttu-id="78939-128">目錄服務會使用此帳戶來驗證使用者或應用程式是否有權連線到資源。</span><span class="sxs-lookup"><span data-stu-id="78939-128">The directory services use this account to verify that the user or application has permission to connect to a resource.</span></span> <span data-ttu-id="78939-129">當使用者或應用程式要求存取資源時，Windows 安全性系統會檢查是否有適當的使用者帳戶或群組帳戶，以允許存取。</span><span class="sxs-lookup"><span data-stu-id="78939-129">When a user or an application requests access to a resource, the Windows security system checks for an appropriate user account or group account to permit the access.</span></span>

<span data-ttu-id="78939-130">一旦藉由呼叫 [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) 函式來移除使用者帳戶，使用者就無法再存取伺服器，除非使用 guest 帳戶。</span><span class="sxs-lookup"><span data-stu-id="78939-130">Once you remove a user account by calling the [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) function, the user can no longer access the server except by using the guest account.</span></span>

<span data-ttu-id="78939-131">因為使用者的密碼是機密的，所以 [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) 函式或 [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) 函式不會傳回它。</span><span class="sxs-lookup"><span data-stu-id="78939-131">Because a user's password is confidential, it is not returned by the [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) function or the [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) function.</span></span> <span data-ttu-id="78939-132">當您呼叫 [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)時，最初會指派密碼。</span><span class="sxs-lookup"><span data-stu-id="78939-132">The password is initially assigned when you call [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd).</span></span>

<span data-ttu-id="78939-133">使用者帳戶資訊可在下列層級取得：</span><span class="sxs-lookup"><span data-stu-id="78939-133">User account information is available at the following levels:</span></span>

-   [<span data-ttu-id="78939-134">**使用者 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="78939-134">**USER\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [<span data-ttu-id="78939-135">**使用者 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="78939-135">**USER\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [<span data-ttu-id="78939-136">**使用者 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="78939-136">**USER\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [<span data-ttu-id="78939-137">**使用者 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="78939-137">**USER\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [<span data-ttu-id="78939-138">**使用者 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="78939-138">**USER\_INFO\_4**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [<span data-ttu-id="78939-139">**使用者 \_ 資訊 \_ 10**</span><span class="sxs-lookup"><span data-stu-id="78939-139">**USER\_INFO\_10**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [<span data-ttu-id="78939-140">**使用者 \_ 資訊 \_ 11**</span><span class="sxs-lookup"><span data-stu-id="78939-140">**USER\_INFO\_11**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [<span data-ttu-id="78939-141">**使用者 \_ 資訊 \_ 20**</span><span class="sxs-lookup"><span data-stu-id="78939-141">**USER\_INFO\_20**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [<span data-ttu-id="78939-142">**使用者 \_ 資訊 \_ 21**</span><span class="sxs-lookup"><span data-stu-id="78939-142">**USER\_INFO\_21**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [<span data-ttu-id="78939-143">**使用者 \_ 資訊 \_ 22**</span><span class="sxs-lookup"><span data-stu-id="78939-143">**USER\_INFO\_22**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [<span data-ttu-id="78939-144">**使用者 \_ 資訊 \_ 23**</span><span class="sxs-lookup"><span data-stu-id="78939-144">**USER\_INFO\_23**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

<span data-ttu-id="78939-145">此外，當您呼叫 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式時，下列資訊層級會是有效的：</span><span class="sxs-lookup"><span data-stu-id="78939-145">In addition, the following information levels are valid when you call the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function:</span></span>

-   [<span data-ttu-id="78939-146">**使用者 \_ 資訊 \_ 1003**</span><span class="sxs-lookup"><span data-stu-id="78939-146">**USER\_INFO\_1003**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [<span data-ttu-id="78939-147">**使用者 \_ 資訊 \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="78939-147">**USER\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [<span data-ttu-id="78939-148">**使用者 \_ 資訊 \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="78939-148">**USER\_INFO\_1006**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [<span data-ttu-id="78939-149">**使用者 \_ 資訊 \_ 1007**</span><span class="sxs-lookup"><span data-stu-id="78939-149">**USER\_INFO\_1007**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [<span data-ttu-id="78939-150">**使用者 \_ 資訊 \_ 1008**</span><span class="sxs-lookup"><span data-stu-id="78939-150">**USER\_INFO\_1008**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [<span data-ttu-id="78939-151">**使用者 \_ 資訊 \_ 1009**</span><span class="sxs-lookup"><span data-stu-id="78939-151">**USER\_INFO\_1009**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [<span data-ttu-id="78939-152">**使用者 \_ 資訊 \_ 1010**</span><span class="sxs-lookup"><span data-stu-id="78939-152">**USER\_INFO\_1010**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [<span data-ttu-id="78939-153">**使用者 \_ 資訊 \_ 1011**</span><span class="sxs-lookup"><span data-stu-id="78939-153">**USER\_INFO\_1011**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [<span data-ttu-id="78939-154">**使用者 \_ 資訊 \_ 1012**</span><span class="sxs-lookup"><span data-stu-id="78939-154">**USER\_INFO\_1012**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [<span data-ttu-id="78939-155">**使用者 \_ 資訊 \_ 1014**</span><span class="sxs-lookup"><span data-stu-id="78939-155">**USER\_INFO\_1014**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [<span data-ttu-id="78939-156">**使用者 \_ 資訊 \_ 1017**</span><span class="sxs-lookup"><span data-stu-id="78939-156">**USER\_INFO\_1017**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [<span data-ttu-id="78939-157">**使用者 \_ 資訊 \_ 1020**</span><span class="sxs-lookup"><span data-stu-id="78939-157">**USER\_INFO\_1020**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [<span data-ttu-id="78939-158">**使用者 \_ 資訊 \_ 1024**</span><span class="sxs-lookup"><span data-stu-id="78939-158">**USER\_INFO\_1024**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [<span data-ttu-id="78939-159">**使用者 \_ 資訊 \_ 1051**</span><span class="sxs-lookup"><span data-stu-id="78939-159">**USER\_INFO\_1051**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [<span data-ttu-id="78939-160">**使用者 \_ 資訊 \_ 1052**</span><span class="sxs-lookup"><span data-stu-id="78939-160">**USER\_INFO\_1052**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [<span data-ttu-id="78939-161">**使用者 \_ 資訊 \_ 1053**</span><span class="sxs-lookup"><span data-stu-id="78939-161">**USER\_INFO\_1053**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

<span data-ttu-id="78939-162">下列功能可讓應用程式檢查密碼合規性。</span><span class="sxs-lookup"><span data-stu-id="78939-162">The following functions enable applications to check password compliance.</span></span>



| <span data-ttu-id="78939-163">函式</span><span class="sxs-lookup"><span data-stu-id="78939-163">Function</span></span>                                                               | <span data-ttu-id="78939-164">描述</span><span class="sxs-lookup"><span data-stu-id="78939-164">Description</span></span>                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78939-165">**NetValidatePasswordPolicyFree**</span><span class="sxs-lookup"><span data-stu-id="78939-165">**NetValidatePasswordPolicyFree**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | <span data-ttu-id="78939-166">釋放 [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) 函式所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="78939-166">Frees the memory allocated by the [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) function.</span></span> |
| [<span data-ttu-id="78939-167">**NetValidatePasswordPolicy**</span><span class="sxs-lookup"><span data-stu-id="78939-167">**NetValidatePasswordPolicy**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | <span data-ttu-id="78939-168">確認密碼符合複雜性、過時、最小長度和歷程記錄重複使用需求。</span><span class="sxs-lookup"><span data-stu-id="78939-168">Verifies that passwords meet complexity, aging, minimum length, and history reuse requirements.</span></span>            |



 

<span data-ttu-id="78939-169">如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理使用者功能達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="78939-169">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user functions.</span></span> <span data-ttu-id="78939-170">如需詳細資訊，請參閱 [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) 和 [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)。</span><span class="sxs-lookup"><span data-stu-id="78939-170">For more information, see [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) and [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).</span></span>

 

 